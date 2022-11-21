### makecab和expand

```cmd
makecab e:/test.txt e:/test.zip
expand e:/test.zip e:/test.txt

dir /b >>name.txt
makecab /f name.txt
expand 1.cab -f:* c:\test\
```

## 分块压缩

7z的分块压缩命令

```bash
7z a name.7z filename -v10m
```

tar的分块压缩

```cmd
tar cjf - filename |split -b 10m - filename.tar.bz2.
```

zip的分卷压缩

```cmd
zip - largefile | split -b 1024k
```

rar的分卷压缩

```cmd
rar a -v10m filename.rar filename
```

### Powershell

```powershell
powershell "Compress-Archive -Path c:\temp\adtemp\ -DestinationPath c:\temp\addc.zip"
```

### 计算文件夹大小

```powershell
#pwsh下执行
Get-ChildItem -Path C:\temp -Recurse | Measure-Object -Sum Length

#cmd下执行
powershell -noprofile -command "'{0:N0}' -f (ls C:\temp -r | measure -s Length).Sum"
```
