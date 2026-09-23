# Stack and Queue Python Package

## Aim

To develop a reusable Python package implementing Stack and Queue using type hints and dataclasses.

## Features

* Stack implementation
* Queue implementation
* Generic type hints
* Python dataclasses
* Simple and reusable code
* Basic operations such as push, pop, enqueue and dequeue

## Package Structure

```text
data_structures/
│
├── __init__.py
├── stack.py
├── queue.py
│
├── main.py
└── README.md
```

## Stack

Stack follows the **LIFO (Last In, First Out)** principle.

### Operations

* `push()` - adds an element
* `pop()` - removes the top element
* `peek()` - returns the top element
* `is_empty()` - checks whether the stack is empty

### Example

```python
from data_structures import Stack

stack = Stack[int]()

stack.push(10)
stack.push(20)
stack.push(30)

print(stack.peek())
print(stack.pop())
```

### Output

```text
30
30
```

## Queue

Queue follows the **FIFO (First In, First Out)** principle.

### Operations

* `enqueue()` - adds an element
* `dequeue()` - removes the first element
* `front()` - returns the first element
* `is_empty()` - checks whether the queue is empty

### Example

```python
from data_structures import Queue

queue = Queue[str]()

queue.enqueue("A")
queue.enqueue("B")
queue.enqueue("C")

print(queue.front())
print(queue.dequeue())
```

### Output

```text
A
A
```

## Data and Result

### Stack Data

```text
10, 20, 30
```

After one pop:

```text
10, 20
```

### Queue Data

```text
A, B, C
```

After one dequeue:

```text
B, C
```

## Complexity Analysis

| Operation      | Stack | Queue |
| -------------- | ----: | ----: |
| Push / Enqueue |  O(1) |  O(1) |
| Pop            |  O(1) |  O(n) |
| Peek / Front   |  O(1) |  O(1) |
| Is Empty       |  O(1) |  O(1) |
| Space          |  O(n) |  O(n) |

For the implemented list-based Queue, `dequeue()` takes O(n) because removing the first element shifts the remaining elements.

## Inference

The package successfully implements Stack and Queue as reusable generic classes. Dataclasses reduce boilerplate code, while type hints make the code easier to understand and maintain.

## Conclusion

Stack and Queue are successfully implemented using Python dataclasses and type hints. The package can be imported and reused in different Python applications.
