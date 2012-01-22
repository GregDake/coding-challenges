Generate Unique Identifiers
============================

Problem
-------
We need to have a utility that generates unique identifiers for a system that runs on multiple machines across several geographically dispersed data centers.  The code will be used for assigning ID’s to messages sent into the system.  The unique identifier code should have no dependency on shared state between data centers since we don't want to introduce dependencies, we want this critical system to be resilient.  In order to perform well the identity generator should not have to read from disk (including a relational database).

Devise a scheme for creating unique identifiers, preferably this scheme allows you to determine which machine and data center generated a given id.  Your challenge is to store the data into a 64 bit long.  You should write the code to generate a new unique identifier, and code to decode/encode from and to the 64 bit representation.

Ideally your scheme will allow for versioning so that we can evolve the scheme in the future as needed.

Discuss the limitations of your scheme.  One example limitation may be that you can only support 1024 identifiers per machine per second.  Therefore you are limiting to 1024 messages/sec per machine, this is a reasonable limitation.  Another such limitation may be how many machines the scheme would support, for example using 6 bits for the machine storage would limit the number of machines to 64.

Sample Test Cases
-----------------

There are not any test cases since this is an open ended challenge.
