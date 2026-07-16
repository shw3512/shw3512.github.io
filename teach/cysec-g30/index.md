# Cybersecurity

- Duration: 30--60 minutes
- Audience: General



## Overview

1. [Fundamentals](#fundamentals)
2. [Your security](#your-security)
3. [Tools](#tools)
4. [Conclusion](#conclusion)
5. [References](#references)
6. [Appendix](#appendix)
    1. [Motivation](#motivation)
    2. [Authentication](#authentication)



##  Goals

Help you...

- Recognize and respond to cyber risk
    - Adopt simple, useful frameworks to manage risk
    - Aim to reduce risk, not eliminate it
- Adopt safe cyber habits
    - Practice cybersecurity best practices (habits over tools)
    - Be informed and confident in your digital decisions
- Know where to go for cyber info
    - Have a reference list of trustworthy cybersecurity tools and information

## Fundamentals

- Definitions
- Axioms
- Frameworks

### Definitions

What is cybersecurity?

- Identify, assess, address, and monitor relevant cyber threats

### Axioms

1. The Internet is
2. Tradeoffs exist
3. Cyberattacks happen

#### The Internet

- The Internet is public
    - Anyone can use it
- The Internet is open
    - Anyone can see Internet traffic
        - Hence encryption (see ≠ understand)
- The Internet is forever
    - [Internet Archive](https://archive.org/) (Wayback Machine)
    - Privacy laws
        - Right to erasure ([GDPR](https://gdpr.eu))
        - Right to delete ([CCPA](https://cppa.ca.gov))

#### Tradeoffs

- Tradeoffs exist
    - Security versus cost
    - Security versus convenience
    - Trust versus time
- Tradeoffs change
    - Technologies change
    - Threats change
    - Values change
- Tradeoffs depend on context

#### Cyberattacks happen

- You can't control...
    - Whether cyberattacks happen (they will)
    - Whether you achieve perfect safety (you can't)
- You can control...
    - How informed you are
        - You're here!
        - Know what to do and where to go
    - How prepared you are
        - How secure are your actions? accounts? devices?
    - What balance _you choose_ among tradeoffs
    - What laws you support (privacy, accountability)
    - What grace you show yourself and others
        - More perfect, never perfect

#### Your turn

Which is riskier?

1. Your bff AirDrops a file to you irl
2. A stranger sends you a file over the Internet

Context:

- Your bff
    - Every file your bff has shared with you recently has been infected with malware
        - (Why is this person still your bff?)
    - The file seems unusually large
- The stranger
    - The stranger is (allegedly) an employee at Microsoft
        - How might you verify this?
    - The file is a security update whose checksums agree with those on Microsoft's website

### Frameworks

- CIA triad
- Risk
- AAA
- OODA loop

#### CIA triad

- Confidentiality
    - Entities can access a resource only if they are authorized
    - Opposite: disclosure
- Integrity
    - Resources are reliable
    - Opposite: alteration
- Availability
    - Entities can access a resource if they are authorized
    - Opposite: denial of service

#### Risk

- Asset
    - Something of value
    - Can be physical, digital, or relational (e.g., reputation)
- Vulnerability
    - A weakness
- Threat
    - Potential danger
- Risk
    - Potential loss
    - Threat exploits a vulnerability of an asset

#### AAA

- Identification
    - Who are you?
- Authentication
    - How do I know you are who you say you are?
        - "Prove" your identity!
- Authorization
    - What are you allowed to do?
- Accounting
    - What did you do?

Example. Monty Python and the Holy Grail \[[YouTube](https://www.youtube.com/watch?v=RbTaP0_Galg)\]

- "[A]nswer me these questions three, ere the other side [you] see."

##### Factors of authentication

1. Something you know
    - Example: password
2. Something you have
    - Example: cell phone
3. Something you are
    - Example: face, fingerprint

##### Multi-factor authentication (MFA)

- The use of two or more _different_ factors during authentication
- Why it helps: defense in depth
- Tradeoff: security versus convenience
    - If you make MFA more convenient, then you make systems and data more secure
        - Example. Integrate fingerprint scanning hardware and software into laptops
        - Example. Integrate face-scanning hardware and software into cell phones



#### OODA loop

1. Observe
2. Orient
3. Decide
4. Act



## Your security

- Account access
- Software
- Devices
- Networks
    - Home router
    - Public Wi-Fi
- Relational
- In public

### Account access

#### Your turn

- How many passwords do you have?
    - Give an order-of-magnitude estimate: 1, 10, 100, 1000,....
- How do you manage your passwords? (Select all that apply.)
    1. I use the same password or similar passwords for most or all of my accounts.
    2. I write down my most commonly used passwords on a piece of paper and keep it on or near my computer.
    3. I save them in my Web browser (for example, using the "remember me" feature).
    4. I write down my passwords in a notebook and look them up when I need them.
    5. I use a password manager.
- What are the tradeoffs for each method of password management listed above?

#### To do

- Use a password manager
- Review the security settings on your accounts
    - Settings to review:
        - Password strength
        - MFA enabled?
        - Security alerts
            - Triggers
            - Delivery options
        - Account-recovery options
    - You don't have to do all your accounts in one sitting!
        - Prioritize accounts by value and risk
- Implement MFA on high-value and high-risk accounts
    - ...and on any account where security benefit outweighs convenience cost

#### Password best practices

- Don't reuse passwords
    - Tradeoff: Security versus convenience
- Make sufficiently long
- Don't use security questions
    - If you do, then use random answers
    - Concern: OSINT, social engineering

#### Password manager

Key benefits:

- Generates and stores unique, complex passwords
- Integrates with common Web browsers (plug-in) and mobile devices (app)
- Auto-fills login credentials only on valid website
    - Protects against spoofed websites

Key risk:

- Keys to the kingdom
    - Make your master password strong (long and memorable)

### Software

#### To do

- Install software (applications, plug-ins, and updates) from trusted sources only
    - Even on trusted sites, be wary
- Review the security settings and permissions of applications
    - (???) which, exactly (???)
- Uninstall unused software

### Devices

#### To do

- Review the security settings on your digital devices
    - Login settings
        - Password? Passcode? Biometric? MFA?
    - Lock-screen timer
        - Enabled? Time frame?
    - Encryption
        - File-level? Full-disk encryption (FDE)?
        - Reduces risk of data disclosure if your device is lost or stolen
- Align the security settings to the device
    - Tradeoff: Security versus cost and convenience
    - Considerations:
        - How mobile is the device?
        - What is the value of the device and of the data on it?
- Regularly apply software patches and updates
    - Automate?

### Networks

- Be wary of public Wi-Fi
- Harden your home router

#### Public Wi-Fi

##### Risks

- Rogue access points
- Man-in-the-middle attack

##### Recommendations

- Enable MFA on sensitive accounts
- Avoid sensitive transactions
    - Banking
    - Entering payment information (online shopping)
- Use HTTPS, not HTTP
    - Benefits of HTTPS over HTTP:
        - Privacy
            - HTTP transmits all data in plaintext
                - This includes usernames, passwords, payment information, etc.
            - HTTPS encrypts Web traffic content
                - Anyone can view related metadata (like sender and receiver address)
        - Integrity
            - HTTPS ensures that your communication with a website is not tampered with
        - Authenticity
            - HTTPS automatically verifies that you're communicating with a legitimate server
                - This prevents spoofing (an attacker pretending to be a website)
                - (!) This does not prevent you from connecting to malicious websites
- If HTTPS is not enough (or not available), then use a virtual private network (VPN)
    - Routes all traffic through an encrypted tunnel to the VPN server
        - Hides your IP address, location, and Web-browsing destinations
    - Note: Shifts trust from the ISP to the VPN provider, who still sees this information

##### References

- [Fortinet](https://www.fortinet.com/resources/cyberglossary/vpn-wifi)

#### Home router

##### To do

- Change default credentials
- Enable strong encryption
    - Best: WPA3
    - Second best: WPA2
    - Don't use: WEP, WPA
- Enable automatic updates
- Disable risky features
    - Remote management
    - Wi-Fi Protected Setup (WPS)
    - Universal Plug and Play (UPnP)
- Create a guest network
    - Enable a separate, strong password

##### References

- [Acronis](https://www.acronis.com/en/blog/posts/hardening-home-router/)
- [Canadian Centre for Cyber Security](https://www.cyber.gc.ca/en/guidance/routers-cyber-security-best-practices-itsap80019)
- [TP-Link](https://www.tp-link.com/ph/blog/1778/wi-fi-security-settings-10-steps-to-secure-your-wifi-router/)
- [US CISA](https://www.cisa.gov/audiences/high-risk-communities/projectupskill/module5)

### Relational

- Social engineering
- Phishing

#### Social engineering

- An attempt to manipulate humans
    - Doesn't require technology (even verbal language!)
        - Example. Threatening actions or gestures

##### Commonly used tactics

- Scarcity
    - "Only one left in stock!"
- Urgency
    - "Order before the countdown timer reaches zero and get 80% off!"
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

##### Phishing

- Social engineering over communication technology

Variants:

- Phishing
    - Via e-mail
- Vishing
    - Via voice call
- Smishing
    - Via SMS

How to detect (often though not always):

- Is unexpected
- Is from an unusual source (e-mail address, phone number)
- Uses a generic greeting
- Uses social-engineering tactics

#### To do

- Listen to your Spidey sense
    - Does something feel "off"?
- Slow down and question
- Verify by using another route
- If it's a phish, then report and delete
    - "Report spam" feature in e-mail client
    - [Forward to APWG](https://apwg.org/reportphishing)

References:

- [Anti-Phishing Working Group (APWG)](https://apwg.org)
- [Bitwarden](https://bitwarden.com/blog/what-is-a-common-indicator-of-phishing/)
- [US CISA](https://www.cisa.gov/secure-our-world/recognize-and-report-phishing)

#### Your turn

Scenario: You get an e-mail from your bank saying that your account may have been compromised and that you need to use the link provided in the e-mail to verify your identity and account activity within 24 hours or your account will be frozen. You use this bank account to pay multiple important bills, several of which come due in the next few days.

What do you do?

1. Ignore the e-mail. It's probably fake.
2. Immediately click the link and provide the requested information---I got bills to pay and things to do!
3. Log in to your bank's website.
    - Using what URL? The URL in the e-mail? The URL from a Web search? The URL you previously bookmarked in your Web browser or password manager?
4. Give your bank a call.
    - Using what phone number? The number in the e-mail? The number on your bank's website? The number on the back of your bank card?
5. Other (explain)

### In public

#### To do

- Configure secure device settings in advance
- Don't leave your devices unattended
- Beware shoulder surfing
    - Bystander, binoculars, camera
- Beware tailgating and piggybacking



## Tools

This section presents reference lists of tools for your cybersecurity toolkit.

Note: If you upload anything (file, link, etc.), then assume others will see it and the information it contains.

### Password managers

- [1Password](https://1password.com)
- [Bitwarden](https://bitwarden.com)
- [Dashlane](https://www.dashlane.com)
- [Keeper](https://www.keepersecurity.com)
- [NordPass](https://nordpass.com)
- [Proton Pass](https://proton.me/pass)

Reviews:

- [Bellator Cyber Guard](https://bellatorcyber.com/blog/best-password-managers)
- [PCMag](https://www.pcmag.com/picks/the-best-password-managers)
- [security.org](https://www.security.org/password-manager/best/)
- [WIRED](https://www.wired.com/story/best-password-managers/)

### Anti-malware

- [Bitdefender](https://www.bitdefender.com/en-us/)
- [Malwarebytes](https://www.malwarebytes.com)

Reviews:

- [CNET](https://www.cnet.com/tech/services-and-software/best-antivirus/)
- [PCMag](https://www.pcmag.com/picks/the-best-antivirus-protection)

### Identify disclosure of personal data (in a data breach)

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

Privacy considerations:

- Article on accidental disclosure from VirusTotal upload \[[ThreatDown](https://www.threatdown.com/blog/accidental-virustotal-upload-is-a-valuable-reminder-to-double-check-what-you-share/)\]
- [VirusTotal's privacy policy](https://virustotal.readme.io/docs/privacy-policy)

### Inspect suspicious URLs (Web sites)

- [AbuseIPDB](https://www.abuseipdb.com)
    - Note. You must enter the domain name (ending in `.com`, `.edu`, etc.), not the full URL
- [VirusTotal](https://www.virustotal.com/gui/)



## Conclusion

### What we learned

- Realities
    - The Internet is public, open, and forever
    - Tradeoffs exist
    - Cyberattacks happen
- What to do
    - Defend in advance
        - Configure secure settings for accounts and devices
        - Apply software patches and updates
        - Use a password manager
        - Use anti-malware software
    - Be alert for social-engineering tactics
        - Slow down, question, and verify
    - Know secure behavior and security tools
        - Mind your public behavior
    - Show grace to yourself and to others

### What to do

- Today
    - Share what you learned with a friend
- This week
    - Enable MFA on sensitive accounts
- This month
    - Install a password manager (app and Web-browser plug-in)
        - Enter account credentials
        - Update passwords to secure alternatives (in the password manager _and_ on the account)
    - Adopt a realistic routine for patching and updating software
        - Automate where possible
- This year
    - Configure secure settings for accounts and devices



## References

1. Andress, Jason (2026). _Foundations of cybersecurity: A straightforward introduction,_ 2nd edition. United States: [No Starch Press](https://nostarch.com/foundations-cybersecurity-2e).
    - ISBN-13: 978-1-7185-0441-7 (e-book), 978-1-7185-0440-0 (paperback)
2. Grubb, Sam (2021). _How cybersecurity really works: A hands-on guide for total beginners._ United States: [No Starch Press](https://nostarch.com/cybersecurityreallyworks).
    - ISBN-13: 978-1-7185-0129-4 (e-book), 978-1-7185-0128-7 (paperback)
3. Kranz, Thomas (2022). _Making sense of cybersecurity._ United States: [Manning Publications](https://www.manning.com/books/making-sense-of-cybersecurity).
    - ISBN-13: 978-1-61729-800-4 (paperback)
4. Martin, Keith (2020). _Cryptography: The key to digital security, how it works, and why it matters._ United States: [WW Norton](https://wwnorton.com/books/9780393867459).
    - ISBN-13: 978-1-32400-430-1 (e-book), 978-1-32400-429-5 (hardcover), 978-0-39386-745-9 (paperback)



## Appendix

### Motivation

#### What's the worst that can happen?

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

#### But hackers won't target me, right?

- How easy is it to steal passwords from a Web browser's password manager?
    - [YouTube](https://www.youtube.com/watch?v=CIOsemj3kl4), [YouTube](https://www.youtube.com/watch?v=-UPweZDohjk)
- Mirai botnet
    - Automatically scans the Internet for potentially vulnerable IoT devices and attempts brute-force logins (mostly using default credentials)
    - At its peak, infects over half a million devices
    - [Cloudflare](https://blog.cloudflare.com/inside-mirai-the-infamous-iot-botnet-a-retrospective-analysis/), [CIS](https://www.cisecurity.org/insights/blog/the-mirai-botnet-threats-and-mitigations), [Google Research](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/46301.pdf), [Wikipedia](https://en.wikipedia.org/wiki/Mirai_(malware))

#### Still, it won't happen to me...right?

- Security expert Troy Hunt, creator of security website [HaveIBeenPwned](https://haveibeenpwned.com), falls victim to phishing
    - [Troy Hunt](https://www.troyhunt.com/a-sneaky-phish-just-grabbed-my-mailchimp-mailing-list/), [Cory Doctorow](https://pluralistic.net/2025/04/05/troy-hunt/#teach-a-man-to-phish), [Adam Shostack](https://shostack.org/blog/learning-from-troy-hunts-sneaky-phish/)
    - Notice how quickly an attack can unfold (automation!)



### Authentication

#### Factors of authentication

Main three:

1. Something you know (knowledge)
2. Something you have (possession)
3. Something you are (inherence)

Others:

4. Something you do (behavior)
5. Somewhere you are (location)

#### Multifactor authentication

- The use of two or more different (!) factors during authentication
- Why it helps: defense in depth
- Tradeoff: Security versus convenience
    - Consider: If you make MFA more convenient, then you can make systems and data more secure.
        - Example: Integrate fingerprint scanning hardware and software into laptops.
        - Example: Integrate face-scanning software into cell phones.

#### Passwords

- Still a common form of authentication

##### Password best practices

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

#### Your turn

For each scenario below, identify (a) what is the identification, authentication, and authorization; and (b) what factors of authentication are used. Which scenarios implement multi-factor authentication (MFA)? Which implementations do you think are most secure? Which are convenient? Why?

1. Before you cross the Bridge of Death, the bridgekeeper asks you your name, your quest, and a secret question.
2. When accessing a website, you are prompted for your username and password.
3. At the entrance to your work (or school, or gym, etc.), you are asked to swipe your ID, then give your date of birth.
4. When signing in for a cybersecurity certification exam, you are asked to present two forms of ID, one with your photograph and one with your signature; sign your name on a digital pad; and sit for a head photograph.
