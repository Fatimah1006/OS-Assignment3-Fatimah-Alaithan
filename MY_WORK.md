# 📝 MY_WORK: Student Information, Development Log, Reflection & Answers

> This is the **only file** your instructor reads to grade Parts 3 and 4 (documentation and video). Everything you write here must be **in your own words**.

---

## 🛑 STOP: Read This Before You Do Anything Else

> ### 1️⃣ Read the whole `README.md` first
> The `README.md` in this repository contains the full instructions: how this assignment continues Assignment 1, the Chapter 5 recap, class descriptions, feature specifications, question prompts and the video script. **If you skip it, you will lose marks.**
>
> ### 2️⃣ Understand the full code before answering any question
> Open `SchedulerSimulationSync.java` and read it **from top to bottom**. You must be able to explain what `SharedStats`, `ReadyQueue`, `CpuWorker`, `RaceWindow.pause()`, `ReentrantLock` and `Semaphore` do **before** you write a single answer in Parts B and C. **Run the original starter first** (it is intentionally broken) and **save its output**: you need it for Question 1 of Part C.
>
> ### 3️⃣ Use only the code of this repository
> Work **only** on `SchedulerSimulationSync.java` from this repository. Do **not** copy or paste code from your previous assignments.
>
> ### 4️⃣ Commit many times, not once
> A single commit, or all commits made in the last hour, costs you **-0.5 mark**. See the [Commit Rules](#-commit-rules-mandatory) below.

**How to use this file:**
1. Fill in your **Student Information** (below) right now.
2. Follow the steps in the **Work Roadmap** in order.
3. Update the **Development Log** *every time* you work on the assignment, not at the end.
4. Do not delete any section header. Replace the `[...]` placeholders with your own text.

---

## 👤 Student Information

> ⚠️ **WARNING:** Fill this in first. Your name and ID must match the student ID you set in `SchedulerSimulationSync.java` (line 304) and the one you say in your video.

| Field | Your Answer |
|-------|-------------|
| **Full Name** | [Write your full name here] |
| **Student ID** | [Write your student ID here] |
| **University Email** | [yourid]@std.psau.edu.sa |
| **GitHub Username** | [your-github-username] |
| **Repository Link** | [https://github.com/Fatimah1006/OS-Assignment3-Fatimah-Alaithan] |
 
---

## 🎥 Video Link

**Video Link**: [https://drive.google.com/file/d/1OWwAn7i228tqdHOxIVjIjf_2qBgWQguf/view?usp=drivesdk]

> ⚠️ **WARNING:** The video must be **publicly accessible** ("Anyone with the link can view") on **Google Drive**, **YouTube (Unlisted or Public)** or any other cloud file-sharing system. A private, restricted or broken link counts as a **missing video (-1 mark)**.
>
> 💡 **TIP:** Open the link in a **private/incognito window** before you submit. If it asks you to log in or request access, it is not public.
>
> 📌 **NOTE:** The link goes in **this file only** (`MY_WORK.md`), **not** in `README.md`. Name your video file `StudentID_Assignment3_Demo.mp4`. It must last **2 to 3 minutes**.

---

## 🗺️ Work Roadmap (follow in this order)

| Step | What to do | Where | Marks |
|:----:|------------|-------|:-----:|
| 0 | Read `README.md`, read the full code, **run the original starter and save its output** (it fails on purpose) | Your IDE | – |
| 1 | Fork, rename, keep the repo **PUBLIC**, set your student ID (line 304), **commit** | GitHub + code | Part 1 (1) |
| 2 | Feature 1: Mutex lock on the ready queue, **commit** | Code | Part 2 (0.25) |
| 3 | Feature 2: Mutex lock(s) on the shared statistics, **commit** | Code | Part 2 (0.25) |
| 4 | Feature 3: Counting semaphore instead of busy waiting, **commit** | Code | Part 2 (0.5) |
| 5 | Development Log (5+ entries, different dates) | This file, Part A | Part 3 (0.5) |
| 6 | Reflection (4 questions) | This file, Part B | Part 3 (0.5) |
| 7 | Technical Answers (4 questions) | This file, Part C | Part 3 (0.5) |
| 8 | Record the video, upload it, paste the link above | Video + this file | Part 4 (1.5) |
| 9 | Final check, then submit the repo link on Blackboard | Blackboard | – |

> 💡 **TIP:** Tick each step off as you go. Do not leave the log, the reflection or the video for the last day.

---

## 🔁 Commit Rules (MANDATORY)

> ### ⚠️ MANY COMMITS ARE REQUIRED. A single bulk commit is penalized (-0.5 mark).

**Minimum: 4 meaningful commits. Aim for 7 or more.**

| # | Commit | Example message |
|:-:|--------|-----------------|
| 1 | Student ID set | `Set my student ID: 441234567` |
| 2 | Feature 1: Ready queue lock | `Feature 1: Protected the ready queue with a ReentrantLock` |
| 3 | Feature 2: Statistics locks | `Feature 2: Added locks to the shared statistics counters` |
| 4 | Feature 3: Semaphore | `Feature 3: Replaced busy waiting with a counting semaphore` |
| 5 | Development log entries | `Docs: Added development log entries 1-3` |
| 6 | Reflection and answers | `Docs: Completed reflection and technical answers` |
| 7 | Video link | `Docs: Added demo video link` |

**Rules:**
- ✅ **One commit per feature.** Do not put all three features in one commit.
- ✅ **Commit after each work session**, and after each part of this file.
- ✅ **Spread your commits over different dates.** Not all in one day.
- ❌ **Do not make all commits in the last hour** before the deadline (November 14, 2026).
- ❌ **No vague messages** like `done`, `update` or `final version`.

> 💡 **TIP:** Your commit history is checked and you **show it in your video** (at least 4 commits visible). Your development log dates should match your commit dates.
>
> 💡 **TIP:** **Use VS Code** (see *Recommended Development Environment* in `README.md` for the full setup). Sign in to GitHub in VS Code, then commit from the Source Control panel (Ctrl+Shift+G) → stage → write a message → Commit → Sync/Push. You can edit and commit this file the same way. **Pushing** matters: commits that are not pushed to GitHub are invisible to the instructor.

---

# Part A: Development Log (0.5 mark)

> ⚠️ **WARNING:** Minimum **5 entries**, spread over **different dates**. Five entries written on the same day, or written all at once at the end, will lose marks and look like a copy. Entry dates should be **between the start of the assignment and the deadline (November 14, 2026)**.
>
> 💡 **TIP:** Write an entry at the **end of each work session**, while you still remember what happened. It takes 5 minutes.
>
> 💡 **TIP:** Be specific. "Worked on the code" is a weak entry. "Added a `ReentrantLock queueLock` to `ReadyQueue` and wrapped the body of `poll()` in `lock()` / `try` / `finally { unlock() }`" is a strong one.
>
> 📌 **NOTE:** Each entry needs: date and time, what you did, details, challenges, solution, and time spent. Real challenges are fine (and expected). Do not invent fake ones.

## Example Entry (do not copy it, write your own)

### Entry 1 - [November 12, 2026, 4:30 PM]
**What I did**: Forked the repository, set my student ID, and ran the original starter

**Details**:
- Forked the starter repository and renamed it
- Changed student ID on line 304 to my actual ID (441234567)
- Ran the original program: 4 CPUs started, three of them picked `P1`, then `IllegalThreadStateException` and the watchdog stopped the program
- Saved the output in a text file for Question 1
- Committed and pushed: `Set my student ID: 441234567`

**Challenges**: I did not understand why the same process was picked by three CPUs

**Solution**: Read `ReadyQueue.poll()` again and found the `RaceWindow.pause()` between reading the head and removing it

**Time spent**: 45 minutes

---

## Your Development Log

### Entry 1 - [13 November ,2026 , 4:00 AM]
**What I did**:
 Set up the project and updated my student information.

**Details**:

*Forked the starter repository on GitHub.
* Opened the project in VS Code.
* Changed the student ID to 446051500.
* Reviewed the Java code to understand the project structure.

**Challenges**:

Understanding the project structure and GitHub setup.

**Solution**:
Reviewed the starter code and configured the repository in VS Code.
**Time spent**:
20 minutes.
---

### Entry 2 - [17 November , 2026, 4:30 AM]
**What I did**:
 Implemented Feature 1 to protect the shared ready queue.
**Details**:
* Added a ReentrantLock called queueLock to the ReadyQueue class.
* Protected the add(), poll(), processOf(), and snapshot() methods.
* Used lock() and try/finally to ensure the lock is always released.
**Challenges**:
Multiple CPU threads could access the shared queue at the same time, causing race conditions.
**Solution**:
Used ReentrantLock to synchronize queue operations and prevent concurrent access issues.
**Time spent**:
30 minutes
---

### Entry 3 - [17 November , 2026 , 5:00 AM]
**What I did**:
Implemented Feature 2 to protect shared statistics.
**Details**:
* Added a ReentrantLock called statsLock to the SharedStats class.
* Protected the shared counters and their getter methods.
* Used lock() and try/finally to safely update and read statistics.
**Challenges**:
Multiple CPU threads could update shared counters simultaneously, causing incorrect values.
**Solution**:
Used statsLock to synchronize access to the shared statistics and prevent race conditions.
**Time spent**:
20 minutes.
---

### Entry 4 - [17 November , 2026 , 6:00 AM]
**What I did**:
Implemented Feature 3 using a counting semaphore.
**Details**:
* Added a Semaphore initialized to zero in the ReadyQueue class.
* Used release() to signal when a process was added.
* Used acquire() to make CPU threads wait until a process became available.
**Challenges**:
CPU threads could repeatedly check an empty queue, wasting CPU resources.
**Solution**:
Used a semaphore to block CPU threads when the queue was empty instead of using busy waiting.
**Time spent**:
20 minutes
---

### Entry 5 - [17 November , 2026 , 7:00 AM]
**What I did**:
Reviewed the synchronization features and organized the Git commits.
**Details**:
* Reviewed the implementation of Features 1, 2, and 3.
* Checked the use of ReentrantLock and Semaphore.
* Worked on separating the Git commits for each feature.
* Updated the MY_WORK.md documentation.
**Challenges**:
The three features were initially combined into one commit, making the commit history difficult to organize.
**Solution**:
Reviewed the Git history and worked on separating the changes into individual feature commits.
**Time spent**:
25 minutes
---

### Entry 6 - [Optional - Date and Time]
**What I did**:

**Details**:

**Challenges**:

**Solution**:

**Time spent**:

---

## Development Log Summary

> 💡 **TIP:** Fill this in **last**, after all entries are written.

**Total time spent on assignment**: [4 hours]

**Most challenging part**:
Separating the Git commits for each feature and managing the repository.
**Most interesting learning**:
Learning how ReentrantLock and Semaphore help prevent race conditions and coordinate CPU threads.
**What I would do differently next time**:
I would create a separate commit immediately after completing each feature to keep the Git history organized.
---

# Part B: Reflection (0.5 mark)

> 🛑 **STOP:** Do **not** start this part until you have read the `README.md`, read the **entire** `SchedulerSimulationSync.java`, run it, and finished the three features.
>
> ⚠️ **WARNING:** Each answer must be **5 to 7 sentences**, in **your own words**. Copied or AI-generated answers without understanding get **0 marks for the whole assignment**. You may be asked to explain them in person.
>
> 💡 **TIP:** Mention concrete things you actually did: a method you wrote, an error you hit, a line of output you saw. Generic answers score low.
>
> 💡 **TIP:** Draft your answer in a few bullet points first, then turn them into sentences.

## Question 1: What did you learn about synchronization?

> 💡 **TIP:** Talk about race conditions (read-modify-write), critical sections, mutual exclusion with `ReentrantLock` and `try/finally`, the role of a counting semaphore, and what surprised you when the starter failed.

**Your Answer:** *(5-7 sentences)*

[I learned that synchronization is important when multiple CPU threads access shared data. Without synchronization, race conditions can happen and cause incorrect results. In Feature 1, I used ReentrantLock to protect the shared ready queue. I learned that try/finally helps make sure the lock is released even if an error occurs. In Feature 2, I protected shared statistics using another lock. In Feature 3, I used a counting semaphore to make CPU threads wait when the queue was empty instead of continuously checking it.]

## Question 2: What was the most challenging part of this assignment?

> 💡 **TIP:** Pick **one** specific challenge (understanding why the starter failed, choosing the lock granularity, the initial value of the semaphore, the shutdown of the CPUs, Git, the video) and say *why* it was hard.

**Your Answer:** *(5-7 sentences)*

[The most challenging part of this assignment was understanding how the counting semaphore works. At first, I was confused about how CPU threads should wait when the ready queue is empty. I had to understand why the semaphore starts with zero permits. I also found it difficult to organize the Git commits because I initially combined the three features into one commit. I reviewed the code and Git history to understand how to fix these issues. This helped me understand synchronization better and the importance of making separate commits for each feature.]

## Question 3: How did you overcome the challenges you faced?

> 💡 **TIP:** Describe your method: reading the slides and the documentation, adding `System.out.println` to debug, running the program many times, re-reading the README, testing after each small change, asking for help.

**Your Answer:** *(5-7 sentences)*

[I overcame the challenges by reviewing the project instructions and reading the Java code carefully. I used System.out.println() to understand how the CPU threads were working. I reviewed the ReentrantLock and Semaphore implementations to understand synchronization better. When I faced problems with Git commits, I checked the Git history in VS Code. I tried different solutions to organize the commits correctly. This helped me understand the code better and improve my problem-solving skills.]

## Question 4: Where can synchronization concepts be applied in real-world applications?

> 💡 **TIP:** Use real applications you know (banking and money transfers, ticket or seat booking, a shared counter on a website, a print queue, a database) and connect each one to what you built here (shared data, critical section, lock or semaphore).

**Your Answer:** *(5-7 sentences)*

[Synchronization is important in many real-world applications. For example, banking systems use synchronization when multiple users access the same account to prevent incorrect balance updates. Ticket booking systems also need synchronization to prevent two people from booking the same seat. In operating systems, synchronization helps multiple CPU threads access shared resources safely. Locks can protect critical sections so only one thread modifies shared data at a time. Semaphores can control when threads are allowed to continue working.]

### Optional: What would you like to learn more about?

[Any topics related to synchronization or operating systems that you're curious about?]

### Optional: How confident do you feel about synchronization concepts now?

[Beginner / Intermediate / Confident. What do you understand well? What needs more practice?]

### Optional: Feedback on the assignment

[Any comments? Was it helpful? Too easy or hard? Suggestions?]

---

# Part C: Technical Answers (0.5 mark)

> 🛑 **STOP:** You cannot answer these questions without understanding the code. Re-read `SchedulerSimulationSync.java` and **run it** first. Your answers must reference **your own code and your own output** (your student ID makes your output and your expected values unique).
>
> ⚠️ **WARNING:** Each answer must be **3 to 5 sentences**, with specific examples from your code or output. Use correct terms: race condition, critical section, mutual exclusion, mutex lock, semaphore, busy waiting, deadlock, producer, consumer.
>
> 💡 **TIP:** Keep the output of the **original starter** and the output of your **final version** in text files or screenshots, so you can copy real snippets for Question 1.

## Question 1: Race Condition in Your Own Output

**Question**: Run the **original starter** (before any fix) and paste the **verification block** of that run. Which value was wrong (expected vs observed)? Explain **step by step**, with two named threads/CPUs, how **one lost update** happens on one of the shared variables (read, `RaceWindow.pause()`, write). Why can the same bug happen on a real machine even without `RaceWindow`, and why is it hard to detect?

> ⚠️ **WARNING:** The snippet must come from **your own run** (with your student ID), not from a classmate or from this README.
>
> 💡 **TIP:** Use a small timeline: *CPU-1 reads `contextSwitchCount` = 12 → CPU-2 reads 12 → CPU-1 writes 13 → CPU-2 writes 13 → one increment is lost.* If your starter run crashed before printing numbers, run it several times (or paste the exception and the watchdog message and explain it).

**Your Answer:** *(3-5 sentences)*

[In my original output, the expected context switches were 32, but the observed value was 0 because the CPU threads crashed before completing their work. For example, CPU-1 and CPU-2 could both read contextSwitchCount as 12, then both write 13 instead of 14, causing one lost update. The original program also showed NullPointerException in ReadyQueue.snapshot() and NoSuchElementException in ReadyQueue.poll() because multiple threads accessed the shared LinkedList without synchronization. RaceWindow.pause() makes race conditions easier to reproduce by creating a delay between reading and writing. Even without this delay, the operating system can interrupt threads at unpredictable times, making race conditions difficult to detect.]

Verification block of the **original starter**:
```
[Context switches: expected 32, observed 0 — MISMATCH
Completed processes: expected 17, observed 0 — MISMATCH
Total service time: expected 129302, observed 0 — MISMATCH
Busy-waiting polls: expected 0, observed 0]
```

Verification block of **my final version**:
```
[Context switches: expected 32, observed 32
Completed processes: expected 17, observed 17
Total service time: expected 129302, observed 129302
Busy-waiting polls: expected 0, observed 0
All shared values are consistent.]
```

**Explanation of the timeline:**
[CPU-1 reads contextSwitchCount = 12. Before CPU-1 updates it, CPU-2 also reads 12. CPU-1 increases the value and writes 13. CPU-2 also writes 13 using its old value. The correct result should be 14, but one update is lost because both threads accessed the shared variable without synchronization.]

## Question 2: Critical Sections and Lock Granularity

**Question**: List the **critical sections** you protected (variables and methods) and the lock(s) you used. **Lock granularity:** did you use **one lock** for the three statistics or **one lock per variable**? Why, and what is the trade-off? Why is the **ready queue** protected by a **different** lock than the statistics? Explain how your solution provides **mutual exclusion**, and discuss **progress** and **bounded waiting** (a default `ReentrantLock` is not fair: what does that imply?).

> 💡 **TIP:** The three counters are independent: does updating `contextSwitchCount` need to block an update of `totalServiceTime`? Also think about what could go wrong (deadlock, or long waiting) if the queue lock and the statistics lock were the **same** lock and a thread held it while doing something slow.

**Your Answer:** *(3-5 sentences)*

I used ReentrantLock to protect the shared data in my program. In ReadyQueue, I used queueLock to protect the add(), poll(), processOf(), and snapshot() methods. In SharedStats, I used statsLock to protect the shared counters, such as contextSwitchCount, completedProcesses, and totalServiceTime. I used separate locks because the ready queue and statistics are independent, allowing different CPU threads to work on them at the same time. Using one lock for everything would reduce concurrency, while holding both locks could cause deadlock or unnecessary waiting.

| Critical section (variable / method) | Lock used | Why it needs protection |

| ReadyQueue.add() | queueLock | Prevents concurrent queue modifications |
| ReadyQueue.poll() | queueLock | Prevents race conditions when removing processes |
| ReadyQueue.processOf() | queueLock | Protects access to queued processes |
| ReadyQueue.snapshot() | queueLock | Prevents errors during queue iteration |
| SharedStats counters | statsLock | Prevents lost updates in shared statistics |
| SharedStats getters | statsLock | Ensures consistent reads of shared values |

## Question 3: Busy Waiting vs Semaphore

**Question**: Describe the **busy waiting** of the starter and its cost (give the `Busy-waiting polls` number from your **starter** run). What does the **value of your semaphore** represent? What is its **initial value** and why? What is its value right after the `numProcesses` initial `add()` calls? Why does the last CPU call `release(totalCPUs)` at the end, and what would happen if it did not?

> 💡 **TIP:** Think about what a CPU does when the queue is empty in the starter, and what a CPU does in your final version (is it running, ready or blocked?). Also check what happens to a CPU blocked in `acquire()` when no process will ever be added again.

**Your Answer:** *(3-5 sentences)*

[In the original starter, CPU threads repeatedly checked the empty ready queue, which could waste CPU time, but my starter output showed 0 busy-waiting polls because all CPU threads crashed early. My counting semaphore starts at 0 because no processes have been added yet, and its permits represent available work. After the 17 initial add() calls, it would have 17 permits if no CPU had acquired any. Using acquire() blocks a CPU thread when no work is available instead of continuously polling the queue. Finally, the last CPU calls release(totalCPUs) to wake blocked threads during shutdown; without it, they could wait forever.]

## Question 4: Classical Problems and Deadlock

**Question**: The CPUs and the ready queue look like a classical synchronization problem of Chapter 5. **Name it**, and say who plays the **producer** and the **consumer** roles (careful: here the CPUs also re-enqueue processes). If the ready queue were **bounded** (capacity `K`), name the **three semaphores** you would need and their **initial values**. Describe a **deadlock scenario** that appears if a thread acquired the **mutex before** waiting on the semaphore (or if two locks were acquired in different orders), and say **which of the four necessary conditions** you would break to prevent it.

> 💡 **TIP:** Recall the bounded-buffer solution of the slides (`empty`, `full`, `mutex`) and the order of `wait()` calls in the producer and the consumer. For the deadlock, think about a producer that holds the mutex while waiting for a free slot that only a consumer (who needs the mutex) can create.

**Your Answer:** *(3-5 sentences)*
The classical synchronization problem in my project is the Producer-Consumer problem. The main thread acts as the producer by adding processes to the ready queue, while CPU threads act as consumers by removing processes for execution. CPU threads can also act as producers when they return unfinished processes to the queue. Synchronization is necessary to prevent race conditions and ensure that multiple CPU threads access the shared ready queue safely.
**Classical problem and roles**:
[The classical problem is the Producer-Consumer problem. The main thread acts as a producer by adding processes to the ready queue. The CPU threads act as consumers by removing processes for execution, but they can also act as producers when they re-enqueue unfinished processes.]

**Semaphores for a bounded queue (name and initial value)**:
[For a bounded queue with capacity K, three semaphores are needed:

* empty = K, representing the available empty slots.
* full = 0, representing the available processes.
* mutex = 1, ensuring mutual exclusion when accessing the queue.]

**Deadlock scenario and prevention**:
A deadlock can occur if a producer acquires the mutex lock before waiting on the empty semaphore when the queue is full. The producer holds the mutex while waiting for an empty slot, but the consumer cannot remove a process because it also needs the mutex. This creates circular wait. To prevent deadlock, the producer should wait on empty before acquiring mutex, breaking the hold-and-wait condition.

## Summary

**Key concepts I understood through these questions:**
1. How ReentrantLock prevents race conditions and protects shared data.
2. How semaphores prevent busy waiting and coordinate CPU threads.
3. How deadlocks happen and why lock ordering is important.

**Concepts I need to study more:**
1. Advanced deadlock prevention techniques.
2. Semaphore synchronization in more complex multithreaded programs.

---

# ✅ Final Checklist (complete before submitting)

> ⚠️ **WARNING:** Go through every line. Blackboard does not accept submissions after the deadline, which is **November 14, 2026**.

**Repository**
- [ ] Repository is **PUBLIC** (Settings → Danger Zone → Visibility)
- [ ] Repository is renamed to `OS-Assignment3-YourFirstName-YourLastName`
- [ ] GitHub account uses the university email (`@std.psau.edu.sa`)

**Code**
- [ ] Student ID is set in `SchedulerSimulationSync.java` (line 304)
- [ ] My code is based **only** on the starter of this repository (nothing copied from previous assignments)
- [ ] Code compiles and runs with no errors, and terminates by itself (no `⛔ WATCHDOG`)
- [ ] Feature 1 (ready queue lock), Feature 2 (statistics locks) and Feature 3 (semaphore, no busy waiting) all work
- [ ] **The four verification lines are ✔ in 5 consecutive runs**
- [ ] Every lock is released in a `finally` block
- [ ] `RaceWindow`, `Config`, the verification block and the watchdog are **unchanged**
- [ ] Each feature has clear comments

**Commits**
- [ ] **At least 4 meaningful commits, ideally 7 or more**
- [ ] **One commit per feature**
- [ ] Commits are spread over **different dates** (not all in the last hour)
- [ ] Everything is **pushed** to GitHub

**This file (`MY_WORK.md`)**
- [ ] Full name and student ID filled in at the top
- [ ] Development log has **5+ entries** on different dates
- [ ] Reflection: 4 questions, 5-7 sentences each
- [ ] Technical answers: 4 questions, 3-5 sentences each, with examples from **your** output (starter output **and** final output pasted in Question 1)
- [ ] No `[...]` placeholders left
- [ ] No section headers deleted

**Video**
- [ ] 2-3 minutes long, named `StudentID_Assignment3_Demo.mp4`
- [ ] Shows your name, ID, repository, 3 features (and your lock granularity choice), IDE execution with the verification block, one synchronization concept, and commit history
- [ ] Link is **public** (tested in an incognito window) and pasted in the **Video Link** section above

**Blackboard**
- [ ] Submit **only** the link to your public GitHub repository

> 🎯 **Good luck!** Start early, commit regularly, and make sure you can explain every line you submit.
