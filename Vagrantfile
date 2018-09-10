# Usage: IE={box} vagrant up
#
# Eg. IE=ie6.xp vagrant up

boxes = {
    "ie6.xp"       => "http://aka.ms/ie6.xp.vagrant",
    "ie7.vista"    => "http://aka.ms/ie7.vista.vagrant",
    "ie8.xp"       => "http://aka.ms/ie8.xp.vagrant",
    "ie8.win7"     => "http://aka.ms/ie8.win7.vagrant",
    "ie9.win7"     => "http://aka.ms/ie9.win7.vagrant",
    "ie10.win7"    => "http://aka.ms/ie10.win7.vagrant",
    "ie10.win8"    => "http://aka.ms/ie10.win8.vagrant",
    "ie11.win7"    => "http://aka.ms/ie11.win7.vagrant",
    "ie11.win81"   => "http://aka.ms/ie11.win81.vagrant",
    "msedge.win10" => "http://aka.ms/msedge.win10.vagrant",
}

unless boxes.has_key? ENV['IE']
    abort('Invalid box supplied')
end

Vagrant.configure("2") do |config|
    config.vm.box = ENV['IE']
    config.vm.box_url = boxes[ ENV['IE'] ]
    config.vm.guest = :windows
    config.vm.boot_timeout = 1
    config.vm.communicator = "winrm"
    config.vm.provider "virtualbox" do |vm|
        vm.gui = true
    end
end

