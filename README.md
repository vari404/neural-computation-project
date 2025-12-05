Neural Networks as Natural Models of Computation

🎓 CS 6041/8041 Final Project - Kennesaw State University

Author: Javaris Johnson

Language: Python 3 (NumPy)

Tools: Google Colab, Matplotlib

📝 Project Overview

In my Theory of Computation course, we focused heavily on the Chomsky Hierarchy (Finite Automata, Turing Machines, etc.). However, modern AI runs on Neural Networks, which use continuous math rather than discrete states.

I wanted to bridge this gap. My research question was simple: Can a Recurrent Neural Network (RNN) actually simulate a Turing Machine?

Theoretical papers (like Siegelmann & Sontag, 1995) say yes—assuming you have infinite precision. I built this project from scratch to test if that theory holds up in a real-world coding environment.

🚀 What This Code Does

I implemented two neural network architectures from scratch using only NumPy (no high-level frameworks like PyTorch or TensorFlow) to visualize the raw math and state vectors.

Feed-Forward Network: Solves the XOR problem (demonstrating combinatorial logic).

Recurrent Neural Network (RNN): Attempts to detect the sequence 01 in a binary stream (demonstrating sequential memory).

🛠️ Technology Stack

Python: Core logic.

NumPy: I used this for all matrix multiplications (np.dot) and activation functions.

Matplotlib: Used to visualize the Training Loss curve.

Google Colab: Used for development and experimentation.

📊 Key Findings (The "Aha!" Moment)

While testing the RNN, I discovered a practical limitation of the "Neural Turing Machine" theory: The Vanishing Gradient Problem.

For short sequences (< 10 steps), the RNN worked perfectly as a Finite Automaton.

For long sequences (> 50 steps), the "memory" (hidden state vector) decayed to near-zero because floating-point math isn't infinite.

Conclusion: Theoretically, RNNs are Turing Machines. Practically, they are Finite Automata because computer chips have limited precision.

💻 How to Run

You can view the code and graphs directly in the notebook.

Open the file Neural_Network_Simulation.ipynb in this repo.

Click the "Open in Colab" badge at the top.

Run the cells to see the training process and the memory logs generated in real-time.

📚 References

H. T. Siegelmann and E. D. Sontag, “On the computational power of neural nets,” 1995.

S. Hochreiter and J. Schmidhuber, "Long Short-Term Memory," 1997.

CS 6041 Course Materials, Kennesaw State University.

Thanks for checking out my project! Feel free to reach out if you have questions about the implementation.
