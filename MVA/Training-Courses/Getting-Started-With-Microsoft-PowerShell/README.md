# Getting Started With Microsoft PowerShell

Windows PowerShell is Microsoft's task automation framework, consisting of a command-line shell and associated scripting language built on top of .NET Framework.

PowerShell provides full access to COM and WMI, enabling administrators to perform administrative tasks on both local and remote Windows systems.
PowerShell has power, depth and flexibility and you can research for yourself, with PowerShell you can create new objects for example, Windows Services File system , DirectoryEntry or the simpler, and .Net Framework based object using fully qualified name like system.DateTime.
PowerShell has ability to use .Net Framework and powershell allows you to build such objects.

Microsoft just kept adding more and more new PowerShell methods to make our life as easy as possible.
Output is always a .NET Object. Please, Remember that PowerShell output is always a .NET object. That output could be a System.Diagnostics.Process a object or System.IO.FileInfo object or a System.String object.
Basically it could be any .NET object whose assembly is loaded into PowerShell including your own .NET objects.

## Don't fear the shell

_The purpose to PowerShell_

* Improved management and automation
* Manage real-time
* Manage large scale

_Admin Developer Model_

Interactive development. Have fun while exploring systems and automation.
No GUIs anymore, nothing wrong using it, however, for automation we need to make things faster.

_cmdlet_

Commands related to PowerShell commands.

_Why not use UNIX commands ?_

UNIX systems are document oriented. And Windows are API oriented.

## Commands

    # List all aliases
    Get-Alias

    # Shows helps
    Get-Help

    # Show how to use a command
    Get-Help Get-Service

    # How to see examples of a specific command
    Get-Help -Examples

    # Show the help in a HTML format
    Get-Help Get-Service -Online

    # Help using wildcards
    Get-Help *service*

    # It show all members (method, property, event, etc) from an object
    dir | Get-Member

    # Record history into a local file
    Start-Transcript

    # All the commands available at PowerShell
    Get-Command

    # Every command must have format: verb-noun
    Get-Command -noun Service    

    #Retrieve all services
    Get-Service     

    # An alias
    cls
    Get-Alias cls

    # All process available
    Get-Process  
    Get-Process -Name MicrosoftEdge

    # Gets all members related to specific object
    Get-Process -Name MicrosoftEdge | Get-Member

    # All properties of an object
    # TIP: Always use the raw data to transfer your information ahead, 'cause another script might use it
    Get-Process -Name MicrosoftEdge | Select-Object *

    # Select multiple properties from an object
    Get-Process -Name MicrosoftEdge | Select-Object ProcessName,SessionId

    # Variables always start with '$' sign
    $zebra = Get-Process MicrosoftEdge    
    $zebra
    $zebra.Name
    $zebra.BasePriority
    $zebra.Kill()

    # Show history for current session
    Get-History  
    Get-History -Examples  
    Get-Help Get-History  

    # Export history to csv format
    Get-Help Get-History | Export-Csv C:\Temp\2017-05-09.csv   
