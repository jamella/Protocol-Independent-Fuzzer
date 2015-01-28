Protocol Independent Fuzzer 
===========================
Version 1.0 12/15/2015

There are 3 requirements to use the fuzzer.

Requirements:
1. Protocol Library
2. Protocol Error Library
3. Templates

A protocol library meaning inputs to actually talk to the specific protocol you have selected to run. This can either be generated by a script or manually.

A protocol error library meaning all of the error codes and descriptions associated with the protocol you have selected to run. This will help determine if the protocol is functioning as it should. 

A template is a collection of packets. This template is manipulated and saved as a different name. Currently, the fuzzer will look for anything you specify when you set up your class. This allows for easy recreation and logging if something unusual happens when running the fuzzer with the current template.


Running the fuzzer:

There are two example classes in fuzzer.py. RDPFuzzer and HTTPFuzzer both will run the fuzzer but for two different protocols. 

When you create your class, there are a number of things that should be defined.

1. Set the target you want to test against.
2. Set the port you want to test against.
3. Set the transport it will either be UDP/TCP.
4. Set the path as this allows you to have a location for all of your templates
5. Set the template type. A template type is something that you want to use to identify that it is a template and should be used when the fuzzer is ran.