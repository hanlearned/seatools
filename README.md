# seatools

seatools 是一个在 seafile 中下载文件的程序
## 环境准备
```bash
pip install seatools
```

## 使用示例

- 上传文件夹

```python
from seatools.api import FileAPI

upload = FileAPI()
upload.connect(username="hanxuecheng@wealthengine.cn", password="xxxxxxx")

# repo_name: 为 seafile 中的目录名称
repo = upload.create_repo(repo_name="test_hxc1")
repo_id = repo.get("id")
upload.upload_folder(r"F:\wealthengine\Project\gbi_test\upload\quad", repo_id)
```

- 删除目录

```python
from seatools.api import FileAPI

upload = FileAPI()
upload.connect(username="hanxuecheng@wealthengine.cn", password="xxxxxxx")

# repo_name: seafile 中的目录名
upload.delete_folder(repo_name="test_hxc1")
```

- 下载文件

```python
from seatools.api import FileAPI

upload = FileAPI()
upload.connect(username="hanxuecheng@wealthengine.cn", password="xxxxxxx")

# repo_name: seafile 中的文件名 test_hxc1
# to_folder: 存放到本地的目录
upload.download_files(repo_name="test_hxc1", to_folder=r"F:\wealthengine\Project\gbi_test\seatools\tests")
```



Sealoader is a program for downloading files in seafile

## Environmental preparation
```bash
pip install seatools
```

## Use example

- Upload folder

```python
from seatools.api import FileAPI

upload = FileAPI()
upload.connect(username="hanxuecheng@wealthengine.cn", password="xxxxxxx")

# test_hxc1 为 seafile 中的目录名称
repo = upload.create_repo("test_hxc1")
repo_id = repo.get("id")
upload.upload_folder(r"F:\wealthengine\Project\gbi_test\upload\quad", repo_id)
```

- Delete a directory

```python
from seatools.api import FileAPI

upload = FileAPI()
upload.connect(username="hanxuecheng@wealthengine.cn", password="xxxxxxx")

# test_hxc1 为目录名
upload.delete_folder("test_hxc1")
```

- download file

```python
from seatools.api import FileAPI

upload = FileAPI()
upload.connect(username="hanxuecheng@wealthengine.cn", password="xxxxxxx")

upload.download_files("test_hxc1", r"F:\wealthengine\Project\gbi_test\seatools\tests")
```

