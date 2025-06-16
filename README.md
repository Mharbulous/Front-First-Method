# FRONT FIRST METHOD
Version:       1.9
Last updated:  [date]

This front first method is a structured process for collaborative AI assisted coding.

The method consists of 10 phases, with each phase described in more detail in \Phases folder.

We are currently working on how best to break up the process into phases based on the following key tenets:

## Key Tenets

### 1. Frontend First

Build the front end first and use the front end as the primary source of truth for defining backend requirements. I.e., the validated UI/UX becomes a specification that drives all subsequent technical decisions.

**Function not Frills.**  Sometimes style elements express functional intent, but sometimes style elements are frills chosen purely for aesthetic appeal.  Because the front end is being used as a tool for AI - human communcation, it is vital that we distinguish style elements that indicate functional intent from frills that are added for aesthetic appeal.  To avoid cluttering the context windows with frills that could be misinterpreted as indicating something that was never intended, styles that communicate functional intent should be separated from frills by storing their respective .css files in the following folder structures:

\src\styles\frills\
\src\styles\indicators\


### 2. Sliding Phase States

- **Phases** are major deliverables with clear governance states
- **Steps** are integrated components within a phase that are developed iteratively together due to their interdependencies

Each phase is in one of three states, analogous to states of matter:
- **Creating**: The current phase being actively worked on.  It is fluid, flexible, and evolving; _like a gas_.
- **Revising**: The previous phase (N-1) can still be modified if needed.  It is moldable but more structured; _like a liquid_.
- **Locked**: All earlier phases (N-2 and before) cannot be changed.  It is fixed and stable; _like a solid_.

This creates a sliding window where only the current phase and the immediately previous phase can be modified, preventing endless backward iteration while maintaining necessary flexibility.

**Example**: When working on Phase 6 (Engineering):
- Phase 6: Creating
- Phase 5: Revising 
- Phases 1-4: Locked



## Phases

Figurout out the best way to 

1. **Research & Planning** (results in PRD)
2. **Content & Navigation** (results in Sitemap)
3. **Layout** (results in Wireframe)
4. **User Interface** (results in Mockup)
5. **Technical Design** (results in Technical Design Document)
6. **Engineering** (results in Backend Specifications)
7. **Prototype** (results in Prototype)
8. **Aesthetics & Design** (results in Alpha Test)
9. **User Testing** (results in Beta Test)
10. **Production Release**

