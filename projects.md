---
title: /projects
layout: page
permalink: /projects
---

# Projects that I'm involved

## [Sydr](https://www.ispras.ru/en/technologies/sydr/) a dynamic symbolic execution tool

Sydr is an automatic test generation tool for complex programs that finds errors
and increases code coverage during testing. Sydr constructs the program’s
mathematical model that allows a fuzzer to explore new execution paths that are
hard to follow via genetic mutation approaches. The tool advances further the
dynamic symbolic execution approach used earlier in Avalanche and Anxiety
analyzers developed in ISP RAS. In contrast with similar open source tools, Sydr
ensures the correctness of generated input data by checking whether the newly
found execution path has the target conditional branches inverted.

Sydr provides:

* Given an execution path, Sydr inverts all conditional branches that depend
on input data. It also supports parallel branches inversion;
* ISP Fuzzer integration to reach the code behind the branches depending on
comparisons with constants;
* Reverse engineering automation such as assisting an expert in reaching a
given program point or collecting a trace of instructions that depend on input
data;
* Support for various input data sources (files, network sockets, environment
variables, standard input stream, command line arguments);
* Security predicates that are used to find errors and to generate input data
to reproduce them (for division by zero, null pointer dereference, out of bounds
access, integer overflow);
* Symbolic execution of multithreaded programs;
* Indirect jumps inversion (in switch statements);
* Formula slicing. Sydr eliminates redundant formulas (not influencing the
conditional branch being inverted) from the path predicate. This feature solves
the problem of undertainting and speeds up SMT solver work for generated
queries.


## [Casr](https://www.ispras.ru/en/technologies/casr/) core dump analysis and severity reporter tool

Casr creates automatic reports for fatal errors happened during program testing
or deployment. The tool works by analyzing Linux coredump files. The resulting
reports contain the fatal error’s severity and additional data that is helpful
for pinpointing the error cause.

Casr provides:

* Detecting critical program faults that can lead to hijacking control flow. 
* Classifying fatal errors into one of 23 classes based on a program state
at a crash time (function return address corruption, null pointer dereference
etc.). Fatal errors are further grouped based on severity, such as exploitable,
potentially exploitable, or denial of service errors.
* Collecting a list of open files and network connections that could be the
reason of a crash.
* An extended error report containing the fatal error’s severity and other
data (OS and package versions, executed command line, call stack, open files and
network connections, register state etc.).
* Reports for hard to reproduce errors such as non-deterministic errors,
cases when the original execution environment is hard or impossible to
reconstruct etc.).
* Integration with monitoring tools (such as Zabbix) that allows system
administrators and devops to receive on the fly notifications about critical
program crashes.
