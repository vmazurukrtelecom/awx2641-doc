## silglefile version of docs


off ver


https://ansible.readthedocs.io/projects/awx/en/24.6.1/


based on copy of files from folder docsite:

https://github.com/ansible/awx/tree/24.6.1/docs/docsite 


howto 

```
python3 -m pip install --upgrade --no-cache-dir pip setuptools
python3 -m pip install --upgrade --no-cache-dir sphinx
#python3 -m pip install --exists-action=w --no-cache-dir -r docs/docsite/requirements.txt
python3 -m pip install --exists-action=w --no-cache-dir -r ./requirements.in

cd /rest_api/
wget https://awx-public-ci-files.s3.amazonaws.com/community-docs/swagger.json

python3 -m sphinx -T -W --keep-going -b singlehtml -d _build/doctrees -D language=en . build1
```

( commands like from  https://app.readthedocs.org/projects/awx-docs/builds/27388302/ )

```

example build result:

https://github.com/vmazurukrtelecom/awx2641-doc/tree/main/build1

