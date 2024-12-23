# GitTips

- [GitTips](#gittips)
  - [版本升级](#版本升级)
  - [指定克隆](#指定克隆)
  - [参考](#参考)


## 版本升级

针对Windows Git 升级

- version <=2.17.1更新命令：

  ```shell
  git update
  ```

- version > 2.17.1更新命令：

  ```
  git update-git-for-windows
  ```

## 指定克隆

有时候，整个项目太大了，我们只想clone项目的某个目录或某个文件

1. 稀疏克隆

   开启Git稀疏克隆，并下载除了具体的文件内容Blob对象之外的其他对象文件，包括tree对象、commit对象、tag对象，以保证git历史记录和项目目录结构的完整性。这样可以实现快速、高效地克隆大型仓库，并节省存储空间。

   ```shell
   git clone --filter=blob:none --sparse <your-git-url>
   ```

2. 指定拉取

   ```shell
   git sparse-checkout add <your-folder>
   ```

   或者

   ```shell
   git sparse-checkout set <your-folder>
   ```

## 参考

[Git只克隆远程仓库的某一个目录或文件](https://blog.csdn.net/qq_58062502/article/details/136511531)

[windows git升级](https://blog.csdn.net/kucoll/article/details/130297768)
