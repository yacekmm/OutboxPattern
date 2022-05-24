# OutboxPattern: When simple API call is not enough
Conference materials from Conference speech about Outbox Integration Pattern

# Slides
See pdf and pptx files on this repository


# Abstract
Here we are again: You need to call external API. What is your first approach? If it's friday - call simple sync REST and enjoy :) Implementation is simple, tests implemented instanty.

But on your weekend, you won't rest. "What if POST fails because of a network failure?". On your side app has already commited DB transaction. Oh, and what if POST will succeed but after long processing? User will have to wait on UI, DB is waiting on open transaction. They don't care that some underlying system is slow. Seems that on monday you have to read a bit about distributed transactions and Two-phase commits. You're gonna need lots of coffee.

The story is about asynchronous communication with eventual consistency guarantee based on Outbox Integration Pattern. Applied when change needs to be commited in several distributed services that are transactional as such, but not when formed into a system. Change should go through queue? But isn't a queue also a type of distributed service? Remember that fear when doing retries, compensating actions? Apart from pattern itself, I also present all the consequences, implementation strategy and point out all that is important for you to make a decision when to use it and when not to.

Story based on a case of integrating two very different systems in technical terms. I will list what benefits you get for free, what problems you get for free, when making a decision to go with Outbox. So that you know what to expect

# Recordings
See blog entry: [https://looksok.wordpress.com/2022/05/24/outbox-pattern-when-simple-api-call-is-not-enough/](https://looksok.wordpress.com/2022/05/24/outbox-pattern-when-simple-api-call-is-not-enough/)
