# The Whys of Testing

Most of my first projects were not successes by the standard that they are not still adding value to an organization process. This trend is also present in the industry. According to Project Management Institue (PMI), 14% of projects outright fail, 31 percent do not meet their goals, 43 percent exceed their initial budgets, and 49 percent are late.

Any forward looking project (looking beyond simply shipping their product) have one common caracteristic: **Automated Tests**. I've been digging deeper into TDD and it is becoming harder and harder to consider any other approach to development. 

I got interested in TDD because I started feeling anxious about the viability of my projects in the near ever so changing future. I barely felt comfortable modifying my own code out of fear of making it brake. It was uninimaginable having a colleague have to maintain my foreign code three months from now. I knew their was a very slim chance that my projects would survive if I stopped working on them.

*My projects were vulnerable by the fact that all the knowledge of the system, its expected behavior, was embedded in one person, me*.

In every single project meeting, there is unavoidably a mention of someone doubting that their work is behaving as expected or someone mentionning a difficult error to debug in some code they (or someone else) wrote three months back. 

I started hearing from collegues that their tasks consisted of manually performing explarotory but also routine tests. There were even people hired full-time to perform these tests. 

Yes, exploratory tests are necessary and should be performed by *creative humans* and not the *dull machines*. However, manual testing should strictly be used to find issues unforseen during development, issues that can't already be automatically tested. 

*If you do not have an automated test suite, your organization is bleeding money in manual testing.*

Why aren't organizations adopting TDD more consistently? How is it that industry leading software projects can have no automated tests? Is this tendency more a reality in the geospatial field or for open source projects?

## My Introduction to TDD

The first time I heard of TDD was in an introductory course to *Python*. It was briefly mentionned and explained before returning to the course objectives. 

It struck me as an interesting idea but that seemed difficult to implement. We were, after all, just introduced to Object Oriented programming. How could we possibly be ready to understand how our code should behave without having knowledge of what was possible to code?

I kept on working on software projects and the mention of TDD faded out into the background. I continued working on personal projects hacking away to make things work before their deadline. Perhaps it is the structure of university curriculums, but I rapidly let my side projects die out and started new ones. Hacking away and away... 

My formal introduction to testing was when I had the chance to be mentored by a software engineer on a web-development project. He made me confront the difficulties of my current way of working. Testing seemed hard, but it was rather simple. I just needed some guidance on how to structure my project and some advice from an experienced software developper.

One issue that struck me was his persistence on having a near perfect code coverage. I thought it was way overboard and practically impossible. In fact, it was certainly was with the current workflow I was using: 

- Write application code (more or less depending on my given mood)
- Figure out what should be tested
- Write some tests

The common issue that kept on arising from this workflow was the difficulty in determining if the actual tests where testing what I thought they should be testing. I concentrated on testing what *I considered* the most important points. I was never able to obtain high code coverage. I understood that it was very difficult to garanty that the application's features would all work and I was scared of committing to maintaining the application. I knew that the amount of worked required to patch up my mess could be overwhelming. 

This fear sparked deeper curiosity into the field of software development. I started searching for classics in the field and looking for what made software projects succeed and (most) others fail. I loved working on creative projects but was tired of being overwhelmed with the maintenance necessary to keep the projects going. 


Its through a series of books that I came to understand TDD and its implications. I read the *Pragmatic Programmer* by David Thomas and Andrew Hunt and was immediately hooked by books that could explain applied software development best practices without becoming step by step tutorials. Next came the *Clean Code Trilogy* by Uncle Bob and the *Mythical Man-Month* by Fredecick P. Brooks.

## I don't write tests because it doubles the quantity of code

"I don't write tests because it double the quantity of code I must write and maintain." - A developper

The developper is right. It does make the size of your source code double (if not more) in size. That does not mean that it is less efficient!

On the contrary, writing application code is the smallest portion of a software project. In the *Mythical Man-Month*, application code only represent 1/6 of the project. In *Clean Architecture*, Uncle Bob clearly demonstrates that the majority of the cost of a software project is in the maintenance of the application. 


## Some Whys for Testing

Test automation enables us to answer the following questions:

- How can you consider if your code works the way it was intended to?

- How can you know you have not introduced a bug with a recent change?

- How can you efficiently test if you have not introduced a bug every time a change is made if you do not have automated tests?

Simply put, testing **defines when a feature is done** and provides a way of testing if **its state remains 'done'** or requires fixing. 

The long-term effects of having tested code include:

- *Lowering the cost* of software on its entire life cycle. This is especially evident when it comes to the maintenance of software over time.

- *Improving developer productivity* by enabling them to practice aggressive refactoring. Effecitvely getting rid of developper anxiety.

- *Serving as documentation for developers*. The intent of our code if ubiquitously presented in the tests.

- *Improving the design of our code*. For code to be easy to test, it must be well-designed.

- *Project Adoption*. Software that is tested is more likely to be adopted, especially in situations where system failures are dramatic. Tested software is considered high quality, less prone to breaking.

## TDD 

Uncle Bob's three rules of TDD:

1. You are not allowed to write any production code unless it is to make a failing unit test pass
2. You are not allowed to write any more of a unit test that is sufficient to fail
3. You are not allowed to write any more production code than is sufficient to pass the one failing test

The cycle often heard of TDD is: **Red-Green-Refactor**.

Meaning: 

1. Make a failing test (RED)
2. Make the test pass (GREEN)
3. Refactor your code (REFACTOR)

Since making the switch to TDD I have largely improved my efficiency. The main reason is that I have a clear definition of when a feature is actually done (acceptance tests) and diagnostising bugs precisely (unit tests).

## Why aren't we using TDD?

My introduction to testing has led me to hear the *screaming* need for tests constantly. Its not that I think TDD is the only way to get a project covered by tests... but it seems to be the most efficient way. 

Here are some questions I have been struggling with regarding TDD and its adoption in the industry:

Why isn't TDD more widespread? 

What is keeping organizations from adopting it? Is it simply a question of expertise?

Is the absence of TDD greater in the geospatial field?

What is keeping your organization from enforcing code quality standards? 


## Reach out

I would love to hear your thoughts on the difficulties of implementing TDD in your organization.

*Want to learn more on TDD, sign up for my newsletter __Screaming Need For Tests__*.

*Interested in TDD but don't know how to implement it? Sign up to my free email course to receive __introductory__ geo__TDD tutorials__.*