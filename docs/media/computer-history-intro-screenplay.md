# Hello, Machine: How Ideas Became Computers

**Document type:** Cartoon screenplay and production brief  
**Status:** Draft for editorial review; no media generated  
**Audience:** Curious beginners learning computing, Rust, and specification-driven development  
**Format:** Thirteen chaptered scenes; illustrated 2D animation with readable graphic inserts  
**Target:** Approximately 18–22 minutes after adding demonstrations and viewer pauses. Timing is provisional; use a table read and animatic to establish the actual runtime. Dialogue alone will run shorter.  
**Companion:** [AI production prompt](computer-history-intro-ai-prompt.md)

## Premise and dramatic arc

Mira wants to make her laptop greet her friend. She assumes that a computer understands what she means. Byte, a small mechanical guide, opens a workshop of ideas to show how people learned to represent information, automate procedures, and program machines. Mira repeatedly improves a yellow instruction card. At the end, she uses that card to define a tiny greeting program precisely enough to test and implement in Rust.

The dramatic question is: **How can we turn an intention into behavior we can trust?**

The historical journey is a fictional teaching device. Developments overlapped across countries and communities. The scenes group ideas for understanding; they do not claim a single inevitable path from ancient counting to Rust or Spec Kit.

## Cast and performance notes

| Character / role | Appearance and voice | Purpose and character arc |
| --- | --- | --- |
| Mira — protagonist | Curious young adult; medium-brown skin, short dark curly hair, teal jacket, cream shirt, dark trousers; yellow pencil behind right ear. Warm, direct voice. | Represents the beginner. Starts impatient for a result, learns to ask better questions, ends ready to build and verify. Makes reasonable mistakes; never treated as foolish. |
| Byte — fictional guide | Palm-sized brass-and-ink automaton; square cream face, two black dot eyes, hinged limbs, small amber indicator. Dry humor, measured voice. | Explains mechanisms with physical demonstrations. Admits limits and distinguishes metaphors from actual machines. Its cartoon personality does not imply historical computers were conscious. |
| Narrator — historical context | Off-screen voice; calm, concise, distinct from Byte. | Supplies dates, attribution, and caveats without interrupting the central interaction. All dialogue is newly written, not historical quotation. |
| Workshop ensemble | Farmers, clerks, weavers, mathematicians, engineers, programmers, and users of varied backgrounds. | Shows collective invention and practical needs. Historical contributors appear in labeled vignettes; background figures are fictional composites. |
| Babbage and Lovelace — historical cameos | Respectful illustrated likenesses based on cleared references. | Appear in the mechanical-computation chapter. Narrator describes their contributions; no invented speech presented as testimony. |
| Logic and computing pioneers — historical cameos | Boole, Shannon, Turing, early computer teams, and later software teams in brief labeled illustrations. | Provide attribution without turning the story into a parade of lone geniuses. |

## Visual and audio direction

- Original watercolor-and-ink illustrations, warm paper grain, graphite outlines, restrained movement. Teal and slate backgrounds; amber/yellow denotes the recurring instruction card. Do not copy reference-video characters, shots, music, or assets.
- Preserve clear silhouettes and character proportions across all eras. Changes in room or machinery do not change Mira's clothes or Byte's design.
- Let the yellow card provide transitions: tally marks → procedure → punched pattern → encoded instructions → source code → acceptance examples. This is a visual metaphor, not a claim about literal historical descent.
- Keep code, dates, equations, and terminal output as clean editable overlays. Do not bake essential text into generated illustrations.
- Use gentle original or properly licensed music under speech. Mechanical clicks become electrical pulses, keyboard taps, and finally a quiet confirmation chime. Preserve silence during learner questions. Never communicate success or failure through color alone.
- Provide captions and a transcript. Read critical on-screen results aloud. Keep important action away from the caption area.

## Screenplay

### Scene 01 — A simple request

**Setting:** Mira's desk, present day. Evening.  
**Approximate allocation:** 1 minute.  
**Idea:** Human intent leaves decisions unstated.

**WIDE:** A laptop, notebook, mug, and blank yellow card. Mira writes “Greet my friend” and places the card in front of the laptop.

**MIRA:** I want one small program. It should say hello to Ada. How complicated can that be?

**INSERT:** A deliberately ambiguous mock interface asks, “Which Ada? What if no name is supplied?” This is a teaching graphic, not a real operating-system message.

**MIRA:** I thought computers were good at following instructions.

**BYTE** unfolds from beside the pencil cup.

**BYTE:** They are. We have spent a very long time learning what an instruction needs to say.

**MIRA:** Who invented the first computer?

**BYTE:** First, we need to decide what we mean by a computer. A calculator? A programmable machine? An electronic one? A machine that stores its own instructions?

**NARRATOR:** The modern computer grew from many inventions and ideas. Our journey follows a few of the connections.

**TRANSITION:** Camera enters the yellow card's paper fibers; they become a sunlit counting table.

**Viewer beat:** Hold on “What must the machine know?” for four seconds.

### Scene 02 — Giving information a shape

**Setting:** An explicitly fictional trading scene, then an abstract counting table.  
**Approximate allocation:** 1½ minutes.  
**Idea:** Representation separates information from the objects represented.

**ACTION:** A trader places one pebble beside each of five baskets. Mira moves the baskets away; the pebbles remain.

**MIRA:** The baskets are gone. We still know how many there were.

**BYTE:** We kept a representation of the quantity.

**GRAPHIC:** Five pebbles → five tally marks → decimal `5`. A second row shows binary `101`. Label both as different notations for the same quantity; do not imply that binary notation appeared in this trading scene.

**MIRA:** Different marks, same number?

**BYTE:** If we agree on how to interpret the marks. A symbol needs rules before it carries a useful meaning.

**DEMONSTRATION:** Mira arranges cards labeled “A”, a musical note, and a colored square. Each becomes a placeholder pattern of bits; only the number example receives a precise numeric encoding here.

**NARRATOR:** Written numerals, counting tools, and calculation practices developed across many societies. This invented scene illustrates an idea; it does not reconstruct their first invention.

**MIRA:** So a computer doesn't contain tiny photographs of everything it knows.

**BYTE:** It stores representations. The interpretation matters.

**Viewer beat:** “How many ways could you represent five?” Hold five seconds.

**TRANSITION:** The tally marks line up into numbered steps.

### Scene 03 — A method someone else can follow

**Setting:** A table shared by Mira and two fictional human calculators.  
**Approximate allocation:** 1½ minutes.  
**Idea:** Algorithms specify procedures; people can execute them.

**ACTION:** Three people add 27 and 15 using the same written procedure. Show units, carrying, and tens. Keep every intermediate value visible.

**MIRA:** We all got forty-two.

**BYTE:** You followed the same procedure with the same inputs.

**MIRA:** Is that already an algorithm?

**BYTE:** Yes. An algorithm is a precise method. It doesn't need a laptop to exist.

**NARRATOR:** For centuries, people developed systematic methods for arithmetic and other problems. “Computer” also became a job title for people who performed calculations.

**ACTION:** Byte replaces 27 and 15 with 18 and 24. The same addition steps still work.

**BYTE:** Notice the difference between the method and the particular numbers.

**MIRA:** The instructions stay. The inputs change.

**INSERT:** `input → procedure → output`.

**COMIC BEAT:** Mira hands Byte a card saying “Do the usual thing.” Byte opens a drawer containing dozens of different “usual things.”

**BYTE:** We may need a more precise procedure.

**TRANSITION:** A drawn carry arrow curves into a gear tooth.

### Scene 04 — Arithmetic becomes machinery

**Setting:** Mechanical workshop; cutaway model, then labeled historical vignette.  
**Approximate allocation:** 2 minutes.  
**Idea:** Physical mechanisms can implement arithmetic; generality is a separate design step.

**CLOSE:** A decimal wheel moves from 9 to 0 and advances its neighbor. Mira turns the handle slowly.

**MIRA:** The carry happened without anyone remembering to do it.

**BYTE:** The mechanism embodies that rule. Mechanical calculators existed before electronic computers.

**NARRATOR:** In the nineteenth century, Charles Babbage designed the Difference Engine to calculate mathematical tables. His later Analytical Engine proposed a more general programmable machine, with a “store” for numbers and a “mill” for operations. The full Analytical Engine was not completed in his lifetime. [S1]

**GRAPHIC:** Label a simplified conceptual model “memory” and “operations.” Clearly identify it as an explanatory model, not a working reconstruction.

**MIRA:** Could we make this same machine do a different job?

**BYTE:** That question changes the design. A special-purpose mechanism and a programmable machine are different ideas.

**ACTION:** A neighboring loom reads punched cards. Separate caption: “Jacquard punched-card control; an influence on Babbage.” [S2]

**MIRA:** The pattern is carried by the cards.

**BYTE:** Change the instructions, change the pattern. The loom is not a general-purpose computer, but this way of controlling a machine helped inspire one.

**NARRATOR:** Ada Lovelace's 1843 notes on the Analytical Engine included a procedure for Bernoulli numbers and explored the machine's potential beyond numerical calculation. [S3]

**ACTION:** Lovelace's historical vignette is accompanied by a narrator-led graphic: numerical patterns become musical notation. No claim that the unbuilt machine actually performed this music.

**MIRA:** A machine could manipulate symbols according to rules—and those symbols could stand for more than quantities.

**TRANSITION:** Holes in the cards become circles in a circuit diagram.

### Scene 05 — Decisions made from switches

**Setting:** Abstract demonstration bench; historically labeled inserts.  
**Approximate allocation:** 1½ minutes.  
**Idea:** Boolean logic can be implemented with switching circuits.

**ACTION:** Byte places two switches in series with a lamp. Mira closes only one. The lamp stays dark. She closes both; it lights.

**BYTE:** This arrangement acts like AND. Both conditions must hold.

**ACTION:** Replace the circuit with two parallel paths. Either switch now completes the circuit. Demonstrate NOT separately with an explanatory logic diagram rather than an unverified physical wiring animation.

**MIRA:** The switches aren't considering the question. Their arrangement determines the result.

**NARRATOR:** George Boole developed an algebra of logic in the nineteenth century. In his 1937 work, Claude Shannon connected Boolean algebra to relay and switching circuits. Logical rules could guide circuit design. [S4]

**OVERLAY:** An AND truth table is constructed one row at a time: `0,0→0`; `0,1→0`; `1,0→0`; `1,1→1`.

**BYTE:** We can combine small operations to build more elaborate ones, including arithmetic.

**Viewer beat:** Freeze before the final row: “Will this lamp light?”

**TRANSITION:** Lit and unlit lamps become a row of bits.

### Scene 06 — A world made from patterns

**Setting:** A quiet field of floating signal cells.  
**Approximate allocation:** 1½ minutes.  
**Idea:** Bits encode choices; meaning depends on interpretation.

**ACTION:** Mira flips one two-state cell. Duplicate it into two, then three cells. Display all patterns in each group.

**BYTE:** One bit distinguishes two possibilities. Two bits distinguish four. Three distinguish eight.

**MIRA:** Eight bits give two hundred and fifty-six patterns.

**BYTE:** Exactly. We usually call eight bits a byte.

**MIRA:** A modest name for your whole personality.

**BYTE:** I contain several teaching metaphors.

**GRAPHIC:** Binary place values `4, 2, 1`; highlight `101` as `4 + 0 + 1 = 5`.

**BYTE:** Binary uses place value, just as decimal does. In hardware, physical signal ranges represent the states. They are not perfect little written zeros and ones.

**ACTION:** A byte pattern `01000001` is shown as decimal 65 when interpreted as an unsigned integer, and as the letter A under ASCII encoding. Label both interpretations explicitly.

**MIRA:** The bits didn't change. The interpretation did.

**TRANSITION:** A pattern enters a memory box; an arrow shows it being read later.

### Scene 07 — The machine that follows other machines

**Setting:** A paper-tape world, labeled “mathematical model.”  
**Approximate allocation:** 1½ minutes.  
**Idea:** Memory, sequence, selection, repetition, and universality.

**ACTION:** Mira moves a marker along a tape, reads a symbol, writes one, and follows a state card. The demonstration is deliberately simple and does not pretend to prove universality.

**BYTE:** A machine can retain information, perform steps in order, choose a next step, and repeat.

**GRAPHIC:** `sequence`, `selection`, `repetition`, `memory` appear beside concrete examples.

**NARRATOR:** In 1936, Alan Turing described a mathematical model of computation and a universal machine able to simulate other machines in that model. This helped make the idea of a general computing machine precise. Other researchers, including Alonzo Church, developed foundational accounts of computation as well. [S5]

**MIRA:** So “general-purpose” means it can follow descriptions of many procedures?

**BYTE:** Yes—with enough time and memory. It doesn't mean every question can be solved by an algorithm. Real computers also have finite resources.

**ACTION:** The tape stretches beyond the room and stops at a labeled resource boundary. Avoid depicting an infinite real machine.

**TRANSITION:** Paper squares become illuminated memory cells.

### Scene 08 — Instructions enter memory

**Setting:** Montage of early computer teams, then an abstract CPU-and-memory model.  
**Approximate allocation:** 2 minutes.  
**Idea:** Electronic computation and stored programs are separate achievements.

**NARRATOR:** Early computing took several paths. Zuse's Z3 used electromechanical relays. Colossus used electronics for specialized wartime codebreaking. ENIAC was a general-purpose electronic machine, initially configured through wiring and switches. Their achievements differ; calling one simply “the first computer” hides those differences. [S6]

**ACTION:** Credit engineering and programming teams. No single figure pulls a lever and invents everything.

**MIRA:** Electronics make switching fast. But how does the machine know which operation comes next?

**BYTE:** We can encode instructions and store them in memory too.

**NARRATOR:** The stored-program idea emerged through multiple contributions. In June 1948, the Manchester Baby successfully ran a program held in electronic memory. [S7]

**GRAPHIC:** A simplified machine fetches an instruction, decodes it, and executes it. Advance a program counter; demonstrate one branch. Label this a teaching model, not an exact depiction of every CPU.

**MIRA:** A program can be loaded like other information.

**BYTE:** And another program can inspect or transform its representation. That becomes very useful when we build programming tools.

**Viewer beat:** “What changes when you load a new program: the instructions, the hardware, or both?” Hold before answering “The instructions can change while the hardware stays.”

**TRANSITION:** Camera pulls out from a glowing switching device.

### Scene 09 — Making computation small

**Setting:** Room-sized electronics → circuit board → chip → desk.  
**Approximate allocation:** 1 minute.  
**Idea:** Manufacturing advances change access to computation.

**NARRATOR:** The transistor was demonstrated at Bell Labs in 1947. Integrated-circuit developments in the late 1950s brought components together on chips. By the early 1970s, microprocessors integrated CPU functions onto single chips. These were collective engineering and manufacturing achievements. [S8]

**ACTION:** Animate a conceptual scale comparison, not a false literal transformation between historically incompatible devices.

**MIRA:** If the CPU fits here, is that the whole computer?

**BYTE:** It still needs memory, input and output, and other supporting parts. Different systems combine those in different ways.

**ACTION:** Components assemble into a small computer. A desk becomes a classroom, then several homes.

**NARRATOR:** Falling size and cost helped computing reach many more people, though access remained uneven.

**TRANSITION:** The yellow card lands beside a keyboard.

### Scene 10 — Teaching tools to translate

**Setting:** Programming workbench with transparent layers.  
**Approximate allocation:** 2 minutes.  
**Idea:** Languages and software layers manage complexity.

**ACTION:** Mira faces a page of machine instructions, then assembly mnemonics, then a higher-level mathematical expression. Mark these as explanatory examples, not exact equivalent listings unless separately verified.

**MIRA:** Can I describe the operation without writing every machine instruction?

**BYTE:** An assembler translates symbolic instruction names. A compiler translates a program into another form. An interpreter executes a program through another program. Real systems can combine these approaches.

**NARRATOR:** Compiler pioneers included Grace Hopper and many others. In 1957, John Backus's IBM team released Fortran, an influential high-level language and compiler for scientific programming. [S9]

**GRAPHIC:** Application → libraries and language tools → operating-system services → machine instructions → hardware. Caption: “A simplified view; real execution paths vary.”

**BYTE:** Libraries let us reuse behavior. Operating systems manage resources and provide services. We don't rebuild every layer for each program.

**ACTION:** Mira connects existing blocks to make a small application, then checks the interface labels before connecting them.

**MIRA:** Each layer hides details, but it still needs rules about how to use it.

**BYTE:** An abstraction helps when its promises are clear.

**TRANSITION:** Two desks appear, separated by a landscape.

### Scene 11 — Machines learn to cooperate

**Setting:** Network landscape; abstract packets; a web of documents.  
**Approximate allocation:** 1½ minutes.  
**Idea:** Protocols and the distinction between Internet and Web.

**ACTION:** A message is split into labeled packets. Paths diverge. A destination reassembles the message in a simplified transport illustration; do not imply every network service guarantees delivery or ordering.

**NARRATOR:** Packet-network research and projects such as ARPANET contributed to the Internet. TCP/IP helped different networks communicate. The history involved many organizations and researchers. [S10]

**MIRA:** They need a shared agreement about the messages.

**BYTE:** A protocol. Independent systems can cooperate when they follow compatible rules.

**ACTION:** Add documents with clickable links above the network infrastructure.

**NARRATOR:** Tim Berners-Lee proposed the World Wide Web at CERN in 1989. The Web is one system using the Internet; they are not the same thing. [S11]

**MIRA:** We've gone from following steps to sharing information around the world.

**BYTE:** And the larger the system, the more places there are for misunderstandings and failures.

**TRANSITION:** A packet turns into the yellow card, back on Mira's original desk.

### Scene 12 — Working is not the same as correct

**Setting:** Present-day desk; AI chat shown as a neutral text interface.  
**Approximate allocation:** 2 minutes.  
**Idea:** Intent, implementation, verification, and language guarantees differ.

**MIRA:** Now I can ask an AI to write the greeting program.

**ACTION:** A fictional AI draft appears, labeled “candidate implementation.” This is not an endorsement of its correctness or a claim about a specific model.

**MIRA:** It compiles. Are we done?

**BYTE:** What should it do without a name? What about an empty argument? Two names?

**ACTION:** Three test cards slide in. Mira sees that the original request never answered those questions.

**MIRA:** I need to decide the behavior before I can judge the code.

**OVERLAY:** Mira writes the actual lesson contract:

| Input | stdout | stderr | Status |
| --- | --- | --- | --- |
| No arguments | `Hello, world!` + newline | Empty | 0 |
| `Ada` | `Hello, Ada!` + newline | Empty | 0 |
| Empty argument | Empty | `error: name must not be empty` + newline | 2 |
| Two arguments | Empty | `error: expected at most one name` + newline | 2 |

**MIRA:** Names get surrounding whitespace trimmed. Internal characters stay. Argument count is checked first.

**BYTE:** Now we have expectations we can test.

**NARRATOR:** Requirements and specifications long predate modern AI. In this repository, Spec Kit helps organize a specification, implementation plan, and work tasks. It does not guarantee the requirements are complete or the implementation correct. [S12]

**ACTION:** Display `spec.md → plan.md → tasks.md → code + verification`. A loop arrow permits revision.

**MIRA:** And why Rust?

**BYTE:** Rust lets us practice explicit types, ownership, borrowing, and error handling. Its ownership rules help govern memory management, with many checks made by the compiler. That doesn't tell us whether a greeting is the one the user wanted. [S13]

**GRAPHIC:** Separate labeled panels: “Compiler: language rules,” “Tests: selected examples,” “Specification: intended behavior.” Never merge them into a “proved correct” badge.

### Scene 13 — Your first instruction

**Setting:** Same composition as Scene 01; warmer dawn light.  
**Approximate allocation:** 1 minute.  
**Idea:** Invite the learner to do the work.

**ACTION:** Mira places the revised yellow card beside three unopened folders: specification, plan, and tasks. A preview terminal shows the target `Hello, Ada!` with the caption “Behavior to build.” Do not portray the repo's unimplemented lesson as already complete.

**MIRA:** I wanted the machine to understand one sentence. Now I can see the representations, rules, programs, and agreements underneath it.

**BYTE:** You don't have to master all of computer science before starting. You can make one small behavior clear, build it, and investigate what happens.

**MIRA, TO VIEWER:** What should our program do when no name is supplied? Make your prediction. Then open the first specification and compare.

**ACTION:** The card becomes a clean title panel. Paper texture fades behind sharp text.

**END CARD:**

```text
Lesson 001 — Greeting CLI
Read the spec. Predict the result. Write a test. Build the behavior.
spec-driven-rust-learning
```

**NARRATOR:** Our first program is small. The ideas behind it have a long history.

**SOUND:** Pencil stroke, quiet keyboard tap, then silence for the learner to continue.

## Editorial and historical guardrails

- Historical cameo dialogue is not used. Mira and Byte are fictional; their conversations and transitions are dramatization.
- Never describe history as one person's invention or a straight line of inevitable progress. Include teams, overlapping work, human calculators, and alternative approaches.
- Do not call the Jacquard loom a general-purpose computer, suggest the Analytical Engine was completed, or equate Turing's abstract model with a built electronic computer.
- Avoid unqualified “first computer” and “first programmer” claims. Explain the relevant achievement instead.
- This is a selected introduction centered on digital programmable computation, not an exhaustive global history. Analog computing, information theory, databases, graphics, distributed systems, and AI history can receive follow-up lessons.
- Source records sometimes distinguish conception, demonstration, publication, and commercial release. Use precise labels for dates and recheck final narration before production.
- No programming language, test suite, AI tool, or specification eliminates all errors. Safe Rust's guarantees have a defined scope; do not apply them indiscriminately to unsafe code or external interfaces.
- No actual Rust lesson implementation is delivered by this screenplay. Follow the repository tasks to build it.

## Sources and fact-check anchors

These sources support historical and technical claims, not the fictional plot or dialogue. Recheck credits, reference-image rights, pronunciation, and any added historical claims before production.

- **S1:** [Computer History Museum — Babbage's engines](https://www.computerhistory.org/babbage/engines/).
- **S2:** [National Museums Scotland — Jacquard loom and computing](https://www.nms.ac.uk/discover-catalogue/the-jacquard-loom-innovation-in-textiles-and-computing).
- **S3:** [Oxford History of Science Museum — Babbage and Lovelace](https://hsm.ox.ac.uk/imagining-ai).
- **S4:** [MIT CSAIL — computing milestones, including Shannon's 1937 work](https://www.csail.mit.edu/news/twenty-five-ways-which-mit-has-transformed-computing).
- **S5:** [Turing's original paper, hosted by Carnegie Mellon](https://www.cs.cmu.edu/~15455/resources/Turing1936.pdf). The mathematical model is not a hardware blueprint.
- **S6:** [Computer History Museum — computer timeline](https://www.computerhistory.org/timeline/computers/). Consult individual machine entries for their distinct capabilities.
- **S7:** [Computer History Museum — stored programs](https://www.computerhistory.org/revolution/story/87).
- **S8:** [Computer History Museum — semiconductor timeline](https://www.computerhistory.org/siliconengine/timeline/).
- **S9:** [IBM — Fortran](https://www.ibm.com/history/fortran). For an expanded Hopper segment, add a dedicated verified source before adding detailed dates or priority claims.
- **S10:** [Internet Society — history of the Internet](https://www.internetsociety.org/internet/history-internet/brief-history-internet/).
- **S11:** [CERN — birth of the Web](https://home.cern/science/computing/the-birth-of-the-web).
- **S12:** [GitHub Spec Kit](https://github.com/github/spec-kit). Local configuration records the installed 1.2.5 version; do not replace local behavior with assumptions from a newer release.
- **S13:** [The Rust Book — ownership](https://doc.rust-lang.org/book/ch04-01-what-is-ownership.html).

## Production review checklist

- [ ] Table-read dialogue and establish actual timing; add purposeful demonstration holds rather than padding narration.
- [ ] Check every number, circuit demonstration, date label, binary pattern, and terminal result.
- [ ] Confirm historical vignettes against the listed sources; obtain or create cleared reference assets.
- [ ] Confirm all thirteen scenes have a visible learner question or conceptual payoff.
- [ ] Review character consistency and visual transitions in a storyboard before animation.
- [ ] Verify the greeting contract against `specs/001-greeting-cli/spec.md`.
- [ ] Review caption accuracy, contrast, text size, and audio balance.
- [ ] Keep a transcript and source credits with the final film.
