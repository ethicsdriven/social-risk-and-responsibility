# Designing for Ethical Online Discourse

## Initial outline
* Software engineers are responsible for design
	* Design is how it works, not how it looks
	* The choices we make have a direct impact on how people use our systems
* Software engineers have an ethical obligation to their users
	* We are hired professionals, that comes with a sense of professional ethics and insight
	* In the same way that lawyers have fiduciary duties, we have responsibilities to our users, our organisation, and society
	* Software engineers have an ethical obligation to push back on decisions that are harmful to individuals and marginalised groups
	* This is part of what’s meant by being a professional
	* Abdication of responsibility is tantamount to complicity
	* If somebody asked you to manufacture a bomb, you would say no. You wouldn’t say, “I’m just a welder, it’s up to my company as to what I’m welding”
	* A company that doesn’t value or address your ethical concerns doesn’t value your professional opinion and doesn’t deserve your time
	* Your job is not to write software – it’s to add value to the business – there is value in getting this stuff right
* Knowing what’s right
	* Systems designed for maximum attention are inherently problematic: attention is maximised by being surprising, alarming, extreme
	* A system that prioritises “engagement” will do so at the cost of moderation, moderate speech, and good discourse
	* Productive discourse is beneficial to users
	* “Freedom of expression” is not inhibited by speech policies
	* “Freedom of expression” is not the same as unfettered speech – e.g. hate speech, national secrets, yelling “fire” in a crowded theatre
* As with any feature, discussion feature benefits should be weighed against their potential costs
	* The best way to mitigate cost is not to build the feature at all
	* The best way to realise cost is to use a risk assessment model that encapsulates the direct costs (i.e. design and development), the ongoing costs (i.e. maintenance and moderation), and the externalities (i.e. cost of inciting violence)
* Checklist for review
	* Ownership
		* Get acknowledgement from the highest levels that the company is responsible for what happens on its platform – frame this around risk if you need to
		* Internally, decide what type of conversation you’re trying to encourage and formalise this so that designs can be discussed in the context of those goals
		* “Anything goes” is never the right answer
		* “Maximise engagement” will backfire
		* Don’t deliver an ultimatum – start a discussion, seek to understand everyone’s point of view and work to frame the issue so it is relatable and important
	* Algorithmic design
		* Using ML to promote content is fraught with danger
			* It is often optimised for engagement/attention, and therefore likely to amplify extreme views or upsetting content as well as encouraging group-think
		* Use ML for detecting harmful content
		* Use ML to combat disinformation
	* User interface design
		* Don’t autoplay media
		* Consider the impact of public versus private speech
		* Anonymous users are emboldened to think that their comments have no consequences (John Gabriel Greater Internet Dickwad theory)
		* Design should be done to support the community goals
	* Segmentation design
		* Consider what impact groups (or forum boards, subreddits, pages, etc.) has on the nature of discourse
	* Policies
		* Don’t hide the policy away behind a link, make it readable and confront the user with it
		* Explicitly call out for the support of marginalised groups
		* Have a moderation and banning policy
		* Protect safety and decency
		* Liken yourself to a bar; if a patron is misbehaving, kick them out – there are other bars to go to
	* Enforcement
		* Factor this into any plan; don’t design a system for speech without taking into account the cost of enforcement
		* Editorial judgement is necessary
		* Self-policing can be effective (e.g. StackOverflow), allow people to be rewarded for demonstrating ideal behaviour with tools to help them moderate – but it is not enough
		* Give tools for users to report behaviour, take reports seriously
		* Pay and support moderators properly
		* Don’t measure speed of judgement, measure qualitatively the quality of the community
		* Empower moderators to have a say in changes to guidelines, they’re closest to the front-lines
		* Have training and mental health support for moderators
			* Consider using a service that can help you vet the content – e.g. compare content hash against a known database of harmful content
		* Allow employees to report enforcement abuses anonymously without fear of reproach
		* Proactively and periodically ask for moderators feelings towards the goals in one-on-ones
		* Ban and block harmful content, including searches
			* e.g. Pinterest blocking anti-vaccination disinformation https://daringfireball.net/linked/2019/02/22/pinterest
	* Privacy
		* Treat the information given to as if it were your own or your family’s
			* Protect that information, secure it, use tools, services, and outside contractors to verify your protection
			* Follow NIST/ISO27001/OWASP standards
		* How do you reconcile this view with privacy? Tension: content should be moderated/conversations should be kept private; how can a private conversation be moderated?
		* Different threat model: public conversations are discoverable, searchable, offer a different kind of risk to private conversations
		* Private conversations should be kept private – ideally, end-to-end encryption
		* Law enforcement has many means of infiltrating conversations, skeleton key decryption at the cost of users’ security does not need to be one of them
	* Situational awareness
		* Be aware of how the shitposting and jokey irony can lead to extremism
		* Be aware of how your platform can be used to spread misinformation, hate speech, and illegal content
		* Keep tabs on the communities and how they’re coming to your site – hate speech cross-polinates
	* Response
		* When an incident happens, be prepared to respond
		* Never respond with “we can’t help it”, or “that’s not our job” – it is your job as ethical system designers
		* Accept responsibility, apologise, point to your long-standing policy and conversation goals, have a public postmortem with a resolution on how you intend to act
* Summary
	* You have a responsibility to your users and to your organisation to design a safe, secure place
	* You have the right and the obligation as professionals to challenge the design of the system beyond merely technical considerations
	* Be smart about how you broach the subject and start the conversation – understand all points of view, present risks, costs, and benefits in a way that everyone can grasp
	* Use the checklist to guide a productive conversation that leads to a beneficial outcome for for your users and your organisation

## Feedback

- Design is how it works as well as how it looks!
- A lot of this stuff is relevant because as Ruby developers we tend to work in small cross-functional teams where our opinions are sought in design discussions - but not everyone does - there is still some waterfallyness out there
- What kind of thing are you thinking of people working on when you talk about this? It might be worth giving some examples - from 'you work at Youtube' to 'you work at Trademe and are doing some things around the forums there' to 'your client wants a review and comment section in their online store' to 'you maintain the Pic's Peanut Butter website and are putting in a live Instagram feed of posts with a particular hashtag'

General thoughts:

- Some places do have security and privacy risk assessment practises, some don't - but I've never seen anywhere with a social harm risk assessment or mitigation model - if we are serious about building social software, should we be running fascist-propaganda-spreading tests as well as penetration tests - is there anywhere that does this?
- As with security, we should be able to detect social harm attacks and activate response procedures - you may run your application differently during a DDOS attack, and you may run your community differently during a social harm attack
- In a lot of cases, exit valves have been built in to this stuff (basically after the 2014-16 ISIS crisis that all of these platforms had, I recommend Rukmini Callimachi's podcast where she talks to someone who namedrops Tumblr, Instagram, Youtube etc in his radicalisation to join ISIS) - but it's basically not being used for economic reasons - and *chan fascists are better at manipulating these things than ISIS were
- Could be worth talking about/looking at some discussions about the HDCA
- Could also be worth talking about multilingual moderation?

Some good sources:

- I really like Clay Shirky's stuff - http://shirky.com/writings/
- Data & Society has some great reports - https://datasociety.net/


## Slides

![](./slides/01.png)
![](./slides/02.png)
![](./slides/03.png)
![](./slides/04.png)
![](./slides/05.png)
![](./slides/06.png)
![](./slides/07.png)
![](./slides/08.png)
![](./slides/09.png)
![](./slides/10.png)
![](./slides/11.png)
![](./slides/12.png)
![](./slides/13.png)
![](./slides/14.png)
![](./slides/15.png)
![](./slides/16.png)
![](./slides/17.png)
![](./slides/18.png)
![](./slides/19.png)
![](./slides/20.png)
![](./slides/21.png)
![](./slides/22.png)
![](./slides/23.png)
![](./slides/24.png)
![](./slides/25.png)
![](./slides/26.png)
![](./slides/27.png)
![](./slides/28.png)
![](./slides/29.png)
![](./slides/30.png)
![](./slides/31.png)
![](./slides/32.png)
![](./slides/33.png)
![](./slides/34.png)
![](./slides/35.png)
![](./slides/36.png)
![](./slides/37.png)
![](./slides/38.png)
![](./slides/39.png)
![](./slides/40.png)
![](./slides/41.png)
![](./slides/42.png)
![](./slides/43.png)
![](./slides/44.png)
![](./slides/45.png)
![](./slides/46.png)
![](./slides/47.png)
![](./slides/48.png)
![](./slides/49.png)
![](./slides/50.png)
![](./slides/51.png)
![](./slides/52.png)
![](./slides/53.png)
![](./slides/54.png)
![](./slides/55.png)
![](./slides/56.png)
![](./slides/57.png)
![](./slides/58.png)
![](./slides/59.png)
![](./slides/60.png)
![](./slides/61.png)
![](./slides/62.png)
![](./slides/63.png)
![](./slides/64.png)
![](./slides/65.png)
![](./slides/66.png)
![](./slides/67.png)
![](./slides/68.png)
