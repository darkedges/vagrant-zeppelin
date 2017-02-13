# vagrant-zeppelin

This project is based heavily on the work done over at [http://arjon.es/2015/08/23/vagrant-spark-zeppelin-a-toolbox-to-the-data-analyst/](http://arjon.es/2015/08/23/vagrant-spark-zeppelin-a-toolbox-to-the-data-analyst/)
and has been updated to work on the latest version of Zeppelin.

## Installation

```bash
git clone https://github.com/darkedges/vagrant-zeppelin.git
cd vagrant-zeppelin
vagrant up
ansible-galaxy install -r ansible/requirements.yml
ansible-playbook -i ansible/inventory ansible/deployZeppelin.yml
```

## Usage

Once completed open a web browser to [http://zeppelin.local.darkedges.com:8080/#/notebook/2AYDJMVVQ](http://zeppelin.local.darkedges.com:8080/#/notebook/2AYDJMVVQ) to start working on the Star Wars Kid Data Dump 
[http://waxy.org/2008/05/star_wars_kid_the_data_dump/](http://waxy.org/2008/05/star_wars_kid_the_data_dump/)
