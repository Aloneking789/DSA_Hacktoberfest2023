# Tower of Hanoi Algorithm

The following code implements the Tower of Hanoi problem, a classic example of a recursive algorithm.

1. The code defines a recursive function `tower_of_hanoi` with the following parameters:
   - `n`: the number of disks to be moved.
   - `source`: the source peg from which disks are moved.
   - `auxiliary`: an auxiliary peg used for intermediate storage.
   - `target`: the target peg where the disks need to be moved.

2. The base case is when `n` is equal to 1. In this case, the function simply prints the move to transfer the smallest disk from the source peg to the target peg.

3. For cases where `n` is greater than 1, the algorithm proceeds as follows:
   - It recursively moves `n-1` disks from the source peg to the auxiliary peg (using the target peg as the auxiliary in the recursive call).
   - It then prints the move to transfer the remaining largest disk from the source peg to the target peg.
   - Finally, it recursively moves the `n-1` disks from the auxiliary peg to the target peg (using the source peg as the auxiliary in the recursive call).

#### Example Usage

You can use the `tower_of_hanoi` function to solve the Tower of Hanoi problem for any number of disks. Here's an example:

```python
n = 3  # Number of disks
tower_of_hanoi(n, 'A', 'B', 'C')
def tower_of_hanoi(n, source, auxiliary, target):
    if n == 1:
        print(f"Move disk 1 from {source} to {target}")
        return
    tower_of_hanoi(n - 1, source, target, auxiliary)
    print(f"Move disk {n} from {source} to {target}")
    tower_of_hanoi(n - 1, auxiliary, source, target)

# Example usage
n = 3  # Number of disks
tower_of_hanoi(n, 'A', 'B', 'C')
```

