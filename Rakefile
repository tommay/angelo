require 'rake/testtask'

Rake::TestTask.new do |t|
  if ENV['TEST_PATTERN']
    t.pattern = ENV['TEST_PATTERN']
  else
    t.test_files = Dir['test/angelo_spec.rb', 'test/angelo/**/*_spec.rb']
  end
end

namespace :test do
  desc 'run "main" tests'
  Rake::TestTask.new :main do |t|
    t.pattern = 'test/main/**/*_spec.rb'
  end
end


task :default => :test
