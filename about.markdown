---
layout: page
title: Whoami
permalink: /about/
---
<style>
  .about-container {
    position: relative;
    max-width: 900px;
    padding: 2.5rem;
    border-radius: 15px;
    overflow: hidden;
    box-shadow: 0 6px 15px rgba(0,0,0,0.1);
  }

  /* Background image visible, no dark filter */
  .about-container::before {
    content: "";
    position: absolute;
    inset: 0;
    background-image: url('{{ site.baseurl }}/assets/images/white-hat-hacker.jpg');
    background-size: cover;
    background-position: center;
    opacity: 0.45;  /* Semi-transparent image */
    z-index: 0;
  }

  /* White overlay to keep text readable */
  .about-container::after {
    content: "";
    position: absolute;
    inset: 0;
    background: rgba(255, 255, 255, 0.6); /* Light white overlay */
    z-index: 1;
  }

  /* Text above overlays */
  .about-text {
    position: relative;
    z-index: 2;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    font-size: 1.15rem;
    line-height: 1.6;
    color: #222;
  }

  @media (max-width: 700px) {
    .about-container {
      padding: 1.5rem 1rem;
    }

    .about-text {
      font-size: 1rem;
    }
  }
</style>

<div class="about-container">
  <div class="about-text">
    <p>
      I’m a cybersecurity analyst with over two years of experience in Security Operations (SOC), currently focused on securing Microsoft 365 environments.<br><br>
      My specialty lies in working with Microsoft Defender XDR, Sentinel, and Entra to build stronger, more resilient defenses. I also have a solid understanding of Zero Trust principles, security assessments, and the fundamentals of detection engineering.
    </p>
    <p>
      Here, I share tips, insights, and things I’ve explored or tested around securing Microsoft 365 and general cybersecurity. It’s a space where I document what I’ve learned, experiment with different approaches, and reflect on practical ways to keep digital tools and data safer. While this is more of a personal interest than part of my formal role, I hope these notes and experiments are useful to others curious about cybersecurity.
    </p>
  </div>
</div>
