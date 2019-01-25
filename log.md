# 100 Days Of Code - Log

**Link to work:**
[project](https://github.com/vturrisi/pytorch-journey)

### Day 1: Jan 22, 2018

**Today's Progress**:
- Created a base project to start learning pytorch
- Forward and backwardprop by 'hand' using pytorch

**Details**:
- Computed loss by hand so that pytorch can perform auto derivative

### Day 2: Jan 23, 2018

**Today's Progress**:
- Grads are now updating
- Needs to review update by hand

**Details**:
- NN learns when using loss function
- NLLLoss is just a negative in pytorch (it expects the input to be in a log form)
- Use CrossEntropyLoss without softmax in the last layer
- Use NLLLoss with *logsoftmax* in last layer

### Day 3: Jan 24, 2018

**Today's Progress**
- Studied how pytorch uses Cpp code (torch/csrc)
- Studied on how to use python with C/Cpp

**Details**:
- Needs to see how pytorch compiles Cpp code
- CONTRIBUTING.md provides more details
- Given a object (e.g. function), function.h holds *only* C code and python_function.h and python_function.cpp contains python wrappers to C code.
