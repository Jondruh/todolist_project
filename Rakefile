require "rake/testtask"
require "bundler/gem_tasks"

desc 'Say hello'
task :hello do
  puts "Hello there. This is the 'hello' task."
end

desc 'Run tests'
task :default => :test 

Rake::TestTask.new(:test) do |t|
  t.libs << "test"
  t.libs << "lib"
  t.test_files = FileList['test/**/*_test.rb']
end

desc 'List files'
task :files do
  files = FileList.new("**/*") do |fl|
    fl.exclude { |f| !File.file?(f) }
  end

  puts files
end