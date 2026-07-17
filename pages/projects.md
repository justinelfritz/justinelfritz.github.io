---
layout: page
title: projects
description: overviews of individual projects
---

<style>
  .card-container {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 1.5rem;
    margin-top: 2rem;
  }
  .project-card {
    background-color: #f7f9fb;
    border: 1px solid #d0d7de;
    border-radius: 6px;
    padding: 1.25rem;
    transition: transform 0.2s, box-shadow 0.2s;
  }
  .project-card:hover {
    transform: translateY(-2px);
    box-shadow: 0 4px 10px rgba(0,0,0,0.08);
  }
  .card-title {
    font-size: 1.15rem;
    font-weight: 600;
    margin-bottom: 0.5rem;
  }
  .card-title a {
    text-decoration: none;
    color: #1a2333;
  }
  .card-desc {
    font-size: 0.9rem;
    color: #555c68;
    line-height: 1.4;
  }
  .card-meta {
    margin-top: 1rem;
    font-size: 0.8rem;
  }
</style>

<div class="card-container">
  <!-- Card 1 -->
  <div class="project-card">
    <div class="card-title"><a href="https://justinelfritz.github.io/pages/co_gap_gps.html">GPS mapping the C&O and GAP</a></div>
    <div class="card-desc">GPS mapping the C&O Canal and Great Allegheny Passage.</div>
  </div>

  <!-- Card 2 -->
  <div class="project-card">
    <div class="card-title"><a href="https://justinelfritz.github.io/pages/laugavegur.html">GPS mapping the Laugavegur</a></div>
    <div class="card-desc">GPS mapping the Laugavegur hiking trail in Iceland.</div>
  </div>

  <!-- Card 3 -->
  <div class="project-card">
    <div class="card-title"><a href="https://justinelfritz.github.io/pages/interest_calculators.html">Compound interest calculations</a></div>
    <div class="card-desc">Calculations for compounding and accumulating interest.</div>
  </div>

  <!-- Card 4 -->
  <div class="project-card">
    <div class="card-title"><a href="https://justinelfritz.github.io/pages/dividend_calendar.html">Ex-Dividend Calendar</a></div>
    <div class="card-desc">A python-based google calendar populator for ex-dividend dates.</div>
  </div>

  <!-- Card 5 -->
  <div class="project-card">
    <div class="card-title">
      <a href="https://justinelfritz.github.io/pages/city-comparison.html" target="_blank">City Comparison Tool</a>
    </div>
    <div class="card-desc">Comparison tool for certain mid-sized american cities.</div>
    <div class="card-meta">
      <a href="https://github.com/justinelfritz/relocation-comparison">View Source Code &raquo;</a>
    </div>
  </div>

  <!-- Card 6 -->
  <div class="project-card">
    <div class="card-title"><a href="https://justinelfritz.github.io/pages/sourdough.html">Re-thinking sourdough</a></div>
    <div class="card-desc">Mathematically robust method for sourdough recipe design.</div>
  </div>

  <!-- Card 7 -->
  <div class="project-card">
    <div class="card-title"><a href="https://justinelfritz.github.io/pages/vsh.html">Fortran VSH Module</a></div>
    <div class="card-desc">A Fortran module for Vector Spherical Harmonics computations.</div>
  </div>
</div>