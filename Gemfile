source :rubygems

gem 'daemons'
gem 'anise'

group :pre_config do
  gem 'activesupport', :require => 'active_support'
  gem 'facets'
end

# Only loaded if a database.yml file exists for a season
group :datamapper do
  gem 'do_mysql' # Change this to whatever adapter you need for your database
  gem 'data_objects'
  gem 'dm-core'
end

# load each leaf's gem requirements in its own group
Dir.glob("#{File.dirname __FILE__}/leaves/*/Gemfile").each do |gemfile|
  eval File.read(gemfile)
end

# Season-specific gem requirements:
#
# group :season_name do
#  gem 'my-gem'
# end