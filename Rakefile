task :build do
  system "bundle exec middleman build"
end

task :serve do
  system "bundle exec middleman"
end

task :deploy do
  system "git add docs"
  system "git commit -m \"New Site\""
  system "git push -u"
end
