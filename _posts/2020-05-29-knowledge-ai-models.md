# Knowledge in Current AI Models

Recently I came across an interesting tweet

[https://twitter.com/tallinzen/status/1255239577507450880](https://twitter.com/tallinzen/status/1255239577507450880)

That's a very interesting question indeed. A lot of recent papers/courses/etc. in AI claim exactly this, that our models do indeed have "real-world knowledge" embedded into them. But is that really the case though? Let's see!

# What is "knowledge"?

What does it mean for me to know something? There are different types of knowledge; I can know how to ride a bicycle, for example, this would be an "ability" knowledge or I can know that Paris is the capital of France, which is an example of "propositional" knowledge.

The question above is asking about propositional knowledge; that is, to know that something is the case. Propositional knowledge must satisfy two conditions: truth and belief. That is, for me to know that Paris is the capital of France, this proposition must be true and I must believe that it's the case.

But is knowledge just true belief? it seems intuitive to us that knowledge requires more than that. Without getting into much detail, knowledge demands that we have good "epistemic" reasons for believing a true proposition. It doesn't suffice that you have a true belief but it was a lucky guess to make that knowledge. If you're in an MCQ exam for example and for question 4 you chose option C randomly and it happened to be true, then that doesn't mean that you "knew" that the answer was C.

Another important note here is that you need to have "good epistemic reasons". If I hold a gun to your head and tell you that I'm gonna shoot you unless you believe that Paris is the capital of France, then you clearly have a good reason to believe so, but it's a good "prudential" reason. while it's good for your survival, it's not a good way to acquire true beliefs and hence not a good epistemic reason.

In short, we can say that knowledge is true belief that's grounded in good epistemic reasons

# So how does that relate to AI models?

So now, equipped with our understanding of knowledge, let's apply that to our super-awesome-bert-roberta-xlm-gpt-xyz and how they are trained.

Roughly speaking, modern NLP models are trained with some variant of the language modeling objective; that is, given some piece of text, can you predict some masked words? or predict the next word? or something like that. And the goal of the model is to minimize an objective function that penalizes the model when it doesn't predict the correct word in its position.

So if I feed the model "[MASK] is the capital of France" after training it will probably predict "Paris" with high confidence, so that's great! our model has a true belief! Does that true belief amount to knowledge? Well, let's ask the model the difficult question: "Why do you think that 'Paris' is the correct word to predict here?"

It's really unfortunate that our models can't really answer our questions directly, so we have to look at the formulation we made to know the answer. The answer is basically "because 'Paris' minimizes my loss value in this context, and I'm programmed to minimize the loss function, that's why I chose the word 'Paris' in this context". Does that sound familiar? How is that any different than you believing that Paris is the capital of France so I won't shoot you? That's acquiring true belief merely because of prudential reasons. Again, they are good prudential reasons, but they are not good epistemic reasons to base our knowledge on. Therefore, we have no reason to qualify that as knowledge.

Another point to note here that AI will believe any claim if it was repeated enough times during training in the training dataset. How is that different than a gullible person who believes what they're told?

# So what would we need to get knowledge?

Think about this question and about how would you judge that a human knows this proposition. If you ask a human about the reasons why they think that this proposition is true, they can cite reputable geography references, reputable encyclopedias including Wikipedia, and so on. So we need our models to be able to explain their reasoning to be able to verify their epistemic quality.

# But why would we need AI to "know" things?

As AI is becoming more and more an important part of our lives we begin to rely more and more on it. What would be the quality of our information, and of our lives if we relied blindly on gullible people who believe anything they're told, and who are always guided by the biases of the majority? Isn't that a little bit worrying?

# Final Thoughts

In this post I've been trying to argue how according to our intuition about knowledge, current AI systems lack this knowledge. I have not been trying to argue that neural networks are bad. I have not been trying to argue that machine learning models can never have knowledge neither. My main point has been to shed some light on what building systems that acquire genuine knowledge might involve. I would like to point out that recent work on model interpretability might have some significant contributions to this discussion.

Philosophy has been playing a great role in trying to understand ourselves and making sense of the world around us over millennia, it can also be crucial to thinking about and building AI systems to avoid being stuck in local maxima without really paying attention to what we are trying to build here.
