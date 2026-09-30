# Specification Phase Exercise

A little exercise to get started with the specification phase of the software development lifecycle. In this exercise, your team specifies a set of improvements and new features for [The Slide Machine](https://theslidemachine.com) — see the [instructions](instructions.md) for detail, and the [background](background.md) for an introduction to the software product you are tasked with extending.

## Team members


Danial: [Github](https://github.com/catw1thtea)
Denise: [Github](https://github.com/denisekos)
Jay : [Github](https://github.com/Jayyu2005)
Zee : [Github](https://github.com/manzim7)

## Review of the Current Application

### Strengths

1. The Slide Machine picks up everything you say.
2. The Slide Machine transcribes your words at the bottom so you can make edits if anything goes wrong.
3. The Slide Machine also summarizes your points if they're too lackluster or too long.
4. For first-time users, the app is very easy to navigate and use.
5. Highly customizable, so users can pick up the slack where the automation falls short.

### Weaknesses

6. As a first-time user, it gets confusing when the presentation ends (it leads to an abrupt ending) since slides are generated as you speak.
7. The slides can change and show the wrong information even if there is only one misspoken word in the transcript.
8. The playback mechanism is very confusing and often goes over the script way too fast, leaving viewers unable to follow the slides.
9. As a new user, the playback feature doesn't announce slide titles or signal when slides are about to end or switch, which can leave out a lot of information and make it hard for the audience to take notes or understand the topic.
10. Tab reordering is finicky and tedious, and it can look like nothing actually changed.
11. When using seed material, TSM tries to finish sentences with direct matches from the material rather than listening to dictation.

### Gaps

12. There is no way to undo a change.
13. It is very difficult to get TSM to add content exactly where you want it, and new content may replace existing content, especially when speaking.

## Prior Art & Originality

We checked the project’s design documents (future work and open questions sections of docs/SPEC.md and docs/ROADMAP.md) and found that the app already has public lecture feeds, search, voting/boosting, and profile pages. What we are proposing as a new feature is the “Following” feature, where students can follow an instructor or a specific course and see their lectures in a dedicated Following tab. Instructors can use this feature similarly to follow students in courses that have many student presentations, making it easier for instructors to access when reviewing presentations to grade.

## Stakeholders
### Student 1: Grace L., CS Student at NYU

**Type of user:** Student

**Goals/Needs**
- Annotate my slides easily (like on GoodNotes or similar apps).
- Showcase code snippets and math formulas for my natural language processing course final presentation.
- Access presentations easily, both my own and my professors'.
- Present smoothly without looking at a script or relying too heavily on speaker notes (a personal struggle).

**Problems/Frustrations**
- Difficult to speak without notes in front of me. I usually see the slide and then speak, not the other way around, so this would take time to get used to.
- Difficult to present code syntax (e.g. when explaining how pointers work in C).
- All presentations that aren't mine are jumbled into the Discovery section in order of last created. It's unorganized, since I have to filter it myself by typing in the professor's name.
- I missed a concept in my presentation and The Slide Machine didn't catch it. This makes me want to go back to conventional presentation software, since missing a critical detail or concept could be very bad.

### Student 2: Mandy T., Econ & DS Student at NYU

**Type of user:** Student

**Goals/Needs**
- Review and access my professors' lecture notes and recordings with ease.
- Explore other people's presentations and topics that might interest me.
- Convenience: present without much effort making the slideshow, just knowing the content in my head.
- Build slides directly from existing material like textbook passages.
- Keep lectures from my different courses organized, since I study both economics and data science.

**Problems/Frustrations**
- The quiz is hard to find because it's hidden inside Settings. It should be on the main toolbar or on the last slide instead.
- You can't turn textbook passages into slides, or turn slides back into speaker notes.
- In subjects like science or math, discussing symbols gets confusing when translating from speech to writing.
- Although I want to present without a lot of practice, I don't want to go in completely blind either. There is currently no way to rehearse (my presentations are graded, and I feel uneasy walking in without practice).
- No way to limit or anticipate the length of a presentation because you can't rehearse it (many of my presentations are capped, e.g. at 10 minutes).

### Student 3: Kennard S., Finance Student at NYU

**Type of user:** Student

**Goals/Needs**
- Present on a wide range of business topics, from economics and finance news to pitches and case studies.
- Match a presentation's colors to the company in a case study.
- Provide appropriate visuals (photographs, diagrams, graphs, numbers, etc.) to help the audience visualize what I'm saying.
- Find strong presentations from classmates or other students to use as examples for case studies and pitches.

**Problems/Frustrations**
- Very text-heavy. Many business professors ask for fewer than 10 words, or none at all, on slides. It would be nice if it generated relevant images instead (e.g. if I say the stock price is falling, it shows the Wall Street bull or a downward graph).
- Visually lacking. Many NYU consulting and finance courses expect slide colors to match the company in the case study, and there isn't enough customization to do that.
- Having the exit ticket link in Settings is unintuitive. It's a feature of the presentation and should be more visible and accessible.
- It would be nice to turn the exit ticket into a questionnaire for a different kind of audience engagement (there's no point giving my professors an exit ticket).

### Instructor 1: Jacqueline K., TA for Intermediate Microeconomics and Discrete Math at UVA

**Type of user:** Instructor

**Goals/Needs**
- Show and explain the different types of graphs and diagrams in microeconomics and how to apply them.
- Give students practice problems and walk through solutions to build problem-solving skills (learning the theory alone is often not enough in economics).
- Keep track of what each student says during the discussion/seminar section.
- View students' biweekly case study presentations on my own time for grading.
- Share students' presentations with each other so everyone can study from all of them.

**Problems/Frustrations**
- It took a while to figure out what features were offered, because the main thing you see is the generated slides and it's unclear where to go from there. I wouldn't have known about the exit quiz ticket if I hadn't been told it was in Settings.
- Visually unappealing. For real lecture slides, it should look better and let me add specific images or diagrams. It can make a basic supply and demand graph if I define it explicitly, but struggles to draw more complicated graphs accurately.
- Visuals can't be moved. I asked it to generate a DFA and it put the wrong one on the slide.
- It struggled to capture all the equations I needed. I had 3, but it only wrote down 2. The layout was also inefficient, with one equation per slide when all could fit on one. It was also hard to make slides for in-lecture exercises (it didn't capture the data and the format was off).

### Instructor 2: Amr E., TA at Georgia Tech

**Type of user:** Instructor

**Goals/Needs**
- Recap mathematical concepts from the professor's lectures with more examples, exercises, solutions, and problem-solving methods.
- Use visuals and text to engage students and help them understand.
- Check students' understanding after my presentation or lecture.
- Let students easily look back at my slideshow to study on their own if they missed the discussion or a detail.

**Problems/Frustrations**
- The quiz lacks math content and visual graphs.
- The Playback feature feels unnecessary because it doesn't spend enough time on each slide. Most slides get skipped since the transcription is much shorter than the slide content.
- It would help to be able to lengthen the time spent on a slide before Playback moves on.
- Images sometimes don't come out the way I want, and I can't edit them.

## Product Vision Statement

The Slide Machine turns what instructors say in class into the slides students study from. However, these slides are difficult to locate locally on the “Discovery” tab. “Following” helps students find those lectures again by letting each student follow the instructors they learn from and see their lectures in a personal view of Discover, without creating class rosters or revealing anything the student couldn't already see.

## User Requirements

### Students

1. As a student, I want to follow my professor so that their new lectures show up without me searching their name every time.
2. As a student, I want to follow a specific course rather than everything a professor posts so that I only see lectures for classes I'm actually taking.
3. As a student, I want a Following tab that shows only lectures from people and courses I follow so that I can review my professors' material without scrolling through unrelated decks.
4. As a student, I want to filter the Following tab by course so that I can focus on one class when studying for its exam.
5. As a student, I want my follows to stay private so that I can organize my feed without instructors or classmates seeing it.
6. As a student, I want followed lectures highlighted in the regular Latest feed so that I can still explore other presentations without losing track of my courses.
7. As a student, I want to edit or unfollow at any time so that my feed stays current from one semester to the next.
8. As a student, I want to follow classmates who share their presentations so that I can study from my peers' work to improve my own presentations.
9. As a student, I want to see everyone I follow in one list so that I can manage my follows in one place.
10. As a student, I want a followed course's lectures shown in the order my professor arranged them so that I can study them in the sequence they were taught.

### Instructors

1. As an instructor, I want students to find my lectures without me sending links after every lecture so that reviewing lecture notes is easy for them.
2. As an instructor, I want my lectures grouped under the course they belong to so that students who follow that course see only relevant material.
3. As an instructor, I want my newest lecture to be most visible to my followers so that students who missed class know what to catch up on.
4. As an instructor, I want to share one link to my course page so that students can follow it in the first week of the semester.
5. As an instructor, I want my lectures' visibility settings respected so that restricted lectures stay restricted, even to followers.
6. As an instructor, I want a lecture I move into the correct course to appear for that course's followers so that a filing mistake doesn't hide it from students.
7. As an instructor, I want the lecture order I arrange to be chronological (newest at the top) so that my followers can track lecture notes by date and order.
8. As an instructor, I want to follow the professor whose course I TA for so that my recap sessions stay aligned with their latest lectures.
9. As an instructor, I want to follow my students' shared presentations so that I can review them for grading on my own time.
10. As an instructor, I want to follow other instructors who teach the same subject so that I can find examples and ideas for my own lectures.

## Activity Diagrams

<img width="502" height="622" alt="Filter drawio" src="https://github.com/user-attachments/assets/1738ebad-775a-40b8-a51d-c80bd68eb310" />
As a student, I want to filter Discover to show only lectures from professors I've tagged, so that I don't have to search through every lecture to find the ones from people I actually follow.

<img width="386" height="577" alt="AddTag drawio" src="https://github.com/user-attachments/assets/db8c6c61-d118-4d5f-8eaf-a4def8eddb0a" />
As a student, I want to tag a professor so that their future lectures are automatically included when I filter Discover to just the people I follow.


## Wireframes

See instructions. Delete this line and place your wireframe diagrams here, covering every new screen and every existing screen your proposal changes, for every type of user.

## Clickable Prototype

[Clickable Prototype](https://www.figma.com/proto/d5Nwgc2r1okL3zrIyM9rIS/Porject-1?node-id=7-2&p=f&viewport=-208%2C245%2C0.14&t=yuIJyxmnDGrqpvM3-1&scaling=scale-down&content-scaling=fixed&starting-point-node-id=7%3A2&page-id=0%3A1)

## Stakeholder Demo

See instructions. Delete this line and place a link to the deck The Slide Machine generated during your presentation here, after you have presented.

## Exit Ticket

See instructions. Delete this line and place a link to the exit-ticket quiz you generated from your demo deck and distributed to the class, along with a short note on what — if anything — you had to correct in the generated questions before publishing.
