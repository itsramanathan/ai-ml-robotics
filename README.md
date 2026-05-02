# ai-ml-robotics
AI ML Robotics Projects

My journey learning AI, ML, Robotics and building products

## #4 Group Anagrams (Medium)

**Pattern:** Hash map with engineered key
**Trick:** The leap from Easy to Medium isn't a new pattern — it's
a new question. Easy problems hand you the key directly (a number,
a char). Mediums force you to engineer one. For anagrams, the
canonical form is the sorted string — anagrams collide on the same
sorted key, so defaultdict(list) groups them in one pass.
**Time:** ~50 min (with brute force, optimal, and full debugging)
**Note:** First Medium. Wrote brute force first (n² with a 'used'
parallel list), then collapsed to ~5 lines using defaultdict(list)
and ''.join(sorted(s)) as the canonical key. The mental move from
brute force → optimal was: notice that sorted(strs[i]) was being
recomputed inside the inner loop, so memoize it once per string
via a hash map.
**Concepts internalized:** [False] * n for parallel state tracking,
range(start, stop) iteration, defaultdict factory pattern, list
comprehension on dict.values(), sorted() returns list (need ''.join).
