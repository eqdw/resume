task :default => :all

desc "Upload to nowhere..."
task :upload do
  #system("scp burke_libbey.pdf og:b/files")
end

desc "Commit to git repo"
task :commit do
  system("git add .; git commit -a -m 'Rake auto-commit'; git push")
end

desc "Build PDF"
task :build do
  system("pdflatex ryan_neufeld.tex")
end

task :all => [:build, :commit, :upload]
