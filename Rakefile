require 'rake'
require 'rake/testtask'
require 'rake/rdoctask'
require 'rubygems'
require 'yard'

require 'jeweler'
Jeweler::Tasks.new do |gem|
  # gem is a Gem::Specification... see http://docs.rubygems.org/read/chapter/20 for more options
  gem.name = "xeroizer"
  gem.homepage = "http://github.com/waynerobinson/xeroizer"
  gem.license = "MIT"
  gem.summary = %Q{Xero library}
  gem.description = %Q{Ruby library for the Xero accounting system API.}
  gem.email = "wayne.robinson@gmail.com"
  gem.authors = ["Wayne Robinson"]
  gem.add_runtime_dependency 'builder', '>= 2.1.2'
  gem.add_runtime_dependency 'oauth',   '>= 0.3.6'
  gem.add_runtime_dependency 'activesupport'
  gem.add_runtime_dependency 'nokogiri'
  gem.add_development_dependency 'mocha'
  gem.add_development_dependency 'shoulda'
end
Jeweler::RubygemsDotOrgTasks.new

desc 'Default: run unit tests.'
task :default => :test

desc 'Test the xero gateway.'
Rake::TestTask.new(:test) do |t|
  t.libs << 'lib'
  t.pattern = 'test/**/*_test.rb'
  t.verbose = true
end

YARD::Rake::YardocTask.new do |t|
  # t.files   = ['lib/**/*.rb', OTHER_PATHS]   # optional
  # t.options = ['--any', '--extra', '--opts'] # optional
end