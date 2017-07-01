# FileMaker Standards: Tracking Solution Changes

## The Problem

Many, but not all, database engines and User Interfaces are programmed in text-based languages (SQL, JavaScript/HTML, etc.).  Whether they are compiled at runtime or beforehand, changes to these solutions are easily tracked and discussed using existing, industry-standard tooling.

Some platforms, however, are not text-based, and so these well-tested tools are not as easily applicable to track changes made as development occurs, and then in production as the solution owners' needs change.  FileMaker is found among this latter group.

Unfortunately, there are many cases where such tracking is desirable, and developers and clients alike would do well to identify the least painful way to leverage the existing toolsets as much as possible.

## Possibly Applicable Regulatory Schemes

For example, in several regulated environments, most developers are already aware of the requirements to track changes to the data stored in these systems, and they implement various known Audit Log schemes appropriately.  However, not as many are aware of the requirements in the same environment to track not only changes to the data _in_ the system, but changes to the _system itself_, including any changes made to the FileMaker solutions.

Commonly encountered environments where this is the case are:
 - HIPAA
 - CFR Part 11

## Developer's own "Good Manufacturing Practice"

In addition to regulatory environments, it is simply good practice for a developer to maintain a log of what was done, and why, especially in a team environment.  Human memory is limited in capacity, and also faulty, so it is best to make records "in the heat of the moment", or, put another way, "while the iron is hot" -- that is, while the memory is fresh of all the reasons with their nuance that any particular decision and change was made.

## Teams and the "Bus Factor"

This is especially true in the team environment, where the "primary developer" may go on vacation, or leave the company, or otherwise become unavailable for any reason or none, including death!  In these cases, it is vital that detailed records be kept.

 - Increases Efficiency in Onboarding
 - Decreases Risk by Increasing ["Bus Factor"](https://en.wikipedia.org/wiki/Bus_factor)

## Current Solutions

### Comments

Some of the aforementioned documentation is done in in-line comments, both in calculations, and in scripts, of course, for immediacy and availability.  But the larger picture should not be tracked in these isolated spaces.

### Various hand-maintained logs

Developers have so far used anything from Word documents to physical notepads and even other FileMaker Databases.  These vary in efficiency, but all require some amount of tedium, more or less.  Of course, any solution is going to require some hand work.  The goal, though, is to minimize it as much as possible, by using existing toolsets that automate as much of that as possible.

## A Proposed Solution

A tool such as Git, particularly when paired with a served solution such as BitBucket or GitHub, should be central to any developer's implementation of change control and issue tracking strategies.  This is easily done for web work and documentation writing, and perhaps even for project planning and design, since often these files are text-based.

But how to integrate FileMaker file change tracking into the mix?  Any standard developed should have the following properties:

### As free as possible

Costs should be minimized or completely eliminated.  This means using open source before licensed software, and one-time-purchase software before subscription-based.

### Minimized "overhead"

The developer should find that the time spent to stick to the standard is minimized, so as to maximize the return on investment.

For example, Copy/Paste might/should be used wherever possible.

### Covers every possible change to a FileMaker solution in some way.

The way each change type is covered may be different from the others, but every change type should be trackable.

### Easy to learn

Aside from the notorious learning curve associated with Git itself, and the slight additional learning curve associated with GitHub or BitBucket (or whatever service is chosen), the standard itself should rely on developer's existing knowledge (assuming intermediate to advanced development skills).

### Minimal setup

This should be true for the developer's computer, and also for each Project itself.  On the other hand, it should be understood that there will be some trade-offs in theses areas, particularly in the interest of minimizing actual ongoing implementation overhead (see above).
