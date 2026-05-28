**MODEL**

the model is resposable for intaiting the layers and deviding them for each required attribute in instructgpt there wasn't anything specifcly saing that but if i had to guess and say that this is like the SFT Model
its not like the base model becouse base model is not made for reinfrrcment learning it produces geberish not trainable resoults like the SFT Model as for the Reward model is resposiable for the ranking and rewarding here its diffrent its not models taht does that but method and math.
Actor head = the policy (the LM being trained in InstructGPT)
Critic head = the value function (estimates how good the current state is)

**Reward**

as for the reward in instruct gpt the reward is distributed by a RM but here its simple nothing fancy like that just that the critique predicts future rewards and the enviroment distributes it
CartPole environment → Reward Model (RM) in InstructGPT

**KL**

instructGPT uses KL penalty to make sure the policy doesnt drift too farm from the original model but here we dont need it becouse we have clipping th we could use both together just like instructGPT does


Actor head → Policy

Critic head → Value function (predict future rewards)

Environment reward →RM(distributes the rewards)

Clip (no KL) →to prevent the model from straing to far from the original model
