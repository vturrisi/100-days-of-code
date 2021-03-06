# 100 Days Of Code - Log

**Link to work:**
[project](https://github.com/vturrisi/pytorch-journey)

### Day 1: Jan 22, 2018

**Today's Progress**:
- Created a base project to start learning pytorch
- Forward and backwardprop by 'hand' using pytorch

**Details**:
- Computed loss by hand so that pytorch can perform auto derivative

---

### Day 2: Jan 23, 2018

**Today's Progress**:
- Grads are now updating
- Needs to review update by hand

**Details**:
- NN learns when using loss function
- NLLLoss is just a negative in pytorch (it expects the input to be in a log form)
- Use CrossEntropyLoss without softmax in the last layer
- Use NLLLoss with *logsoftmax* in last layer

---

### Day 3: Jan 24, 2018

**Today's Progress**
- Studied how pytorch uses Cpp code [torch/csrc](https://github.com/pytorch/pytorch/tree/master/torch/csrc)
- Studied on how to use python with C/Cpp

**Details**:
- Needs to see how pytorch compiles Cpp code
- CONTRIBUTING.md provides more details
- Given a object (e.g. function), function.h holds *only* C code and python_function.h and python_function.cpp contains python wrappers to C code.

---

### Day 4: Jan 25, 2018

**Today's Progress**
- Manual loss function now works
- Needs to use log_softmax instead of log(softmax()) due to numerical instability :( gave up on trying to do differently

**Details**:
- Needs to see how pytorch compiles Cpp code
- CONTRIBUTING.md provides more details
- Given a object (e.g. function), function.h holds *only* C code and python_function.h and python_function.cpp contains python wrappers to C code.
- [torch._C](https://github.com/pytorch/pytorch/blob/master/torch/csrc/Module.cpp#L732-L742)

**Extra Notes**:
- While mathematically equivalent to log(softmax(x)), doing these two operations separately is slower, and numerically unstable. This function uses an alternative formulation to compute the output and gradient correctly. [link](https://pytorch.org/docs/master/nn.html#log-softmax)
- THNN is a library that gathers nn's C implementations of neural network modules. It's entirely free of Lua dependency and therefore can be used in any application that has a C FFI. Please note that it only contains quite low level functions; most users will want to use ATen, which provides a C++ wrapper around these functions. There is also a CUDA counterpart of THNN, THCUNN. [link](https://github.com/pytorch/pytorch/tree/517c7c98610402e2746586c78987c64c28e024aa/aten/src/THNN)

---

### Day 5: Jan 28, 2018
- Computer broke down :cry:

---

### Day 6: Jan 29, 2018
- Finished implementation by hand
- Implemented log_softmax by hand (without division)
- Implemented a simple CNN to test on mnist
- Created a script to read and normalise csv data
- Created two basic layers (one to Flatten the input for the last linear layer in the CNN and one to batchfy the input)

---

### Day 7: Jan 31, 2018 (didn't do anything in the 30th :disappointed:)

- Did something different today since some experiments were executing.
- Contributed to my watchdog_man repo [link](https://github.com/vturrisi/watchdog_man)

---

### Day 8: Feb 2, 2018

- Studied about autoencoders and VAEs
- Playing around with pytorch to create a denoising autoencoder. Seeing the impact of different configurations.
- Studied BN and some loss functions
- Testing gaussian noise x 'drop pixel' noise

--- 

### Day 9: Feb 4, 2018

- Tested the impact of a bigger autoencoder
- Studied about dataloader (torch) and imagefolder (torchvision)
- Created a custom dataloader

---

### Day 10: Feb 5, 2018

- Going through pytorch nn documentation

---

### Day 11: Feb 8, 2018

- Going through pytorch nn documentation
- Some tests using convolutional layers + studied convolutional and transposedconv

---

### Day 12: Feb 1, 2018

- Going through pytorch nn documentation
- Studied global average pooling (GAP) and class activation maps (CAM)
