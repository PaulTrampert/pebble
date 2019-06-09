Vagrant.configure("2") do |config|
  config.vm.box = "archlinux/archlinux"

  config.vm.provision "shell", inline: "pacman -S --noconfirm python"

  config.vm.provision "ansible", run: "always" do |ansible|
    ansible.playbook = "tests/test.yml"
    ansible.galaxy_role_file = "requirements.yml"
    ansible.galaxy_roles_path = "~"
    ansible.galaxy_command = "sudo ansible-galaxy install --role-file=%{role_file} --roles-path=%{roles_path} --force --keep-scm-meta"
  end
end
