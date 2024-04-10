# A Kernel Seedling
We create a /proc/count file that shows the current number
of running processes. 

## Building
```shell
make
sudo insmod proc_count .ko
```

## Running
```shell
cat /proc/count
```
number of processes (as outputted): 134

## Cleaning Up
```shell
sudo rmmod proc_count
```

## Testing
```python
python -m unittest
```
Ran 3 tests in 9.368s
OK

Report which kernel release version you tested your module on
(hint: use `uname`, check for options with `man uname`).
It should match release numbers as seen on https://www.kernel.org/.

```shell
uname -r -s -v
```
Linux 5.14.8-arch1-1