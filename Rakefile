require "rake/testtask"

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

desc 'List files (unhidden only)'
task :list_files do
  require 'find'
  Find.find('.') do |file|
    next if file =~ /\/\./ || !File.file?(file)
    puts file.gsub(/^\.\//, '')
  end
end
