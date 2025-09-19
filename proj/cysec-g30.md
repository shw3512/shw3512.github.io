# Cybersecurity

- Audience: General
- Presentation length: 30 minutes



<!--
Reorganize presentation to focus on real-world applications, not theory.
After "Realities" section, give two or three sections focusing on single
area. In each area, give brief (!) background and theory, then give tips
and example scenarios for group discussion. Focus on engagement and
generating discussion and desire to know more, not delivering "content".

- Devices
    - Device security settings (auto screen-lock, etc.)
- Authentication
    - MFA
    - Password management
- Phishing
    - Discuss general social engineering, include in examples
- Networks
    - Public Wi-Fi
    - How to test and harden home router
- Summary
    - Gather (restate) helpful resources
        - VirusTotal
        - Password generators
-->



## Overview

0. [Realities](cysec-g30.md#realities)
1. [Fundamentals](cysec-g30.md#fundamentals)
2. [Attacks](cysec-g30.md#attacks)
3. [Authentication](cysec-g30.md#authentication)
4. [Tools](cysec-g30.md#tools)
5. [Conclusion](cysec-g30.md#conclusion)
6. [References](cysec-g30.md#references)



## Realities

1. Tradeoffs
    - Tradeoffs exist
        - Security versus cost
        - Security versus convenience
        - Trust versus time
    - Tradeoffs change
        - Technology changes
        - Threat landscape changes
        - Values change
    - Tradeoffs depend on context
        - Example. Your bff AirDrops a file to you irl, versus a stranger sends you a file over the Internet
            - Every file your bff has shared with you recently has been infected with malware.
            - (!!!) The stranger is an employee at Microsoft, and the file is a security update whose MD5 and SHA-512 checksums agree with those on Microsoft's website.
2. The Internet
    - The Internet is public
        - Anyone can use it
    - The Internet is open
        - Anyone can see Internet traffic
    - The Internet is forever
        - [Internet Archive](https://archive.org/) (Wayback Machine)



## Fundamentals

### What is cybersecurity?

CIA triad:

- Confidentiality
    - Only entities that are authorized to access a resource can do so
    - Opposite: disclosure
- Integrity
    - Data are reliable
    - Opposite: alteration
- Availability
    - Resources are available when they are needed
    - Opposite: denial of service



## Attacks

### Examples

#### In the news

- Stuxnet worm (2010)
    - Destroys centrifuges at an air-gapped Iranian nuclear facility
    - [IEEE](https://spectrum.ieee.org/the-real-story-of-stuxnet), [Kaspersky](https://www.kaspersky.com/resource-center/definitions/what-is-stuxnet), [Wikipedia](https://en.wikipedia.org/wiki/Stuxnet), [WIRED](https://www.wired.com/2014/11/countdown-to-zero-day-stuxnet/), [YouTube : CFR Education](https://www.youtube.com/watch?v=djUHvCyPYhY), [YouTube : Darknet Diaries](https://www.youtube.com/watch?v=9DCwyuH29SI)
- Remote hijacking of car (2015)
    - Hackers kill the engine on a highway and drive the car into a ditch
    - [YouTube : WIRED](https://www.youtube.com/watch?v=MK0SrxBC1xs), [WIRED](https://www.wired.com/video/watch/hackers-wireless-jeep-attack-stranded-me-on-a-highway)
- NotPetya encrypting malware (2017)
    - Cripples firms, causing an estimated 10B USD in damages
    - [Cloudflare](https://www.cloudflare.com/learning/security/ransomware/petya-notpetya-ransomware/), [Wikipedia](https://en.wikipedia.org/wiki/Petya_(malware_family)), [WIRED](https://www.wired.com/story/notpetya-cyberattack-ukraine-russia-code-crashed-the-world/), [YouTube : Cybernews](https://www.youtube.com/watch?v=3-MSlNVqzYY)
- Colonial Pipeline ransomware attack (2021)
    - Highlights vulnerabilities in US critical infrastructure
    - [US CISA](https://www.cisa.gov/news-events/news/attack-colonial-pipeline-what-weve-learned-what-weve-done-over-past-two-years), [US DOE](https://www.energy.gov/ceser/colonial-pipeline-cyber-incident), [Wikipedia](https://en.wikipedia.org/wiki/Colonial_Pipeline_ransomware_attack)

#### But, it won't happen to me...right?

- How easy is it to steal passwords from a Web browser's password manager?
    - [YouTube](https://www.youtube.com/watch?v=CIOsemj3kl4), [YouTube](https://www.youtube.com/watch?v=-UPweZDohjk)
- Security expert Troy Hunt, creator of security website [HaveIBeenPwned](https://haveibeenpwned.com), falls victim to phishing
    - [Troy Hunt](https://www.troyhunt.com/a-sneaky-phish-just-grabbed-my-mailchimp-mailing-list/), [Cory Doctorow](https://pluralistic.net/2025/04/05/troy-hunt/#teach-a-man-to-phish), [Adam Shostack](https://shostack.org/blog/learning-from-troy-hunts-sneaky-phish/)
    - Notice how quickly an attack can unfold (automation!)
- Mirai botnet
    - Automatically scans the Internet for potentially vulnerable IoT devices and attempts brute-force logins (mostly using default credentials)
    - At its peak, infects over half a million devices
    - [Cloudflare](https://blog.cloudflare.com/inside-mirai-the-infamous-iot-botnet-a-retrospective-analysis/), [CIS](https://www.cisecurity.org/insights/blog/the-mirai-botnet-threats-and-mitigations), [Google Research](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/46301.pdf), [Wikipedia](https://en.wikipedia.org/wiki/Mirai_(malware))

### Social engineering

- An attempt to manipulate
    - Doesn't require technology (or even verbal language!)
        - Example. Threatening actions or gestures

#### Commonly used tactics

- Scarcity
    - "Only one left in stock!"
- Urgency
    - "Order before the countdown timer reaches zero and get 25% off!"
- Intimidation
    - Fear
        - "Your tax return is being investigated for fraud that carries penalties of prison terms of up to five years and fines of up to $250,000."
- Authority
    - "Nine out of ten doctors agree."
    - "The experiment requires that you continue."
        - From psychologist Stanley Milgram's experiments on obedience to authority \[[Wikipedia](https://en.wikipedia.org/wiki/Milgram_experiment)\]
- Trust
    - Social proof
        - "Everyone else is doing it."
    - Familiarity
        - "You know me."
- Likeableness
    - Pity
        - "They deserve a better life than this. Donate your money, time, and action now."

#### Phishing

- Social engineering via e-mail
- Spear phishing: targeted phishing
    - Example. Successful spear-phishing attack during the 2016 US presidential election \[[Wikipedia](https://en.wikipedia.org/wiki/Podesta_emails)\]

##### Phishing indicators (may or may not apply!)

- Bad grammar, spelling
    - Advances in large language models (LLMs) have enabled attackers to mitigate this indicator
- Your name is missing or misspelled
- Fishy (or look-alike) sender e-mail address

#### Tips to mitigate social engineering

- Listen to your Spidey sense
    - Does something feel "off"?
- Slow down and question
- Use another route

### Your turn

Scenario: You get an e-mail from your bank saying that your account may have been compromised and that you need to use this link to verify your identity and account activity within 24 hours or your account will be frozen. You use this bank account to pay multiple important bills, several of which come due in the next few days.

What do you do?

(Example options)

- Log in to your bank's website.
    - Using what URL? The URL in the e-mail? The URL from a Web search? The URL you previously bookmarked in your Web browser or password manager?
- Give your bank a call.
    - Using what phone number? The number in the e-mail? The number on your bank's website? The number on the back of your bank card?



## Authentication

### Introduction

- Authentication versus identification (versus authorization)
    - Identification: Who are you?
    - Authentication: How do I know you are who you say you are?
        - "Prove" your identity!
    - Authorization: What are you allowed to do?
- Example. Monty Python and the Holy Grail \[[YouTube](https://www.youtube.com/watch?v=RbTaP0_Galg)\]
  - "[A]nswer me these questions three, ere the other side [you] see."

### Factors of authentication

Main three:

1. Something you know (knowledge)
2. Something you have (possession)
3. Something you are (inherence)

Others:

4. Something you do (behavior)
5. Somewhere you are (location)

### Multifactor authentication

- The use of two or more different (!) factors during authentication
- Why it helps: defense in depth
- Tradeoff: Security versus convenience
    - Consider: If you make MFA more convenient, then you can make systems and data more secure.
        - Examples. Integrate fingerprint scanning hardware and software into laptops. Integrate face-scanning software into cell phones.

### Passwords

- Still a common form of authentication

#### Poll questions

(Ask aloud to the group, answer silently to yourself.)

- How many passwords do you have?
    - Give an order-of-magnitude estimate: 1, 10, 100, 1000,....
- How do you manage your passwords? (Select all that apply.)
    1. I use the same password or similar passwords for most or all of my accounts.
    2. I write down my most commonly used passwords on a piece of paper and keep it on or near my computer.
    3. I save them in my Web browser (for example, using the "remember me" feature).
    4. I write down my passwords in a notebook and look them up when I need them.
    5. I use a password manager.
- Discuss the tradeoffs of each method of password management.

#### Password best practices

- Don't reuse passwords
    - Tradeoff: Security versus convenience
- Make sufficiently long
    - Complex?
        - Tradeoffs
            - "Research has shown...that users respond in very predictable ways to the requirements imposed by composition rules.... For example, a user that might have chosen “password” as their password would be relatively likely to choose “Password1” if required to include an uppercase letter and a number, or “Password1!” if a symbol is also required." ([NIST SP 800-63](https://pages.nist.gov/800-63-3/sp800-63b.html#appA))
            - "Highly complex memorized secrets introduce a new potential vulnerability: they are less likely to be memorable, and it is more likely that they will be written down or stored electronically in an unsafe manner." ([NIST SP 800-63](https://pages.nist.gov/800-63-3/sp800-63b.html#appA))
            - See also [xkcd](https://xkcd.com/936/)
- Use a password manager (maybe?)
    - Tradeoffs
        - Keys to the kingdom
        - You trust the password manager for secure implementation and operations
    - If you use a password manager, then...
        - Use a strong master password
        - Strongly consider enabling MFA

### Your turn

For each scenario below, identify (a) what is the identification, authentication, and authorization; and (b) what factors of authentication are used. Which scenarios implement multi-factor authentication (MFA)? Which implementations do you think are most secure? Which are convenient? Why?

1. Before you cross the Bridge of Death, the bridgekeeper asks you your name, your quest, and a secret question.
2. When accessing a website, you are prompted for your username and password.
3. At the entrance to your work (or school, or gym, etc.), you are asked to swipe your ID, then give your date of birth.
4. When signing in for a cybersecurity certification exam, you are asked to present two forms of ID, one with your photograph and one with your signature; sign your name on a digital pad; and sit for a head photograph.



## Tools

Tools for your cybersecurity toolkit

Note: If you upload anything (file, link, etc.), then assume others will see it and the information it contains.

### Data breach

- [HaveIBeenPwned](https://haveibeenpwned.com)

### Inspect suspicious e-mails

- [CheckPhish](https://checkphish.bolster.ai)
- [EasyDMARC](https://easydmarc.com/tools/phishing-url)
- [IPQS](https://www.ipqualityscore.com/free-email-verifier)
- [Keepnet](https://keepnetlabs.com/free-phishing-email-analysis)
- "Top 10 email analysis tools for phishing" \[[Keepnet](https://keepnetlabs.com/blog/top-10-email-analysis-tools-for-phishing)\]

### Inspect suspicious files or links

- [Bitdefender](https://www.bitdefender.com/en-us/consumer/link-checker)
- [Joe Sandbox](https://www.joesandbox.com)
- [VirusTotal](https://www.virustotal.com/gui/)

- Article on accidental disclosure from VirusTotal upload \[[ThreatDown](https://www.threatdown.com/blog/accidental-virustotal-upload-is-a-valuable-reminder-to-double-check-what-you-share/)\]
- [VirusTotal's privacy policy](https://virustotal.readme.io/docs/privacy-policy)

### Inspect suspicious URLs (Web sites)

- [AbuseIPDB](https://www.abuseipdb.com)
    - Note. You must enter the domain name (ending in `.com`, `.edu`, etc.), not the full URL

### Device settings

- Login settings
    - Passcode? Password? Biometric? MFA?
- Lock-screen timer
- Encryption
    - File-level or full-disk encryption (FDE)
    - Reduces risk of data disclosure if your device is lost or stolen

### Public behavior

- Open Wi-Fi
- Shoulder surfing
    - Bystander, binoculars, camera
- Device settings
    - Leave your device unattended?



## Conclusion

- Realities
    - Tradeoffs exist
    - The Internet is public, open, and forever
- Cyberattacks can and will happen
    - Be alert for commonly used social-engineering tactics
    - Know what to do (generally) and tools to use (specifically)
- Tools for your cybersecurity toolkit
    - Software (anti-malware, sandboxes)
    - Password management
    - Device settings
    - Public behavior



## References

1. Grubb, Sam (2021). _How Cybersecurity Really Works: A Hands-On Guide for Total Beginners._ United States: No Starch Press.
    - ISBN-13 978-1-7185-0128-7 (paperback)
2. Martin, Keith (2020). _Cryptography: The key to digital security, how it works, and why it matters._ United States: WW Norton.
    - ISBN-13 978-1-3240-0430-1 (e-book), 978-1-3240-0429-5 (hardcover), 978-0-3938-6745-9 (paperback)
