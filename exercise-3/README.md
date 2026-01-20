# Stack Corruption Mitigation Exercise

## Roadmap

* Compile a program vulnerable to stack corruption
  * Demonstrate the vulnerability
* Enable linkage-based compartmentalisation
  * Show that the vulnerability is mitigated
* Use `gdb` to understand why the vulnerability is mitigated
  * Backtrace: `bt`
  * List compartments: `info compartments`
 
## Instructions

1. Run `make normal` to build the vulnerable program.
   * Run `./normal`.
   * What stack addresses do you see? Can you reach one from the other?
   * Can you successfully corrupt data in the caller's frame from the callee?
2. Now run `make compart` to build the compartmentalised program.
   * Run `./compart`.
   * What stack addresses do you see? Can you reach one from the other?
   * It is impossible to corrupt data in the caller's frame from the callee. Why?

## References

CheriBSD manual: [`c18n(7)`](https://man.cheribsd.org/cgi-bin/man.cgi/c18n)
