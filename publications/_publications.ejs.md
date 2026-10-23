```{=html}
<ul class="publication-list list">
<% for (const item of items) { %>
  <li class="publication-entry" <%= metadataAttrs(item) %>>
    <div class="publication-year listing-date"><%- item.date %></div>
    <div class="publication-body">
      <h2 class="publication-title listing-title"><%- item.title %></h2>
      <p class="publication-authors listing-authors"><% const names = String(item.authors).split(', '); names.forEach((name, index) => { %><% if (index) { %>, <% } %><% if (name === 'Man Chen') { %><strong><%- name %></strong><% } else { %><%- name %><% } %><% }); %></p>
      <% if (item.journal) { %><p class="publication-journal listing-journal"><%- item.journal %></p><% } %>
      <% if (item.links && item.links.length) { %>
      <div class="publication-resources" aria-label="Resources for <%- item.title %>">
      <% for (const link of item.links) { const icons = {Journal: 'journal-text', 'Pre-Print': 'file-earmark-text', Preprint: 'file-earmark-text', Code: 'code-slash', Data: 'database', 'Supplementary materials': 'paperclip', PDF: 'file-earmark-pdf'}; %>
        <a class="btn btn-outline-primary btn-sm" href="<%- link.href %>"><i class="bi bi-<%- icons[link.text] || 'link-45deg' %>" aria-hidden="true"></i> <%- link.text %></a>
      <% } %>
      </div>
      <% } %>
      <% if (item.abstract) { %><details class="publication-abstract"><summary>Abstract</summary><p><%- item.abstract %></p></details><% } %>
    </div>
  </li>
<% } %>
</ul>
```
