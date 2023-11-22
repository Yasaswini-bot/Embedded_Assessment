# Embedded_Assessment
1.Circular Queue Implementation in Python

Overview

This Python class provides a basic implementation of a circular queue. A circular queue is a data structure that follows the First In, First Out (FIFO) principle, with the added feature that when the queue is full, writing new data overwrites the oldest data.

CircularQueue Class

Initialization

class CircularQueue:
    def __init__(self, capacity):
        """Initialize a circular queue with a specified capacity.

        Args:
            capacity (int): The maximum capacity of the circular queue.
        """
        self.capacity = capacity
        self.queue = [None] * capacity
        self.read_index = 0
        self.write_index = 0

Methods

is_empty():

def is_empty(self):

    """Check if the circular queue is empty.

    Returns:
        bool: True if the queue is empty, False otherwise.
    """
    
is_full():

def is_full(self):

    """Check if the circular queue is full.

    Returns:
        bool: True if the queue is full, False otherwise.
    """
    
read_queue():

def read_queue(self):

    """Read the oldest data from the queue.

    Returns:
        Any: The oldest data in the queue, or None if the queue is empty.
    """
    
write_queue(data):

def write_queue(self, data):

    """Write data to the queue.

    If the queue is full, the oldest data is overwritten.

    Args:
        data: The data to write to the queue.
    """
    
clear_queue():

def clear_queue(self):

    """Clear the circular queue."""    


2.extract_payload Function

Overview

The extract_payload function is designed to extract payload data from a given input array based on a specific data format. The function checks if the input array is of sufficient length and, if so, retrieves the payload length and extracts the corresponding payload data.

Function Signature

def extract_payload(input_array):

    """Extracts the payload from the given data and returns the payload data in a new array.

    Args:
        input_array: The input array containing the data.

    Returns:
        A new array containing the payload data, or None if the input array is not sufficient.
    """

Usage

input_array = [0o0, 0o2, 0o0, 0o11, 0o1, 0o1, 0o2, 0o3, 0o4, 0o5, 0o6, 0o7, 0o10, 0o11, 0o12, 0o13, 0o14, 0o15, 0o16, 0o17] 

output_array = extract_payload(input_array)

print(output_array)

In the provided example, the extract_payload function is used with an input array containing octal values. The output will be the payload data extracted from the input array.

Function Behavior

If the length of the input array is greater than or equal to 6 (indicating the presence of sufficient data), the function extracts the payload length from the element at index 4.
The payload data is then extracted from the input array starting from index 5 and spanning the length of the payload.
The extracted payload data is returned as a new array.
If the input array is not sufficient (length < 6), the function returns None.    
