# Cybersecurity

- Audience: General
- Presentation length: 30 minutes



## Overview

0. [Realities](cysec-g30.md#realities)
1. [Attacks](cysec-g30.md#attacks)
2. [Authentication](cysec-g30.md#authentication)
3. [Best practices](cysec-g30.md#best-practices)
4. [Practice](cysec-g30.md#practice)



## Realities

1. People face tradeoffs
    - Security v convenience
    - Trust v time
    - Different balance in different settings with different people (entities, etc.)
        - Your bff AirDrops a photo to you irl
        - A stranger sends you a file on the Internet
2. The Internet...
    - is open
        - Anyone can see Internet traffic
    - is public
        - Anyone can use it
    - is forever
        - [Internet Archive](https://archive.org/) (Wayback Machine)



## Attacks

### Social engineering

- Manipulation
    - Doesn't require technology (not even verbal language!)
        - Threatening gestures (!!!) (insert image)

#### Phishing

- (!!!) Definition
- Spear phishing: targeted phishing
    - (!!!) Definition
    - Example (!!!) (from real life)

##### Phishing indicators (may or may not apply!)

- Bad grammar, spelling
- Your name is missing or misspelled
- Fishy (or look-alike) sender e-mail address

##### Commonly used tactics

- Urgency
- Intimidation
- Authority
- Familiarity
- Trust
- Pity

##### Tips

- Listen to your Spidey sense
    - Does something feel "off"?
- Slow down and question
- Use another route
    - Scenario: You get an e-mail from your bank saying that your account may have been compromised and you need to use this link to verify your identity and account activity within 24 hours or your account will be frozen. What do you do?
        - One option: Instead of clicking the link, give your bank a call.
            - Using what phone number? The number in the e-mail, the number on their website, the number on the back of your bank card,...?



## Authentication

### Introduction

- (!!!) Definition
- Compare: authentication versus identification (versus authorization)
    - Example: Monty Python
- Scenarios (in each, say what is identification, authentication, and authorization)
    1. You visit a website and are prompted for your username and password.
    2. You go to work (or school, or the gym, etc.) and are asked to give your ID card, then your name and birthday.
    3. (???) You register your marriage (congratulations!) and are asked for your name, date of birth, and fingerprints.

### Factors of authentication

1. Something you know
2. Something you have
3. Something you are

- In each of the scenarios above, identify which factor of authentication is used

### Multifactor authentication

- (!!!) Definition
- Must be different _factors_ (categories)!
- Why it helps
    - Defense in depth
- Tradeoff: Security versus convenience
    - (!!!) Ways to make MFA more convenient
        - (!!!) Example (from real life)

### Passwords

- Still common form of authentication
- Poll questions (ask aloud, answer to yourself)
    - How many passwords do you have? (order of magnitude estimate)
    - How do you manage them all? (Select all that apply.)
        1. I use the same password for all my accounts.
        2. I write down my most commonly used passwords on a sticky note and post it on my computer screen \| keyboard \| desk drawer.
        3. I save them in my Web browser (using the "remember me" feature).
        4. I write down my passwords in a notebook and look them up when I need them.
        5. I use a password manager.
- Tradeoffs!



## Best practices

### Passwords

- Do not reuse
- Make sufficiently long
    - Complex?
    - See [NIST](https://pages.nist.gov/800-63-3/sp800-63b.html#appA), [xkcd](https://xkcd.com/936/)
- Use a password manager (maybe?)
    - Tradeoffs
    - If you use a password manager, then...
        - make sure your password for it is strong
        - strongly consider enabling MFA

### Suspicious files and links

- [VirusTotal](https://www.virustotal.com/gui/)
    - Note: If you upload a file, then assume others will see it (and potentially the info it contains)
        - For more info, see [this article](https://www.threatdown.com/blog/accidental-virustotal-upload-is-a-valuable-reminder-to-double-check-what-you-share/) and [VirusTotal's privacy policy](https://virustotal.readme.io/docs/privacy-policy)

### Device settings

- Login settings
- Lock-screen timer
- Encryption
    - If your device is lost or stolen

### Public settings

- Open Wi-Fi
- Shoulder surfing
    - Bystander, binoculars, camera
- Device settings
    - Leave your device unattended?



## Practice

1. On your way home from work, school, the library, etc., you find a USB flash drive on which is written the tiny message, "If found, please mail to address in README file." What do you do?

(!!!) Additional scenarios, time permitting
