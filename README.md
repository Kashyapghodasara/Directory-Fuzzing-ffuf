# Directory-Fuzzing-ffuf
**ffuf** stands for **“Fuzz Faster U Fool.”** It is a fast web fuzzer written in Go and is commonly used for discovering web content and testing different parts of HTTP requests. It's a tool used for web enumeration, fuzzing, and directory brute forcing <br><br>
Its basic idea is simple: give ffuf many candidate values from a wordlist, put each value where you place the FUZZ keyword, send the requests, and inspect which responses look interesting.

### Requirement : Seclists
**SecLists** is a collection of multiple types of lists used during security assessments. List types include usernames, passwords, URLs, sensitive data patterns, fuzzing payloads, web shells, and many more.
