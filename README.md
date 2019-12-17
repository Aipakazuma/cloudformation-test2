https://qiita.com/izanari/items/78258251cced2f713b33

ここを参考にやっているけどできない。。。


できた！！

s3はグローバルなのですでに作成されている場合はバケットを作成できないエラーにハマった....

# example

```sh
$ aws cloudformation deploy --template-file sample.yml --stack-name "stack-003"
```


# samコマンドを試す


https://qiita.com/hf7777hi/items/e68948c948eb303b1900


```sh
$ cd my-app/hello_world/
$ pip install -r requirements.txt -t build/ 
$ cp hello_world/*.py build/

# confirm local command lambda
$ sam local invoke -e events/event.json

# confirm local lambda
$ sam local start-lambda

# delpy
$ sam package --template-file template.yaml --output-template-file packaged.yaml --s3-bucket automatic.classification.illegal.av
$ sam deploy --template-file packaged.yaml --stack-name my-app --capabilities CAPABILITY_IAM --region us-west-2
```
