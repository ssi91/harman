# Plan Alignment

While slices are being implemented, the code changes but the Plan does not update itself, so the two
drift apart: a slice gets blocked, the code deviates from a decision, a review shows that a decision
was wrong. Later slices, reviews, and the final audit all rely on the Plan, so an outdated Plan
misleads them. Plan Alignment brings the two back together — it updates the Plan to match the code,
or adds slices that bring the code back to the Plan.

*Writing the artifacts* and *Diagrams* in `SKILL.md` apply to everything you write; *Slice status*,
*Operating principles*, *Editing the live Plan*, and *Alignment log entry* below refer to its
sections too.

1. **Read what is new since your last Alignment log entry** — entries in the slices' Implementation
   logs (with the Independent Programmers' applied and rejected findings), Code Review Reports, and
   any feedback the Human gives you now. If nothing is new, say so and stop: there is nothing to
   align.
2. **Take the status of every slice** (see *Slice status*).
3. **Check the code**, at the Plan's level of detail — line-level correctness is the Reviewer's job.
   Slices built in parallel live in other worktrees: look for each slice's code where its log says
   it is — worktree, branch, and commit. For each slice that became done since your last entry: are
   the files, types, signatures, contracts, module boundaries, and dependency directions its
   instructions, decisions, and diagrams prescribed actually there? Compare what changed since `Base` — in your
   checkout (`git diff --stat <Base>`, plus untracked files, minus `.harman/`) and in each slice's
   worktree or commit — with the files the logs name: a changed file no entry accounts for is
   unlogged work. Then check that the code the remaining slices build on still matches their
   instructions — paths, names, signatures, line references.
4. **Collect what needs your attention**:
   - `BLOCKED` questions, and reports that a Plan instruction is wrong or impossible;
   - deviations from the Plan — the logged ones, and the unlogged ones step 3 turned up;
   - Reviewer findings that name a Plan decision (`D<n>`) as the defect, and findings the
     Independent Programmer rejected as conflicting with one;
   - observations the Independent Programmer logged about problems outside its slice;
   - blind spots the implementation has exposed;
   - remaining slices made stale by what was built.
5. **Resolve each item**, justified by the *Operating principles*:
   - **accept** — the implementation stands; revise the Plan to match it;
   - **remediate** — the implementation must change; amend a not-started slice or add a new one;
   - **decide** — a question gets a new or revised `D<n>`, and the slice instructions it implies;
   - **dismiss** — nothing changes; give the reason (out of scope, already covered by
     `<taskID>-S<n>`, does not reproduce). Out-of-scope problems are still reported to the Human;
   - **NEEDS HUMAN** — product intent or an external constraint; give your recommended default so
     work is not blocked meanwhile.
6. **Align the Plan** — decisions, slices, and every diagram they reach — following *Editing the
   live Plan*.
7. **Append an entry** in the *Alignment log entry* format, even when the Plan did not change: it is the checkpoint your
   next alignment and the audit start from.
8. **Tell the Human**: the slice status, what changed in the Plan, what NEEDS HUMAN, and which slices
   are ready to implement. If every slice is now `done`, say that the Final Architect Audit is next.
