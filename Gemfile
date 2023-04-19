source "https://rubygems.org"

gemspec

gem 'gettext', '>= 3.1.3', '< 4.0.0'

group :test do
  gem 'rake', '~> 10.1.0'
  gem 'thor'
  gem 'minitest', '~> 5.18'
  gem 'minitest-spec-context'
  gem 'simplecov'
  gem 'mocha', "< 1.14.0"
  gem 'ci_reporter_minitest',  "~> 1.0.0", :require => false

end

# load local gemfile
['Gemfile.local.rb', 'Gemfile.local'].map do |file_name|
  local_gemfile = File.join(File.dirname(__FILE__), file_name)
  self.instance_eval(Bundler.read_file(local_gemfile)) if File.exist?(local_gemfile)
end
