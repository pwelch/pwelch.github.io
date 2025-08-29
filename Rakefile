# frozen_string_literal: true

desc 'Build the Jekyll site'
task :build do
  sh 'bundle exec jekyll build'
  puts 'build available in ./_site'
end

desc 'Run the Jekyll site locally'
task :serve do
  sh 'bundle exec jekyll serve'
end

desc 'Copy _site contents to root directory'
task :stage do
  sh 'cp -r _site/* .'
end

desc 'Clean up the _site directory'
task :clean do
  sh 'rm -rf _site' if Dir.exist?('_site')
  sh 'rm index.html' if File.exist?('index.htm')
end

desc 'Show available rake tasks'
task :default do
  sh 'rake -T'
end
