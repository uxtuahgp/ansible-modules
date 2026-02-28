## Ansible Modules Homework ##
  

### Pre task 1 ###  
Created repository   
[ansible-modules](https://github.com/uxtuahgp/ansible-modules.git)  

### Pre Task 2 ###  
Got ansible rep from github

### Pre Tasks 3-5 ###  
It does not work with default branch of the ansible repo
SO i've been urged to get specific tag to make it compatible with my ansible version

```  
alex@uxtu-note:~/Study/ansible/ansible-modules/ansible$ git checkout tags/v2.17.14
...
alex@uxtu-note:~/Study/ansible/ansible-modules/ansible$ cd ~/Study/ansible/ansible-modules/ansible  
alex@uxtu-note:~/Study/ansible/ansible-modules/ansible$ python3 -m venv venv  
alex@uxtu-note:~/Study/ansible/ansible-modules/ansible$ . venv/bin/activate  
```  

### Pre Tasks 6-9 ###  
```  
(venv) alex@uxtu-note:~/Study/ansible/ansible-modules/ansible$ pip install -r requirements.txt
Collecting jinja2>=3.1.0
  Downloading jinja2-3.1.6-py3-none-any.whl (134 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 134.9/134.9 KB 1.4 MB/s eta 0:00:00
Collecting PyYAML>=5.1
  Using cached pyyaml-6.0.3-cp310-cp310-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl (770 kB)
Collecting cryptography
  Downloading cryptography-46.0.5-cp38-abi3-manylinux_2_34_x86_64.whl (4.5 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 4.5/4.5 MB 19.2 MB/s eta 0:00:00
Collecting packaging
  Downloading packaging-26.0-py3-none-any.whl (74 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 74.4/74.4 KB 9.2 MB/s eta 0:00:00
Collecting resolvelib<2.0.0,>=0.8.0
  Downloading resolvelib-1.2.1-py3-none-any.whl (18 kB)
Collecting MarkupSafe>=2.0
  Downloading markupsafe-3.0.3-cp310-cp310-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl (20 kB)
Collecting typing-extensions>=4.13.2
  Using cached typing_extensions-4.15.0-py3-none-any.whl (44 kB)
Collecting cffi>=2.0.0
  Downloading cffi-2.0.0-cp310-cp310-manylinux2014_x86_64.manylinux_2_17_x86_64.whl (216 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 216.5/216.5 KB 18.2 MB/s eta 0:00:00
Collecting pycparser
  Downloading pycparser-3.0-py3-none-any.whl (48 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 48.2/48.2 KB 6.9 MB/s eta 0:00:00
Installing collected packages: typing-extensions, resolvelib, PyYAML, pycparser, packaging, MarkupSafe, jinja2, cffi, cryptography
Successfully installed MarkupSafe-3.0.3 PyYAML-6.0.3 cffi-2.0.0 cryptography-46.0.5 jinja2-3.1.6 packaging-26.0 pycparser-3.0 resolvelib-1.2.1 typing-extensions-4.15.0
(venv) alex@uxtu-note:~/Study/ansible/ansible-modules/ansible$ . hacking/env-setup

Setting up Ansible to run out of checkout...

PATH=/home/alex/Study/ansible/ansible-modules/ansible/bin:/home/alex/Study/ansible/ansible-modules/ansible/venv/bin:/home/alex/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/snap/bin
PYTHONPATH=/home/alex/Study/ansible/ansible-modules/ansible/test/lib:/home/alex/Study/ansible/ansible-modules/ansible/lib
MANPATH=/home/alex/Study/ansible/ansible-modules/ansible/docs/man:/home/alex/.local/share/man:/usr/local/man:/usr/local/share/man:/usr/share/man

Remember, you may wish to specify your host file with -i

Done!
(venv) alex@uxtu-note:~/Study/ansible/ansible-modules/ansible$ deactivate
alex@uxtu-note:~/Study/ansible/ansible-modules/ansible$ . venv/bin/activate && . hacking/env-setup

Setting up Ansible to run out of checkout...

PATH=/home/alex/Study/ansible/ansible-modules/ansible/bin:/home/alex/Study/ansible/ansible-modules/ansible/venv/bin:/home/alex/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/snap/bin
PYTHONPATH=/home/alex/Study/ansible/ansible-modules/ansible/test/lib:/home/alex/Study/ansible/ansible-modules/ansible/lib:/home/alex/Study/ansible/ansible-modules/ansible/test/lib:/home/alex/Study/ansible/ansible-modules/ansible/lib
MANPATH=/home/alex/Study/ansible/ansible-modules/ansible/docs/man:/home/alex/.local/share/man:/usr/local/man:/usr/local/share/man:/usr/share/man

Remember, you may wish to specify your host file with -i

Done!


```  

### Tasks 1-2 ###  
Created py file   

### Task 3 ###  


  