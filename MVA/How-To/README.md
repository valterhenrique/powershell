# How-To

## How to Install the Hyper-V PowerShell Module

1. ist all features name "hyper-v" in Windows 10:

    Get-WindowsOptionalFeature -Online -FeatureName *hyper-v* | select DisplayName, FeatureName


2. Install the entire Hyper-V stack (hypervisor, services, and tools)

    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V-All

[Reference](http://www.altaro.com/hyper-v/install-hyper-v-powershell-module/)