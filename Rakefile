namespace :greeting do 
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola from rake'
  task :hola do 
    puts 'hola de Rake!'
  end
end

desc 'starts a console'
task :console do
  system "rake -T"
end

namespace :db do 
  task :environment do
    require_relative './config/environment'
  end

  desc 'migrate changes to your database'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'Loads the seed data from db/seeds.rb'
  task :seed do 
    system "ruby db/seeds.rb"
  end
end

