通过文件名找文件实体数据块的流程是。
（1）在目录中找到文件名所在的目录项。
（2）从目录项中获取 inode 编号。
（3）用 inode 编号作为 inode 数组的索引下标，找到 inode。
（4）从该 inode 中获取数据块的地址，读取数据块。

在操作系统引导块后面的依次是超级块、空闲块的位图、inode 位图、inode 数组、根目录、空闲块区域。

![截图 2023-08-21 16-45-53](/home/cccmmf/操作系统/操作系统真象还原/mycode/fs/note/screenshot/截图 2023-08-21 16-45-53.png)