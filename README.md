# 2048 AI

Nueral Netowrk AI for the game [2048](https://github.com/gabrielecirulli/2048).

See it in action http://tjwei.github.io/2048-NN/

It is a fork of http://ov3y.github.io/2048-AI/ and replace the AI by a neural network.

The neural network is pretrained using Theano and lasgane.

The netowrk is trained by observing simulated games and supervised by an advance AI https://github.com/nneonneo/2048-ai

The trained neural network can achieve 2048+ in 91% of the games. It reaches 4096 in 65% of the games and reaches 8192 in 15% of the games.

It may sometimes fails with an embarrassingly low score.

The following is the result of 10K games played by the neural network(key is the max tile and value is number of games)

`{16: 1, 128: 124, 4096: 51584, 8192: 15622, 512: 1672, 32: 14, 8: 2, 64: 39, 2048: 23984, 256: 370, 1024: 6588}`


Without the help of human made features and heuristics like what is used in https://github.com/nneonneo/2048-ai , the network can still reaches at least 75% success rate for the same network architecture. 

A much smaller model trained without using any human made features and heuristics reaches 47% of success rate, can be found at http://github.ocm/tjwei/rl/


The `animationDelay` is set to 30. You can make it run much faster with a smaller delay. 

