VAGRANT_INSTANCE_NAME   = "vagrantbase"

Vagrant.configure("2") do |config|
  config.vm.box = 'dummy'
  config.vm.box_url = './dummy.box'

  config.vm.hostname = VAGRANT_INSTANCE_NAME
  config.vm.define VAGRANT_INSTANCE_NAME do |d|
  end
  
  config.ssh.private_key_path = '~/.ssh/id_rsa'
  config.ssh.username = 'ansible'

  config.vm.provider :vsphere do |vsphere|
    # The host we're going to connect to
    #vsphere.host = 'vsphere2.mind.unm.edu'                            
    vsphere.host = 'vcenter.mind.unm.edu'                            

   # The host for the new VM
    vsphere.data_center_name = 'MRN'

   # The host for the new VM
    #vsphere.compute_resource_name= 'vsphere2.mind.unm.edu'                            

    # The resource pool for the new VM
    #vsphere.resource_pool_name = ''

    vsphere.clone_from_vm = true
    vsphere.insecure = true

    # The template we're going to clone        
    vsphere.template_name = 'Neuroinformatics/ubuntu1204-ni-ansible-vagrant-template-vm'

    # The name of the new machine
    vsphere.name = VAGRANT_INSTANCE_NAME

    # vSphere login
    vsphere.user = 'changemevsphereuser' 

    # vSphere password
    vsphere.password = :ask
    
    # Datastore for NI machines
    vsphere.data_store_name = 'VNX05'
    
    # Folder for NI
    vsphere.vm_base_path = 'Neuroinformatics'

    # If you don't have SSL configured correctly, set this to 'true'
    vsphere.insecure = true                                    
  end
end
