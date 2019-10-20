# Index Page
<% @posts.each do |post| %>
  <div><a href='<%= "/posts/#{post.id}" %>'><%= post.title %></a></div>
<% end %>

# Using Link to 
<% @posts.each do |post| %>
  <div><%= link_to post.title, "/posts/#{post.id}" %></div>
<% end %>

# refactor
<% @posts.each do |post| %>
  <div><%= link_to post.title, post_path(post.id) %></div>
<% end %>