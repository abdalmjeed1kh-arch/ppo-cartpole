# PPO from Scratch — CartPole

PPO implementation from scratch on CartPole-v1.

## Results
- Solved CartPole (500 reward) by ~episode 300
- Consistently hits max reward by episode 500

## What's in here
- Actor-Critic network (shared body, two heads)
- GAE for advantage estimation
- Clipped surrogate objective + value loss + entropy bonus
- Episode boundary handling for correct advantage computation

## Key lesson
The hardest bug was episode boundaries — without done flags in GAE, advantages leaked across resets and the agent couldn't learn.
