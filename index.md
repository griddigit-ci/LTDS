---
layout: default
title: Long Term Development Statement Information Hub (Sample site)
---

# Long Term Development Statement (LTDS)

![Product Banner](https://via.placeholder.com/800x200)


## About LTDS

The publication of Long Term Development Statements (LTDS), describing the characteristics and development of GB electricity distribution networks, is a long standing obligation on distribution network operators (DNOs), mandated through a direction, pursuant to paragraph 25.2 of the standard conditions of the Electricity Distribution Licence and described in detail in the Form of Long Term Development Statement (FoS).

The revised FoS introduces important new requirements for grid model data to be provided using the Common Information Model (CIM) and for the publication of Capacity Heatmap data (an example of heatmap is available <a href="https://opengridsystems.github.io/network-heatmaps-example/" target="_blank">here</a>).

Blah Blah Blah.
2nd Friday

<div class="section" id="packages">
  <h2>Documentation</h2>

  <div class="package">
    <h3>Main documents</h3>
    <p><strong>Documents published by Ofgem are available here...</strong></p>
    <ul>
      <li>Doc 1</li>
      <li>Doc 2</li>
      <li>Doc 3</li>
    </ul>
  </div>

  <div class="package">
    <h3>Current release</h3>
    <p><strong>Release 3.0.0: 1 May 2027</strong> </p>
    <ul>
      <li>Doc 1</li>
      <li>Doc 2</li>
      <li>Doc 3</li>
      <li>Doc 4</li>
      <li>Doc 5</li>
    </ul>
  </div>

  <div class="package">
    <h3>Past releases</h3>
    <ul>
      <li>Release 2.1.0, 1 Dec 2026</li>
      <li>Release 1.1.0, 1 Aug 2024</li>
      <li>Release 1.0.0, 1 May 2024</li>
      <li>Priority Support</li>
    </ul>
  </div>
</div>

<div class="section" id="features">
  <h2>Examples of LTDS</h2>
  <p>Explore available examples:</p>
  <ul>
    <li>Example 1</li>
    <li>Example 2</li>
    <li>Example 3</li>
    <li>Example 4</li>
  </ul>
</div>

## Latest News

<div id="news">
  <h2>Important changes</h2>
  <div class="news-item">
    <h3>Release 3.0.0 published</h3>
    <p>We have just released new update of LTDS packaged as release 3.0.0</p>
    <a href="https://link-to-news-article.com" target="_blank">Read more</a>
  </div>
  <div class="news-item">
    <h3>LTDS IOP registration is now open</h3>
    <p>An IOP to test current implementations of LTDS is scheduled on 2 Jul 2029. All concerned DNOs and vendors are invited to register...</p>
    <a href="https://link-to-news-article.com" target="_blank">Read more</a>
  </div>
  <div class="news-item">
    <h3>A webinar on next release is planned on 3 May 2030</h3>
    <p>GB CIM Governing Body will be condicting a webinar on 3 May 2030. ...</p>
    <a href="https://link-to-news-article.com" target="_blank">Read more</a>
  </div>
</div>

<div class="section" id="features">
  <h2>LTDS Governance and Standardisation</h2>
  <p>The GB Governing body is discussing standardisation on the following GB extensions:</p>
  <ul>
    <li>Extension 1</li>
    <li>Extension 2</li>
    <li>Extension 3</li>
    <li>Extension 4</li>
  </ul>
</div>

<div class="section" id="github-issues">
  <h2>GitHub Open Issues</h2>
  <p>To report an issue or to check existing issues, visit our <a href="https://github.com/your-username/your-repository/issues">GitHub Issues page</a>.</p>
  <div id="issues"></div>


</div>

<div class="section" id="contact">
  <h2>Contact</h2>
  <p>For more information, please contact us at <a href="mailto:email@example.com">email@example.com</a>.</p>
  <p>Follow us on <a href="https://twitter.com/yourusername">Twitter</a> for updates.</p>
</div>

<script>
  // Fetch and display GitHub issues
  fetch('https://api.github.com/repos/griddigit/ltds/issues')
    .then(response => {
      if (!response.ok) {
        throw new Error('Network response was not ok ' + response.statusText);
      }
      return response.json();
    })
    .then(data => {
      const issuesContainer = document.getElementById('issues');
      if (data.length === 0) {
        issuesContainer.innerHTML = '<p>No open issues at the moment.</p>';
      } else {
        data.forEach(issue => {
          const issueElement = document.createElement('div');
          issueElement.className = 'issue';
          issueElement.innerHTML = `<h3><a href="${issue.html_url}">${issue.title}</a></h3><p>${issue.body}</p>`;
          issuesContainer.appendChild(issueElement);
        });
      }
    })
    .catch(error => {
      console.error('There was a problem with the fetch operation:', error);
      document.getElementById('issues').innerHTML = '<p>Failed to load issues. Please try again later.</p>';
    });

  // Example of fetching news data (replace with your own source)
  fetch('https://api.example.com/news') // Replace with your news API URL
    .then(response => {
      if (!response.ok) {
        throw new Error('Network response was not ok ' + response.statusText);
      }
      return response.json();
    })
    .then(data => {
      const newsContainer = document.getElementById('news');
      data.articles.forEach(article => {
        const articleElement = document.createElement('div');
        articleElement.className = 'news-item';
        articleElement.innerHTML = `<h3>${article.title}</h3><p>${article.description}</p><a href="${article.url}" target="_blank">Read more</a>`;
        newsContainer.appendChild(articleElement);
      });
    })
    .catch(error => {
      console.error('There was a problem with the fetch operation:', error);
      document.getElementById('news').innerHTML = '<p>Failed to load news. Please try again later.</p>';
    });
</script>
