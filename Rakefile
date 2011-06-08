require 'rake'
require 'rubygems'
require 'fileutils'
require "rake/testtask"
require 'rubygems/package_task'
include FileUtils

spec = Gem::Specification.new do |s|
  s.platform = Gem::Platform::RUBY
  s.name = "yahoo-finance"
  s.version = "0.0.2"
  s.author = "Herval Freire"
  s.email = "herval@hervalicio.us"
  s.homepage = "http://hervalicio.us/blog"
  s.platform = Gem::Platform::RUBY
  s.summary = "A wrapper to Yahoo! Finance market data (quotes and exchange rates) feed"
  s.files = FileList["{bin,lib}/**/*"].to_a
  s.require_path = "lib"
  s.autorequire = "yahoo_finance"
  s.has_rdoc = false
  s.extra_rdoc_files = ["README", "HISTORY"]
end

Rake::TestTask.new do |t|
  t.libs << "lib"
  t.test_files = Dir["test/**/*_test.rb"]
end
Gem::PackageTask.new(spec) do |pkg|
    pkg.need_zip = true
    pkg.need_tar = false
end

