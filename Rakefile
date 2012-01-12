task :default => :all

desc "Upload to nowhere..."
task :upload do
  system("scp eqdw.pdf eqdw.net:resume.pdf")
end

desc "Commit to git repo"
task :commit do
  system("git add .; git commit -a -m 'Rake auto-commit'; git push")
end

desc "Build PDF"
task :build do
  system("rm eqdw.pdf")
  system("pdflatex eqdw.tex")
end

task :all => [:build, :commit, :upload]
