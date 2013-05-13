desc 'Build site'
task :build do
  system('jekyll')
end

desc 'Build and deploy'
task :deploy => :build do
  sh 'rsync -rtzh --progress --delete _site/ doozer:~/jekyll/blog.jameschevalier.us'
end

desc 'Run Jekyll with serve --watch --drafts --baseurl /'
task :dev do
  system('jekyll serve --watch --drafts --baseurl /')
end

desc 'Create a new draft post; needs title=TITLE'
task :post do
  title = ENV['title']
  slug = "#{Time.now.strftime('%Y-%m-%d')}-#{title.downcase.gsub(/[^[:alnum:]]+/, '-')}"

  file = File.join(
    File.dirname(__FILE__),
    '_posts',
    slug + '.html'
  )

  File.open(file, "w") do |f|
    f << <<-EOS.gsub(/^    /, '')
    ---
    layout: post
    title: #{title}
    published: false
    tags:
    ---

    EOS
  end

  system ("#{ENV['EDITOR']} #{file} &")
end
