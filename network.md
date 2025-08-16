---
title: Networking and Architecture
---
<nav>
  <a href="/">About</a>
  <a href="/ai">Artificial Intelligence</a>
  <a href="/software">Software Development</a>
  <a href="/network"  class="active">Networking and Architecture</a>
  <a href="/mobile">Mobile Development</a>
  <a href="/game">Gaming and Game AI</a>
  <a href="/other">Logical and Functional Programming</a>
</nav>

<style>
nav {
  display: flex;
  gap: 20px;
  margin-bottom: 40px;
}
nav a {
  color: #00ffff;
  text-decoration: none;
  font-weight: bold;
  padding: 6px 12px;
  border: 1px solid #00ffff;
  border-radius: 4px;
  transition: background 0.2s, color 0.2s;
  font-size: 13px;
}
nav a:hover {
  background: #00ffff;
  color: #000;
}
nav a.active {
  background: #00ff00;
  color: #000;
  border-color: #00ff00;
}
</style>
### Simulation

**Cache Simulator:**

Click below to watch!
<video controls="controls" src="vids/cache.mp4">
    Your browser does not support the HTML5 Video element.
</video>

I created a Cache simulator using C, simulated an L1 cache using the Least Recently Used(LRU) replacement
algorithm, and included an option to incorporate prefetching

### Other

**Bit Manipulation:**

Click below to watch!

[![](images/bit.png)](vids/bit.mp4)

Using C and restricted to using only the 6 Bit Operators included with C, I created a series of Bit
functions from guring out a bit's parity to palindrome checking.