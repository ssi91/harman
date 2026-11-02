# Planning

Turn the Task into the Plan, `$HARMAN_DIR/<taskID>/plan/`. The shared sections of `SKILL.md` apply throughout; write each file from its template in [plan-templates.md](plan-templates.md).

1. **Read the Task.** Its words go into `plan.md` verbatim; do not silently reinterpret it.
2. **Study the code**:
   - find where the change lands:
     - the modules;
     - the seams;
     - the abstractions;
   - call out every prior design that blocks the change as a Refactor — never work around it silently;
   - record the commit you studied as the Plan's `Base`: the Final Architect Audit measures the implementation from it.
3. **Settle the Glossary** before anything else gets a name (see *Glossary* in `SKILL.md`).
4. **List the Blind spots**:
   - anything the Task leaves unstated, such as:
     - unspecified behaviour;
     - unclear ownership;
     - missing acceptance criteria;
     - unhandled edge cases;
     - integration and migration questions;
   - if there are none, say so.
5. **Make the Decisions** (see *Decision making* in `SKILL.md`):
   - every Blind spot gets a Decision;
   - every prior design that blocks the change gets a Refactor.
6. **Depict the change**:
   - in `plan.md`, the **Architecture** — one of:
     - a component diagram of what the Task touches, in its target state, its parts marked by class (see the template):
       - added;
       - changed;
       - removed;
     - one line: "No structural change — <why>";
   - in each Decision's Detailed document:
     - **Flows** — for each runtime flow the Decision changes, a sequence diagram before and after;
     - **Contracts and data** — for each public contract, code-level dependency, or data shape it changes, a class or ER diagram before and after;
   - in `plan.md`, under *Flows* and *Contracts and data* — links to those Decisions.
7. **Slice.** Split the work into the smallest independently completable units, numbered from 1 in dependency order. Each slice:
   - touches one concern, and is reviewable on its own;
   - is detailed enough that the implementer makes no architectural decisions — name these where you already know them:
     - files;
     - types;
     - signatures;
     - call sites;
   - declares its dependencies on other slices;
   - may be built at the same time as any slice it has no dependency path to, each in its own worktree — so two such slices must not touch the same file; if they would, make one depend on the other;
   - carries **Completion criteria** that are checkable — a passing test, an observable behaviour, a command that exits clean. If a slice truly cannot have one, write `Completion criteria: none — <why>` rather than inventing a vague one.

   Then:
   - draw the Slice graph: an arrow from each slice to every slice that depends on it, so the build order, and the slices with no path between them — buildable in parallel — show at a glance;
   - fill each Decision's *Slices*, in its row of `plan.md` and in its Detailed document.
8. **Write the Plan** — every file, from its template. A Task too small to decompose still gets a single-slice Plan rather than no Plan — downstream roles depend on the files existing.
9. **Validate** the Plan (see *Validation* in `SKILL.md`).
10. **Tell the Human**:
    - the Plan's path;
    - the slice count;
    - which slices can be built in parallel.
