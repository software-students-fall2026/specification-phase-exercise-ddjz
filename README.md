# Specification Phase Exercise

A little exercise to get started with the specification phase of the software development lifecycle. In this exercise, your team specifies a set of improvements and new features for [The Slide Machine](https://theslidemachine.com) — see the [instructions](instructions.md) for detail, and the [background](background.md) for an introduction to the software product you are tasked with extending.

## Team members

[Andy Chi](https://github.com/ac11238)
[Eddy Zhang](https://github.com/Yded21)
[Miki Osada](https://github.com/mosada2515)
[Tyler Wu](https://github.com/uwtz)

## Review of the Current Application

See instructions. Delete this line and replace with your team's findings from using the live app at https://theslidemachine.com — at least 10 specific observations, each labeled as a strength, a weakness, or a gap, and drawn from more than one team member's use of the app.

## Prior Art & Originality

See instructions. Delete this line and replace with a short statement of what your team checked (the project's Future Work and Open Questions, its roadmap, and its open issues and pull requests) and which parts of your proposal are original — new work not already specified, scheduled, or proposed by someone else.

## Stakeholders

## Stakeholder Research

For this exercise, we focused on two main stakeholder groups: students and instructors. 

We conducted interviews on two students and two teachers. Each stakeholder considered the current  model of the Slide Machine workflow.

The interviews focused on four questions:

What would you use The Slide Machine for?

What parts of AI-generated slides would you trust or not trust?

What information would you want before relying on a generated slide?

What would make reviewing or studying from generated slides easier?

The issue was clear. Both students and instructors did not know where the generated content was pulled from. 

## Stakeholder 1 — John

User Type: Student

Background: John is a NYU student who studies computer science and he uses the slides to mostly review for his exams or quizzes 

Goals / Needs

John wants to know that slides are representative of what the professor went over during class. Knowing that will give him a good idea of what the professor thinks are important facts or points in the class. He also wants to make sure that everything on the slides are reliable. 

Problems / Frustrations

His main frustration was that he couldn't easily tell whether information came from the professor or the AI and because of that he worries about studying incorrect AI-generated information that is not relevant to the class. She is not sure what versions of the information to trust. 

Observations

While reviewing a generated deck, John immediately wanted to know where a factual statement came from. He looked for some kind of citation or source indicator.

He said he would feel more comfortable studying from generated slides if he could click on a statement and see the relevant part of the professor's lecture or the supporting course material.

His main concern was very much a question of  "Where did this come from?"

## Stakeholder 2 — Josh

User Type: Student

Background: Daniel is a senior at SPS studying real estate

Goals / Needs

He uses the slides to help him remember what happened during the lecture. He also expressed desire to see the original explanation behind the short bullet points professors often uses because he believes that those often lack in depth and information in general.

Problems / Frustrations

He thought that AI generated bullet points actually removed important context and he couldn't tell whether something is a summary or new information added by the AI. 

Observations

Daniel was especially interested in the connection between a generated slide and the original lecture. He explained that a short bullet may make sense during class but become confusing later.He said that seeing the relevant lecture transcript would often be more useful than receiving another AI-generated explanation.His feedback suggested that source information could help students both verify information and restore lost context.

Instructor Stakeholders

## Stakeholder 3 — Professor Phillip Yoo

User Type: Instructor

Background: Mr. Yoo teaches Math at his NYC high school

Goals / Needs

He wants the source of the generated slides to only come from his lecture and pre-nurtured information to not confuse his students. He wants questionable AI-generated information to be easy to identify and have references throughout the slides. 

Problems / Frustrations

Mr. Yoo's expressed that the difference between uploaded material and generated content is not always obvious and that he is hesitant to share a deck without knowing whether the AI introduced new information even if that information is correct. 

He cannot easily tell what came directly from his speech and what was added by the AI.

Comparing every slide with the transcript would take too much time.

Small factual changes introduced during summarization may be hard to notice.

The relationship between uploaded material and generated content is not always obvious.

He is hesitant to share a deck without knowing whether the AI introduced new information.

Observations

Mr.Yoo was comfortable with the AI shortening or reorganizing his words. His concern increased when the generated text became more specific than what he remembered saying. He preferred the idea of a post-lecture review queue that would surface only the slides most likely to require attention.

## Stakeholder 4 — Mr. Avinash Vemuri

User Type: Instructor

Background: Mr. Vemuri teaches computer science at his high school at the Hill school 

Goals / Needs

His goal was to correct generated information without reviewing everything manually. He also wants quiz questions to be based on material he trusts. 

Problems / Frustrations

He worries that incorrect generated content could later become a quiz question.

Observations

Mr. Vemuri focused strongly on uploaded course materials. Because students are expected to use those readings, he wanted those documents to remain visible in the review process.

He said she would want to know two things when examining questionable content:

What did I say?

What do the course materials say?

He also preferred questionable slide content to be identified before it could influence quiz generation.


## Product Vision Statement

See instructions. Delete this line and place your Product Vision Statement here — one sentence describing the improvements and new features your team is proposing for The Slide Machine.

## User Requirements

Student:
- As a student, I want to be able to initate an AI auto checker, which will provide citations for the content of the slides, so that I can check on the factuality of the slide.
- As a student, I want to click the AI checker button to see sources relating to the content of the slide so that I know the slide is trustworthy.
- As a student, I want to click on the inlined citation to see sources relating to the content of the slide, and vice versa, so that I know the statement is trustworthy.
- As a student, I want to click on individual citations provided by the AI auto checker and open a seperate page with the source so that I can do further readings on the topic.
- As a student, I want the opened source to have related text highlighted so that I don't have to go looking for where the citation is refering to.
- As a student, I want the AI auto checker to provide additional resources from the web relating to the content of the slide so that multiple sources can be checked to reduce biases and inaccuracies.
- As a student, I want to see the result of the AI auto checker from the instructor or other students so that I don't have to run it again.
- As a student, I want to see edits made to the citation by the instructor so that I have the most up to day version of it.
- As a student, I want to be notified when the content of the citation has been modified so that I can see the latest changes.
- As a student, I want to mark certain citations for review so that the instructor can look over potentially inaccurate citations.

Instructor:
- As an instructor, I want to be able to initate an AI auto checker so that I can examine the accuracy of the contents and provide students with additional resources.
- As an instructor, I want to click on the citation links to open the source so I can examine the accuracy of the slides.
- As an instructor, I want to click on the citation to see where in the slide it is refering to so that I can check if it is cited correctly.
- As an instructor, I want to edit the citations so that I can remove false citations and provide students with accurate sources.
- As an instructor, I want to be notified when students have mark a citation for review so that I can immediately go review the accuracy of the citation.
- As an instructor, I want to mark citations as reviewed so that students know the citations is not unchecked AI generated content.
- As an instructor, I want to see the result of the AI auto checker from the students so that I review them for accuracy.
- As an instructor, I want to be the only one who can run citations so that students won't see AI generated info without first being reviewed by me.
- As an instructor, I want to limit what source files can be accessed through citation so that I can keep certain information private.
- As an instructor, I want to the AI to provide additional resources to the student so that they can do further readings.

## Activity Diagrams

See instructions. Delete this line and place images of your UML Activity diagrams here, each with the text of the user story it illustrates.

## Wireframes
<table>
  <tr>
    <td><img src="images/wireframe1.png" alt="wireframe 1" width="100%"></td>
    <td><img src="images/wireframe2.png" alt="wireframe 2" width="100%"></td>
  </tr>
  <tr>
    <td><img src="images/wireframe3.png" alt="wireframe 3" width="100%"></td>
    <td><img src="images/wireframe4.png" alt="wireframe 4" width="100%"></td>
  </tr>
  <tr>
    <td><img src="images/wireframe5.png" alt="wireframe 5" width="100%"></td>
    <td><img src="images/wireframe6.png" alt="wireframe 6" width="100%"></td>
  </tr>
  <tr>
    <td><img src="images/wireframe7.png" alt="wireframe 7" width="100%"></td>
    <td><img src="images/wireframe8.png" alt="wireframe 8" width="100%"></td>
  </tr>
</table>

## Clickable Prototype

Public prototype link: https://www.figma.com/proto/m49LvJzO3ys8Qu3oYZOTyc/Untitled?node-id=1-2&t=tivDDNUHfqrbaIVC-1&scaling=min-zoom&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=1%3A2&show-proto-sidebar=1 

## Stakeholder Demo

See instructions. Delete this line and place a link to the deck The Slide Machine generated during your presentation here, after you have presented.

## Exit Ticket

See instructions. Delete this line and place a link to the exit-ticket quiz you generated from your demo deck and distributed to the class, along with a short note on what — if anything — you had to correct in the generated questions before publishing.
