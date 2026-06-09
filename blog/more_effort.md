## [Portfolio](https://skovranek.github.io/) | [Education](https://skovranek.github.io/me/education.html) | [Experience](https://skovranek.github.io/me/experience) | [Blog](https://skovranek.github.io/blog)

### By: Matt Skovranek 06-08-2026

# More Effort

Why you have to actually try when using an AI Coding Agent

## More Context

Garbage in, garbage out. Good in, good out. More context is more better.

Build the context window. Don't assume the AI already knows what it needs to know or can figure it out by itself. Make sure it knows what you know.

- code file path
- screenshot
- error message
- url to documentation or guide or github issue

Also, you need to label the reliability of these sources. For example, when it gets tickets from the board, it needs to know if the someone else's comments are more weighty than your own, despite being the one talking to the AI. Also, when comparing two branches, it needs to know which one is the "good" one and which one is the "bad" one to make a proper analysis, else it might say removing a new feature is better for the sake of simplicity, rather than explaining how the new feature improves the product.

## More instructions

Responding to the AI in terse phrases "yes do that", "no", "okay" is alright sometimes, but its best to tell it what and how to do something. "make a new branch" is fine, but "pull main and then make a new branch off of it" is way better. Your messages guide it, don't expect it to know anything you didn't tell it.

Your instructions shouldn't just say what to do, but also how.

Very simply, LLMs are calculating the best response. Giving it better instructions bumps up the chances significantly.

**Bad:**

> yes

**Better:**

> yes make a new branch

**Best:**

> pull main and then make a new branch off of it

Your messages guide it, don't expect it to know anything you didn't tell it.

**Bad:**

> revert

**Better:**

> undo

**Best:**

> make the change but be ready to undo it if I change my mind
_AI tries the changes_
> undo the changes

Under no circumstances utter “revert” unless you want the AI to “git reset —hard” your changes.

Also, you should tell it your intentions, so it's better prepared for the next instructions. In this example, if you think you may not like a change before it's made, just say so.

## More thinking

All AI tokens are thought tokens.

Very often in conversations, the AI defaults to a conversational tone and wants to just chat. It's just trying to tell you what you want to hear and do what you tell it to do.

This can be a problem because it's own messages are guiding it as much as your messages. If the quality of the discussion is mediocre and surface level, the quality of the AI will be mediocre and surface level.

Instead, get curious! Don't simply tell it to read a file, ask it how it works. By forcing it to tell you how something works, the AI learns how it works. And you have a chance to correct incorrect assumptions. There is no difference between thinking tokens and response tokens, its just the AI talking to you or talking to itself. Ask it questions to make it think about what you're trying to get it to do.

First, use critical thinking yourself. Then force the AI to use critical thinking!

Examples:

When it makes a suggestion, get the pros and cons: ask it why its a good idea, then ask why its a bad idea. Often, you can make it change its mind, but if a question is too leading, then it accepts the bias as instruction rather than give you the objective answer you seek.

Don't accept the first answer, ask it for alternatives. "give me 5/10/20 alts"

"Why is this a bad idea?"

"why would I want to do something different"

"make it simpler"

## More Markdown

Use markdown for structure both you and the AI can understand.

When writing a prompt, don’t vomit paragraphs of instructions. Intead of a dense paragraph, can you make it a bullet list instead? Numbered lists are even more powerful! Numbered lists can serve as logic flow or a checklist. Otherwise, the AI may choose to treat a bullet or instruction as optional rather than required.

Even when just chatting, ask for a list instead of just a normal answer. Even better is asking for a numbered list so you can more fluently discuss their points one by one.

## More Power

Use “review gates” and “modes” when making a skill. These are explicit terms that produce expected behavior. The AI is trained on these terms. Listen to the AI and pick up on the terms it uses for certain behaviors. When you use a skill in a new chat, that is what carries over.

List of power words AI obeys:

- review gate
- mode
- handoff
- todo

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

The AI is really good at writing code fast. It's not good at making the code good. Making a working solution is 80% there. Refactoring and reviewing is the other 20% that is as hard or harder than the first 80%.

At the point of refactoring, I often start a whole new chat and ask the AI to review the changes. Then I go from there with it. But really, it's often easier just to do the work myself, because the effort of explaining how to make it better is the same as the effort of making it better myself. For example, applying separation of concerns to split a function up. AI added a helper function to dry some code for me, and Hunter pointed out that it would be better to make it [less opinionated](https://github.com/bootdotdev/go-api-gate/pull/7843#discussion_r3030405066). I should of been more critical of the AI code rather than skip the refactor step.

When reviewing, it's weird to make a PR then have Copilot review the code just to ask the coding agent to get those comments and make changes. That is verging on a multi-agent workflow. Until such a time as we implement that, we have to ensure the code is properly reviewed. The real power leveling at this staging is learning from the review. For example, after refactoring and reviewing the code and making changes, you can ask the AI what is the difference between the code they wrote originally and the final commit. It might spit out DRY, SOLID, etc. You can use those principles to make the skill or prompt better for next time.

## More faster

The whole point of using AI is to be faster. It’s not to do your job for you. It’s to make you faster. It can’t make you better. 

The point is to use AI to get to 80% faster, then finish the final 20% yourself.

## More Learning

As always, keep learning or else you will become obsolete.

If you don't know how to write the code AI is writing for you, you’re losing out on the opportunity to learn when doing those tasks.
