# Motivation
- reliable
- efficient

connection is abstracted as "wire-like"

Unit: Frame

# Problem
- channels make errors
- nonzero propagation delay

# Solution
- detect
- correct

# Functions
- Providing a well-defined service interface to the network layer
- Dealing with transmission errors
- Regulating the flow of data so that slow receivers are not swamped by fast senders

A frame(structure): Flag Header Payload-field Trailer Flag

# RELIABILITY IS AN OVERALL GOAL

# Services To Network layer
- Transferring data from the network layer (source machine -> destination machine)
- Transmit the bits to destination machine

# Designed to offer:
- Unacknowledged connectionless service (Ethernet, no guarantee)
- Acknowledged connectionless service (wireless systems: 802.11 WIFi, each frame individually Acknowledged)
- Acknowledged connection-oriented service (frame sent numbered, right order)
    - first phase: exchange both init_var and counters for keeping track of
    - second phase: transmit frames
    - third phase : release connection, free up vars, buffers and resourses 


# Framing
- Byte count: in frame's header, specify number of bytes (count may be wrong during transmitting, and then misunderstand the right start and end point)
- Flag bytes with byte stuffing: Flag byte on the start and end of the frame, one frame two flags, Two consecutive flag bytes indicate the end of one frame and the start of the next.
- Flag bits with bit stuffing: flag may be same as some data, insert a special escape byte (ESC) just before each ‘‘accidental’’ flag byte in the data
                                 removes the escape bytes before giving the data to the network layer. This technique is called byte stuffing.
- Physical layer coding violations:


# Error Control

# Flow Control

