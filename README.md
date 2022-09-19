# How to simulate 10000 concurrent users accessing your system

There are many enterprise services that can test your system to simulate heavy traffic. However, there are two free programs to do it if your system doesn't have billions of users like Facebook. One is using a desktop application called JMeter. The other one is using a program called 'siege' using a single command line.

## 1. JMeter
https://www.guru99.com/jmeter-performance-testing.html

## 2. siege

`$ sudo apt-get install siege`

`$ siege -c30 -t10M http://localhost:3000` (30 concurrent users for 10 minutes)

## How many concurrent users should I test for?

The real issue is not what kind of tools you need to use, but how many concurrent users you should test for and for how long. Answers to these can only come from a real experience. If you have a couple of million registered users for your service, a few hundred concurrent user for a few hours would a normal number for a busy day. This was the case for my booking systems with 7 million registered users.

Start with a low number and gradually increase it. You really don't have to test for 10000 concurrent user especially if the system will be on an elastic/scalable server instance. Even with the most sophisticated stress tests, you won't be able to test for the situation when millions of people in the world want to access your system all at once. They all have different environments.

Please, message me if you want to use my expertise in load balancing projects. Most issues are with the design of the software.
