QingYu development configurations
================================

*Link pip to pip3
     sudo ln -s /usr/bin/pip3 /usr/bin/pip

*npm registry setting
    npm config set registry https://artifacthub-tip.oraclecorp.com/api/npm/npmjs-remote

*Language setting
    Config file:/edx/etc/lms.yml 
    
    ```
    LANGUAGE_CODE: zh-hans
    ```
    
* Create orgnization 
insert into organizations_organization (created, modified, name, short_name, active) VALUES (NOW(), NOW(), 'QINGYU', 'qy01', 1);

source ../venvs/edxapp/bin/activate
source ../edxapp_env 

paver update_assets lms --settings=production
paver update_assets cms --settings=production


pip install pdfplumber==0.5.22
pip install aliyun-python-sdk-core
pip install edx-django-utils==3.13.0
pip install matplotlib

log path
/edx/var/log/

python -m pip list

git clone https://github.com/rcmachado/mako-pipeline.git
python setup.py install

paver update_assets lms --settings=devstack



git remote set-url origin https://github.com/USERNAME/REPOSITORY.git


python manage.py cms dumpdata pdfexam.MapTestCheckItem > ccss_items_init_data.json
python manage.py cms loaddata ccss_items_init_data.json



