# ⟨SW⟩ Sliding Window — Master Course

A complete, self-contained study website for mastering the **Sliding Window** pattern in DSA — covering all patterns, 20 LeetCode problems, an interactive visualizer, and a full cheat sheet. Built for interview prep and competitive programming.

> 🌐 **No installation. No internet required. Just open the HTML file in any browser.**

---

## 📸 Preview

| Section | What's inside |
|---|---|
| **Theory** | Core concept, when to use it, both templates, complexity table |
| **Visualizer** | Step-by-step animated walkthrough of fixed & variable window algorithms |
| **Patterns** | All 6 patterns as expandable cards with full Python templates |
| **Problems** | 20 LeetCode problems with hints & code skeletons, filterable by difficulty/pattern |
| **Cheat Sheet** | Interview decision tree, key tricks, and all 6 templates side-by-side |

---

## 🚀 Getting Started

1. **Download** `sliding-window-course.html`
2. **Open** it in any browser (Chrome, Firefox, Safari, Edge)
3. **Study** — all 5 sections are instantly accessible, works fully offline

That's it. No npm, no build step, no dependencies.

---

## 📚 What's Covered

### Core Theory
- What sliding window is and why it reduces O(n²) to O(n)
- When to use it vs. when not to (subsequences, backtracking, etc.)
- The key insight: every element enters and leaves the window at most once

### 6 Patterns (with templates)

| # | Pattern | Type | Key Idea |
|---|---|---|---|
| 1 | Fixed Size Window | Fixed | Build first window, then slide by 1 |
| 2 | Variable Window — Maximize | Variable | Expand right, shrink left when invalid |
| 3 | Variable Window — Minimize | Variable | Expand until valid, shrink while still valid |
| 4 | Exactly K — Subtraction Trick | Variable | `atMost(k) − atMost(k−1)` |
| 5 | Monotonic Deque | Fixed + Deque | O(n) window max/min using a deque |
| 6 | Window + HashMap | Variable + Map | Track frequencies with Counter/dict |

### 20 LeetCode Problems

| # | Problem | Difficulty | Pattern |
|---|---|---|---|
| 643 | Maximum Average Subarray I | 🟢 Easy | Fixed |
| 3 | Longest Substring Without Repeating Characters | 🟡 Medium | Variable + Map |
| 76 | Minimum Window Substring | 🔴 Hard | Variable + Map |
| 239 | Sliding Window Maximum | 🔴 Hard | Deque |
| 567 | Permutation in String | 🟡 Medium | Fixed + Map |
| 438 | Find All Anagrams in a String | 🟡 Medium | Fixed + Map |
| 904 | Fruits Into Baskets | 🟡 Medium | Variable + Map |
| 1004 | Max Consecutive Ones III | 🟡 Medium | Variable |
| 424 | Longest Repeating Character Replacement | 🟡 Medium | Variable + Map |
| 209 | Minimum Size Subarray Sum | 🟡 Medium | Variable |
| 992 | Subarrays with K Different Integers | 🔴 Hard | Exact-K |
| 1248 | Count Number of Nice Subarrays | 🟡 Medium | Exact-K |
| 930 | Binary Subarrays With Sum | 🟡 Medium | Exact-K |
| 1493 | Longest Subarray of 1s After Deleting One Element | 🟡 Medium | Variable |
| 1876 | Substrings of Size Three with Distinct Characters | 🟢 Easy | Fixed |
| 1696 | Jump Game VI | 🟡 Medium | Deque |
| 340 | Longest Substring with At Most K Distinct Characters | 🟡 Medium | Variable + Map |
| 159 | Longest Substring with At Most 2 Distinct Characters | 🟡 Medium | Variable + Map |
| 795 | Number of Subarrays with Bounded Maximum | 🟡 Medium | Variable |
| 1425 | Constrained Subsequence Sum | 🔴 Hard | Deque |

---

## 🧠 Key Tricks

**The "Exactly K" trick**
```
subarrays with exactly k distinct = atMost(k) − atMost(k−1)
```
Converts seemingly hard exact-count problems (LC 992, 930, 1248) into two easy variable-window passes.

**Counting all valid subarrays ending at `right`**
```python
ans += right - left + 1
```
When the window is valid, this counts every subarray ending at the current right pointer.

**Monotonic deque for O(n) window max**
```python
# Maintain decreasing order of values (by index)
# Front of deque = max of current window
while dq and nums[dq[-1]] < nums[i]:
    dq.pop()
dq.append(i)
```

**Interview decision flow**
```
1. Contiguous subarray/substring?  → Sliding Window
2. Fixed size k?                   → Fixed template
3. Variable size?                  → Expand/shrink template
4. Frequency tracking needed?      → Add HashMap
5. Window max/min needed?          → Add Monotonic Deque
6. Exactly k constraint?           → atMost(k) − atMost(k−1)
```

---

## 🗂 File Structure

```
sliding-window-course.html   ← the entire course, single file
README.md                    ← this file
```

Everything is bundled into one HTML file — styles, scripts, content, and the visualizer. No external dependencies.

---

## 🛠 Built With

- Vanilla HTML, CSS, JavaScript — zero frameworks, zero dependencies
- [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) for code blocks
- [Syne](https://fonts.google.com/specimen/Syne) for headings
- Dark theme optimized for long study sessions

---

## 📖 Recommended Study Order

1. Start with **Theory** — understand the mental model and both templates cold
2. Use the **Visualizer** — step through both examples until the pointer movement clicks
3. Read through all **Patterns** — understand when each one applies
4. Work **Problems** in order: Easy Fixed → Easy Variable → Medium → Hard
5. Keep **Cheat Sheet** open during practice contests or mock interviews

---

## 🤝 Contributing

Found a bug, want to add more problems, or improve a template? PRs are welcome.

1. Fork the repo
2. Edit `sliding-window-course.html` (all content is in one file)
3. Open a pull request with a short description of what you changed

---

## 📄 License

MIT — free to use, share, and modify.

---

*Built as a focused, no-fluff study resource. If this helped you crack an interview, consider starring the repo ⭐*
