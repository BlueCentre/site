---
layout: page
title: Blog
permalink: /blog/
---

<div class="hero" style="padding: 4rem 0;">
  <div class="wrapper">
    <h1>Our Blog</h1>
    <p>Insights, tutorials, and updates from the Vitruvian Software team on AI, DevOps, and open-source development.</p>
  </div>
</div>

<div class="content-section">
  <div class="wrapper">
    {%- if site.posts.size > 0 -%}
      <div class="post-list">
        {%- for post in site.posts -%}
        <article class="card fade-in-up" style="margin-bottom: 2rem;">
          <div style="display: flex; justify-content: space-between; align-items: flex-start; margin-bottom: 1rem;">
            <div>
              {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
              <span class="post-meta" style="color: var(--text-muted); font-size: 0.9rem;">{{ post.date | date: date_format }}</span>
              <div style="margin-top: 0.5rem;">
                {%- if post.categories.size > 0 -%}
                  {%- for category in post.categories -%}
                    <span style="background: var(--primary-accent); color: white; padding: 0.2rem 0.6rem; border-radius: 12px; font-size: 0.8rem; margin-right: 0.5rem;">{{ category }}</span>
                  {%- endfor -%}
                {%- endif -%}
              </div>
            </div>
          </div>
          
          <h2 style="margin-bottom: 1rem;">
            <a href="{{ post.url | relative_url }}" style="text-decoration: none; color: var(--text-color);">
              {{ post.title | escape }}
            </a>
          </h2>
          
          {%- if post.excerpt -%}
            <p style="color: var(--text-muted); margin-bottom: 1.5rem;">{{ post.excerpt | markdownify | strip_html | truncate: 200 }}</p>
          {%- endif -%}
          
          <div style="display: flex; justify-content: space-between; align-items: center;">
            <a href="{{ post.url | relative_url }}" class="button">Read More</a>
            {%- if post.author -%}
              <span style="color: var(--text-muted); font-size: 0.9rem;">by {{ post.author }}</span>
            {%- endif -%}
          </div>
        </article>
        {%- endfor -%}
      </div>
    {%- else -%}
      <div class="text-center" style="padding: 4rem 0;">
        <div style="max-width: 600px; margin: 0 auto;">
          <div style="background: var(--card-bg); padding: 3rem 2rem; border-radius: var(--border-radius); border: 1px solid var(--border-color);">
            <h2 style="color: var(--primary-accent); margin-bottom: 1.5rem;">📝 No Posts Yet</h2>
            <p style="font-size: 1.1rem; margin-bottom: 2rem;">We're preparing exciting content about our latest projects and development insights.</p>
          </div>
        </div>
      </div>
    {%- endif -%}
  </div>
</div>

<div class="content-section">
  <div class="wrapper">
    <h2 class="text-center">What to Expect from Our Blog</h2>
    <p class="text-center mb-2">We share insights and tutorials on the technologies we're passionate about:</p>
    
    <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 2rem; margin: 2rem 0;">
      <div class="card fade-in-up">
        <h3>🤖 AI Development</h3>
        <p>Deep dives into AI agent development, best practices, and real-world applications using our ADK framework.</p>
      </div>
      
      <div class="card fade-in-up">
        <h3>⚙️ DevOps Insights</h3>
        <p>Practical DevOps tutorials, automation strategies, and workflow optimizations from our team's experience.</p>
      </div>
      
      <div class="card fade-in-up">
        <h3>📊 Project Updates</h3>
        <p>Behind-the-scenes looks at our open-source projects, release notes, and feature announcements.</p>
      </div>
      
      <div class="card fade-in-up">
        <h3>💡 Technical Deep Dives</h3>
        <p>Detailed technical explanations, architecture decisions, and case studies from our development work.</p>
      </div>
    </div>
  </div>
</div>

<div class="content-section text-center">
  <div class="wrapper">
    <h2>Stay Updated</h2>
    <p class="mb-2">Get notified when we publish new blog posts and project updates:</p>
    
    <div style="background: var(--card-bg); padding: 2rem; border-radius: var(--border-radius); border: 1px solid var(--border-color); max-width: 500px; margin: 2rem auto;">
      <h4 style="margin-bottom: 1rem; color: var(--primary-accent);">📢 Subscribe for Updates</h4>
      <p style="margin-bottom: 1.5rem; font-size: 0.95rem;">Follow us on GitHub and Twitter to get notifications about new posts and project releases.</p>
      <div style="display: flex; gap: 1rem; justify-content: center; flex-wrap: wrap;">
        <a href="https://github.com/BlueCentre" class="button">🔔 Watch on GitHub</a>
        <a href="https://twitter.com/ipv1337" class="button" style="background: var(--gradient-secondary);">Follow on Twitter</a>
      </div>
    </div>
  </div>
</div>
