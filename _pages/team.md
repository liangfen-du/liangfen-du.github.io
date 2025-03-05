---
layout: archive
# title: "Team"
permalink: /team/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

<div class="team-container">
  <style>
    .team-container {
      margin-bottom: 30px;
    }
    .team-member {
      display: flex;
      flex-direction: row;
      margin-bottom: 40px;
      align-items: flex-start;
    }
    .team-member-image {
      flex: 0 0 200px;
      margin-right: 20px;
    }
    .team-member-image img {
      width: 100%;
      aspect-ratio: 3/4;
      border-radius: 50%;
      border: 3px solid #f2f2f2;
      object-fit: cover;
    }
    .team-member-info {
      flex: 1;
    }
    .team-member-info h2 {
      margin-top: 0;
      margin-bottom: 10px;
      color: #333;
    }
    .team-member-info h3 {
      margin-top: 0;
      margin-bottom: 15px;
      color: #666;
      font-weight: normal;
    }
    .team-member-info p {
      margin-bottom: 10px;
      line-height: 1.5;
    }
    .team-member-contact {
      margin-top: 15px;
    }
    .team-member-contact a {
      margin-right: 15px;
      text-decoration: none;
    }
    @media (max-width: 768px) {
      .team-member {
        flex-direction: column;
      }
      .team-member-image {
        margin-right: 0;
        margin-bottom: 20px;
        width: 150px;
      }
    }
  </style>


  <!-- Postdoctoral Researchers -->
  <h1>Postdoctoral Researchers</h1>
  
  <div class="team-member">
    <div class="team-member-image">
      <img src="/images/liangfen-photo-square.jpg" alt="Postdoc Name">
    </div>
    <div class="team-member-info">
      <h2>Postdoc Name</h2>
      <h3>Postdoctoral Researcher</h3>
      <p>Research focus and brief description of their work in the lab. Information about their background, expertise, and current projects.</p>
      <div class="team-member-contact">
        <a href="mailto:postdoc@example.com"><i class="fas fa-envelope"></i> Email</a>
        <a href="https://scholar.google.com/" target="_blank"><i class="ai ai-google-scholar"></i> Google Scholar</a>
      </div>
    </div>
  </div>

  <!-- PhD Students -->
  <h1>PhD Students</h1>
  
  <div class="team-member">
    <div class="team-member-image">
      <img src="/images/phd1.jpg" alt="PhD Student Name">
    </div>
    <div class="team-member-info">
      <h2>PhD Student Name</h2>
      <h3>PhD Candidate</h3>
      <p>Research topic and brief description of their doctoral work. Information about their academic background and research interests.</p>
      <div class="team-member-contact">
        <a href="mailto:phd@example.com"><i class="fas fa-envelope"></i> Email</a>
        <a href="https://github.com/" target="_blank"><i class="fab fa-github"></i> GitHub</a>
      </div>
    </div>
  </div>

  <!-- Master Students -->
  <h1>Master Students</h1>
  
  <div class="team-member">
    <div class="team-member-image">
      <img src="/images/master1.jpg" alt="Master Student Name">
    </div>
    <div class="team-member-info">
      <h2>Master Student Name</h2>
      <h3>Master's Student</h3>
      <p>Research focus and brief description of their work. Information about their academic interests and goals.</p>
      <div class="team-member-contact">
        <a href="mailto:master@example.com"><i class="fas fa-envelope"></i> Email</a>
      </div>
    </div>
  </div>

  <!-- Alumni -->
  <h1>Alumni</h1>
  
  <div class="team-member">
    <div class="team-member-image">
      <img src="/images/alumni1.jpg" alt="Alumni Name">
    </div>
    <div class="team-member-info">
      <h2>Alumni Name</h2>
      <h3>Former PhD Student (2018-2022)</h3>
      <p>Brief description of their work in the lab and their current position or career path after graduation.</p>
      <div class="team-member-contact">
        <a href="mailto:alumni@example.com"><i class="fas fa-envelope"></i> Email</a>
        <a href="https://scholar.google.com/" target="_blank"><i class="ai ai-google-scholar"></i> Google Scholar</a>
      </div>
    </div>
  </div>
</div>

