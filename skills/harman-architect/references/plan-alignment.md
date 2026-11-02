# Plan Alignment

While slices are being implemented, the code changes but the Plan does not update itself, so the two drift apart: a slice gets blocked, the code deviates from a Decision, a review shows that a Decision was wrong. Later slices, reviews, and the final audit all rely on the Plan, so an outdated Plan misleads them. Plan Alignment brings the two back together — it updates the Plan to match the code, or adds slices that bring the code back to the Plan.

The shared sections of `SKILL.md` apply throughout; write any new Plan file from its template in [plan-templates.md](plan-templates.md).

1. **Read what is new** since your last Alignment log entry — if nothing is new, say so and stop: there is nothing to align:
   - entries in the slices' Implementation logs, with the Independent Programmers' applied and rejected findings;
   - Code Review Reports;
   - any feedback the Human gives you now.
2. **Take the status of every slice** (see *Slice status*).
3. **Check the code**, at the Plan's level of detail — line-level correctness is the Reviewer's job:
   - slices built in parallel live in other worktrees: look for each slice's code where its log says it is:
     - worktree;
     - branch;
     - commit;
   - for each slice that became done since your last entry, check that what its instructions, Decisions, and diagrams prescribed is there:
     - files;
     - types;
     - signatures;
     - contracts;
     - module boundaries;
     - dependency directions;
   - compare what changed since `Base` — in your checkout (`git diff --stat <Base>`, plus untracked files, minus `.harman/`) and in each slice's worktree or commit — with the files the logs name: a changed file no entry accounts for is unlogged work;
   - check that the code the remaining slices build on still matches their instructions:
     - paths;
     - names;
     - signatures;
     - line references.
4. **Collect what needs your attention**:
   - `BLOCKED` questions, and reports that a Plan instruction is wrong or impossible;
   - Deviations from the Plan — the logged ones, and the unlogged ones step 3 turned up;
   - Reviewer findings that name a Decision (`D<n>`) as the defect, and findings the Independent Programmer rejected as conflicting with one;
   - observations the Independent Programmer logged about problems outside its slice;
   - Blind spots the implementation has exposed;
   - remaining slices made stale by what was built.
5. **Resolve each item**, justified by the *Operating principles*:

   | Resolution | What happens |
   | --- | --- |
   | **accept** | The implementation stands; revise the Plan to match it. |
   | **remediate** | The implementation must change; amend a not-started slice or add a new one. |
   | **decide** | A question gets a new or revised Decision, made as *Decision making* says, and the slice instructions it implies. |
   | **dismiss** | Nothing changes, for a stated reason:<br>• out of scope<br>• already covered by `<taskID>-S<n>`<br>• does not reproduce<br>Out-of-scope problems are still reported to the Human. |
   | **NEEDS HUMAN** | Product intent or an external constraint the Human defers or can't be asked about; give your recommended default so work is not blocked meanwhile. |

   - A Decision you add records no new Blind spot: its *Closes* names what raised it.
   - A revised Decision loses its ✓ unless the Human approves the revision.
   - A term that comes up follows *Glossary*.
6. **Align the Plan**, following *Editing the live Plan*:
   - its Decisions;
   - its slices;
   - every diagram they reach.
7. **Validate** the Plan when it changed (see *Validation*).
8. **Append an entry** in the *Alignment log entry* format, even when the Plan did not change: it is the checkpoint your next alignment and the audit start from.
9. **Tell the Human**:
   - the slice status;
   - what changed in the Plan;
   - what NEEDS HUMAN;
   - which slices are ready to implement;
   - if every slice is now `done`, that the Final Architect Audit is next.
