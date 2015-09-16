## Intro

Hi! My name  is Hermes Pique and I work at Facebook. Facebook is a great company that allows me to do many things, and one of them is help with accessibility.
 
Today I'm going to try something different. There's going to be no slides in this presentation. Nothing to see. And we're going to do a couple of activities. So I kindly ask you to close your laptops, and listen closely.
 
Let's talk about something that is deeply related with accessibility but that is not often associated with software: empathy.
 
By “empathy” I mean the textbook definition of the word. That is, empathy as the capacity to understand another persons' perspective.
 
To illustrate, I'd like us to do  a quick experiment.

## Activity: Credit Card Numbers

Take out any credit or debit card and hold it with your hands.
 
So there's a plastic card in front of you. Now close your eyes, and try to read the embossed numbers only using your fingers.
 
One by one. Picture the numbers in your head as you discover them. 4, 9, 4, 0. No need to say them out loud, just doing it to illustrate.
 
I'll give you a minute.
 
Got it? Easy? Hard? Probably a bit harder than you might have expected.
 
Congratulations! You put yourself in the position of someone who can't see. 
 
Now, the embossing in credit cards is not for blind people. It's there for imprinting. But embossing is the basis for braille, and your capacity to understand braille readers -your empathy for them-, has probably increased a little bit.
 
## The Disconnect

Why is empathy important? As developers, there's always a disconnect between the way we experience our products and the way our users do.
 
In our world, in the iOS development world, this disconnect starts with the Simulator. Which is where we spend most of our time testing apps.
 
The Simulator has access to all of the host computer resources. It never runs out of space, doesn't have other apps running in background. It's fast, allows us to iterate quickly. And we love it for it! Ask any Android developer what they think of their emulators.
 
But it doesn't stop with the Simulator. We tend to have the latest and greatest devices and OS. Who here has an iPhone 6 or 6 Plus? Raise your hand. iPhone 5? More than 50% of iPhone users still have an iPhone 5S or lower. That doesn't match what we see in this room. We might have even an iPhone 6S already!
 
It's not just about the device. We're tech savvy and work in a booming industry. We will most likely have a very good data plan and the best Wifi available.
 
And it's not even about technology. Most of us live in a first-world country and statistically motor or visual impairments are rare among us. We're a very specific and fortunate subset of the world. 

## A Vicious Circle

The disconnect between us and the people who use our apps is dangerous. 
 
We are the first user of our creations, and it's natural for us to think of -well- us when designing or coding apps. Yet, we represent a very small subset of people. This is specifically relevant for developers who work in isolation, such as independent app developers.
 
Still, most of the time we make conscious decisions to reach audiences different than us. Development time and resources are limited, so we pick our battles. Do we support iOS 8? iOS 7? That's 10% of iOS users to date. What about languages? English? Español? Right-to-left languages? If we have a test plan, shall we be include accessibility support in it? 
 
Those are all conscious decisions, and there are very good reasons to restrict your audience, specially in startups where focus is key.
 
It's the unconscious decisions that are most problematic. Did we notice when our app binary size grew above 100MB? Or when the sever started sending high quality images instead of thumbnails? 
 
If we're not careful, we might lose whole countries whose citizens don't have easy access to Wifi or who have bad connections in average, like Bolivia, to name one.
 
Eventually this becomes a vicious circle. We target a limited audience, which excludes the rest of the world. Since the rest of the world doesn't use our app, we don't hear about them, then we don't pay attention to their needs, and we never encounter their problems ourselves, so we keep building for the limited audience we first picked.
 
We're leaving people out, and we might not even notice.
 
The only way to break this vicious circle is with empathy. 

## The Visually Impaired

I want to focus on one specific kind of user as an example of applying empathy to our work: visually impaired people. This is because I had the opportunity of doing a lot of work with them in mind at my current job.
 
The WHO -the World Health Organization- estimates 285 million people with visual impairment, of which 39 millions are blind and the rest have low vision. In Spain alone we have 1 million. Not all of these are iPhone users of course, but the more accessible apps we make, the more reasons they will have to get an iPhone.
 
You might think this number is not big enough. Thinking of impaired users as numbers misses one very important thing. The effort you put into them makes a much bigger impact in their life. 
 
Making your app delightful with animations can make the difference between a 4 star and a 5 star rating. 
 
Making you app accessible makes the difference between people with impairments being able to use your app or not at all. An accessibility user is worth much more than the number one, and it doesn't require much effort, just empathy.
 
So how do we gain empathy for the visually impaired? If you have the opportunity, I wholeheartedly recommend witnessing a blind person using their smartphone. I had the opportunity a handful of times and learned two core things. 
 
That performing very simple operations in apps is often a struggle. But more importantly, I learned that making this better for them is within my reach.
 
If you don't know anyone blind with a smartphone, there's a more immediate way to increase your empathy for low vision or blind users. Simply, use your app as they would do. 

## Screen Readers

Visually impaired people use screen readers. A screen reader is one form of assistive technology that reads back what's on the screen. Typically, ensuring compatibility with a screen reader will also ensure compatibility with other kinds of assistive technologies.
 
The iOS screen reader is called VoiceOver and it's used by both the visually and motor impaired.
 
VoiceOver is  top of class when it comes to screen readers, and it's one of the reasons why many visually impaired people opt for iPhone devices. 
 
Not only VoiceOver describes elements on the screen, it also  redefines touch gestures to interact without requiring sight or precision. 
 
The 3 most basic gestures are: tap to describe an element, double tap to select it -this is the equivalent of a tap without VoiceOver-, and swipe to focus on the next or previous element. There's more gestures, but those are the most used.
 
To control VoiceOver there's a framework called UIAccessibility. I'm not going to cover the APIs, there's great WWDC talks that do that. Instead I'm going to do something much more useful. I'm going to teach you the most convenient way to turn VoiceOver on and off. 

## Activity: Accessibility Shortcut

Please take out your iPhone this time and unlock it.
 
Go to Settings and then General.
 
Within General look for the Accessibility option. Select it.
 
The Accessibility page has a lot of interesting options. If you haven't already, I recommend you to explore them. Right now we're going to ignore them and scroll all the way to the bottom to Accessibility Shortcut. Select it.
 
The Accessibility Shortcut defines the action of a home button triple tap. Please select VoiceOver.
 
Close Settings and triple tap the home button. Tap, tap, tap.
 
This will turn VoiceOver on. It might take a few seconds. Play on the screen with the 3 gestures I mentioned before. Tap to describe the current element, double tap to select it, swipe to change focus. I'll give you a minute.
 
Triple tap the home button again to deactivate VoiceOver. 

## Labeling

Now you're 3 taps away from testing your app with VoiceOver at any time. No need to do it now. But once you do, try closing your eyes.
 
The first thing you might notice once you test your app with VoiceOver is that a lot of it just works. UIKit components support accessibility by default and will often give VoiceOver the best possible description for themselves.
 
Still, VoiceOver might need a little guidance. For example, custom icons need to be labeled. This is because VoiceOver can't process images. It doesn't know that a gear is a settings button, or that a plus mean add a post. It might know they're buttons, but not what they do. 
 
So after the conference you go back to your place and try your app with VoiceOver. More or less everything you expect is there. You might be tempted to think that labelling everything in your app is enough. And yes, it might make your app accessible, functional. 
 
Labelling is perfunctory work. It's something you do tick out accessibility from a checklist. That's not what empathy is about. I'll give you 2 examples.

## Example: Wiggling Password Field

First example. Consider a login form with a password field.  When the user enters an invalid password the password field will wiggle, and perhaps change color. This is an example of using animations as visual cues, and giving something as mundane as a password field a little bit of personality.
 
For blind users, neither the animation nor the change in color will be perceptible. If we don't do anything VoiceOver users might be able to figure out that something went wrong and retry anyway. 
 
Or maybe not, and they might stop using the app. This is not a great experience, and defeats the intention we had when adding the wiggle animation.
 
How do we convey the same information in VoiceOver mode? How can we give VoiceOver users a similar experience? Fortunately the solution is very simple. We can play a nice error sound and make VoiceOver announce what just happened: "Invalid user or password." The sound takes replaces the animation.
 
This small work goes beyond labelling. We're actually designing behaviour specifically for VoiceOver users. It's still much easier than coding a wiggling animation, though.
 
It's easy to break things for some when we have only ourselves in mind when we test. Would we have detected that the wiggling password field was not accessible if we don't use the app with VoiceOver ourselves? Probably not. 

## Example: Gmail

Second example. We're going to look at a real app you might know. Let me turn on VoiceOver on my device.
 
Action: Toggle VoiceOver.
 
VoiceOver: VoiceOver On, Gmail, double tap to open.
 
Action: Double tap Gmail.
 
VoiceOver: Gmail, Inbox.
 
I'm talking about Gmail. 
 
Here is a search of my recent flights confirmations with easyJet, rendered in a nice table view. I'm going to go over each email using the swipe gesture to change focus. Listen carefully.
 
Action: Select first email, then multiple Swipes.
 
VoiceOver: “easyJet: Your booking...”, Select, checkbox, unchecked, double-tap to toggle setting, Star, checkbox, unchecked, double tap to toggle setting , “easyJet: Your booking...”, Select, checkbox, unchecked, double-tap to toggle setting, Star, checkbox, unchecked, double tap to toggle setting , “easyJet: Your booking...”, Select, checkbox, unchecked, double-tap to toggle setting, Star, checkbox, unchecked, double tap to toggle setting.
 
You might have noticed that after each email, we focus two checkboxes. This email list is certainly accessible, but it's a bit cumbersome to navigate, as we have to do 3 swipes per message. Also, when swiping quickly it's easy to forget the email that corresponds to a given checkbox.
 
For non VoiceOver users the cost of showing the Select and Favorite options for each email is relatively small in terms of UI space. It's just a checkbox at each side of the email.
 
For VoiceOver users, it's as if each email required 3 table view cells.
An alternative would be to hide these checkboxes from VoiceOver and use double tap and hold -the VoiceOver equivalent for long press- to make the corresponding actions show up as a dialog. This is what Twitter does for tweet actions, for example.
 
So with this change a VoiceOver user would go from email to email with swiping. If they want to select or favorite an email, they can double tap and hold to access these options. To make this discoverable, we can add a hint for each message: “Double tap and hold for to select or favorite”.
 
Would we have thought of these improvements if we don't seriously use the app with a screen reader? Probably not.

## Conclusions

The best way to discover how to improve our app for VoiceOver is to use it with VoiceOver. There's no magic. Without training, it's practically impossible to detect problems like the wiggling password field or the cumbersome email list from code alone.
 
By using apps with VoiceOver we put ourselves in the shoes of impaired users. This is what empathy is all about, and it's a principle that applies to all types of users.
 
Are you doing right-to-left support properly? Change your language to Hebrew and open your app. See what brakes.
 
Want to see how it really feels to use your app on the go? Try it with a 3G connection on the device, not Wifi in the Simulator. Turn off Wifi for a week.
 
If we limit ourselves to our own perspective, to our code and our tools, we will either ignore the needs of others, or simply do perfunctory work. 
 
There is a natural disconnect between the way we experience our apps and the way our users do. So we need to make an extra effort to be empathetic.
 
The first step to empathy is awareness. Awareness that others have different perspectives. I hope that if nothing else, this talk prompts you to explore how others really perceive your app, be it an average user, or someone whose life will be significantly better thanks to your efforts. 
 
And by doing so, it might change your life as well. I know it did for me. 
Thank you. And if you’re interested in making your app accessible, I’ll be around if you want to talk about it or check it out together.