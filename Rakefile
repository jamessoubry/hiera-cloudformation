=begin
Copyright 2013-2014 FanDuel Ltd.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

	http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
=end

require 'rubygems'
require 'rubygems/package_task'
require 'rake/testtask'

spec = Gem::Specification.new do |gem|
	gem.name          = "carinadigital-hiera-cloudformation"
	gem.version       = '0.0.2.2'
	gem.authors       = ["carinadigital"]
	gem.email         = ["carinadigital@gmail.com"]
	gem.summary       = %q{Multiregion CloudFormation backend for Hiera}
	gem.description   = %q{Forked from hiera-cloudformation. Multiregion cloudFormation quieries of stack outputs or resource metadata for Hiera.}
	gem.homepage      = "https://github.com/carinadigital/hiera-cloudformation"
	gem.license       = "Apache License (2.0)"

	gem.files         = Dir['{bin,lib,man,test,spec}/**/*', 'Rakefile', 'README*', 'LICENSE*']
	gem.executables   = gem.files.grep(%r{^bin/}) { |f| File.basename(f) }
	gem.test_files    = gem.files.grep(%r{^(test|spec|features)/})
	gem.require_paths = ["lib"]

	gem.add_development_dependency "rake"
	gem.add_runtime_dependency "aws-sdk"
	gem.add_runtime_dependency "timedcache", "~> 0.4.0"
	gem.add_runtime_dependency "json", "~> 1.8.0"
end

Gem::PackageTask.new(spec) do |pkg|
	pkg.need_tar = true
end

Rake::TestTask.new do |t|
  t.pattern = 'test/*_test.rb'
  t.verbose = true
end
