# IT314 - Software Engineering <br>
## Lab 5 - Static Analysis
****
Name : Devdeep Shetranjiwala  
Student ID: 202001150
****
> Static Analysis: <br>
Static analysis is a method of examining the source code of a software program without
executing it.


> Static Analysis Tools:<br>
Static analysis tools are software tools that analyze the source code of a program without
executing it.


Tool of my choice for this lab : 
```
pylint
```
I used poweshell to do this lab.<br>
How to install :
```
pip install pylint 
```
How to use :
```
python -m pylint <file name> 
```
For more info : 
```
https://pypi.org/project/pylint/
```

 Github repository to analyze file : 
   ```
https://github.com/Devdeep-J-S/Python.git
```
 There are 5 types of error : 
|Pylint category | Description |
|----------------|-------------|
|Convention (C)|Programming standard violation|
|Refactor (R)|Bad code smell|
|Warning (W)|Python-specific problems|
|Error (E)|Likely code bugs|
|Fatal (F)|An error prevented further Pylint processing|

Code : 
```
 https://github.com/Devdeep-J-S/Python/blob/master/neural_network/convolution_neural_network.py
 ```
Output :
 ![Output of pylint](https://github.com/Devdeep-J-S/Lab-5_202001150/blob/main/images/Screenshot%20(2).png)
 
 Understanding the errors:<br>
 As mentioned earlier in type of errors this code covers most of the errors.
 Some types are mentioned here : 
 ```
 * C0116: Missing function or method docstring (missing-function-docstring)
 * C0200: Consider using enumerate instead of iterating with range and len (consider-using-enumerate)
 * C0103: Variable name "rp" doesn't conform to snake_case naming style (invalid-name)
 * R0913: Too many arguments (8/5) (too-many-arguments)
 * E0401: Unable to import 'matplotlib' (import-error)
 * W0105: String statement has no effect (pointless-string-statement)
 * W0612: Unused variable 'data_focus1' (unused-variable)
 ```
 ## Another examples : <br>
 Code : 
 ```
 https://github.com/Devdeep-J-S/Python/blob/master/dynamic_programming/viterbi.py
 ```
 Output :
![Output](https://user-images.githubusercontent.com/75716586/227497620-4e65a097-900b-406d-b4d5-a5779ae013b6.png)

 Code : 
 ```
 #!/usr/bin/env python3


def climb_stairs(number_of_steps: int) -> int:
    """
    LeetCdoe No.70: Climbing Stairs
    Distinct ways to climb a number_of_steps staircase where each time you can either
    climb 1 or 2 steps.

    Args:
        number_of_steps: number of steps on the staircase

    Returns:
        Distinct ways to climb a number_of_steps staircase

    Raises:
        AssertionError: number_of_steps not positive integer

    >>> climb_stairs(3)
    3
    >>> climb_stairs(1)
    1
    >>> climb_stairs(-7)  # doctest: +ELLIPSIS
    Traceback (most recent call last):
        ...
    AssertionError: number_of_steps needs to be positive integer, your input -7
    """
    assert (
        isinstance(number_of_steps, int) and number_of_steps > 0
    ), f"number_of_steps needs to be positive integer, your input {number_of_steps}"
    if number_of_steps == 1:
        return 1
    previous, current = 1, 1
    for _ in range(number_of_steps - 1):
        current, previous = current + previous, current
    return current


if __name__ == "__main__":
    import doctest

    doctest.testmod()
```


 Output : <br>
![Output](https://user-images.githubusercontent.com/75716586/227498303-dd4dbfdc-36c8-4ecf-b912-0bd63f9576d9.png)
 
