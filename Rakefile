task :default => [:dev]

task :dev=> [:clean] do |t|
    puts 'Serving development site'
    sh 'JEKYLL_ENV=development bundle exec jekyll serve --livereload'
end

task :prod => [:clean] do |t|
    puts 'Serving production site'
    sh 'JEKYLL_ENV=production bundle exec jekyll serve --livereload'
end

# Maintenance tasks
task :clean do
    puts 'Cleaning Jekyll files'
    sh 'bundle exec jekyll clean'
end

task :imageoptim => [:clean] do |t|
    puts 'Crunch site images using image_optim'
    sh 'image_optim -r . --verbose'
end
