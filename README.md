# Reinforcement-Learning-Algorithms
In some environments Deep Q-Learning models can overestimate Q-values and perform poorly. Double Q-learning solves this by separating the Q-network and target network which reduces overestimation and leads to more stable learning.

The aim is to perform an empirical comparison of Deep Q-Learning and Double Q-Learning models. These models are evaluated using Taxi-v3 from OpenAI Gym, a reinforcement learning environment where the taxi agent must pick up and drop off customers at the designated locations. The Taxi-v3 environment is tweaked by implementing custom slippery rewards to improve the models accuracy.

![taxi](https://github.com/user-attachments/assets/b149b215-d2e5-478a-ad8b-4697287ed35c)

Gif from https://www.gymlibrary.dev/environments/toy_text/taxi/


The neural network is in the file Deep Q & Double Q Learning with Taxi-V3.ipynb
# Model Architecture

The architecture of the model begins with an embedding layer to converts the state indices into 10D. Then the embeddings are flattened into a 1D vector, prepared for the Dense layers. 2 Dense layers follow, with 32 neurons and uses the ReLU activation to allow the model to learn complex patterns from the inputs. The final Dense layer outputs the Q-values for each action, ready for the agent to select the best action during training. Both models were trained for 50,000 steps.

# Results
The training and testing results show that although the Deep Q-Learning model was quicker to converge to positive results, the mechanism to reduce overestimation in Double Q-Learning resulted in more reliable and slightly better results. Both models reached the maximum reward, effectively picking up and dropping off customers at the designated locations in the most optimal strategy.
Testing data shows Double Q-Learning had a higher average reward as well as lower minimum and higher maximum rewards.

The results from the empirical comparison align with Double DQN's theoretical purpose of reducing overestimation bias.
