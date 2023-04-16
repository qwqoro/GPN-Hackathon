![banner](banner.gif)

<p align="center">
    <code> [ Solution to the Task 1: <a href="GPN_Task-1.pdf"><code>GPN_Task-1.pdf</code></a> ] </code><br>
  	<code> [ Solution to the Task 2: <a href="GPN_Task-2.pdf"><code>GPN_Task-2.pdf</code></a> ] </code><br>
  	<code> [ Solution to the Task 3: <a href="GPN_Task-3_Rules"><code>GPN_Task-3_Rules</code></a> ] </code><br><br>
  	Brief overviews: &nbsp; <b>
		<a href="#-overview-task-1">Task 1</a> |
		<a href="#-overview-task-2">Task 2</a> |
		<a href="#%EF%B8%8F-overview-task-3">Task 3</a>
	</b>
</p><br>

> My solution to the tasks given within the Gazprom Neft Hackathon of the year 2023.


# 🔍 Overview: Task 1

### Problem
The task was to review code stored within [the provided files](https://github.com/gpn-intern/vuln-code) (_\*each file represents an independent web application_) and to create [a report](GPN_Task-1.pdf) regarding vulnerabilities found during the analysis.

### Results
| Case № | Technologies | Findings |
| :-- | :-: | :-- |
| [1](https://github.com/gpn-intern/vuln-code/tree/main/Пример%201) | `Python`, `Flask` | `[Relative Path Traversal]` [`[CWE-23]`](https://cwe.mitre.org/data/definitions/23.html) |
| [2](https://github.com/gpn-intern/vuln-code/blob/main/Пример%202.txt) | `JS`, `PHP` | `[Cross-Site Scripting]` [`[CWE-159]`](https://cwe.mitre.org/data/definitions/159.html) |
| [3](https://github.com/gpn-intern/vuln-code/blob/main/Пример%203.txt) | `JS` | `[Cross-Site Scripting]` [`[CWE-159]`](https://cwe.mitre.org/data/definitions/159.html) [`[CWE-360]`](https://cwe.mitre.org/data/definitions/360.html) |
| [4](https://github.com/gpn-intern/vuln-code/blob/main/Пример%204.txt) | `Go` | `[Broken Authentication]` [`[CWE-287]`](https://cwe.mitre.org/data/definitions/287.html) |
| [5](https://github.com/gpn-intern/vuln-code/blob/main/Пример%205.txt) | `C` | `[Buffer Overflow]` [`[CWE-120]`](https://cwe.mitre.org/data/definitions/120.html) |
| [6](https://github.com/gpn-intern/vuln-code/blob/main/Пример%206.txt) | `NodeJS` | `[CORS Misconfiguration]` [`[CWE-942]`](https://cwe.mitre.org/data/definitions/942.html) |
| [7](https://github.com/gpn-intern/vuln-code/blob/main/Пример%207.txt) | `PHP` | `[Absolute Path Traversal]` [`[CWE-36]`](https://cwe.mitre.org/data/definitions/36.html) `[Server-Side Request Forgery]` [`[CWE-918]`](https://cwe.mitre.org/data/definitions/918.html) |
| [8](https://github.com/gpn-intern/vuln-code/blob/main/Пример%208.txt) | `JS` | `[OpenRedirect]` [`[CWE-601]`](https://cwe.mitre.org/data/definitions/601.html) `[Cross-Site Scripting]` [`[CWE-83]`](https://cwe.mitre.org/data/definitions/83.html) |
| [9](https://github.com/gpn-intern/vuln-code/blob/main/Пример%209.txt) | `Python`, `Flask` | `[Server-Side Template Injection]` `[Command Injection]` [`[CWE-1336]`](https://cwe.mitre.org/data/definitions/1336.html) |

# 💻 Overview: Task 2

### Problem
The task was to examine [the provided web application](https://github.com/gpn-intern/vuln-app) and to create [a report](GPN_Task-2.pdf) regarding vulnerabilities found during the analysis.

### Results
I have separately conducted both White-box and Black-box testing of the provided web application to evaluate security from the point of view of both the developer and the potential attacker.

| Method of software testing | Findings |
| :-- | :-- |
| White-box | `[Weak credentials]` [`[CWE-1391]`](https://cwe.mitre.org/data/definitions/1391.html) |
| White-box | `[Hard-coded plaintext credentials]` [`[CWE-798]`](https://cwe.mitre.org/data/definitions/798.html) |
| White-box | `[Hard-coded plaintext secret key]` [`[CWE-321]`](https://cwe.mitre.org/data/definitions/321.html) |
| Black-box, White-box | `[Debug mode on]` [`[CWE-489]`](https://cwe.mitre.org/data/definitions/489.html) |
| Black-box, White-box | `[SQL Injection]` [`[CWE-89]`](https://cwe.mitre.org/data/definitions/89.html) [`[CVE-2022-34265]`](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-34265)

# ⌨️ Overview: Task 3

### Problem
The task was to write <a href="https://github.com/returntocorp/semgrep">Semgrep</a> rules that would find bugs that lead to the vulnerabilities listed above in <a href="#results">the overview of the Task 1</a> and <a href="#results-1">the overview of the Task 2</a>.

### Results
- Have a look at the resulting rules: <a href="GPN_Task-3_Rules"><code>GPN_Task-3_Rules</code></a></br>
- And have a look at the resulting [Semgrep](https://github.com/returntocorp/semgrep) report: <a href="GPN_Task-3_Report.txt"><code>GPN_Task-3_Report.txt</code></a>
