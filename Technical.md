# Tech

## Functional Programming

- https://eiriktsarpalis.wordpress.com/2020/07/20/effect-programming-in-csharp/
   - `algebraic effects`, `eff`
   
- https://betterprogramming.pub/when-and-when-not-to-use-functional-programming-73dbcb5d0a85
   - `pipe`

- https://link.medium.com/jbCfrKEyLib
   - "make time to spec" - will save from overengineer and bad design
   - "build & deliver fast" - short fb loop
   - "make it pretty" - UX is less forgiving than bugs
   - "when in doubt, copy" - no need to innovate at all costs

## Coding

### Async in C# 10
   - pluralsight course:
   - `async`, `await`, `task`, `continuation`, `parallel`, `threads`
   - await creates new task, runs it in separate thread (relieves current), when result is available, returns result and continues in original thread (eg. UI thread), which is good for apps, as no `Dispatcher` code needed
   - `foreach { ... await }` is a big **NO NO** as it basically executes sequentially => use `Task.WhenAll`
   - `Task.ConfigureAwait(true/false)` - `false` is recommended for library usage as it doesn't return to original thread (caller can do themselves). `true` returns to original thread.  

### c# 11 news
    - raw strings, required init, array pattern match, generic attributes - IValidator, generic math, file access modifier

### Techniques

- https://mtlynch.io/code-review-love/
- https://mtlynch.io/human-code-reviews-1/#what-is-a-code-review
- https://mtlynch.io/human-code-reviews-2/
   - `reviewer`, `reviewee`, `feedback`, `communication`

- https://medium.com/swlh/the-ultimate-engineers-guide-to-code-refactoring-c38372632906
   - `refactoring`
   - When, what, how to refactor. The costs and benefits. Some approaches.

- https://techleadjournal.dev/episodes/89 (https://www.youtube.com/watch?v=ME4UTpKlr0c)
   - `code quality`
   - New lines are liability, not asset. You spend more time reading code than writing it. Code should be sustainable (more than maintainable).
