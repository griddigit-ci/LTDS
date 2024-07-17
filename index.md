---
layout: default
title: Product Introduction
---

# Welcome to Our Product

![Product Banner](https://via.placeholder.com/800x200)

## About Our Product

Our product is designed to revolutionize the way you handle your tasks. It's reliable, efficient, and user-friendly.

<div class="section" id="packages">
  <h2>Packages</h2>

  <div class="package">
    <h3>Basic Package</h3>
    <p><strong>Price:</strong> $19.99/month</p>
    <ul>
      <li>Feature 1</li>
      <li>Feature 2</li>
      <li>Feature 3</li>
    </ul>
  </div>

  <div class="package">
    <h3>Professional Package</h3>
    <p><strong>Price:</strong> $49.99/month</p>
    <ul>
      <li>Feature 1</li>
      <li>Feature 2</li>
      <li>Feature 3</li>
      <li>Feature 4</li>
      <li>Feature 5</li>
    </ul>
  </div>

  <div class="package">
    <h3>Enterprise Package</h3>
    <p><strong>Price:</strong> Contact us for pricing</p>
    <ul>
      <li>All features in Professional</li>
      <li>Feature 6</li>
      <li>Feature 7</li>
      <li>Priority Support</li>
    </ul>
  </div>
</div>

<div class="section" id="features">
  <h2>Key Features</h2>
  <p>Explore the amazing features that make our product stand out:</p>
  <ul>
    <li>Highly customizable</li>
    <li>Intuitive user interface</li>
    <li>Seamless integration with existing tools</li>
    <li>24/7 customer support</li>
  </ul>
</div>

<div class="section" id="github-issues">
  <h2>GitHub Issues</h2>
  <p>To report an issue or to check existing issues, visit our <a href="https://github.com/your-username/your-repository/issues">GitHub Issues page</a>.</p>
  <div id="issues"></div>
</div>

<div class="section" id="contact">
  <h2>Contact</h2>
  <p>For more information, please contact us at <a href="mailto:email@example.com">email@example.com</a>.</p>
  <p>Follow us on <a href="https://twitter.com/yourusername">Twitter</a> for updates.</p>
</div>

<script>
  fetch('https://api.github.com/repos/your-username/your-repository/issues')
    .then(response => response.json())
    .then(data => {
      const issuesContainer = document.getElementById('issues');
      data.forEach(issue => {
        const issueElement = document.createElement('div');
        issueElement.className = 'issue';
        issueElement.innerHTML = `<h3><a href="${issue.html_url}">${issue.title}</a></h3><p>${issue.body}</p>`;
        issuesContainer.appendChild(issueElement);
      });
    });
</script>
