#!/usr/bin/env rake
# Add your own tasks in files placed in lib/tasks ending in .rake,
# for example lib/tasks/capistrano.rake, and they will automatically be available to Rake.

require File.expand_path('../config/application', __FILE__)

Obtvse::Application.load_tasks

desc 'clear old sessions'
task :clear_old_sessions => :environment
  ActiveRecord::Base.connection.execute("DELETE FROM sessions WHERE updated_at < #{1.day.ago.to_s}")  
end
