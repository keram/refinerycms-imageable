source 'https://rubygems.org'

gemspec

gem 'refinerycms-i18n', github: 'keram-refinery/refinerycms-i18n', branch: 'refinery_light'
gem 'refinerycms-clientside', '~> 0.0.1', github: 'keram-refinery/refinerycms-clientside', branch: 'master'
gem 'refinerycms-links', '~> 0.0.1', github: 'keram/refinerycms-links', branch: 'master'
gem 'refinerycms-blog2', '~> 1.0.0', github: 'keram/refinerycms-blog2', branch: 'master'

git 'git://github.com/keram-refinery/refinerycms.git', branch: 'refinery_light' do
  gem 'refinerycms'

  group :development, :test do
    gem 'refinerycms-testing'
  end
end

# Database Configuration
platforms :jruby do
  gem 'activerecord-jdbcsqlite3-adapter'
  gem 'activerecord-jdbcmysql-adapter'
  gem 'activerecord-jdbcpostgresql-adapter'
  gem 'jruby-openssl'
end

platforms :ruby do
  gem 'sqlite3'
  gem 'mysql2'
  gem 'pg'
end

# Gems used only for assets and not required
# in production environments by default.
gem 'sass-rails', '~> 4.0.1'
gem 'coffee-rails', '~> 4.0.1'
gem 'uglifier', '~> 2.4.0'

gem 'turbolinks'

gem 'jquery-rails', '~> 3.1.0'
gem 'i18n-iso639matrix', '~> 0.0.1', github: 'keram/i18n-iso639matrix', branch: 'master'


gem 'acts_as_opengraph', '~> 0.0.5'
# Load local gems according to Refinery developer preference.
if File.exist? local_gemfile = File.expand_path('../.gemfile', __FILE__)
  eval File.read(local_gemfile)
end
