
task default: [:build]

task :build do
    sh 'bundle exec jekyll build --incremental'
end

task :doctor do
    sh 'bundle exec jekyll doctor'
end

task :draft do

File.open("_drafts/new.md", "w") do |post|
      post.puts("---")
      post.puts("layout: post")
      post.puts("title: ")
      post.puts("---")
      post.puts
    end
end

task :github do
    sh 'git push origin master'
end

task :perf do
    sh 'siege -c 20 -t 30S -b example.com'
end

task :styles do
    sh 'sass --sourcemap=none --watch scss:css'
end

task :tags do
    sh 'git push origin --tags'
end

task :webmentions do
    sh 'npx webmention https://chrisfinazzo.com/rss.xml --limit 1 --send'
end
