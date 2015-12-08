require 'rake/clean'

CC = "gcc"

SRCS = FileList["**/*.c"]
OBJS = SRCS.ext('o')

CLEAN.include(OBJS)
CLOBBER.include("make_circle")

task :default => "make_circle"

file "make_circle" => "make_circle.o" do
  sh "#{CC} -o make_circle make_circle.o"
end

file "make_circle.o" => "make_circle.c" do
  sh "#{CC} -c make_circle.c"
end
