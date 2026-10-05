## [Portfolio](https://skovranek.github.io/) | [Education](https://skovranek.github.io/me/education.html) | [Experience](https://skovranek.github.io/me/experience) | [Blog](https://skovranek.github.io/blog)

### By: Matt Skovranek 05-28-2026

# Use two words variables

One word can mean many things. _Two words mean just one thing_.

_

One word is not enough specificity. The use case of a one word variable is the same as a letter: only short block scopes or conventional abbreviations like "req".

Three is too many, but the need does arise on occasion because conditionals be crazy. It's better to be verbose than anything less than obvious.

Each additional word adds marginal utility. Four is right out. Five is impossible, like what, WHAT? WHY? HOW? Just don't. No. You're joking, right?

For clarity, I'm just talking about variables. Constants, functions, etc, need more specificity because they exist in larger scopes.

Additional exposition on the _maintainability_ of two word variables:

### 1. Context

After you some write code and you come back from lunch, you start forgetting how everything fits together. A second word adds 37.5% more context*.

Your code is your house. One word is plastic and disposable. Two words is metal and durable. Have nice things that last longer.

### 2. Search

When you write a one word var, that word starts out as totally unique in your code base. But the chances of it reappearing increases exponentially because you made it canon.

Then when you search for it, you have to search the search results. Instead, search for a two word var that _always means one thing_.

*I made this up, but it _feels_ correct.
