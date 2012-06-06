require 'rubygems'
require 'rake'

desc 'Default: run unit tests'
task :default => :test

begin
  require 'rspec'
  require 'rspec/core/rake_task'
  desc 'Run the unit tests'
  RSpec::Core::RakeTask.new(:test)
rescue LoadError
  task :test do
    raise "You must have rspec 2.0 installed to run the tests"
  end
end

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    gem.name = "super_awesome_resource_serializer"
    gem.summary = %Q{Quickly create custom serializations for resources}
    gem.description = %Q{Quickly create custom serializations for resources rather than relying on the generated ones.}
    gem.authors = ["Brian Durand"]
    gem.email = ["mdobrota@tribune.com", "bdurand@tribune.com"]
    gem.files = FileList["lib/**/*", "spec/**/*", "README.rdoc", "Rakefile", "License.txt"].to_a
    gem.has_rdoc = true
    gem.rdoc_options << '--line-numbers' << '--inline-source' << '--main' << 'README.rdoc'
    gem.extra_rdoc_files = ["README.rdoc"]
    gem.add_dependency('activesupport')
    gem.add_development_dependency('rspec', '>= 2.0.0')
  end
rescue LoadError
end
