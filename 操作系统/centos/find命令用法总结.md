# 如何删除某个目录下面扩展名为 .php文件？
`find ./ -name *.php |xargs rm -f`
# 查找以.php为扩展的文件中带有 "eval字符"件文件
 find /var/www/quanjingke.com/snsv2/ -name "*.php" | xargs grep "eval" >saomiao.txt
# 查找今天创建的扩展名是.php的文件
find ./ -ctime 0 -name "*.php"
# 查找今天被修改的文件
find ./ -mtime 0
#查找最近30分钟修改的当前目录下的.php文件

find . -name '*.php' -mmin -30
# 按照字节查找
find   /home   -size   +512k                查大于512k的文件
find   /home   -size   -512k               查小于512k的文件