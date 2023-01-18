PRIVATE_KEY_PATH = "~/.ssh/id_rsa"

Vagrant.configure("2") do |config|
  config.vm.define "droplet1" do |droplet|
    droplet.vm.provider :digital_ocean do |provider, override|
      override.ssh.private_key_path = PRIVATE_KEY_PATH
      override.vm.box = 'digital_ocean'
      override.vm.box_url = DO_BOX_URL
      override.nfs.functional = false
      override.vm.allowed_synced_folder_types = :rsync
      provider.token = TOKEN
      provider.image = 'rockylinux-8-4-x64'
      provider.region = 'lon1'
      provider.size = 's-1vcpu-1gb'
    end
  end
end
