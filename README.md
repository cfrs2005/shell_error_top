#  常见SHELL错误 ,那些年爬过的坑

本文来自 chinaunix活动:
http://bbs.chinaunix.net/thread-4260917-1-1.html

看着蛮感兴趣的,而且shell坑确实很多,神烦

原文地址: http://mywiki.wooledge.org/BashPitfalls





- [for i in $(ls *.mp3)](docs/1.md)
```
cp $file $target
Filenames with leading dashes
[ $foo = "bar" ]
cd $(dirname "$f")
[ "$foo" = bar && "$bar" = foo ]
[[ $foo > 7 ]]
grep foo bar | while read -r; do ((count++)); done
if [grep foo myfile]
if [bar="$foo"]; then ...
if [ [ a = b ] && [ c = d ] ]; then ...
read $foo
cat file | sed s/foo/bar/ > file
echo $foo
$foo=bar
foo = bar
echo <<EOF
su -c 'some command'
cd /foo; bar
[ bar == "$foo" ]
for i in {1..10}; do ./something &; done
cmd1 && cmd2 || cmd3
echo "Hello World!"
for arg in $*
function foo()
echo "~"
local varname=$(command)
export foo=~/bar
sed 's/$foo/good bye/'
tr [A-Z] [a-z]
ps ax | grep gedit
printf "$foo"
for i in {1..$n}
if [[ $foo = $bar ]] (depending on intent)
if [[ $foo =~ 'some RE' ]]
[ -n $foo ] or [ -z $foo ]
[[ -e "$broken_symlink" ]] returns 1 even though $broken_symlink exists
ed file <<<"g/d\{0,3\}/s//e/g" fails
expr sub-string fails for "match"
On UTF-8 and Byte-Order Marks (BOM)
content=$(<file)
for file in ./* ; do if [[ $file != *.* ]]
somecmd 2>&1 >>logfile
cmd; (( ! $? )) || die
y=$(( array[$x] ))
read num; echo $((num+1))
IFS=, read -ra fields <<< "$csv_line"
export CDPATH=.:~/myProject
OIFS="$IFS"; ...; IFS="$OIFS"
hosts=( $(aws ...) )
```