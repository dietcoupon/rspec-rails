source "http://rubygems.org"

%w[rspec rspec-core rspec-expectations rspec-mocks].each do |lib|
  library_path = File.expand_path("../../#{lib}", __FILE__)
  if File.exist?(library_path)
    gem lib, :path => library_path
  else
    gem lib
  end
end

gem "rake", "0.8.7"
gem "cucumber", "0.10.0"
gem "aruba", "0.2.2"
gem "rcov", "0.9.9"
gem "relish", "0.2.0"
gem "guard-rspec", "0.1.9"
gem "growl", "1.0.3"
gem "ZenTest", "~> 4.4.2"

if RUBY_PLATFORM =~ /darwin/
  gem "autotest-fsevent", "~> 0.2.4"
  gem "autotest-growl", "~> 0.2.9"
end

gem "ruby-debug", :platforms => :ruby_18
gem "ruby-debug19", "~> 0.11.6", :platforms => :ruby_19

platforms :ruby_18, :ruby_19 do
  gem "rb-fsevent", "~> 0.3.9"
  gem "ruby-prof", "~> 0.9.2"
end

platforms :jruby do
  gem "jruby-openssl"
end

#### rspec-rails only
gem "rails", :path => File.expand_path("../vendor/rails", __FILE__)
gem "rack", :git => "git://github.com/rack/rack.git"
gem 'webrat', "0.7.2"
gem 'sqlite3-ruby', :require => 'sqlite3'
