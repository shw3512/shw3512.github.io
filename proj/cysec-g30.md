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
1. [Attacks](cysec-g30.md#attacks)
2. [Authentication](cysec-g30.md#authentication)
3. [Best practices](cysec-g30.md#best-practices)
4. [Practice](cysec-g30.md#practice)



## Realities

1. People face tradeoffs
    - Security v cost and convenience
    - Trust v time
    - Different balance in different settings with different people (entities, etc.)
        - Your bff AirDrops a photo to you irl
        - A stranger sends you a file over the Internet
2. The Internet is...
    - Open
        - Anyone can see Internet traffic
    - Public
        - Anyone can use it
    - Forever
        - [Internet Archive](https://archive.org/) (Wayback Machine)



## Attacks

### Examples

#### In the news

- Stuxnet worm (2010) destroys centrifuges at air-gapped Iranian nuclear facility ([IEEE](https://spectrum.ieee.org/the-real-story-of-stuxnet), [Kaspersky](https://www.kaspersky.com/resource-center/definitions/what-is-stuxnet), [Wikipedia](https://en.wikipedia.org/wiki/Stuxnet), [WIRED](https://www.wired.com/2014/11/countdown-to-zero-day-stuxnet/), [YouTube : CFR Education](https://www.youtube.com/watch?v=djUHvCyPYhY), [YouTube : Darknet Diaries](https://www.youtube.com/watch?v=9DCwyuH29SI))
- Hackers hijack car remotely (2015), killing the engine on a highway and (separately) driving it into a ditch ([YouTube : WIRED](https://www.youtube.com/watch?v=MK0SrxBC1xs), [WIRED](https://www.wired.com/video/watch/hackers-wireless-jeep-attack-stranded-me-on-a-highway))
- NotPetya encrypting malware (2017) cripples firms, causing estimated 10B USD in damages ([Cloudflare](https://www.cloudflare.com/learning/security/ransomware/petya-notpetya-ransomware/), [Wikipedia](https://en.wikipedia.org/wiki/Petya_(malware_family)), [WIRED](https://www.wired.com/story/notpetya-cyberattack-ukraine-russia-code-crashed-the-world/), [YouTube : Cybernews](https://www.youtube.com/watch?v=3-MSlNVqzYY))
- Colonial Pipeline ransomware attack (2021) highlights vulnerabilities in US critical infrastructure ([US CISA](https://www.cisa.gov/news-events/news/attack-colonial-pipeline-what-weve-learned-what-weve-done-over-past-two-years), [US DOE](https://www.energy.gov/ceser/colonial-pipeline-cyber-incident), [Wikipedia](https://en.wikipedia.org/wiki/Colonial_Pipeline_ransomware_attack))

#### But, it won't happen to me...right?

- How easy is it to steal passwords from a Web browser's password manager? ([YouTube](https://www.youtube.com/watch?v=CIOsemj3kl4), [YouTube](https://www.youtube.com/watch?v=-UPweZDohjk))
- Security expert Troy Hunt, creator of security website [HaveIBeenPwned](https://haveibeenpwned.com), falls victim to phishing ([Troy Hunt](https://www.troyhunt.com/a-sneaky-phish-just-grabbed-my-mailchimp-mailing-list/), [Cory Doctorow](https://pluralistic.net/2025/04/05/troy-hunt/#teach-a-man-to-phish), [Adam Shostack](https://shostack.org/blog/learning-from-troy-hunts-sneaky-phish/))
    - Notice how quickly an attack can unfold (automation!)

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

#### Commonly used tactics

- Scarcity
- Urgency
- Intimidation
    - Fear
- Authority
- Trust
    - Social proof
    - Familiarity
- Likeableness
    - Pity

#### Tips

- Listen to your Spidey sense
    - Does something feel "off"?
- Slow down and question
- Use another route

### Your turn

Scenario: You get an e-mail from your bank saying that your account may have been compromised and that you need to use this link to verify your identity and account activity within 24 hours or your account will be frozen. You use this bank account to pay multiple important bills that come due in the next few days.

What do you do?

- Option: Instead of clicking the link, log in to your bank's website.
    - Using what URL? The URL in the e-mail? The URL from a Web search? The URL you previously bookmarked in your Web browser or password manager?
- Option: Instead of clicking the link, give your bank a call.
    - Using what phone number? The number in the e-mail? The number on your bank's website? The number on the back of your bank card?



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

- Don't reuse
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
