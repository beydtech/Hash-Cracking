# Hash-Cracking
**Document the hash cracking process, the tools used, and the results achieved. Discuss the significance of strong password hashing algorithms.**

Password Hashing

Password hashing is a method used to protect passwords by converting them into a fixed-length string of characters, which is typically a hash. This process is one-way, meaning it's computationally infeasible to reverse the hash back to the original password. Hashing ensures that even if a database is compromised, the actual passwords remain protected.


 Tools for Cracking Hashed Passwords

Two widely used tools for password cracking are:

- Hashcat: A fast and versatile password recovery tool that supports various hashing algorithms and attack modes. [2]

- John the Ripper: A powerful password cracker that combines several cracking modes and supports a wide range of hash types. [3]


 Hash Cracking Process

1. Identify the Hash Type

Before cracking, determine the hash type (e.g., MD5, SHA-1, bcrypt). Tools like hashid or hash-identifier can assist in identifying the hash algorithm based on the hash string's characteristics.

2. Prepare the Hash File
  Sent the phishing email to a select group of employees, ensuring compliance with the agreed-upon scope and permissions.

---

📊 Outcomes

- Email Open Rate: Approximately 80% of targeted employees opened the email.
- Credential Submission: Around 60% entered their login credentials on the fake portal.
- Reporting: Only 10% reported the suspicious email to the IT department.

---

🔍 Analysis of Effectiveness

The simulated attack demonstrated the organization's vulnerability to social engineering tactics, particularly phishing.

- Success Factors:
  - Realistic email content and appearance increased credibility.
  - Lack of employee training on identifying phishing attempts contributed to the high credential submission rate.

- Areas for Improvement:
  - Implement regular cybersecurity awareness training.
  - Introduce multi-factor authentication to reduce the risk of credential compromise.
  - Establish clear protocols for reporting suspicious communications.

 Recommendations

1. Employee Training: Conduct regular workshops on recognizing and handling phishing attempts.
2. Email Filtering: Enhance email security systems to detect and quarantine potential phishing emails.
Save the hash(es) into a text file, with each hash on a new line. For example:



5f4dcc3b5aa765d61d8327deb882cf99
e99a18c428cb38d5f260853678922e03


3. Select an Attack Mode

Common attack modes include:

- Dictionary Attack: Uses a wordlist of common passwords.

- Brute Force Attack: Tries all possible combinations within a given character set.

- Hybrid Attack: Combines dictionary and brute force methods.

4. Execute the Attack

Using Hashcat:

For a dictionary attack on MD5 hashes:



hashcat -m 0 -a 0 hashes.txt wordlist.txt



- -m 0: Specifies MD5 hash type.

- -a 0: Indicates a dictionary attack.

- hashes.txt: File containing hashes.

- wordlist.txt: File containing potential passwords.

Using John the Ripper:

For a dictionary attack:



john --wordlist=wordlist.txt hashes.txt



5. Review the Results

After the attack, the tools will display any cracked passwords. For example:

5f4dcc3b5aa765d61d8327deb882cf99:password
e99a18c428cb38d5f260853678922e03:abc123

Importance of Strong Password Hashing Algorithms

 Simulated Phishing Tests: Periodically run internal phishing simulations to assess and improve employee vigilance.
 Incident Response Plan: Develop and communicate a clear procedure for reporting and responding to suspected phishing attacks
 Not all hashing algorithms offer the same level of security. Older algorithms like MD5 and SHA-1 have known vulnerabilities and are susceptible to collision attacks, making them unsuitable for password hashing.

Modern algorithms like bcrypt, scrypt, and Argon2 are designed to be computationally intensive, slowing down brute-force attacks and providing better security. These algorithms also incorporate salting, which adds random data to each password before hashing, ensuring that identical passwords result in different hashes.


 Best Practices

- Use Strong Hashing Algorithms: Implement bcrypt, scrypt, or Argon2 for password hashing.

- Implement Salting: Always add a unique salt to each password before hashing to prevent rainbow table attacks.

- Enforce Strong Password Policies: Encourage users to create complex passwords that are harder to crack.

- Regularly Update Security Measures: Stay informed about the latest security practices and update your systems accordingly.
