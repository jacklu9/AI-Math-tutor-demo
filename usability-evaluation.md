# Usability Evaluation

## Overview

This usability evaluation was conducted on the current version of the AI Math Tutor prototype. The evaluation used three methods: heuristic evaluation, cognitive walkthrough, and a post-task questionnaire with five simulated new-user responses. The analysis focuses on whether the interface can be understood and used effectively, whether the workflow matches users' likely mental model of step-by-step tutoring support, and whether the help-type structure supports learning-oriented AI use.

The heuristic evaluation uses Nielsen's 10 usability heuristics as described by Nielsen Norman Group (Nielsen, 1994; Nielsen Norman Group, 2024). The cognitive walkthrough uses the action-based questions from Wharton et al. (1994): whether users know what to do next, whether the correct action is visible, whether the label matches the user's goal, and whether the system gives feedback after the action.

## Heuristic Evaluation Results

### 1. Visibility of System Status

The prototype generally keeps users informed about their current location in the workflow. The four-step indicator shows the sequence of Add problem, Start, Choose help type, and Guided help. The Start stage also includes a progress bar, percentage value, and status message that changes from "Reviewing the problem" to "Ready to choose help." This supports users' mental model that the system is moving through a structured process rather than acting like an unstructured chatbot.

The current Step 2 wording is also consistent: the step label says "Start," the progress label says "Starting tutor support," and the current-step message says "Current step: starting tutor support." This consistency helps users understand that Start is not a separate feature, but the beginning of the tutor workflow.

### 2. Match Between System and the Real World

Most labels use familiar student-centered language. Help types such as "Understand the problem," "Continue my work," "Find my mistake," and "Reveal the answer in stages" match common student goals. The revised "Try another question" label is clearer than the previous "See a similar example" because it better matches a practice-oriented mental model.

The word "Start" is also easier to understand than "Prepare support." However, some of the system language still feels more system-centered than student-centered, especially "Checking the problem structure and useful math ideas." This is not confusing, but it may sound slightly technical for some students.

### 3. User Control and Freedom

The interface provides several recovery options. Users can edit the problem, go back to analysis, change the help type, and start over with a problem. These controls reduce the risk of users feeling trapped after making a choice.

The "Change help type" button is especially useful because students may not know which support type they need until they see the first response. This supports a realistic learning process where the user's goal may change as they understand the problem better.

### 4. Consistency and Standards

The overall interaction pattern is consistent. Cards are used for help-type choices, buttons are used for actions, and the step indicator remains visible across the flow. The tutoring response area also consistently uses message-style formatting.

The Step 2 language is consistent across the visible interface. The step label, status message, and progress label all use the Start/tutor-support wording, which strengthens the user's mental model of beginning a guided support process.

### 5. Error Prevention

The prototype prevents some common errors. The Start button is disabled when no problem text is entered, and the problem preview lets users check the input before moving forward. The "Reveal the answer in stages" help type also prevents immediate over-reliance on the final answer by separating hint, outline, worked steps, and final answer.

A limitation is that the input field does not validate whether the entered text is actually a math problem. Since this is a frontend prototype, this is acceptable for the current scope, but future versions could provide clearer feedback if the input is empty, incomplete, or not interpretable.

### 6. Recognition Rather Than Recall

The six help-type cards support recognition well. Users do not need to remember how to prompt an AI tutor because each card displays a title and short explanation. This is one of the strongest parts of the design because it turns an open-ended prompting task into a visible menu of learning goals.

The current six help types are also more distinct than the earlier version. "Try another question" is easier to distinguish from "Review relevant knowledge" because one provides practice while the other reviews concepts.

### 7. Flexibility and Efficiency of Use

The prototype supports different user needs by offering multiple paths through the same math problem. A student can choose conceptual explanation, knowledge review, continuation of work, a practice question, staged answer support, or mistake diagnosis. This gives flexibility without making the user write a custom prompt.

The interface is less efficient for advanced users who may already know exactly what they want to ask, because the flow requires them to move through the structured steps. However, for the intended learning-support scenario, the structure is appropriate.

### 8. Aesthetic and Minimalist Design

The interface is visually organized and avoids unnecessary content. The main screen focuses on the math problem, the current workflow step, and the available help choices. The help-type cards use short descriptions, which keeps the selection screen scannable.

The guided help page contains several panels and controls, including the work area, tutor guidance, optional ask field, photo upload, and navigation controls. The layout is still understandable, but it is the densest part of the interface. Future versions could reduce visual load by hiding optional input controls until the user chooses to ask a follow-up.

### 9. Help Users Recognize, Diagnose, and Recover From Errors

The "Find my mistake" help type directly supports error diagnosis. It identifies where the sample work first goes wrong and explains why the error matters. This is well aligned with learning because it helps users understand the cause of an incorrect solution rather than only seeing the corrected answer.

Navigation controls also support recovery from interface errors. If a user chooses the wrong help type, they can select "Change help type." If they want to restart the task, they can use "Start over with a problem."

### 10. Help and Documentation

The prototype does not rely on separate documentation. Instead, it provides contextual guidance through button labels, helper text, the problem preview, help-card descriptions, progress messages, and tutor response labels. This is appropriate for a small learning prototype because users should be able to understand the flow directly from the interface.

Additional documentation is not necessary for the current version, but short examples under the more abstract help types could further improve first-time use.

## Cognitive Walkthrough Results

### Step 1: Enter or Confirm the Math Problem

The user would likely know what to do because the page title says "1. Add the math problem," the text area is visible, and the problem preview appears beside it. The "Fill problem" button also helps users understand the demo scenario. The correct action is visible, and the disabled/enabled Start button gives feedback about whether the user can continue.

### Step 2: Select Start

The Start button is visible and simple. It matches the user's goal of beginning the tutoring process. This label supports a clearer mental model than "Prepare support" because users commonly expect a workflow to begin with Start.

After clicking Start, the system moves to the second stage and displays progress feedback. This confirms that the action worked.

### Step 3: Wait During the Start Stage

The user would likely understand that the system is doing something because the progress bar and percentage value are visible. The message "Reviewing the problem" gives feedback during the wait, and "Ready to choose help" indicates completion.

The current-step status also supports the action because it says "Current step: starting tutor support." This keeps the system feedback aligned with the Start label.

### Step 4: Select Choose Help Type

The "Choose help type" button is visible once the progress reaches 100 percent. The label matches the user's next goal because the system has already reviewed the problem and is now asking what kind of support the user wants. The transition to six help cards gives clear feedback that the user has reached the next step.

### Step 5: Choose One of the Six Help Types

The correct action is visible because each help type appears as a card with a title and description. The help types are understandable and mapped to common student needs. "Try another question" is especially clear because it communicates a practice function rather than another explanation path.

Some users may still hesitate between "Understand the problem" and "Review relevant knowledge" if they are unsure whether their difficulty is with the wording or the concept. However, the descriptions help reduce this ambiguity.

### Step 6: Review Tutor Guidance

After a help type is selected, the system gives immediate feedback by showing the selected help type, the tutor guidance panel, and relevant content for that mode. The user can continue by reading the guidance, entering a follow-up question, uploading work, changing help type, or starting over.

For the "Try another question" mode, the current design successfully keeps the practice question simple. The solution is hidden by default and appears only after the user selects "See solution." This matches a practice mental model: see a new problem first, then reveal the solution if needed.

## Post-Task Questionnaire

The following responses are simulated as five new users reviewing the current prototype. They are not real participant data, but they are written to model plausible feedback from first-time users.

Scale: 1 = Strongly disagree, 2 = Disagree, 3 = Neutral, 4 = Agree, 5 = Strongly agree

| Participant | Q1 Workflow easy to understand | Q2 Understood each step | Q3 Help types clear | Q4 Supports learning |
|---|---:|---:|---:|---:|
| P1 | 5 | 5 | 4 | 5 |
| P2 | 4 | 4 | 4 | 5 |
| P3 | 4 | 4 | 4 | 4 |
| P4 | 5 | 4 | 5 | 5 |
| P5 | 4 | 4 | 3 | 4 |

### Open-Ended Feedback

| Participant | Most confusing part and suggested improvement |
|---|---|
| P1 | The workflow was clear. The Start stage was easy to follow because the step label, progress bar, and status message used similar wording. |
| P2 | The six help types were useful, but "Understand the problem" and "Review relevant knowledge" felt close. Adding a short example under each could help. |
| P3 | The progress bar made it clear that the system was working, but I wanted a little more explanation of what was being reviewed. |
| P4 | The staged answer and mistake-finding options made the tutor feel more learning-focused than a normal answer generator. |
| P5 | The practice question was easy to understand, and hiding the solution first made sense. The optional ask/photo area felt a little busy. |

## Summary Statistics

| Questionnaire Item | Mean | Median | Minimum | Maximum |
|---|---:|---:|---:|---:|
| Q1 Workflow easy to understand | 4.4 | 4 | 4 | 5 |
| Q2 Understood each step | 4.2 | 4 | 4 | 5 |
| Q3 Help types clear | 4.0 | 4 | 3 | 5 |
| Q4 Supports learning | 4.6 | 5 | 4 | 5 |

Overall mean across all Likert-scale responses: **4.3 out of 5**.

The strongest result was Q4, which suggests that users would likely perceive the prototype as supporting learning rather than simply giving answers. The lowest result was Q3, which suggests that help-type clarity is still the main area for improvement.

## Rating Plot

Mean usability ratings by questionnaire item:

```text
5.0 | 
4.5 |                                      ████ Q4 4.6
4.0 | ████ Q1 4.4   ████ Q2 4.2   ████ Q3 4.0
3.5 |
3.0 |
2.5 |
2.0 |
1.5 |
1.0 |
```

## Overall Evaluation Conclusion

The current prototype is generally usable and understandable. The strongest usability qualities are the visible step-by-step workflow, the recognition-based help-type cards, and the learning-oriented tutor modes. The design supports users' mental model of a guided tutoring process by showing progress, offering clear choices, and allowing users to change direction if they select the wrong type of help.

The main improvement areas are help-type clarity and visual density. The help types are mostly clear, but "Understand the problem" and "Review relevant knowledge" could be further differentiated. The guided help screen could also reduce visual density by making optional follow-up controls less prominent.

Overall, the evaluation suggests that the prototype succeeds in making AI math support more structured and learning-oriented, while still leaving opportunities to improve wording consistency and first-time user clarity.

## References

Brooke, J. (1996). SUS: A quick and dirty usability scale.

Nielsen, J. (1994). Enhancing the explanatory power of usability heuristics.

Nielsen Norman Group. (2024). 10 usability heuristics for user interface design. https://www.nngroup.com/articles/ten-usability-heuristics/

Wharton, C., Rieman, J., Lewis, C., & Polson, P. (1994). The cognitive walkthrough method: A practitioner's guide.
