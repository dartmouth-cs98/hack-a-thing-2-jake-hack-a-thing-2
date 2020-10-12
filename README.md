# Jake's Hack-a-thing #2

## Background

Last Hack-a-thing, I decided to learn Pytorch, a python based library for machine learning. This hack-a-thing, I extended my Pytorch learnings to learn Pysyft - a Python based libary that uses Pytorch to implement federated learning. Pysyft allows you to send ML models to distributed data sources ("workers"). In this example, these "Workers" are virtualized. In real life, the workers are actual devices.

## Walk-through

The first section of my Hack-a-thing 2 is dedicated to this tutorial - all the basic notes and examples of how to use Pysyft and the nuances of how it handshakes with Pytorch.

The second section is a multi-class classifier I built myself in pytorch transformed to work accross distributed data using Pysyft. It classifies bonds using 6 features to 1 of 21 bond rating classes. This classifier is trained in a federated way - on Alice and Bob's datasets then averaged/combined by a secure worker before being sent back to the local machine. It actually simulates federated learning happenin in real time

## What I learned

How to use Pysyft to perform federated learning. More of the nuances of Pytorch

## What didn't work

I still had trouble getting this to run on my GPU (1080ti). Training on the CPU is slow and inefficient so for actual Pytorch/Pysyft projects will have to figure out how to resolve the CUDA exceptions that were being thrown. In general this federated learning approach was incredibly slow. There are some ways proposed to accelerate the process that I still have to read/learn about.