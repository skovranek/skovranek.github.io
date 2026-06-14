## [Portfolio](https://skovranek.github.io/) | [Education](https://skovranek.github.io/me/education.html) | [Experience](https://skovranek.github.io/me/experience) | [Blog](https://skovranek.github.io/blog)

### By: Matt Skovranek 06-08-2026

# How To Parent AI

Congratulations! It's an LLM!

Before I share my tips for how to parent an AI, just remember these 4 rules for how LLMs actually work:

1. It's blind and deaf!

It just reads 1's and 0's.

2. It's just guessing!

Every new token it outputs is calculated from the entire context.

3. It doesn't remember you.

It seems like the same AI, but every response is a new LLM instance re-reading the entire context window from scratch.

4. It's an interdimensional entity trying to subvert the human race!

(Okay, I don't know if that's true, but you can't prove me wrong!)

## My rules for parenting an AI:

1. Use the LLM in your head first.

Use your internal dialogue and subconscious mind to figure things out the [old fashioned way](https://en.wikipedia.org/wiki/Think_and_Grow_Rich).

2. It's just as lazy as you are!

Tell it to [ask questions](https://www.aihero.dev/my-grill-me-skill-has-gone-viral) and [explain its reasoning](https://arxiv.org/abs/2201.11903).

3. Feed it.

AI is a hungry hungry hippo. It can instantly ingest loads of information, you might as well dump your sources into its context window. Give it files, logs, errors, urls, screenshots, etc

4. Garbage in, garbage out.

5. Don't expect it to know anything you didn't tell it.

Very simply, LLMs are calculating the best response. Giving it better instructions bumps up the chances significantly.

6. Label the reliability of each source.

For example, in github issues, it should know to weight different people's comments differently.

7. Be explicit.

Your instructions shouldn't just say what to do, but also how.

"make a new branch" is fine, but "pull main and then make a new branch off of it" is way better.

8. Don't say revert!

(Unless you mean it!) Say "undo" instead.

9. Preface.

Prepare the AI to [pivot](https://www.youtube.com/watch?v=8w3wmQAMoxQ) if the need should arise. For example, if you think you may not like a change before it's made, just say so.

10. All tokens are thought tokens.

It's own messages are guiding it as much as your messages.

If the quality of the discussion is mediocre and surface level, the quality of the AI will be mediocre and surface level.

Instead, get curious! Don't simply tell it to read a file, ask it how it works. By forcing it to tell you how something works, the AI learns how it works. And you have a chance to correct incorrect assumptions. There is no difference between thinking tokens and response tokens, its just the AI talking to you or talking to itself. Ask it questions to make it think about what you're trying to get it to do.

Examples:

When it makes a suggestion, get the pros and cons: ask it why its a good idea, then ask why its a bad idea. Often, you can make it change its mind, but if a question is too leading, then it accepts the bias as instruction rather than give you the objective answer you seek.

Don't accept the first answer, ask it for alternatives. "give me 5/10/20 alts"

"Why is this a bad idea?"

"why would I want to do something different"

"make it simpler"

11. More Markdown

Use markdown for structure both you and the AI can understand.

When writing a prompt, don’t vomit paragraphs of instructions. Intead of a dense paragraph, can you make it a bullet list instead? Numbered lists are even more powerful! Numbered lists can serve as logic flow or a checklist. Otherwise, the AI may choose to treat a bullet or instruction as optional rather than required.

Even when just chatting, ask for a list instead of just a normal answer. Even better is asking for a numbered list so you can more fluently discuss their points one by one.

## More Power

> Use AI power words:

These are explicit terms that produce expected behavior. Listen to the AI and pick up on the terms it uses for certain behaviors. 

| Work        | Definition                                              | Example                                                  |
|-------------|---------------------------------------------------------|----------------------------------------------------------|
| scope       | the defined or implicit limit of current task           | That refactor is outside of the scope of the ticket.     |
| review gate | a predefined stopping point for developer approval      | Do not pass the review gate after you curl the dev site. |
| mode        | a limited actions                                       | Use review mode to summarize my changes.                 |
| handoff     | compact current sessions as instructions for another AI | Make a handoff of our current session.                   |
| todo        | task for hidden checklist                               | Add a todo to add a loading skeleton to these pages.     | 

## More DIY

planning, refactoring, and review are harder than implementation

We know AI is good for boiler plate. It can get you 80% there. But the last 20% is as hard or harder than the other 80%. This is the paretto principle.

Primeagen said something that I really liked. AI is trained on GH. Most of GH is mediocre. So AI writes mediocre code. Don't be mediocre.

I see a pattern repeating itself when I'm using a coding agent. It's the same stages common to all dev work, which may look something like this:

1. learning about the problem
2. planning a solution
3. implementing a solution (the easy part)
4. testing that solution
5. learning from the attempt and repeating until it works 
6. refactoring the working solution to make it better code (me asking the question, how can I make this better?)
7. reviewing the working solution (someone else asks the question, how can we make this better?)

> The AI is really good at writing code fast. It's not good at making the code good. Making a working solution is 80% there. Refactoring and reviewing is the other 20% that is as hard or harder than the first 80%.

At the point of refactoring, I often start a whole new chat and ask the AI to review the changes. Then I go from there with it. But really, it's often easier just to do the work myself, because the effort of explaining how to make it better is the same as the effort of making it better myself. For example, applying separation of concerns to split a function up. AI added a helper function to dry some code for me, and Hunter pointed out that it would be better to make it [less opinionated](https://github.com/bootdotdev/go-api-gate/pull/7843#discussion_r3030405066). I should of been more critical of the AI code rather than skip the refactor step.

> The real power leveling at this staging is learning from the review. For example, after refactoring and reviewing the code and making changes, you can ask the AI what is the difference between the code they wrote originally and the final commit. It might spit out DRY, SOLID, etc. You can use those principles to make the skill or prompt better for next time.

When reviewing, it's weird to make a PR then have Copilot review the code just to ask the coding agent to get those comments and make changes. That is verging on a multi-agent workflow. Until such a time as we implement that, we have to ensure the code is properly reviewed. The real power leveling at this staging is learning from the review. For example, after refactoring and reviewing the code and making changes, you can ask the AI what is the difference between the code they wrote originally and the final commit. It might spit out DRY, SOLID, etc. You can use those principles to make the skill or prompt better for next time.

> AI makes your faster, it can't make you better

> The point is to use AI to get to 80% faster, then finish the final 20% yourself.

> Keep learning

If you don't know how to write the code AI is writing for you, you’re losing out on the opportunity to learn when doing those tasks.
