# COMP9021-2022

若需要提供详细的咨询指导，可联系V信codingtutor

COMP9021, Trimester 1, 2022
1.1. Aims. The purpose of the assignment is to:
• design and implement an interface based on the desired behaviour of an application program; • practice the use of Python syntax;
• develop problem solving skills.
1.2. Submission. Your program will be stored in a file named polygons.py. After you have developed and tested your program, upload it using Ed (unless you worked directly in Ed). Assignments can be submitted more than once; the last version is marked. Your assignment is due by April 25, 10:00am.
1.3. Assessment. The assignment is worth 13 marks. It is going to be tested against a number of input files. For each test, the automarking script will let your program run for 30 seconds.
Late assignments will be penalised: the mark for a late submission will be the minimum of the awarded mark and 10 minus the number of full and partial days that have elapsed from the due date.
1.4. Reminder on plagiarism policy. You are permitted, indeed encouraged, to discuss ways to solve the assignment with other people. Such discussions must be in terms of algorithms, not code. But you must implement the solution on your own. Submissions are routinely scanned for similarities that occur when students copy and modify other people’s work, or work very closely together on a single implementation. Severe penalties apply.
2. General presentation You will design and implement a program that will
• extract and analyse the various characteristics of (simple) polygons, their contours being coded and stored in a file, and
• – either display those characteristics: perimeter, area, convexity, number of rotations that keep the polygon invariant, and depth (the length of the longest chain of enclosing polygons)
– or output some Latex code, to be stored in a file, from which a pictorial representation of the polygons can be produced, coloured in a way which is proportional to their area.
Call encoding any 2-dimensional grid of size between between 2 × 2 and 50 × 50 (both dimensions can be different) all of whose elements are either 0 or 1.
Call neighbour of a member m of an encoding any of the at most eight members of the grid whose value is 1 and each of both indexes differs from m’s corresponding index by at most 1. Given a particular encoding, we inductively define for all natural numbers d the set of polygons of depth d (for this encoding) as follows. Let a natural number d be given, and suppose that for all d′ < d, the set of polygons of depth d′ has been defined. Change in the encoding all 1’s that determine those polygons to 0. Then the set of polygons of depth d is defined as the set of polygons which can be obtained from that encoding by connecting 1’s with some of their neighbours in such a way that we obtain a maximal polygon (that is, a polygon which is not included in any other polygon obtained from that encoding by connecting 1’s with some of their neighbours).
