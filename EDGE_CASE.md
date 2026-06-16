# Document your edge case here
- To get marks for this section you will need to explain to your tutor:
1) The edge case you identified
2) How you have accounted for this in your implementation

# Edge Case: Mark out of valid range

## Case
A student's mark should be between 0 and 100 inclusive. A call could send a mark outside of that range (e.g. -5) which is not a valid score.

## Handling
In POST /students and PUT /students/{id}, if a mark is provided and not in the valid range, the request is rejected with a 404 error. The student's mark defaults to None if they have not been graded yet (no mark provided).