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
5. [References](cysec-g30.md#references)



## Realities

1. People face tradeoffs
    - Security v cost and convenience
    - Trust v time
    - Different balance in different settings with different people (entities, etc.)
        - Your bff AirDrops a photo to you irl
        - A stranger sends you a file over the Internet
2. The Internet is...
    - Public
        - Anyone can use it
    - Open
        - Anyone can see Internet traffic
    - Forever
        - [Internet Archive](https://archive.org/) (Wayback Machine)



## Attacks

### Examples

#### In the news

- Stuxnet worm (2010) destroys centrifuges at air-gapped Iranian nuclear facility ([IEEE](https://spectrum.ieee.org/the-real-story-of-stuxnet), [Kaspersky](https://www.kaspersky.com/resource-center/definitions/what-is-stuxnet), [Wikipedia](https://en.wikipedia.org/wiki/Stuxnet), [WIRED](https://www.wired.com/2014/11/countdown-to-zero-day-stuxnet/), [YouTube : CFR Education](https://www.youtube.com/watch?v=djUHvCyPYhY), [YouTube : Darknet Diaries](https://www.youtube.com/watch?v=9DCwyuH29SI))
- NotPetya encrypting malware (2017) cripples firms, causing estimated 10B USD in damages ([Cloudflare](https://www.cloudflare.com/learning/security/ransomware/petya-notpetya-ransomware/), [Wikipedia](https://en.wikipedia.org/wiki/Petya_(malware_family)), [WIRED](https://www.wired.com/story/notpetya-cyberattack-ukraine-russia-code-crashed-the-world/), [YouTube : Cybernews](https://www.youtube.com/watch?v=3-MSlNVqzYY))
- Colonial Pipeline ransomware attack (2021) highlights vulnerabilities in US critical infrastructure ([US CISA](https://www.cisa.gov/news-events/news/attack-colonial-pipeline-what-weve-learned-what-weve-done-over-past-two-years), [US DOE](https://www.energy.gov/ceser/colonial-pipeline-cyber-incident), [Wikipedia](https://en.wikipedia.org/wiki/Colonial_Pipeline_ransomware_attack))

#### But, it won't happen to me...right?

- Hackers hijack car remotely (2015), killing the engine on a highway and driving it into a ditch ([YouTube : WIRED](https://www.youtube.com/watch?v=MK0SrxBC1xs), [WIRED](https://www.wired.com/video/watch/hackers-wireless-jeep-attack-stranded-me-on-a-highway))
- How easy is it to steal passwords from a Web browser's password manager? ([YouTube](https://www.youtube.com/watch?v=CIOsemj3kl4), [YouTube](https://www.youtube.com/watch?v=-UPweZDohjk))
- Security expert Troy Hunt, creator of security website [HaveIBeenPwned](https://haveibeenpwned.com), falls victim to phishing ([Troy Hunt](https://www.troyhunt.com/a-sneaky-phish-just-grabbed-my-mailchimp-mailing-list/), [Cory Doctorow](https://pluralistic.net/2025/04/05/troy-hunt/#teach-a-man-to-phish), [Adam Shostack](https://shostack.org/blog/learning-from-troy-hunts-sneaky-phish/))
    - Notice how quickly an attack can unfold (automation!)

### Social engineering

- An attempt to manipulate
    - Doesn't require technology (or even verbal language!)
        - Example. Threatening actions or gestures

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

#### Phishing

- Socially engineering via e-mail
- Spear phishing: targeted phishing
    - Example. Successful spear-phishing attack during the 2016 US presidential election ([Wikipedia](https://en.wikipedia.org/wiki/Podesta_emails))

##### Phishing indicators (may or may not apply!)

- Bad grammar, spelling
    - Advancements in large language models (LLMs) have enabled attackers to mitigate this indicator
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

- Compare: authentication versus identification (versus authorization)
    - Identification: Who are you?
    - Authentication: How do I know you are who you say you are?
        - "Prove" your identity!
    - Authorization: What are you allowed to do?
- Example. Monty Python and the Holy Grail ([YouTube](https://www.youtube.com/watch?v=RbTaP0_Galg))
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

- Use of two or more different factors during authentication
    - Must be different _factors_ (categories)!
- Why it helps
    - Defense in depth
- Tradeoff: Security versus convenience
    - Consider: Make MFA more convenient, and you can make systems and data more secure
        - Examples. Integrating fingerprint scanning hardware and software into laptops. Integrating face-scanning software into cell phones.

### Passwords

- Still a common form of authentication

#### Poll questions

(Ask aloud to the group, answer silently to yourself.)

- How many passwords do you have?
    - Give an order-of-magnitude estimate: 1, 10, 100, 1000,....
- How do you manage your passwords? (Select all that apply.)
    1. I use the same password or similar passwords for most or all of my accounts.
    2. I write down my most commonly used passwords on a sticky note and post it on my \{ computer screen \| keyboard \| desk drawer \}.
    3. I save them in my Web browser (for example, using the "remember me" feature).
    4. I write down my passwords in a notebook and look them up when I need them.
    5. I use a password manager.
- Discuss the tradeoffs of each method of password management.

#### Password best practices

- Don't reuse
- Make sufficiently long
    - Complex?
    - See [NIST](https://pages.nist.gov/800-63-3/sp800-63b.html#appA), [xkcd](https://xkcd.com/936/)
- Use a password manager (maybe?)
    - Tradeoffs
    - If you use a password manager, then...
        - make sure your password for it is strong
        - strongly consider enabling MFA

### Your turn

For each scenario below, identify (a) what is the identification, authentication, and authorization; and (b) identify the factors of authentication used. Which scenarios implement multi-factor authentication (MFA)? Which implementations do you think are most secure? Which are convenient? Why?

1. Before you cross the Bridge of Death, the bridgekeeper asks you your name, your quest, and a secret question.
2. When accessing a website, you are prompted for your username and password.
3. At the entrance to your work (or school, or gym, etc.), you are asked to swipe your ID, then give your name and date of birth.
4. When signing in for a cybersecurity certification exam, you are asked to present two forms of ID, one with your photograph and one with your signature; sign your name on a digital pad; and sit for a head photograph.



## Best practices

### Suspicious files and links

- [Joe Sandbox](https://www.joesandbox.com)
- [VirusTotal](https://www.virustotal.com/gui/)

Note: If you upload a file, then assume others will see it (and potentially the info it contains).

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



## References

1. Grubb, S. (2021). How Cybersecurity Really Works: A Hands-On Guide for Total Beginners. United States: No Starch Press.
    - ISBN-13 978-1-7185-0128-7
