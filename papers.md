---
title: /papers
layout: page
permalink: /papres
---

# Papers

## Sydr: Cutting Edge Dynamic Symbolic Execution
\[[paper](https://arxiv.org/abs/2011.09269)\]

Vishnyakov A., Fedotov A., Kuts D., Novikov A., Parygina D., Kobrin E.,
Logunova V., Belecky P., Kurmangaleev Sh. Sydr: Cutting Edge Dynamic Symbolic
Execution. 2020 Ivannikov ISPRAS Open Conference (ISPRAS), IEEE, 2020, pp.
46-54. DOI: 10.1109/ISPRAS51486.2020.00014

### Abstract

The security development lifecycle (SDL) is becoming an industry standard.
Dynamic symbolic execution (DSE) has enormous amount of applications in computer
security (fuzzing, vulnerability discovery, reverse-engineering, etc.). We
propose several performance and accuracy improvements for dynamic symbolic
execution. Skipping non-symbolic instructions allows to build a path predicate
1.2--3.5 times faster. Symbolic engine simplifies formulas during symbolic
execution. Path predicate slicing eliminates irrelevant conjuncts from solver
queries. We handle each jump table (switch statement) as multiple branches and
describe the method for symbolic execution of multi-threaded programs. The
proposed solutions were implemented in Sydr tool. Sydr performs inversion of
branches in path predicate. Sydr combines DynamoRIO dynamic binary
instrumentation tool with Triton symbolic engine. We evaluated Sydr features on
64-bit Linux executables.

## CASR: core dump analysis and severity reporter tool
\[[russian&nbsp;paper](https://ispranproceedings.elpub.ru/jour/article/download/1317/1106)\]
Fedotov A. N., Kurmangaleev S. F. CASR: core dump analysis and severity reporter
tool //Proceedings of the Institute for System Programming of the RAS. – 2020. –
vol. 32. – №. 4. – pp. 89-96 (in Russian). DOI: 10.15514/ISPRAS-2020-32(4)-6

### Abstract

Despite the fact that software development uses various technologies and
approaches to diagnose errors in the early stages of development and testing,
some errors are discovered during operation. To the user, errors often look like
a program crash while running. To collect reports on program crashes, a special
analysis component is built into the operating system. Such a component is
present in both Windows OS and Linux-based OS, in particular Ubuntu. An
important parameter is the severity of the error found, and this information is
useful to both the developer of the distribution kit and the user. In
particular, users with such diagnostics can take organizational and technical
measures before the release of a bug fix from the software developer. The
article introduces CASR: a tool for analyzing a memory image at the time of a
process termination (coredump) and reporting errors. The tool allows you to
assess the severity of the detected crash by analyzing the memory image, as well
as collect the necessary information for the developer to help fix the defect.
Such information is: OS distribution version, package version, process memory
card, state of registers, values of environment variables, call stack, signal
number that led to abnormal termination, etc. Severity assessment enables the
software developer to correct errors, which are the most dangerous in the first
place. CASR can detect files and network connections that were open at the time
of the crash. This information will help reproduce the error, and will help
users and administrators take action in the event of an attack on the system.
The tool is designed to work on Linux OS and supports x86 / 64, armv7
architectures and can be supplied as a package for Debian-based distributions.
The tool has been successfully tested with several open source bugs.

## Crash Processing for Selection of Unique Defects
\[[paper](https://link.springer.com/content/pdf/10.1134/S0361768818060154.pdf)\]
Niskov F. V., Fedotov A. N., Kurmangaleev S. F. Crash processing for selection
of unique defects //Programming and Computer Software. – 2018. – pp. 44. – №. 6.
– pp. 445-452. DOI: 10.1134/S0361768818060154

### Abstract

Nowadays, software developers often face the following problem: there is a large
amount of inputs that cause the program to crash. In practice, this amount of
inputs is too large to be analyzed manually in a reasonable time. This paper
contains an overview and analysis of existing methods for this problem. A new
method for analyzing crashes to select unique defects is proposed. The method is
based on comparison of control flow graphs (CFGs). For this purpose, a special
metric is introduced: the graphs are considered similar if the metric does not
exceed a certain threshold, which is a filtering parameter. Information about
the graphs is collected dynamically at runtime through instrumentation of the
program’s binary code. The method is applicable to binary executables and does
not require any debugging information. The developers, having estimated their
time and effort, can significantly reduce the number of crashes to be analyzed.
In addition, an effective algorithm for fixing software bugs that cause crashes
is proposed. The method is implemented as part of the fuzzer developed at the
Institute for System Programming of the Russian Academy of Sciences (ISP RAS)
and tested on a set of programs for x86-64/Linux. The test results show that the
number of crashes to be analyzed can be reduced by several times.

## Software defect severity estimation in presence of modern defense mechanisms
\[[russian&nbsp;paper](http://www.ispras.ru/proceedings/docs/2016/28/5/isp_28_2016_5_73.pdf)\]

Fedotov A.N., Padaryan V.A., Kaushan V.V., Kurmangaleev Sh.F., Vishnyakov
A.V., Nurmukhametov A.R. Software defect severity estimation in presence of
modern defense mechanisms. Trudy ISP RAN/Proc. ISP RAS, vol. 28, issue 5, 2016.
pp. 73-92 (in Russian). DOI: 10.15514/ISPRAS-2016-28(5)-4

### Abstract

This paper introduces a refined method for automated exploitability evaluation
of found program bugs. During security development lifecycle a significant
number of crashes is detected in programs. Because of limited resources, bug
fixing is time consuming and needs prioritization. It should be the matter of
highest priority to fix exploitable bugs. Automated exploit generation technique
is used to solve this problem in practice. Generated exploit confirms the
presence of a critical vulnerability. However, state-of-the-art publications
omit modern defense mechanisms preventing exploitation. It results in lowering
of an evaluation quality. This paper considers modern vulnerability exploitation
prevention mechanisms. An evaluation of their prevalence and efficiency is also
presented. The method can be applied to program binaries and doesn’t require any
debug information. Proposed method is based on symbolic interpretation of traces
obtained by a full-system emulator. Our method can demonstrate a real
exploitability for stack buffer overflow vulnerability with write-what-where
condition even when DEP, ASLR, and “canary” operate together. The implemented
method capabilities were shown on model examples and real programs.

## Automated exploit generation for stack buffer overflow vulnerabilities
\[[paper](https://link.springer.com/content/pdf/10.1134/S0361768815060055.pdf)\]

Padaryan V. A., Kaushan V. V., Fedotov A. N. Automated exploit generation for
stack buffer overflow vulnerabilities //Programming and Computer Software.
2015, vol. 41, No. 6, pp. 373-380. DOI: 10.1134/S0361768815060055

### Abstract

An automated method for exploit generation is presented. This method allows one
to construct exploits for stack buffer overflow vulnerabilities and to
prioritize software bugs. The method is based on the dynamic analysis and
symbolic execution of programs. It could be applied to program binaries and does
not require debug information. The proposed method was used to develop a tool
for exploit generation. This tool was used to generate exploits for eight
vulnerabilities in Linux and Windows programs, of which three were not fixed at
the time this paper was written.
