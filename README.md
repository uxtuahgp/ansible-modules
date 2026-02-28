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

1. Made a code modifications/additions to:  
* Add parameters path and content  
* Check if file with given path exists  
* Check if file contains the same content as we passed  
* Write file if it's required  
* Set result properties  

### Task 4 ###  
1. Created params.json file to test my module  
```  
{
    "ANSIBLE_MODULE_ARGS": {
        "name": "hello",
        "new": true,
        "path": "/tmp/555",
        "content": "upopabylasobaka"
    }
}

```  

2. Tested module with 3 different cases  
* File exists and have the same content  
* File exists and dont have the same content  
* File does not exists  
```  
(venv) alex@uxtu-note:~/Study/ansible/ansible-modules/ansible$ ls -l /tmp/555
-rw-rw-r-- 1 alex alex 15 фев 28 18:47 /tmp/555
(venv) alex@uxtu-note:~/Study/ansible/ansible-modules/ansible$ cat /tmp/555
upopabylasobaka(venv) alex@uxtu-note:~/Study/ansible/ansible-modules/ansible$ python3 my_own_module.py params.json 

{"changed": false, "original_message": "hello", "message": "The same file content exists", "invocation": {"module_args": {"name": "hello", "new": true, "path": "/tmp/555", "content": "upopabylasobaka"}}}
(venv) alex@uxtu-note:~/Study/ansible/ansible-modules/ansible$ echo nebylosobaki > /tmp/555
(venv) alex@uxtu-note:~/Study/ansible/ansible-modules/ansible$ python3 my_own_module.py params.json 

{"changed": true, "original_message": "hello", "message": "File exists. Updating file with our content", "invocation": {"module_args": {"name": "hello", "new": true, "path": "/tmp/555", "content": "upopabylasobaka"}}}
(venv) alex@uxtu-note:~/Study/ansible/ansible-modules/ansible$ rm /tmp/555
(venv) alex@uxtu-note:~/Study/ansible/ansible-modules/ansible$ python3 my_own_module.py params.json 

{"changed": true, "original_message": "hello", "message": "File does not exists. Creating new file with out content", "invocation": {"module_args": {"name": "hello", "new": true, "path": "/tmp/555", "content": "upopabylasobaka"}}}


```  

### Task 5 ###  
Created playbook 
```  
---
- name: check my_own_module
  hosts: localhost
  tasks: 
  - name: run the module
    my_own_module:
      name: "hello"
      new: true
      path: "/tmp/666"
      content: "ne u popa byla sobaka"
    register: testout
  - name: dump output
    debug:
      msg: '{{ testout }}'

```  

Have set env to run playbook with custom module and tried to test module  
```  
(venv) alex@uxtu-note:~/Study/ansible/ansible-modules$ ANSIBLE_LIBRARY=./ansible/lib:./ansible/

(venv) alex@uxtu-note:~/Study/ansible/ansible-modules$ ansible-playbook ./main.yml 
[WARNING]: No inventory was parsed, only implicit localhost is available
[WARNING]: provided hosts list is empty, only localhost is available. Note that the implicit localhost does not match 'all'

PLAY [check my_own_module] *********************************************************************************************************************************************************************************

TASK [Gathering Facts] *************************************************************************************************************************************************************************************
ok: [localhost]

TASK [run the module] **************************************************************************************************************************************************************************************
changed: [localhost]

TASK [dump output] *****************************************************************************************************************************************************************************************
ok: [localhost] => {
    "msg": {
        "changed": true,
        "failed": false,
        "message": "File does not exists. Creating new file with out content",
        "original_message": "hello"
    }
}

PLAY RECAP *************************************************************************************************************************************************************************************************
localhost                  : ok=3    changed=1    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   

```  

### Task 6 ###  
Have run playbook one more time to test on idempotence
```  
(venv) alex@uxtu-note:~/Study/ansible/ansible-modules$ ansible-playbook ./main.yml 
[WARNING]: No inventory was parsed, only implicit localhost is available
[WARNING]: provided hosts list is empty, only localhost is available. Note that the implicit localhost does not match 'all'

PLAY [check my_own_module] *********************************************************************************************************************************************************************************

TASK [Gathering Facts] *************************************************************************************************************************************************************************************
ok: [localhost]

TASK [run the module] **************************************************************************************************************************************************************************************
ok: [localhost]

TASK [dump output] *****************************************************************************************************************************************************************************************
ok: [localhost] => {
    "msg": {
        "changed": false,
        "failed": false,
        "message": "The same file content exists",
        "original_message": "hello"
    }
}

PLAY RECAP *************************************************************************************************************************************************************************************************
localhost                  : ok=3    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   

```  
### Tasks 7-8 ###  
```  
(venv) alex@uxtu-note:~/Study/ansible/ansible-modules$ deactivate
alex@uxtu-note:~/Study/ansible/ansible-modules$ ansible-galaxy collection init my_own_namespace.yandex_cloud_elk
- Collection my_own_namespace.yandex_cloud_elk was created successfully
```  

### Task 9 ###  
Copied module file into plugins  

### Task 10 ###  
Created role 
```  
alex@uxtu-note:~/Study/ansible/ansible-modules/my_own_namespace/yandex_cloud_elk/roles$ ansible-galaxy role init my_role
- Role my_role was created successfully

```  

### Task 11 ###  
Made a playbook to test role  
```  
---
- name: check my_own_module
  hosts: localhost
  roles:
    - my_role

```  

### Task 12 ###  
Added collection to the repo 
