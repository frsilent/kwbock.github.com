namespace :jekyll do
  desc 'Delete generated _site files'
  task :clean do
    system 'rm -rf _site'
  end
  
  desc 'Run the jekyll dev server'
  task :server do
    system "jekyll --server --auto"
  end

end

namespace :blog do 
  desc 'Generate a new blog post'
  task :post do |t, args|
    unless ENV['title']
      puts "USAGE: rake blog:post title=<TITLE>"
      next
    end

    title = ENV['title']
    comments = ENV['comments']

    new_post_file = %W{#{Time.now.strftime("%Y-%m-%d")} #{title.downcase.gsub(" ","-")}}.join("-")
    File.open("_posts/#{new_post_file}.md", 'w') do |f|
      f.puts "---"
      f.puts "layout: post"
      f.puts "title: #{title}"
      f.puts "comments: true"
      f.puts "---"
    end
  end
end