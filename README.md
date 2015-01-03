## Usage

1. Modify VAGRANT_INSTANCE_NAME in Vagrantfile to be the name of the new server
2. Modify vagrant file: vsphere.user to be a user with the proper permissions
3. Run `vagrant up --provider=vsphere`

## Requirements

1. vagrant
2. vagrant-vsphere plugin

## Requirement setup
1. Install vagrant:
`wget https://dl.bintray.com/mitchellh/vagrant/vagrant_1.7.1_x86_64.deb
dpkg -i vagrant_1.7.1_x86_64.deb'
2. Install latest ruby: 
```
sudo apt-get install ruby1.9.1 ruby1.9.1-dev \
  rubygems1.9.1 irb1.9.1 ri1.9.1 rdoc1.9.1 \
  build-essential libopenssl-ruby1.9.1 libssl-dev zlib1g-dev
sudo update-alternatives --install /usr/bin/ruby ruby /usr/bin/ruby1.9.1 400 \
         --slave   /usr/share/man/man1/ruby.1.gz ruby.1.gz \
                        /usr/share/man/man1/ruby1.9.1.1.gz \
        --slave   /usr/bin/ri ri /usr/bin/ri1.9.1 \
        --slave   /usr/bin/irb irb /usr/bin/irb1.9.1 \
        --slave   /usr/bin/rdoc rdoc /usr/bin/rdoc1.9.1
sudo update-alternatives --config ruby
sudo update-alternatives --config gem
```
3. Install vmware vagrant dependency:
`sudo gem install nokogiri`
4. Install vmware vagrant plugin: 
`sudo vagrant plugin install vagrant-vsphere`

