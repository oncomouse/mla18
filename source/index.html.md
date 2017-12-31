---
title: MLA 18 – Info Sec
description: |
  This site is a guide for anyone interested in using better information security practices in your work as an academic. Specifically created in support of a workshop at MLA 2018 in NYC.
---
# <small class="pl4">MLA 18</small> <br> Commonsense Information Security for Academics
{:.lh-solid.mb5-ns.mb3}

## Tonight's Outline
{:.lh-title}

The goal of tonight's event is to help you. We want to answer your questions about information security: how should I be securing my data? Should I be worried? What are best practices? Where can I learn more?
{:.pl4-ns}

We will go over the basics of information security, including what it is and how encryption, the main tool of information security, works. We will also talk about practical approaches to analyzing how much security you may need. After that, we plan to turn it over to your questions, concerns, and ideas.
{:.pl4-ns}

1. What is Information Security?
	* What is Encryption?
	* Why do we Need it?
1. Why Should *I* Care?
	* Threat Modeling
1. What Can I Do?
	* Your Questions
{:.pl4-ns}

## Encryption

Encryption is the process of transforming a message that anyone can read (called "plaintext") into one that only people with certain tools can read (called "ciphertext"). An old example (used a lot in spy movies) is a book code. In a book code, you and I agree to communicate securely and decided on a particular edition of a very long book (often the Bible) to use as a message "key". Instead of sending each other the words of our messages, we could send numbers that represent a page number and the particular word on that page that was in the plain text (so if I wanted to encrypt the word "tomorrow," I would find "tomorrow" in my key text; say it is the 55th word on page 243. I could send you "`243,55`" in place of "tomorrow" and, using your copy of the key, you would go to the 243rd page, find the 55th word, and then now I was saying "tomorrow"). We would have to keep our book's secure; if anyone else knew what edition of the Bible we were using as a key, they could read our messages.
{:.pl4-ns}

Encryption is important because, on the Internet, anyone can read your messages. If you have access to any network hardware between my computer and the Internet (say at my ISP or further up at a trunk fiber provider) and I am not using any encryption on my traffic, you can see everything I'm doing: passwords, emails, bank account numbers, all of it. So, encryption is something we need online. However, how do we share a key before we communicate with new people? Do we have to find an edition of the Bible in common with our bank's? Thankfully, no: there is a technology called [Public-key cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography) that is reasonable secure for most applications and allows me to talk privately with anyone, without first agreeing on a key.
{:.pl4-ns}

However, the original designers of the Internet were not prepared for the degree to which it would be used nefariously (which seems obvious in retrospect, but I digress). Many of tools we need to secure our data online are not turned on because they are either inconvenient for us or slightly more expensive computationally for service providers.
{:.pl4-ns}

## Threat Modeling

Information security starts with a practice known as "threat modeling," that asks each of us to ask five questions to better understand how much threat we are under and what responses these threats might necessitate.
{:.pl4-ns}

The five questions:
{:.pl4-ns}

1. What do you want to protect? (**assets**)
1. Who do you want to protect it from? (**adversaries**)
1. How bad are the consequences if you fail? (**threats**)
1. How likely is it that you will need to protect it? (**capabilities**)
1. How much trouble are you willing to go through in order to try to prevent those? (**risk**)
{:.pl5-ns}

How you answer these questions determines your approach to information security. However, regardless of how ominous the threats you identify are, we can all benefit from adopting some basic security procedures.
{:.pl4-ns}

The big thing to remember about information security: the only truly secure information is the stuff you memorize, never write down, and never tell anyone. Obviously, that won't work for most people, in most applications, most of the time. So, we have to write things down, store them on a computer, and connect that computer to the Internet; however, just because doing so inherently exposes us to risks, does not mean we should give up hope or be overly confident in our protections. The trick to threat modeling is to have a strong sense of where threats may be coming from, so that we can avoid particularly risky behavior.
{:.pl4-ns}

* [EFF Handout on Threat Modeling](https://sec.eff.org/uploads/upload/file/15/Threat_modeling_handout.pdf)

## Resources
{:.lh-title}

Security is all about what you are willing to give up and what you are willing to gain. With that in mind, this list of resources is ordered from easy changes that we should all probably adopt up to things that are a bit more complicated and specialized. However, all of the categories here contain tools that can benefit us.
{:.pl4-ns}

### Browser Extensions

**Definition:** A browser extension adds functionality to your web browser beyond the basics. There are several that help protect your privacy online. They are a good first step in the world of information security.
{:.pl4-ns}

**Best Practice:** Install an ad-blocker (to prevent possible malware infection) and [HTTPS Everywhere](https://www.eff.org/https-everywhere%20) (to force your browser to use secure connections). Beyond that, a privacy protector such as [Privacy Badger](https://www.eff.org/privacybadger) is a solid choice, as well, but it can break a lot of websites, so read up on how it works before installing.
{:.pl4-ns}

* Recommended ad blocker for desktop: [uBlock Origin](https://github.com/gorhill/uBlock#installation)
* [MacWorld's list of best ad blockers for iOS](https://www.macworld.co.uk/feature/iosapps/best-ad-blocker-for-iphone-ipad-3665858/)
* [Adblock Plus for Android](https://adblockplus.org/android-about)
	- People recommend this one, but bear in mind: ABP lets companies pay to get through its filters
* [HTTPS Everywhere](https://www.eff.org/https-everywhere%20)
* [Privacy Badger](https://www.eff.org/privacybadger)
	- Be aware Privacy Badger has a learning curve
	- It *will* break websites
{:.pl4-ns}

### Password Managers
{:.lh-title}

**Definition:** A password manager stores your passwords in a secure blob on a remote server. Many of the best (ie. non-free) password managers offer browser extensions that will fill in password and other information (such as credit cards) for you. Most claim that they do not have plaintext of any data you store in them.
{:.pl4-ns}

**Best Practice:** Beyond storing your passwords, the best practice is to use a built-in password generator to create random, long passwords for your various services (usually as long as a service will allow you to use) and let the password manager track them for you. Then, you use an equally long but more memorable password to access your password manager (also, I find it's best to not use a password manager for any passwords you have to type frequently, such as a university account).
{:.pl4-ns}

* [PC Magazine's roundup of Best Password Managers](https://www.pcmag.com/article2/0,2817,2407168,00.asp)
	- They like [Dashlane](https://www.dashlane.com/), [Sticky Password Manager](https://www.stickypassword.com/), and [Keeper](https://keepersecurity.com/)
* I've used [LastPass](https://www.lastpass.com) forever, but it is a bit confusing to set up.
* [XKCD Password Generator](http://preshing.com/20110811/xkcd-password-generator/)
	- A famous [XKCD comic strip](https://xkcd.com/936/) outlined a more secure algorithm for generating long, secure passwords. Use this to generate your password manager master password and any other passwords you enter frequently by hand (university or computer logins).
{:.pl4-ns}

### Two-Factor Authentication
{:.lh-title}

**Definition**: Two-factor authentication (2FA) is a login system that requires you to use *two* different means of authentication. Usually this is one you know (a password) and one you keep with you (a cellphone or an RSA cryptographic token)
{:.pl4-ns}

**Best Practice:** Two-factor can be a bit inconvenient (and don't forget your authentication token at home!), but it really does increase your security and is essential on any email address that may contain sensitive information. Be aware that SMS (text messaging) is subject to a pretty scary man-in-the-middle attack, so do not rely on SMS as a good enough second factor in 2FA (though it is better than not using 2FA).
{:.pl4-ns}

* [List of Every Service Offering 2FA](https://twofactorauth.org/)
* [Google 2-Step Authentication](https://www.google.com/landing/2step/)
* [NetID 2FA](https://gateway.tamu.edu/duo-enroll/)
	- Sample University Account Enrollment Page
	- Check if your university has a similar program!
* [Apple 2FA](https://support.apple.com/en-us/HT204915)
{:.pl4-ns}

### VPNs
{:.lh-title}

**Definition:** A **V**irtual **P**riviate **N**etwork (VPN) is a service that creates a secure bridge through a public network from your computer to a private network. For instance, a common VPN application is accessing university library resources from off campus. To avoid having to add EZ-Proxy links to each journal you access, you could connect to your university's VPN. Then, to journals and the like, it looks like your connection is coming from the university's network instead of your home ISP.
{:.pl4-ns}

**What does that mean?** VPNs are a bit like a magical teleportation spell. If you access the Internet at home via Comcast, you appear as a Comcast customer to websites you visit. Using a VPN to connect to your university, however, routes all your web traffic through Comcast's network to your university's; once the traffic is at your university, it is then forwarded to the site you wanted in the first place. This re-routing makes it appear as though you are accessing a website from work instead of as a Comcast customer.
{:.pl4-ns}

**Why Use One?** If you've used a VPN before, chances are it's to securely access university resources. Many academics who work on sensitive research materials are required to use a VPN to access their data. However, you probably do not want to use your university's VPN for general web browsing, because then your university would have a record of every site you visited. Instead, you might use a VPN if you were concerned about local surveillance practices or copyright laws and wanted to route around them. In that case, you could contract with a VPN in a country with a more favorable jurisdiction. Additionally, if you are concerned about records existing of your web usage, many commercial VPN services do not keep records on their customers, so by using a VPN, you remove some of the possibilities for your ISP (or other groups) to keep tabs on your online usage.
{:.pl4-ns}

**Best Practices:** VPNs are useful in two main circumstances:
{:.pl4-ns}

1. You frequently access the Internet through insecure public wi-fi (libraries, hotels, coffee shops, etc).
2. You are concerned about your ISP or people watching your connection knowing where you go online.
{:.pl5-ns}

Most of us are more likely to find ourselves in **#1** than in **#2**; however, that it is not a reason to avoid a VPN. If you are accessing your email, student grades, your research, or your bank accounts over a public wifi (while traveling or working in public), connecting to a VPN (even your university VPN) beforehand is a solid practice. If, however, you are concerned with your online behavior being tracked, university VPNs are more than likely storing this information, so you, in the second case, you should consider investing in a commercial VPN service with strong privacy policies.
{:.pl4-ns}

* [A Good Overview of VPNs from *Forbes*](https://www.forbes.com/sites/leemathews/2017/01/27/what-is-a-vpn-and-why-should-you-use-one/#61df0b034b8f)
* [Virtual Private Network at TAMU](http://it.tamu.edu/Network_and_Internet_Access/Virtual_Private_Networks/Virtual_Private_Network_VPN/index.php)
	- An example of a university VPN
	- Search your university's website to see if you have access to one!

### Further Reading
{:.lh-title}

* [*Vice Guide to Not Getting Hacked*](https://motherboard.vice.com/en_us/article/d3devm/motherboard-guide-to-not-getting-hacked-online-safety-guide)
	- A lot of ideas for this event came from this guide. It's *very* thorough.
	- The section on securing your mobile phone is especially recommended.