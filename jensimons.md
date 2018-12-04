**Jeffrey Zeldman**: Hello, and welcome to the Big Web Show, everything web that matters. I’m Jeffrey Zeldman, your host, and my guest today is the amazing, the incredible Jen Simmons. Hi, Jen.

**Jen Simmons**: Hi, Jeffrey. I’m so excited. I haven’t been on a podcast in such a long time. I actually have missed it so much, so thank you for having me.

**Jeffrey Zeldman**: It’s fun. It’s my pleasure. Thank you for coming on the show. Jen, if you don’t know, is a designer advocate at Mozilla. She’s the creator of the Firefox Grid Inspector, which someone on Twitter today said was probably not the Dreamweaver or the Macaw, but was like, part of that … We used to talk, “Is web design ever going to be done visually and not by coders?” and said, “No, it couldn’t be,” and so this might be the start of it. This person was saying that there’s this … It wasn’t the Grid Inspector, it was the silhouette, the curve-

**Jen Simmons**: The Shape Path Editor.

**Jeffrey Zeldman**: The Shape Path Editor, which, actually, that’s something you do want to do visually. That’s not something particularly semantic. Anyway, I distracted myself in my enthusiasm. She’s the Firefox Grid Inspector creator, member of the CSS Working Group. She’s been teaching you how CSS Grid changes everything in web graphic design with a variety of online free articles and videos, chiefly in Layout Land, and she’s an advocate for designers, for good semantic code. She’s an advocate for justice and representation and inclusion in our medium, which is a whole other thing, and she’s also someone who’s been doing design for, like, more than 20 years, and before that, was in theatre design, and theatre generally. She’s the creator of one of the most popular podcasts ever for web people, The Web Ahead, which has been on hiatus while she’s been doing everything else. Welcome to the show, Jen Simmons.

**Jen Simmons**: Thank you.

**Jeffrey Zeldman**: Welcome back, I should say. We’ve had several of these conversations in the past.

**Jen Simmons**: Yeah.

**Jeffrey Zeldman**: You have a new thing that you’ve been talking about a lot, which I find very exciting. Intrinsic Web Design. You talked about it at An Event Apart Seattle a couple weeks ago in Seattle, Washington. Tell the good people what Intrinsic Web Design means, what it’s all about.

**Jen Simmons**: Yeah, so I stood onstage at An Event Apart, super nervous, because that is the place where Ethan Marcotte, eight years prior, had coined the term Responsive Web Design, sticking a flag in the ground, saying, “Hey, we’ve been doing layout in this way in the past, I’m going to draw a line, and now in the future, we should be doing it this way. This way’s a better way to do it. This is what I predict we’re going to be doing,” and Ethan was right. For eight years we did Responsive Web Design, which he defined as having a fluid grid, fluid images or flexible images, and using media queries to change the design at different break points. Make your design fit on mobile screens and desktop screens at the same time by going back to the roots of the medium, making things inherently squishy so that it would flow and be fluid depending on whatever the screen size is. We all know this, Responsive Web Design.

**Jeffrey Zeldman**: Right, and the web was inherently flexible, it’s just up until that point, up until we had those tools, and that way of thinking about it, the flexibility was kind of ugly most of the time. It was liquid design where someone with a giant monitor would have 18,000 characters in a line of text, which isn’t readable. We didn’t really want to do fixed width. We didn’t really want to pretend that the web was print. Well, there’s a lot of … Kind of, we did too, actually. I mean, you’ve been going back looking at lots of the earliest, I mean, right? David Segal and Hillman Curtis and Lynda Weinman.

**Jen Simmons**: Yeah, and so, I mean, Intrinsic Web Design is a name that I gave to this new era, because I think we’re really in a new era of layout design, and for anybody who’s been doing this for a while, you’ll remember these other eras that we had, where we’ve used HTML tables for a long time. We used Flash for a long time to do the whole website. We had this debate between fluid web design and fixed-width web design, and each of those eras had names where we would say things like, “Fluid versus fixed,” and everybody immediately knew what that was. You didn’t have to start over and define everything, and responsive was that kind of word. I feel like we need a new word for a new era where we can say, “Oh, it’s not that float-based thing where everything’s set in widths with using percents. It’s this new set of technologies.”

It’s not just because the tech is new, it’s also because the possibilities of what you can actually do are new, and the ways in which you can get content to morph and shift and change based on how much space is available is actually really different than Responsive Web Design. Over the last couple years, as I’ve been exploring and making demos and teaching people and showing people what’s possible, I kept using the word responsive, and kept thinking, “Well, this is just an evolution of Responsive Web Design. This is like Responsive Web Design bonus edition, with extra super powers,” but I finally got to the place towards the end of last year where it just felt like, “No, we need a new word.” It’s not Responsive Web Design. The way that I think about layouts and everything I’m doing, and the approach that I’m using … Specifically layout.

Nothing in the rest, or about what mobile is, or how content should be structure in a content management system. All of that is definitely the same. I’m just talking about layout, that layout itself, and the graphic design itself, had changed significantly enough that I wanted a new word so we could say, “Oh, yeah, that new thing,” and it includes CSS Grid, but it’s not just about CSS Grid. It’s also about using Flexbox, and kind of rediscovering what Flexbox is actually intended to be for. Plus, it’s about using some floats sometimes, using things like CSS shapes or object-fit, using a flow content, using multi-column. Some of these things are old, and they’ve been around for a long time, but it’s about thinking about the whole system of layout, and how all these pieces fit together in a brand new way.

**Jeffrey Zeldman**: Also, there’s now a framework. I hate to use that work with what it’s come to mean, but there’s actually a standardised … It’s the difference between tools and frameworks, I think. No, what am I looking for? There’s a framework that allows you to do these things without cheating. In the old days, you could make a curved shape by cobbling together a table layout with thousands of tiny pieces of imagines, for example, or thousands of little divs and spans to create a curved box, and then we eventually just had curves in CSS, and so all that we’ve been graduating towards, where CSS is actually a layout language, and I think when you talk about Intrinsic Web Design, what I take from it is, this isn’t a cheat anymore. It’s not a hack anymore, not that there was anything wrong with … We had to do what we had to do, right?

**Jen Simmons**: Right.

**Jeffrey Zeldman**: But now we don’t have to do those things. Now there’s actually some inherent tools. The standards, the specifications, these are the first … Especially Grid, it’s the first specification that’s actually designed for layout. When the folks from my era of standards design fighting, when they talked about layout, really what they meant was layout like Microsoft Word means layout. They meant in the document flow, you could set something to the left or to the right, you could centre something, you could make it bigger or smaller. Those things are layout, but they’re not layout as a graphic artist thinks of them, as a designer or an art director thinks of them.

They’re layout as someone who uses Microsoft Word thinks of them, as a scientist thinks of them, so anything else that we wanted to do, we had to cheat, and people became famous for coming up with these elaborate cheats, which is great. The creativity of the time was great, but we had so many hacks, and then we’d argue about, “Well, does this hack ruin the semantics?” Like, I would be against a certain popular framework because in order to do what it did, it forced you to use lots of non-semantic stuff, and fill your page with junk. I’m weirdly purist about that stuff, and I always thought, like, the dream is that you can just write markup and have elements flow like a design, and now you can.

**Jen Simmons**: Well, and as I’ve been looking at this, especially over the winter, the more I was digging in and writing the talk that I gave at An Event Apart a couple weeks ago, I realised that there’s actually been this pendulum swinging back and forth and back and forth where on the one hand, there’s been a group of people at any given time … This didn’t just happen in 2008\. This has been happening the entire time, where there’s one group of people saying, “Hey, we really need to respect the medium of the web. We need to have some kind of, you know, this is what the web is,” and you don’t get all of that, “Eye candy. Who needs eye candy?” You don’t get all of that pretty, pretty whatever. This is about having solid technology supporting the web and letting the technology tell us what the medium is.

On the other side of the pendulum is, “We really want to create something graphic or artistic or pulling in from the tradition of film or sculpture or art or whatever, and using visual language and communication languages to really convey to our users what’s going on,” whether you’re talking about branding or you’re talking about user experience, or you’re talking about just art. “We don’t care how hacky the code has to be. We don’t care what it takes to get there. We’re going to use tables for layout. We’re going to use Flash. We’re going to use these things because this is the way that we have right now to make art, and to create something that’s actually visually strong.”

**Jeffrey Zeldman**: Or, “Because our client or their customer expects a certain level of polish.” They won’t believe that they’re really at the Chase Bank if it doesn’t look somewhat visually organised, and they won’t be able to use it.

**Jen Simmons**: Right. We get that today when people have fights about whether or not you’re going to style form elements, for example, because there’s people who say, “Look, the form elements are part of the user interface of the software of the operating system that people are using. It comes with the browser. You don’t get to style them according to your brand. Get over it,” and then there’s other people who say, “No, we have to make this look like our bank or our whatever, and so we’ve got to style the drop-downs. We’ve got to style all of these little pieces, and if you don’t give us the CSS to apply to those form elements, then we’re not going to use your form elements. Everything’s going to be a div and a span, and we’re going to write a whole bunch of JavaScript, because we have to style these elements.” It’s that same tension.

**Jeffrey Zeldman**: And you know, we take sides in this argument, but both of these points of view are valid.

**Jen Simmons**: They’re actually both valid, and I feel like we’ve been in this world recently, and me too, in this world of like, “Look, Responsive is all over the medium, and if the designs aren’t quite as good as we want them to, too bad. We need to stay part of the web.” Part of when Responsive was introduced, it was about pushing that idea of, “It needs to be part of the medium. It needs to be what mobiles phones want us to be,” which is true, and as a way to get rid of the fixed-width layout era. The fixed-width layout era, I think, was much more of, “Well, this is what’s going to look good for visual design.” Now, to our eyes today it looks very old and hacky and weird, but at the time, it was the most beautiful that we could get.

**Jeffrey Zeldman**: And it printed well. You remember this, there were clients who would say, “How does the website look?” and then they’d look at it on a printout, or they’d look at it mounted on foam core, blown up and mounted on foam core, so we were coming from an era where that’s what their ad agency did. Their ad agency would bring ads mounted on foam core, and they expected the people making their website, which they looked at as design, not user experience design, interaction design, all that stuff. They looked at it purely as visual design, which is an important part of it, but not all of it.

**Jen Simmons**: It is important.

**Jeffrey Zeldman**: It’s very important.

**Jen Simmons**: I mean, really, what we want is we want both. We want to be able to have beautiful designs that convey brand, that use everything that we know about visual communication, whether that comes from print or film, or art, or sculpture, or whatever, and really leverage that, while simultaneously making it be really good code, semantic, accessible, reusable.

**Jeffrey Zeldman**: And performant and accessible, all that.

**Jen Simmons**: Performant. Performance is super important. SCO is super, so we want to do both at the same time.

**Jeffrey Zeldman**: It’s a false dichotomy. We seem to love that in our industry, where we’ll go like, “No, you don’t get to make it pretty,” or, “Oh, that’s just pretty.” There are people who diss Dribbble because you say, “Ah, that’s just aesthetically pleasing,” and like, what’s wrong with that? “That’s just an illustrator showing their tremendous talent.” Oh, well, we certainly don’t want that. It’s not a serious website unless it’s somewhat unpleasant to read. It should look sort of like it’s an Excel spreadsheet. Like, no, no, it should be beautiful.

**Jen Simmons**: But I think the fight has come from the limitations of the tech. We talk ourselves into doing it one way, and then we talk ourselves into doing it the other way. It’s okay to typeset everything in images, because that’s the only way you’re going to get custom fonts, and then later it’s like, “No, you shouldn’t typeset everything in images. You need to use real text on a real website. It needs to be real text, and if that means there’s only five fonts that you get to choose from, well, good luck with Georgia, again, because that’s what you’re going to keep using.” And then finally, web fonts came along, and we didn’t have to make that choice anymore. It could be a custom font, the font we wanted, and it could be real text that actually worked like real text, both at the same time. I think that’s where we’re at with layout right now. I think for the first time, we don’t have to choose hacks versus boring layout. We get to have both at the same time.

**Jeffrey Zeldman**: Responsive Web Design’s absolutely brilliant, let’s just acknowledge. It’s fricking brilliant, but it was still to some extent, because this is all we had, pretending we had columns, using flows to pretend we had columns because that’s we had, and it was brilliant, but now we don’t have to pretend. We actually have columns. Right now on your Twitter feed, which is twitter.com/jensimmons, there’s a pinged tweet, columns with percentages, and columns where some are fixed and some are percentages, and it’s just, you have this little animated GIF, which I guess you extracted from the Layout Land video on YouTube, and it’s just the most beautiful thing to watch.

**Jen Simmons**: Yeah, so I want to talk about that.

**Jeffrey Zeldman**: Okay.

**Jen Simmons**: Yeah, if you go to youtube.com/layoutland, you’ll see my entire channel, and there’s a three-part series that I just did this last week, showing people different ways to define tracks in CSS Grid. Those videos are specifically about CSS Grid, because there’s a couple things, if anybody wants to learn CSS Grid … Many of you listening may already be in the process of learning it if you write CSS. There’s a whole process of learning the syntax of how to define a grid, and then how to place items on a grid, or how to use the auto-placement algorithm, but the real juiciness of Grid starts to come once you’ve gotten past those basics, and then you sort of sit back and you think, “Well, how is it that I want to define my rows or my columns?” Even if we just think about columns, just kind of to think about things that we’re familiar with, defining columns. With the Responsive Web Design, you would define, “This is going to be 25%, 25%, 25%, 25%,” in which case, you ended up with four equal-width columns. They weren’t really columns, but we’ll pretend just to make it easier on an audio podcast. We’ll just pretend that those columns existed somehow.

You can do that in Grid. You can do percent-based columns, or you might use FR units, where you go, “One FR, one FR, one FR, one FR, one FR,” which is just a much, much easier way to tell the browser, “I would like to have four columns that each get one quarter of the space,” and then if you start to squish it, which I know normal users don’t, but us as designers, in your head, you should be squishing it in your mind’s eye, or as a developer, you’re squishing it just to see that it is working at every size possible, at every pixel. If you imagine squishing it, when you squish it, all four of those columns are going to get smaller at the same time, the same amount smaller, and then when you make it bigger, they all get bigger at the same time, the same amount bigger. Like, duh, of course. That’s all we’ve had so far. Grid gives us ways to actually define that flexibility so that it works in a more complicated way, where maybe certain tracks, certain columns, collapse.

They squish down to zero, while another column stays exactly the same size the whole time, and then, when there’s not enough space … Let’s say you’re getting smaller and smaller and smaller, you have two empty columns that are each one FR, and then you have a centre column of text that’s defined with a minmax() unit. Then the FR columns will shrink and shrink and shrink and shrink until they’re collapsed to zero, and then the minmax() syntax will kick in, and it will go from the maximum, whatever the maximum was, whether you set it in ems or pixels or character units, or you could set it in any of them. They’re all legitimate, but then you could squish it smaller, smaller, smaller, until it hits the minimum, and then it will stop squishing. It gives you two stages of changing things. Those FRs only collapse to zero because they’re empty. If they had content in them, they would collapse down to the min content width of those tracks, so if they had pictures in them or something, they wouldn’t-

**Jeffrey Zeldman**: They stay open even with no content in them. That in itself, right? Like, things that stay open even when there’s no content. That’s so new to CSS, and that’s so wonderful.

**Jen Simmons**: Yeah, and you could define fixed-width columns. You could say, “I want this column to always be 200 pixels.” You can use pixels again. It’s okay to use pixels again.

**Jeffrey Zeldman**: Thank you.

**Jen Simmons**: And then you can also use auto, so you’ve got these four possibilities. You’ve got fixed-width, you got FR units, you’ve got minmax(), and you’ve got auto, and when you combine those four different things together, you actually end up with four stages of things squishing or growing at separate moments. Like, one set will squish, and then another set will squish, and then another set will squish, and the last set will never squish. That blows my mind, and I didn’t read that. You can’t read the spec and understand that that’s what’s going to happen. I figured that out by making demos and then sitting there and looking at my demos and being like, “What is going on? This is amazing? Artistically, this is so juicy. There’s so much here that we could do.” Where you define text, for example, in an article, that like, ranges from one width to another width. It never gets smaller. It never gets bigger, and then you sort of separately define what’s going to happen with your white space, and your white space grows and shrinks, if it’s available, and then once you’ve run out of white space, then other things happen. This is all without any media queries. You don’t have to use media queries to make these things happen.

**Jeffrey Zeldman**: I want to say two things. I just have to pause and say two things. The first is, like, you’re describing purely visual things, and you are so good at what you do that I’m seeing them all in my head.

**Jen Simmons**: Good.

**Jeffrey Zeldman**: I think it is amazing that you can talk about this stuff and have people visualise, even, obviously, it’s super clear on Layout Land, where there’s video and you’re looking at what’s happening, but you understand it well enough and articulate it well enough that I’m actually seeing it and it all makes sense, and even someone, honestly, who wasn’t a coder, who had just the minimum of experience, like maybe four hours once having someone explain what CSS is, you’d get it. It’s very accessible, which I think is great because new technologies are always challenging. New ways of thinking are always challenging. You get kind of entrenched around what you’re good at and feel threatened by what’s new, and yet you just make it seem like complete common sense, and I find that really exciting.

The other thing I find really exciting is that this is like, you know, so the first web font demos were done by developers, and they were interesting and looked okay, but once designers, real designers, super talented designers got their hands on web fonts, whole new thing took place, and the same with Responsive Design. Ethan himself, really good designer, so his stuff looked beautiful, but other early Responsive Designs were more by mostly people who were super talented as developers, with some design expertise, but not tonnes of it. Then you get this new wave of very talented designers. Once very talented designers play with these things just the way you have been and see what they can do, and sort of have this living clay under their fingers where they can basically take magazine layouts, almost in this God-like way, just take … Here’s this magazine layout, and then you sort of mush your hands together and it becomes this other layout that’s equally amazing. I think once people see what they can do, there’ll be whole new levels of thought.

**Jen Simmons**: Yeah.

**Jeffrey Zeldman**: Like, any new technology, the first thing people do is imitate an old technology, right? So, drum machine gets invented and the first thing people do is use it like a regular drummer, but just to save money by not hiring a drummer, and then eventually, other people come along and make new musical forms with stuff no drummer could play, so it becomes this different, right, like, this late-’90s … What was it called? Not Grit Grunge. I forget what it was called. It had, “Gr,” in it somewhere, but it was like … Grind? I forget what it was called, but it was like this super fast house music that had these incredible drum beats that … When someone played with a drum machine, they would let you know, “We don’t just have to imitate what a human drummer would do. We could also do these other things.”

We’re going to have layouts that are really rethinking everything. I think one of the things I found very exciting with you as an evangelist is that you’re massively competent with the technology and at explaining it, but you also have this other thing where you’re talking about design, and I think people get really … It’s like people from both sides of that divide, where there is a divide, developers and designers, like, people who really feel much more comfortable with design or much more comfortable with development still can come together on this, and just be really excited by it.

**Jen Simmons**: Yeah. I’m excited, and I really hope that people who are designers, who don’t code, who either really don’t want to and won’t ever, or who have been thinking about it in the back of their minds, but they kind of never got around to it, but maybe they’re open to it. Maybe they will learn CSS any minute now, any month now. I really want all of those people to pay attention to what’s possible with CSS Grid, because even if you never write a line of code in CSS Grid, understanding what you can do with it is super important, I think, as a designer. Even if you only draw static drawings, you’ve got to understand how the flexibility models are different.

**Jeffrey Zeldman**: But you know, like, Sketch and Adobe XD have some responsiveness built in, and they’re not using code, but they’re just, this is what designers are going to want to do, so it’s part of the tool. I think if someone at Adobe is listening right now, make sure that when Adobe XD … It already has flexibility in the way a graphic design-oriented person can create stuff. Make it so that it uses these principles. You don’t have to be using the code. The principles exist. You don’t have to have a browser. You could use the same principles to make another kind of software.

**Jen Simmons**: Yeah, it’ll be interesting. I haven’t used those programmes or those features yet, but I wonder if they are, in fact, designed around the mental model of Responsive Web Design so closely that they’re not going to be able to give people, at least not yet, a way to do this Intrinsic Web Design, and have these multiple stages of flexibility where one thing squishes and then the next thing squishes after the first thing is finished. Yeah, if you make those programmes, you should totally check this out, because I would love to see the tools reflect the new capabilities of the web and be able to do these new things as well.

**Jeffrey Zeldman**: I mean, you’ve shown demos before, even just things that have been impossible that are done in magazines all the time, where like, there’s facing pages, and in the left page, there’s a full-page portrait of a person, and on the right, there’s beautifully set text about their achievements, you know, what they did, and you could split the screen on the web and try to make that work, but you were always sort of compromising with, “Well, depending on the depth of the browser, the face gets squished, or we start cropping part of the face out.” There’s all these compromises, but they didn’t really work, and now you can actually start thinking in terms of layouts like that, where it works like a magazine layout, but at the same time, it’s flexible. That’s uncanny.

**Jen Simmons**: Yeah, because you don’t have any control over the aspect ratio of the viewport, so if you want to make that kind of cover layout with a photo on the left and a title that’s both centred vertically and horizontally on the right, it was impossible in the float-based world. You could do that layout, but you had to know how many characters and how long the text was, or your math was going to get thrown off, and you probably needed to be fixed-width, because that way you could control some of those things more carefully, but if you wanted to make it in a fluid layout, then you had absolutely no control over the bottom edge. You had no idea whether it was going to be shorter or taller than the viewport itself, and you just had to be like, “Whatever, we don’t pay attention to the thing down there that some people call the fold. The fold doesn’t exist. We don’t care. It’s not possible. Don’t ask me to do a layout that has anything to do with that bottom edge.”

We did see Apple use vertical media queries. For a long time before Apple made their website respond horizontally, their website did respond vertically, and they would change the layout based on the height of the viewport at certain breakpoints where they’d say, I guess, sort of like, “If you were on this kind of laptop, get this layout, or this size of image, or this size of text, and if you have a taller screen, then make that image be bigger, or make that text be bigger,” but that was a very rudimentary way to swap out one fixed layout for another fixed layout at certain breakpoints. It wasn’t at all squishy. It didn’t respond.

**Jeffrey Zeldman**: What did we call that? When we did it horizontally, we used to have … adaptive layout, right?

**Jen Simmons**: Oh, yeah. I guess it’s a little bit of an adaptive layout in the vertical direction.

**Jeffrey Zeldman**: But it was a vertically adaptive layout. It seemed like magic at the time, though. I remember being very impressed by that stuff.

**Jen Simmons**: It was great, and people were writing about this, whatever, I don’t know, like, five to seven years ago, but the thing I’m trying to explain to people now is actually different, where like you said, you could do it where you can give an image both a height and a width, and use object-fit cover so that that image is not squished, that you don’t break the aspect ratio of the image itself, so if it’s a portrait of a human, you don’t end up with a face that’s squished, or if it’s a building, you don’t end up with a building that’s far too wide or far too narrow, where you honour the aspect ratio of the image, and yet, you set a fixed height and a fixed width that might be flexible. Might be like a two FR width and a one header vh height, and use object-fit cover to ask the browser to crop the image and have it sort of slide around so that the outer frame of the image and the image itself are handled independently. Things you could do with background. You’ve been able to do that with background images for a long time, but now you can actually do it with content images.

I also think that it is a matter of us reigniting our creativity. We can look back at earlier days of the web like the table-based layout era, or the Flash era, to get some really interesting ideas about our initial creative ideas about what to do with this medium of the web. I also think there’s a tonne in print. I’ve been looking especially at the early 20th century and the modern era when the photo typesetting machine came along and people were using paste-up to do layouts instead of using all metal. There was a boom in creativity in layouts, and VU magazine and other magazines, and kind of a whole new way to do visual communication through print because the technology changed. I’ve been looking into that, and I’m really enjoying taking some of these old very, very classic, very, very famous graphic design examples, and just challenging myself, and being like, “All right, that’s fixed, and it’s cool and beautiful. How can I recreate that in a medium that’s not fixed, and make some sort of flexibility model to handle this. Like, which parts should be fixed, which parts should be fluid? Which things should line up with which things?” Because the grid makes it super easy to code. It’s just a matter of having the right vision for what it is that you want to do.

**Jeffrey Zeldman**: It’s like opening a different part of your brain. It’s like playing three-dimensional chess.

**Jen Simmons**: Yeah, and that’s why I look a lot at film and at sculpture, too.

**Jeffrey Zeldman**: Which gets us into viewport. Film gets us into viewport. I want to talk about viewport and sculpture, and real white space, but before we do that, can I take a quick commercial break?

**Jen Simmons**: Yes.

**Jeffrey Zeldman**: Okay. I want to thank our sponsor today, Simple Contacts. Big Web Show is brought to you by Simple Contacts. Simple Contacts is a convenient way to renew your contact lens prescription and reorder your brand of contacts from anywhere in minutes. It’s vision care simplified. Here’s how it works. Need to renew your prescription? Take a five-minute vision test from your phone or computer. It’s reviewed by a licenced doctor. You receive a renewed one-year prescription and reorder your contacts. Have an unexpired prescription? Just upload a photo of your doctor’s information and you order our lenses. Simple Contacts offers convenience. Renew your prescription and reorder your brand of contacts from anywhere in minutes. No more doctors’ offices or waiting rooms. Speed. The vision test is self-guided and takes less than five minutes. Think of how much time you’ll save compared to making an appointment, getting to the eye doctor, taking time off, and so on.

Reliability. It’s designed by doctors and licenced ophthalmologists, and they review every test carefully to make sure your eyes look healthy, and that your vision hasn’t changed. Gives you choice. Simple Contacts offers all the brands of lenses you’re familiar with, including options for astigmatism, multi-focused lenses, coloured contacts, and more. Support. Simple Contacts customer support ensures every customer is 100% satisfied. You get text updates on your order and can ask questions or reorder via text any times. Savings. The vision test is only $20\. Compare that to an annual appointment which, without insurance, could cost you over $200\. The contact lens prices are unbeatable, standard shipping is free, and best of all, they’re offering a promotion to listeners of The Big Web Show. Just a reminder, this isn’t a replacement for your period eye health exam. Get $30 off your contacts at simplecontacts.com/bws, or enter code BWS at checkout. That’s simplecontacts.com/bws, or enter code BWS at checkout for $30.

Thank you, Simple Contacts, and we’re back with Jen Simmons talking about other ways of approaching layout, being influenced by things like sculpture and film language. Let’s start with the viewport. You tweeted something recently about, like, what does it mean to design for a medium that has a viewport?

**Jen Simmons**: I got an MFA in Film Production a decade ago? A little more than a decade ago, so I spent five years at film school, and some of those years were reading theory and learning about the history of film-making, and just studying the medium of film-making and learning about the evolution of when they first invented the film camera. It was this whole evolution of figuring out, what the heck is this thing and what is this medium?

**Jeffrey Zeldman**: Inventing editing.

**Jen Simmons**: Yeah, inventing editing. Inventing the idea that you could do one shot close up and another shot far away, and you could cut from one of those shots to the other one of those shots.

**Jeffrey Zeldman**: Do you remember the Kuleshov experiment? Did they tell you about that?

**Jen Simmons**: Yeah. Yeah, yeah.

**Jeffrey Zeldman**: Yeah, that was a great one. They had an actor take a neutral face, and they cut to a plate of food, and people said, “Oh, the poor man is starving. What great acting.” They showed them a woman changing into a nightgown and they said, “Oh, that lecher.” They read into his neutral face.

**Jen Simmons**: Right. That they could show the same exact clip of this man, but because of what it was cut against, over here it was cut against a violent scene, over there it was cut against food, over there it was cut against something else, and you would have different ideas about who this man is or what he is up to based on the shots that were in between the pictures of him. The pictures of him were actually the same the whole time.

**Jeffrey Zeldman**: Your brain filled in the gap between the two shots.

**Jen Simmons**: Yes.

**Jeffrey Zeldman**: Connected them. It was actually based on classic Marxism. Like, thesis, antithesis, synthesis. Was that Marx or was that Hegel?

**Jen Simmons**: I don’t remember.

**Jeffrey Zeldman**: Was that Hegel?

**Jen Simmons**: I should pull the books off my shelf to look some of this up.

**Jeffrey Zeldman**: It was one thing, and another thing, and then we connect them, but can we do that in web design?

**Jen Simmons**: The thing for web design is that there’s a frame. We have a frame, and if you’re shooting through a film camera, you have a frame, so the whole thing about cinematography is figuring out how do I take this camera, with this very tiny frame that only captures a little slice of the, “Real world,” and I have things move across that frame, or I pan the camera and I reveal things over time. That’s a pretty complicated question to figure out if you want to be a great cinematographer. How do you make choices? How do you have things go through the frame? What I’ve realised over the last several years as I’ve been digging deeper and deeper into all of these things is that we have a medium with a frame, and that’s maybe the bigger difference between print and web. It’s not just that the edges, that the paper is a fixed size, and the web is we don’t know how big. It’s that with paper, you look at the whole thing at once, or at least you look at a magazine spread all at once.

**Jeffrey Zeldman**: Yeah, you take it in all at once.

**Jen Simmons**: You look at two pages of a book all at once. You look at the book cover all at once. You look at a poster all at once, but there is this element of time on the web where things are scrolling through the frame, and I don’t think we really think about that very much. How is that more like a film, and not so much like a magazine?

**Jeffrey Zeldman**: Here’s a simple example everyone will get. In a horror movie, the monster is just off camera, and it suddenly comes into camera and everyone screams. That trick is just, there was some information that was hidden from us, and then it’s suddenly revealed, and we have a visceral reaction. That can happen as you’re scrolling. You could have something very surprising occur, and also, it doesn’t have to be vertical scrolling. LukeW used to talk about one way of organising content for mobile is, if you must, put the less important material just off camera, just outside of the viewport, but leave some indication, like there’s a little arrow or something that you can drag. When we were making carousels, we were practising  for this, for this way of thinking, because we had to show that there’s more than you can see here, and here’s an affordance that will let you, if you wish to, look at the other stuff, and also, there could have been surprises in what’s there.

**Jen Simmons**: Yeah, well, and you’re describing having a monster just out of frame and come into frame. Like, I don’t know how many of us are making websites with monsters on them, but I do think there’s a way in which you could think about what is it that people see when they first load the page, and then as they scroll, what do they see next? They scroll the things that they saw at first away, and then new things come into view, and we’re sort of used to thinking about what’s above the fold and making sure that that above-the-fold experience, that first screen loading experience, is really impactful, although in some ways now, what we’re doing is so trite that it has lost all impact. But before it became super-duper trite, we were doing things like, “Oh, we’ll have this hero graphic,” or, “Oh, we’ll make sure that the logo and the nav bar is at the top to make sure that everybody sees those and they know where they are.”

**Jeffrey Zeldman**: The first hero graphic was probably impactful, you know. The first time someone had …

**Jen Simmons**: Oh, I remember. It was beautiful.

**Jeffrey Zeldman**: “It’s a family. It’s a healthy family sitting on a bench. That’s never been done on an insurance company website. It’s filling the screen. How bold.”

**Jen Simmons**: It was really beautiful when it was new, but it’s just not new anymore, and the other thing is, those of us who have been around long enough, we remember before the thing where you have the logo on the top left and then you have a set of links horizontally across the top of the screen. That was a thing that got invented. Not to say that we shouldn’t keep doing that, but just to say we should realise that those are things that we made up at a certain time, and they may or may not continue to serve us. If they serve us, do them, but if they don’t serve us, you could maybe put the links on the side, or in the middle, or on the bottom edge, because you can actually control the bottom edge now. You can make sure that they’re shown above the bottom edge. I don’t know. I think there are ways that, even if you have the typical header at the top and you have an article, which is sort of the most basic kind of web design you can think about, you still can think about, like, what happens when you scroll partway through? The only thing that happens these days is ads pop into view. Ads get lazy like that.

**Jeffrey Zeldman**: It asks you to subscribe to the newsletter to continue reading.

**Jen Simmons**: Right. The overlay shows up and you can’t scroll because the stupid thing is on top of you. There could be other things that happen, and I think a lot about the data visualisations that show up around the election, or in election seasons, or some of the really great graphic design that has been done during the election seasons by important newspapers and publications. It will be interesting to see what they do given the reality of Intrinsic Web Design and what you can create now, because there is a way in which you could just make it a little more intentional what you’ve designed for that experience as someone scrolls something new into the viewport.

**Jeffrey Zeldman**: I think we don’t have time as part of our layouts, is one of the things I’m taking from what you’re saying, and I think it’s really important. I’ve got this giant monitor, and let’s go away from the article page. We know what the article page is. Let’s think about the homepage, which is where the client or the company, our product, we want to show all the things. We want to say so many things about ourselves, and who we’re for and what we represent, and what to do if you’re a salesperson, and where you should look if you’re a teacher, and where you should look if you’re a student. We do all these jobs on the homepage, and we talk about the customer’s journey, but we design in Photoshop or Sketch or whatever, where we’re looking like we look at a magazine layout, where we see everything at once. On our tall monitors, we see the whole thing and it’s like, “That’s a pleasing page design. My eye can scan the whole thing at once and it looks really beautiful on my big monitor,” but what’s happening is people are looking on their phones or on their laptops.

Let’s say laptop, because that removes the responsiveness part of the equation. They’re looking on their laptop and they’re seeing a piece of the story, and when they look down to the next thing, it may not be what they expect. They may not see, “How did I get from A to B? We haven’t gone from apples to oranges, we’ve gone from apples to bicycles. How did that happen? That’s not what I was expecting when I scrolled.” There’s actually a journey, a storytelling, time-based journey in scrolling, that I don’t think about when I’m designing a page, but I need to, and the more we can design on smaller screens, where we’re actually deciding in the browser and designing, to some extent, in the browser, the more we can start to think about that stuff.

**Jen Simmons**: Yeah, when we emailed these PDFs to each other, that’s where we kind of go wrong, especially if you’re looking at the PDF sort of zoomed out so you can see the entire PDF all at once. You’re the only person in the entire world who will ever experience the website like that. That’s not actually a website. That’s a PDF of a printout of a website that doesn’t exist and never will.

**Jeffrey Zeldman**: It’s kind of hard to have that conversation. There are people who insist on looking at it that way, and when you try to scroll to show this customer the journey that you actually thought about, they really want to see the whole thing, and then they have an issue or a problem with the whole thing, and again, they’re having an issue or a problem with something no one else in the universe will ever see.

**Jen Simmons**: Now, if you zoom in on that PDF, you can start to replicate the experience of the website because scrolling kicks in and a viewport kicks in, and you can only see a bit of it at a time, but I feel like the meetings are not acknowledging that reality of only seeing a little bit at a time of the page, and what people really want is they want to see the whole thing because they just want to think about it all at once, and they don’t want to think about, or we aren’t facilitating conversations where we have a chance to think about what you just described so beautifully, which is storytelling through a time-based journey.

**Jeffrey Zeldman**: Yeah, I think I was just paraphrasing you.

**Jen Simmons**: Yeah, but I like the phrasing of it. Storytelling through a time-based journey, that’s a perfect way to say it, because that’s what it is. You know, way back in the day before the web was invented, when everybody was talking about hypertext and hypertext medium, and hypermedia, and HyperCard was a programme some of us were using, and we were trying to understand what digital is, and what does it mean to be using a computer at all, and people were making CD-ROMs and video games were this thing, there was a lot of conversation about … And early websites did this too, where you had splash pages, and the journey, and you landed on a splash page, and then you clicked, and then you watched the intro movie, and then you clicked.

**Jeffrey Zeldman**: The entrance tunnel.

**Jen Simmons**: The entrance tunnel, yeah. People hate it. Users do not want that, so we can’t go back to that.

**Jeffrey Zeldman**: They loved it at first. The original users loved it because the web was an underground, kind of elite phenomenon. There weren’t that many people exploring it, and those who were, they were people who knew their way around the internet, to some extent. The first site that I worked on, where you saw an animated bat before there was Flash … They were movie fans who were interested in the underground aspects of the web.

**Jen Simmons**: I think there’s a couple things that were true. One of them is that we didn’t go to the web to get things done. We went to the web to explore this new cool thing.

**Jeffrey Zeldman**: Right. Back then, that’s what we did.

**Jen Simmons**: You didn’t go there because you needed toilet paper and you needed it in 15 minutes, and you didn’t want to go to the store, you went there because you wanted to discover things.

**Jeffrey Zeldman**: That’s why the early web designers hated Jakob Nielsen, because he was saying customers need the blue underline links. They want reliability. He was talking about usability-

**Jen Simmons**: Right. Speed.

**Jeffrey Zeldman**: … and he was right, and he saw what the web was becoming. He saw what Amazon was, but people wanted to go to K10K and explore a visual … a small group of people, very passively.

**Jen Simmons**: It was more like a video game. Like, “Oh, we’re going to hang out and play some video games.” Like, “Oh, I’m going to hang out and surf the web for a little while,” like it was a game too.

**Jeffrey Zeldman**: Right. A video game shouldn’t be, “Here are all the rewards that you can get, and there’s no mystery, and we’re going to reveal everything at once. Which rewards would you like?”

**Jen Simmons**: Put them in a shopping card and be done with it in under 90 seconds.

**Jeffrey Zeldman**: When I bought my first … I’d had a Windows PC. Well, I’ve had a DOS PC, and then a Windows laptop, and my first Mac was actually a Power Tower, Tower Power … It was a Power Computing clone. Power Computing clone.

**Jen Simmons**: Oh, right.

**Jeffrey Zeldman**: It was ugly, but it was a Mac, just in PC hardware, and to sweeten the deal, they gave you like 10,000 fonts. I didn’t know 10,000 fonts means three good ones if you’re lucky. They had a game. I wish I knew the name of this game. This was my first experience using a computer-based game, and you were walking into this dark cave, and things would leap out at you out of the dark, and I loved it so much. I hated the fact that you got killed and had to start over, because what I wanted to do was just spend hours exploring all the things that the artist had created. I just wanted to see all the creatures, you know what I mean? I wanted to see them come out at me. I wish I knew the name of this game. It obviously wasn’t a hit. I’ve discussed it with other people. Nobody remembers this thing.

**Jen Simmons**: Well, if somebody knows, they should ping you on Twitter or something, right, and let you know.

**Jeffrey Zeldman**: Even if I knew, I can’t play it now. I would need a System 6 Mac to play it.

**Jen Simmons**: Yeah, but that’s what, over at archive.org, they’re doing that. They’re setting up VMs that you can access from across the web to run and play old video games and old programmes from old operating systems.

**Jeffrey Zeldman**: That is a good point, and that is the greatest thing. I really want to do that, but it was about this time-based exploration, and people who made video games really got that. We can do that. It doesn’t mean make a website with characters and fake navigation and all that, but it means, think about this experience. I think that’s a really exciting way to think about-

**Jen Simmons**: The other thing is that back in the day, we were using modems, and modems are really slow, so if you went to a website at all, you were prepared to sit there for 15, 20, 30 seconds to wait for it to load, so if it took another five, 10, 20 seconds for it to show you an experience, you were like, “Well, this is just what I’m doing right now.”

**Jeffrey Zeldman**: You’d go make yourself a cup of coffee and come back when it downloaded.

**Jen Simmons**: The reality is just very different now, because now we work on the web, and we have tasks we’re trying to accomplish, and wasting people’s time is a killer. I’m not talking about creating that kind of an experience that takes more time. We don’t want that, but I think there is a way in which you can acknowledge that the fact that people are scrolling means they are seeing your thing over a period of time, and just designing for that reality.

**Jeffrey Zeldman**: I would love to keep talking about that, but we’re actually starting to run out of time and I want to get to one more thing that is part of Intrinsic Web Design and part of Grid, is real white space.

**Jen Simmons**: Yes.

**Jeffrey Zeldman**: Right?

**Jen Simmons**: Yeah, I was just about to say, I feel like you think about the viewport, there’s this tendency, especially designing a homepage, to want to cram everything into the above-the-fold experience of the viewport, and by acknowledging that this happens through time and that people do scroll, it frees us up to really let ourselves have more white space, and to not cram things so close together. I mean, we’ve always been able to have white space. You just put a big wide margin on something and you’re going to get white space, but recently, I forget who … I guess it’s the Vignellis. Lella and Massimo Vignelli were talking about white space and it being intentional. Like, just having a bunch of extra space isn’t really what’s meant by white space. What’s meant by white space is by intentionally designing clean, clear shapes, beautiful shapes, beautiful things that just look beautiful by having empty space, by having white space. Maybe it’s not white. Maybe it’s yellow or maybe it’s pink or whatever, but having this white space.

Grid lets us do that, not just throw extra space at the screen, but to control the white space and proportion the white space out, so maybe you always have this thing that’s a quarter of the height, always, or you have this way in which these two things overlap each other, because overlap is something else we can do in CSS Grid, and so the white space around those two overlapped photos is this beautiful L-shape, and it just maintains itself all the time, no matter how tiny the screen or how big the screen, and that you’ve designed the flexibility model such that the white space itself is creating branding, or feeling, or experience. It’s going to hard, but we need to let ourselves space everything out and have white space on the web.

**Jeffrey Zeldman**: I assume you’re going to write a book at some point, but one of the nice things with starting with Layout Land is that a lot of these concepts, they’re so elastic, they’re so time-based, that video is a great way to teach them.

**Jen Simmons**: Yeah.

**Jeffrey Zeldman**: It’s hard in a book.

**Jen Simmons**: Yes, because a book doesn’t squish, so basically, I’ll do-

**Jeffrey Zeldman**: Screenshots of different states.

**Jen Simmons**: … yeah, storyboards of different states. Either like, “This is what it looks like narrow, wide, in-between. This is what it looks like the first moment.” This is something I’ve talked about last year as well, where if we want to get away from the PDF, or we want to get away from thinking so statically, and we want to think more flexibly, and we want to think about time-based experiences, how do we do that without it taking forever to come up with the drawings or the communication medium? I think that you can do that with paper and pen. You can do that when you can draw storyboards. This is what the book would have, too, is like, how do you show this flexible, dynamic medium in a print book, or even a static eBook, by storyboards.

**Jeffrey Zeldman**: I love storyboards, and I love drawing the stuff anyway. It’s so freeing to draw the interface you think you’re … Obviously there’s a million decisions you haven’t made yet, and it’s really sloppy, and half the stuff you think you’re designing probably isn’t possible, but it’s a great way to just rough out ideas and discard them, and there’s no attachment. If I spend 16 hours in Photoshop making a comp, and then you go, “Nah,” I’m hurt. If I code that thing, and then you say, “Nah,” I’m hurt. I’m like, “I don’t want.” There’s always this hostility between designers and their bosses, designers and the marketing team, designers and developers, and it’s counterproductive, and I think if you start lo-fi and sketch, “This is the idea I have,” plus, it would free you to, again, once you’ve familiarised yourself with the things thank you can do in Intrinsic Web Design, then you can just sketch. You could maybe cut pieces of paper apart and show how you want things to work, and then sit down and maybe comp a couple of those phases, but you’d have those pieces of paper. You could make a mock-up, and the probably at some point, you get so good at the code that it’s easier to code then. I get the feeling that most of your layout ideas, you’re not starting in Sketch or Photoshop, you’re either starting with pencil or you’re starting in code.

**Jen Simmons**: Yeah. Personally, I like to use giant pieces of chart paper so that I don’t have to ever run to the edge of the page. I don’t want the edge of a small piece of paper affecting what I’m doing, so I just use chart paper, but I draw small. I draw small on chart paper, and then you sort of have this infinite canvas situation, and then I go to code, because the code is familiar to me. Also, I used to use QuarkXPress, Photoshop, illustrated or freehand, PageMaker, SuperPaint, and it was such a fun thing to have happy accidents happen where you meant to use this blur in Photoshop, but you accidentally hit something else and then you actually really liked it, and so you went ahead and went with that instead of the thing you meant to. I like having happy accidents in CSS. That’s how I’ve discovered a lot of the things that I am now talking about, because I’ve just been messing around in CSS and seeing what happens.

**Jeffrey Zeldman**: Instead of getting angry, “It didn’t work the way I expected,” you’re like, “Oh, that’s interesting. It worked differently than I thought. What could I do with this?”

**Jen Simmons**: I think it’s easier to learn code now. It’s always been really, really hard to learn float-based layout CSS, but you know, I feel like now, don’t bother.

**Jeffrey Zeldman**: Because they were not logical.

**Jen Simmons**: Yeah, because it was crazy. But now it’s like, don’t bother. Learn floats, because floats are cool for certain small things, but don’t learn that old school float-based whatever whatever, just blow that off and learn CSS Grid, learn Flexbox.

**Jeffrey Zeldman**: Floats are good for insets.

**Jen Simmons**: They’re good for floating and image and having text wrap around that image.

**Jeffrey Zeldman**: Yeah, exactly.

**Jen Simmons**: And applying CSS Shape, maybe, to the image, so now it’s not a rectangle. Now it’s a circle.

**Jeffrey Zeldman**: I’ve got a rectangular shape, a photograph of an author, I make the picture a circle in CSS, and I set it to the left or right of their name.

**Jen Simmons**: And then you flow the text around the circle instead of around the square. Yeah, so I would like to talk a little about the tools that are coming out in Firefox for all of these things.

**Jeffrey Zeldman**: Sure.

**Jen Simmons**: Because as I’ve been getting deeper into this and being like, “Oh my gosh, let’s … ” I got this job at Mozilla, and a big part of my job at Mozilla is to help platform engineering figure out well, what CSS do we need to be implementing. Like, “Oh, we haven’t implemented CSS Shapes yet. Let’s implement CSS Shapes,” which, by the way, we’re almost done with. Maybe it will come out at the end of this summer. Maybe it will take a little bit longer, but we’re getting closer and closer to having that be done. Also, it became kind of obvious in learning Grid and talking with folks about Grid, especially Rachel Andrew and Eric Meyer, and a whole bunch of folks in New York City who come to this thing called CSS Layout Club, or folks that I talk to on Slack, it became pretty obvious that we needed a tool. It was really hard, when you’re coding Grid, to know what’s broken, because of course it’s going to be broken, because you’re half-coding, it’s half-built. It’s broken. Like, well, why is it broken? Is it because I don’t know what I’m doing, or is it because the code on the container is wrong, or is it because the items are in the wrong place?

Having the grid be invisible made it really hard, so we were like, “We need a tool,” and so we’ve built … It’s been to Firefox since Grid landed, the day that Grid landed, a tool for inspecting Grid, and that tool is only getting better and better. There’s more and more features. I was in two meetings today talking to folks about adding the features that we need to add to it. But also, then we have CSS Shapes, and the Shape Path Editor. There was an extension made for Chrome by the folks at Adobe, including Rasvan Caliman and Alan Stearns, and it was awesome. You probably saw me present it two dozen times onstage at An Event Apart. Audiences always love that thing, so I was like, “I would really like to see us put that into Firefox,” and now it’s in Firefox. You can go to use Firefox. Nightly, especially, is the best place to see some of these tools that haven’t come out yet.

**Jeffrey Zeldman**: Where do people who don’t know, where do they go to get Firefox Nightly? Just Google Firefox Nightly?

**Jen Simmons**: The easiest way is go to nightly.mozilla.org, and it will land you on the correct page, and you scroll down that page a bit, maybe, and you get to Firefox Nightly. It’s a copy of Firefox that is the developer edition. It’s not the developer edition, but it’s like your dev server, like if you’re building a website and it’s like your dev server where you’re putting every night, developers are pushing their latest code onto the server so everybody can check it out and see what’s going on. Nightly is that.

**Jeffrey Zeldman**: It’s cool, too. It’s got a nice, cool night colour scheme.

**Jen Simmons**: Yeah. I think it’s a beautiful colour scheme.

**Jeffrey Zeldman**: I kind of prefer it to the orange fox now. It’s not a fox. Is it a fox?

**Jen Simmons**: It’s a fox, but it’s a purple fox with a green tail and a blue belly. But Nightly has all of the latest, and you can also turn on flags, and I make videos about how to do this. You can go to about:config in the URL bar, and go clickety click click on some crazy nerdy nerd stuff, and like, things that are kind of half-built, they’re not really ready to be in Nightly, they’re sort of still broken, they’ll be behind a flag and you can flip the flag on your copy of Nightly, and then they will be there and you can use them even earlier. And you know, Nightly, every once in a while, is broken. The other day it was crashing on me, but mostly it’s pretty stable, and I use it for my development browser. I use it to write code and to learn things.

We have the Shape Path Editor. It’s coming. It works on click path and it works on CSS shape-outside, like if you have a polygon or you have a circle, or you have … I was going to say triangle. That’s not a thing, but you have another shape, an oval, then you can adjust. That’s the thing you were talking about earlier. If you create a polygon, and then you need to make a refinement to it, it’s far easier to do that in a developer tool in Firefox Shape Path Editor because you don’t have to try to do the math in Illustrator and transfer the math over or whatever. We’re also working on a giant revision to the fonts panel that’s in Firefox. The fonts panel in Firefox right now will show you what font’s being used and where that font’s loading from, but the fonts panel that we’re creating is going to have sliders for variable fonts, so you can adjust variable fonts, and play around with those sliders. That’s kind of the first thing we’ll ship, but I really want us to reveal font features.

**Jeffrey Zeldman**: Yes. Reveal all the open type font features.

**Jen Simmons**: Reveal all the open type font features-

**Jeffrey Zeldman**: Ligatures.

**Jen Simmons**: … so, “Does my font have kerning? Does it have ligatures? What the heck is an old style numeral?” Just status information on whether or not it’s there, whether or not it’s working, and also on just like a drop-down. “Show me a drop-down, and I want to switch from small caps to not small caps, and I want to see what that does.”

**Jeffrey Zeldman**: Will it spit out the code for you? Will it spit out the CSS that addresses that?

**Jen Simmons**: Yup.

**Jeffrey Zeldman**: Okay.

**Jen Simmons**: Yup. What it will do, the editors will immediately rewrite the CSS that’s in what’s called the Rules pane, like the place where the CSS is, it will update that CSS, and you can copy-paste it the way that you’ve always copy-pasted it in the past and put it into your code. But also, our team is working, the developer tools team is working pretty hard on figuring out how to make the tool, to evolve these tools into something that’s more modern, where you could save the code that’s in the browser, that you could email the code that’s in the browser. You could handle it in a much more expected kind of way according to more modern software practises, so if you accidentally refreshed it or something, you wouldn’t lose your work. You could take those changes and put them somewhere else. There’s several folks working on that, trying to figure out how to make that work.

There are other tools. There’s a whole roadmap of, like, eight tools that we’re working on. I don’t remember all the rest of, but that’s the plan. It’s a tiny team. There’s not a lot of us, and we’re just sort of finding our way there. I periodically put videos up and tweet about them, if you follow me on Twitter. They’re not part of the YouTube channel. They’re actually on Vimeo, on my Vimeo channel, where I’ll put up a video that’s like, “Hey, look at this cool new thing. It just landed. Can you give us feedback? What do you think of this?” It’s especially helpful for people to use it when they’re writing real code, like you’re making a real website, and maybe you start using our Flexbox inspector, which is sort of at the very early stages, and you can see that, “Oh, yeah, this isn’t actually that useful. What would be more useful is this other thing,” and let us know. Help us. Remind us. Or say, “Yeah, actually, this is super helpful. This is super exciting. We definitely want more of this. We like this.” That kind of feedback can be very, very helpful.

**Jeffrey Zeldman**: This is great. We got Nightly. We got YouTube Layout Land. We got Twitter.com/jensimmons. Where else should people look for you?

**Jen Simmons**: They can go to jensimmons.com. It’s a horrible, terrible website, at least right now, in April 2018, it is. Sometime, hopefully, I’ll have time to make it better and blog there. I am working on some more things besides videos for layout.land.

**Jeffrey Zeldman**: Right.

**Jen Simmons**: They are still a ways off. I’m trying to get help for that so I can get some more velocity and get that stuff done.

**Jeffrey Zeldman**: And jensimmons.com has all these resources like designing with Grid, slides resources and more, video progressing our layouts, video revolutionise your page, real art direction on the web, et cetera, et cetera, et cetera, et cetera.

**Jen Simmons**: There are five one-hour talks there that if people really want to go in depth and you want to sit and watch an hour-long talk, or a 40-minute talk, totally watch those. Also, my YouTube channel has a lot of that same content, but in 10-minute chunks.

**Jeffrey Zeldman**: It’s chunked down into little 10, which is great. One of the most daunting things to me about videos is that I have to set aside movie time, and the beautiful thing with the 10-minute chunks is like, I just want to learn this one thing. I just want to learn what it means that I can layer white space. What does that mean, overlapping white space? Now I know. Now I get that, okay.

**Jen Simmons**: I also made them because I am hoping people will email them to other people on their team, where they’re like, “I know how to us initial-letter, and we should be using initial-letter, and these people are driving me crazy. We should be using this, but I can’t go over there and teach them everything.” It’d be like, “Well, email them the video. It’s seven minutes long. I show everything you need to know about initial-letter, and then your team can have a meeting where you decide whether or not you want to use it, where everybody has a little bit more understanding of what it is.” That’s my hope is that not only are they good for you to watch, but they’re also good for you to send to your colleagues to help you have better conversations with them, or your clients, even.

**Jeffrey Zeldman**: Any chance you’ll be reviving thewebahead.net soon?

**Jen Simmons**: I hope so, but I have so many projects going on that it’s not rising to the top. I want to build layout.land, I want to do season two of Layout Land video series, and I’m continuing to work on these tools all the time, and I got to rewrite my conference talk, and I got two books to write. Oh, and I got to redo jensimmons.com, and then maybe, maybe I’ll do The Web Ahead podcast. I miss it. I like doing it. I want to do it, but it’s especially a lot of work to book guests, and manage sponsorships and all that stuff, that I just haven’t … I don’t know if it’s going to happen sometime soon.

**Jeffrey Zeldman**: I often say this, but I think all of us are very grateful to you and Rachel Andrew for really bringing us here. Obviously, a lot of browser engineers are to be thanked, but the advocacy and teaching that you two have done over the past five years to really make this happen is pretty incredible, like a two-person, next-generation web standards project, just the two of you. I really appreciate it.

**Jen Simmons**: Thank you. Yeah, there was a big group of people who invented Grid and invented all the CSS, and I was not one of those people, and there’s a big group of people implementing it, building these tools, building the browsers, and I am not that kind of an engineer. My hope has been that, because I’ve seen CSS come where there was potential and we didn’t seize on the potential, and we used it in kind of a very limited way, and we didn’t have to be limited. It’s like, I really want us to jump way forward in graphic design and go back to the kinds of thinking that we started with, with thinking about it as an artistic medium, and thinking about how do we really design experiences that, with the budgets we have, with the time we have, and totally understandably, but still, even in small waves, just take everything to the next level and make sites that sing, because for some reason I care about that very deeply. I love design, and I want to see really, really great designs out there.

**Jeffrey Zeldman**: Making sites that sing. What a beautiful way to close the show. Jen Simmons, thank you so much. We’ll be back with another Big Web Show next week. Thank you. Bye.

### Show Notes & Links

*   [Jen Simmons (@jensimmons) | Twitter](https://twitter.com/jensimmons)
*   [Layout Land – YouTube – YouTube](https://www.youtube.com/layoutland)
*   [Jen Simmons](http://jensimmons.com/)
*   [Try New Browser Features in Pre-Release Versions | Firefox](https://www.mozilla.org/en-US/firefox/channel/desktop/#nightly)
*   [Jen Simmons | Labs](http://labs.jensimmons.com/)
*   [Layout Land](http://www.layout.land/)