# Results

I built xv6 in the `xv6/` folder on the Linux/IIT setup (had to skip my Mac — no cross-compiler there). Started QEMU with `make qemu-nox`, then at the xv6 shell I ran:

```text
testsymlink
```

Everything passed. Output looked basically like:

```text
PASS: symlink created
PASS: read through symlink
PASS: loop detected (open failed)
testsymlink done
```

So symlink creation works, reads follow the symlink to the real file, and a tiny loop hits the depth limit and `open` fails like it should.
