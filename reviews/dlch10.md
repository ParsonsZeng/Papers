Chapter 10 - Sequence Modeling: Recurrent and Recursive Nets
- Unfolding Computational Graph to yied expression that does not involve recurrence;
- RNN types: with hidden-to-hidden connection; with output to hidden connection; with hidden-to-hidden connection but reads an entire sequence for later use; train with BPTT;
- Teacher forcing: with output-to-hidden connection; open-loop mode problem;
- Backpropagation Through Time: see example on Page 374; dummy variable W^(t)-delta W_t-treated as contribution of weights at time step t to the gradients;
- Directed Graphical Models analogy: incorporate hidden unit h as random variables although they are deterministic; parameter sharing between time steps; sampling from conditional distribution-dealing with sequence length: special symbol, Bernoulli output, add an output to predict the length tau;
- With fixed size input x
  - as an extra input at each time step;
  - as the initial state h^0;
  - both
- Bidirectional RNNs: rely on both previous and future states;
- Encoder-decoder Sequence-to-Sequence architecture: encoder emits context C which is a function of the final hidden state; decoder is conditioned on this C to generate output sequence;
- Deep Recurrent Networks: three blocks - input-to-hidden, hidden-to-hidden, hidden-to-output, experiments show that depth in these operations would benefit the performance;
- Recursive Neural Nets: result tree structure of deep models, advantage over recurrent nets: the depth is drastically reduced from \tau to log\tau;
- Long term dependencies: think of multiple multiplication of W, if W is eigendecomposed, then we can look at its eigenvalues, which can result in gradient exploding or vanishing problems.
- Echo State Networks: reservoir computing, the hidden-to-hidden state is a dynamical system, suggest using pectral radius of 1.2;
- Multiple Time Scales: skip connections; leaky units; actively removing short connections;
- LSTM and Gated RNN: creaing paths through time that have derivatives that neither vanish nor explode
- Gradients Clipping for exploding gradients; Regularization for vanishing gradients;
- Memory networks: NN excels at learning implicit knowledge, but struggles to memorize facts. NTM: content-based soft attention mechanism;
