# s3-cfn-samples

## ①デフォルトのS3を作成するテンプレート
引数： バケット名

```console
$ aws cloudformation deploy --template-file s3-default.yml \
--stack-name demo-s3-default --parameter-overrides \
S3BucketName=kento-demo-s3-backet
```



## ②アプリケーションからのアクセスを許可したS3を作成するテンプレート

引数： バケット名

```console
$ aws cloudformation deploy --template-file s3-web-access.yml \
--stack-name demo-s3-web-access --parameter-overrides \
S3BucketName=kento-demo-s3-backet
```

![s3-web-access](/Users/kento/Programing/AutomationProjects/s3-cfn-samples/images/s3-web-access.png)





## ③ファイルのバージョニング用のS3を作成するテンプレート

30日でGlacierに保存される
引数１： バケット名
引数２： タグ名

```console
$ aws cloudformation deploy --template-file s3-versioning.yml \
--stack-name demo-s3-versioning --parameter-overrides \
S3BucketName=kento-demo-s3-backet　NameTagPrefix=ProjectAA
```



![s3-versioning-1](/Users/kento/Programing/AutomationProjects/s3-cfn-samples/images/s3-versioning-1.png)



![s3-versioning-2](/Users/kento/Programing/AutomationProjects/s3-cfn-samples/images/s3-versioning-2.png)



![s3-versioning-3](/Users/kento/Programing/AutomationProjects/s3-cfn-samples/images/s3-versioning-3.png)

