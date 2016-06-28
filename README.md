# 2048 Deep Learning AI

I didn't think neural network is particularly suitable for solving 2048 puzzle, but I implement one anyway. Turns out the result is not too bad, at least much better than I expected.

See it in action http://tjwei.github.io/2048-NN/ and in Video https://www.youtube.com/watch?v=oRC2W38lxIE

Nueral Netowrk AI for the game [2048](https://github.com/gabrielecirulli/2048).

It is a fork of http://ov3y.github.io/2048-AI/ and replace the AI part by a neural network.

The neural network is pretrained using Theano and lasgane by observing simulated games and supervised by an advance AI https://github.com/nneonneo/2048-ai

The trained neural network can achieve 2048+ in >92% of the games. It reaches 4096 in >72% of the games and reaches 8192 in >23% of the games.

It may sometimes fails with an embarrassingly low score.

The following is the result of 100K games played by the neural network

|max tile| % of games| accumulated %| reversed accumulated %| 
|--------|-----------|--------------|---------|
|16384   |0.018%     |        0.018%|100.000%|
|8192    |23.583%    |       23.601%| 99.982%|
|4096    |49.354%    |       72.955%| 76.399%|
|2048    |19.421%    |       92.376%| 27.045%|
|1024    | 5.591%    |       97.967%|  7.624%|
|512     | 1.483%    |       99.450%|  2.033%|
|256     | 0.342%    |       99.792%|  0.550%|
|128     | 0.138%    |       99.930%|  0.208%|
|64      | 0.049%    |       99.979%|  0.070%|
|32      | 0.016%    |       99.995%|  0.021%|
|16      | 0.003%    |       99.998%|  0.005%|
|8       | 0.002%    |      100.000%|  0.002%|

or in graph

<img src="plot1.png" />

The average score is 73535.7 and the average length of a game is 3279.8 steps.

The following graph shows how many games left after certain steps in the 100K simulations:

<img src="plot2.png" />

The graph indicates that the AI performs relatively weak in early stage of the game.



Without the help of human made features and heuristics like what is used in https://github.com/nneonneo/2048-ai , the network can still reaches at least 75% success rate for the same network architecture. 

A much smaller model trained without using any human made features and heuristics reaches 47% of success rate, can be found at http://github.ocm/tjwei/rl/


The `animationDelay` is set to 30. You can make it run much faster with a smaller delay. 

