
# Q2 - Music Playlist Editor

## Objective
To compare ArrayList and LinkedList for playlist
operations and evaluate ArrayDeque for an Up Next queue.

## Experimental Workloads

| Playlist Size | Collection |
|---:|---|
| 1,000 | ArrayList, LinkedList, ArrayDeque |
| 10,000 | ArrayList, LinkedList, ArrayDeque |
| 30,000 | ArrayList, LinkedList, ArrayDeque |

## Experimental Results

Record the actual execution times from the terminal.

| Size | Collection | Add End (ms) | Front Insert/Remove (ms) | Middle Insert/Remove (ms) | K-th Access (ms) | Iteration (ms) |
|---:|---|---:|---:|---:|---:|---:|
| 1,000 | ArrayList | | | | | |
| 1,000 | LinkedList | | | | | |
| 10,000 | ArrayList | | | | | |
| 10,000 | LinkedList | | | | | |
| 30,000 | ArrayList | | | | | |
| 30,000 | LinkedList | | | | | |

## ArrayDeque Experiment

| Playlist Size | End Operations Time (ms) |
|---:|---:|
| 1,000 | |
| 10,000 | |
| 30,000 | |

## Complexity Analysis

| Operation | ArrayList | LinkedList | ArrayDeque |
|---|---|---|---|
| Add at end | O(1) amortized | O(1) | O(1) amortized |
| Insert at front | O(n) | O(1) | O(1) |
| Insert in middle | O(n) | O(n) traversal | Not supported by index |
| Remove at front | O(n) | O(1) | O(1) |
| Access k-th element | O(1) | O(n) | Not supported by index |
| Full iteration | O(n) | O(n) | O(n) |

## Engineering Recommendation

ArrayList is suitable for playlists where users frequently
access songs by index, add songs at the end and iterate
through the playlist.

LinkedList may be useful when frequent insertions and
removals occur at known positions through a list iterator.
However, locating a middle position requires traversal.

ArrayDeque is suitable for an Up Next queue because it
supports efficient insertion at both ends and removal
from the front.

## Conclusion

The experiment compares the performance of different
collections for playlist operations.

The final decision is based on measured execution times,
operation requirements and Big-O complexity.
