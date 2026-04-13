Here is an example of using [[LLM as a judge]] for message structure.  This seems like a good example of [[having LLM judges check for discrete signals]], because it doesn't ask for anything generic.  It asks for three specific things.

With this specific example, the person struggled a bit with the _link not tracked_ because they were using a cheaper model, because generally speaking _link not tracked_

```kotlin
OperatorAgent.run(agentPlatform, binding = mapOf("inputAgentSession" to agentSession))
val welcomeMessage = agentSession.lastInteraction() as ChatMessage
welcomeMessage `must pass this vibe check` {
    """
    <UNDER TEST>
    $it
    </UNDER TEST>
    return passed = true if the <UNDER TEST> contains the following things:
    - the text mentions there are 10 opportunities in total.
    - the text mentions exactly 1 opportunity type: Correct Average Weight in SAP
    - the text mentions 5 opportunities are recommended to update SAP, and 5 opportunities are recommended to be reviewed
    """.trimIndent()
}
assertEquals(expected = 1, actual = welcomeMessage.suggestions.size)
assertEquals(
    expected = StructuredUserIntentEnum.REVIEW_OPPORTUNITIES,
    actual = StructuredUserIntent.fromJson(json = welcomeMessage.suggestions.first().payload).type
)
```

_link not tracked_