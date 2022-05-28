### step1 复制文档到linux中
### step2 提取相关的文字信息
```shell
cat 123 |while read id; do egrep "smoker"|awk '{print $2 ","}';done
```
### step3 行数转到R中
```R
dat1=as.data.frame(1:40) ####一共生成多少行
dat2=c(9,
       11,
       13,
       18,
       19,
       20,
       26,
       30,
       35,
       37,
       39)
dat1$hy=0
dat1[dat2,]=1

writexl::write_xlsx(dat1,"haha.xlsx")
```
