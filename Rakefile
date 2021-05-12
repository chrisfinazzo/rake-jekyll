
task default: [:build]

task :build do
  sh 'bundle exec jekyll build --incremental'
end

task :doctor do
  sh 'bundle exec jekyll doctor'
end

task :post do

File.open("_drafts/new.md", "w") do |post|
    post.puts("---")
    post.puts("layout: post")
    post.puts("title: ")
    post.puts("---")
    post.puts
  end
  sh 'bbedit _drafts/new.md'
end

task :link do

File.open("_links/new.md", "w") do |post|
    post.puts("---")
    post.puts("layout: link")
    post.puts("title: ")
    post.puts("---")
    post.puts
  end
  sh 'bbedit _links/new.md'
end

task :note do

File.open("_notes/new.md", "w") do |post|
    post.puts("---")
    post.puts("layout: note")
    post.puts("title: ")
    post.puts("---")
    post.puts
  end
  sh 'bbedit _notes/new.md'
end

task :reply do

File.open("_notes/new.md", "w") do |post|
    post.puts("---")
    post.puts("layout: reply-to")
    post.puts("title: ")
    post.puts("---")
    post.puts
  end
  sh 'bbedit _notes/new.md'
end

task :repost do

File.open("_notes/new.md", "w") do |post|
    post.puts("---")
    post.puts("layout: repost-of")
    post.puts("title: ")
    post.puts("---")
    post.puts
  end
  sh 'bbedit _notes/new.md'
end

task :tweet do

File.open("_notes/new.md", "w") do |post|
    post.puts("---")
    post.puts("layout: note")
    post.puts("title: ")
    post.puts("---")
    post.puts
  end
  sh 'bbedit _notes/new.md'
end

task :github do
    sh 'git push origin master'
end

task :perf do
    sh 'siege -c 20 -t 30S -b example.com'
end

task :styles do
    sh 'sass --watch --style=compressed sass/app.scss:css/app.css'
end

task :tags do
    sh 'git push origin --tags'
end

task :webmentions do
    sh 'npx webmention https://example.com/rss.xml --limit 1 --send'
end
