## DevSecOps

- Refers to integrating security practices in DevOps Security model

- Average cost of data breach in 2020 is $2.86 million, global cyber crime $6 trillion

- 90% of webapp is vulnerable to hacking & 68% are vulnerable to breach of sensitive data in 2020

### Terminologies

**Vulnerability**: Security vulnerability is the code flow or a system misconfiguration that hacker can use to gain unauthorized access to a system or network.

**Exploit**: The method used to exploit a vulnerability. Usually a custom software or a sequence of commands. Exploit kits can be embedded in web pages to scan for vulnerabilities and inject malware or viruses when weakness is found.

**Threat**: Actual or hypothetical event in which one or more exploits use a vulnerability to mount an attack

## Web App Vulnerabilities

### Types of vulnerabilities

- Common vulnerabilities and weaknesses. Find on:
  - 1st list: https://owasp.org/www-project-top-ten
  - 2nd list: https://cwe.mitre.org/top25/archive/2023/2023_top25_list.html

### Three Category of security weakness

- **Porous defenses**: A porous defenses weakness is one that could allow users to bypass or spoof **authentication** and **authorization** process. **Authentication** verifies the identity of something trying to access a system while authentication is the set of access and usage permission. The **attacks** that happens are: credential stuffing attacks, hijacking of session ids, stealing login credentials or man in the middle attack. Examples of vulnerabilities:

  - weak password encoding
  - insufficiently protected credentials
  - missing or single factor authentication
  - insecurity inherited permissions
  - sessions that don't expire.

- **Risky Resource management**: Such as memory, function and open-source frameworks. The vulnerabilities types:

  - out of bound read or write / buffer overflow
  - path traversal etc

- **Insecure Interaction between components**: This kind of vulnerabilities happens because modern application nowadays send and receive data across a wide range of services, threads and processes.The vulnerabilities are:
  - **cross site scripting**: User inputs are not handled securely enabling injection of client side script into web pages viewed by other users.
  - **Cross site request forgery**: improper verification of whether a seemingly legitimate and authentic request was intentionally sent. These attacks are often mountain via **social engineering** vectors such as bogus emails that trick a user to click a link which sends a _forged_ request to site where user is already authenticated.
  - Attacks of the category happen via backdoor attacks, scripting attacks, worms, trojan horse etc.

### Top vulnerability

#### Broken Access Control

- 94% of application has some sort of broken access control.
- Access control make sure that users cannot act outside of their intended permissions.
- This vulnerability can lead to unauthorized information disclosure, or modification or even destruction of database.

### References

- https://www.youtube.com/watch?v=F5KJVuii0Yw&list=PLWKjhJtqVAbkzvvpY12KkfiIGso9A_Ixs&index=16
