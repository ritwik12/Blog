---
layout: post
title: A Basic Neural Network!!
---

<p style="text-align:justify;">
This post consist of A Basic Neural Network Implementation using Tensorflow, Keras, Numpy and Python.</p>

<h3>Tensorflow</h3>

<p style="text-align:justify;">
Deep neural networks are all about networks of neurons, with each neuron learning to do its own operation as part of a larger picture. 
Data such as images enters this network as input, and flows through the network as it adapts itself at training time or predicts outputs in a deployed system.
</p>

<p style="text-align:justify;">
Tensors are the standard way of representing data in deep learning. Simply put, tensors are just multidimensional arrays, an extension of two-dimensional tables (matrices) to data with higher dimensionality. Just as a black-and-white (grayscale) images are represented as “tables” of pixel values, RGB images are represented as tensors (three-dimensional arrays), with each pixel having three values corresponding to red, green, and blue components.</p>

<p style="text-align:justify;">
In TensorFlow, computation is approached as a dataflow graph (Figure below). Broadly speaking, in this graph, nodes represent operations (such as addition or multiplication), and edges represent data (tensors) flowing around the system.</p>

![_config.yml]({{ site.baseurl }}/images/tensorflow.png)
<i>A dataflow computation graph. Data in the form of tensors flows through a graph of computational operations that make up our deep neural networks.</i>

<h3>TensorFlow Architecture</h3>

<p style="text-align:justify;">
Tensorflow architecture works in three parts:</p>

<ul>
  <li>Preprocessing the data</li>
  <li>Build the model</li>
  <li>Train and estimate the model</li>
</ul> 

<p style="text-align:justify;">
It is called Tensorflow because it takes input as a multi-dimensional array, also known as tensors. You can construct a sort of flowchart of operations (called a Graph) 
that you want to perform on that input. The input goes in at one end, and then it flows through this system of multiple operations and comes out the other end as output.
<br> <br>
  
This is why it is called TensorFlow because the tensor goes in it flows through a list of operations, and then it comes out the other side.</p>

<h3>Keras</h3>

<p style="text-align:justify;">
Keras is a minimalist Python library for deep learning that can run on top of Theano or TensorFlow.
<br> <br>

It was developed to make implementing deep learning models as fast and easy as possible for research and development.
<br> <br>

It runs on Python 2.7 or 3.5 and can seamlessly execute on GPUs and CPUs given the underlying frameworks. It is released under the permissive MIT license.</p>

<h3>Installation</h3>


Create a Virtual Environment 

```
pip3 install virtualenv

virtualenv -p ~/home tensorflow
```

Activate Virtual Environment 

```
source ~/home/tensorflow/bin/activate
```

Install Tensorflow

```
pip3 install tensorflow
```

Install Keras

```
pip3 install Keras
```
Install Numpy

```
pip3 install numpy
```

<h3>Artificial Neural Network</h3>

<p style="text-align:justify;">
In Layman's terms a Artificial Neural Network is the artificial implementataion of how the human brain works, It consists of 
Neurons which we call Nodes or units.
</p>
<p style="text-align:justify;">
A neural network is composed of a number of nodes, or units, connected by links. Each link
has a numeric weight associated with it. Weights are the primary means of long-term storage
in neural networks, and learning usually takes place by updating the weights. Some of the units
are connected to the external environment, and can be designated as input or output units. The
weights are modified so as to try to bring the network's input/output behavior more into line with
that of the environment providing the inputs.</p>

<p style="text-align:justify;">
Artificial Neural Networks are of different types. Such as Convolutional Neural Network (CNN), Recurrent Neural Network (RNN), etc. A very basic single layer neural network is known as Perceptron. We will not go into much detail here.
</p>

<h3>Implementation</h3>

We will start with a very basic mathematical relation between X and Y. 

![_config.yml]({{ site.baseurl }}/images/xandy.png)

<p style="text-align:justify;">
Here, Different values of X and Y are given. There's a formula that maps X to Y. Computing that manually is kind of tough as we need to do lots of Hit and trials to arrive at a conclusion.
</p>

So, the conclusion is:

```
Y = 2X - 1
```

We can use a Neural Network to compute this for us in fraction of seconds. What a Neural Network will do is to guess the value
again and again just like we were doing by Hit and Trial.
<br><br>
Below is the code to implement this,
<br><br>

<script src="https://gist.github.com/ritwik12/3d3f34c652bccd045ff1e0898568162c.js"></script>

<br><br>
This code will give the following output:

![_config.yml]({{ site.baseurl }}/images/outputneural.png)

Here, We can see that we got the value of Y as 18.987537 for a X = 10.0.

We should have got Y = 19.0 but as we have trained our model for 500 epochs only and that too with very little training data i.e just 6 values of X and Y. So this much discrepancies in results are common and ewxpected.

