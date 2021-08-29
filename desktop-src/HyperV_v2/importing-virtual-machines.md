---
description: L’exemple C# suivant montre comment utiliser la méthode MigrateVirtualSystemToHost pour effectuer une migration simple d’un ordinateur virtuel.
ms.assetid: A3E4AAA2-3AE6-4D7D-8D7B-1ED367D398C0
title: Migration d’ordinateurs virtuels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9be4bb1fee9628bcd5aa5cd1f787372bc8bb32191a42529a56db786a2e836866
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118392452"
---
# <a name="migrating-virtual-machines"></a>Migration d’ordinateurs virtuels

L’exemple C# suivant montre comment utiliser la méthode [**MigrateVirtualSystemToHost**](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md) pour effectuer une migration simple d’un ordinateur virtuel. Cet exemple utilise des pools de ressources pour obtenir les chemins d’accès de disque dur virtuel corrects. Ce code est extrait de l' [exemple de migration d’ordinateur virtuel Hyper-V](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Hyper-V%20virtual%20machine%20migration%20sample).

La syntaxe de la ligne de commande pour exécuter cet exemple est la suivante :

**MigrationSamples.exe VM-and-Storage-simple** *SourceHost* *DestinationHost* *VmName*

où les paramètres sont les suivants :

-   *SourceHost* est le nom de l’hôte actuel de la machine virtuelle.
-   *DestinationHost* est le nom de l’hôte de destination.
-   *VmName* est le nom de l’ordinateur virtuel.


```CSharp
/// <summary>
/// Migrates a VM without any modification, using all defaults.
/// Resource pools will be used to get correct path for the VHDs.
/// </summary>
/// <param name="sourceHost">Migration source hostname</param>
/// <param name="destinationHost">
/// Migration destination hostname
/// </param>
/// <param name="vmName">VM name.</param>
public
void
VmAndStorageMigrationSimple(
    string sourceHost,
    string destinationHost,
    string vmName
    )
{
    ManagementScope srcScope = new ManagementScope(
        @"\\" + sourceHost + @"\root\virtualization\v2", null);

    using (ManagementObject migrationSettingData = GetMigrationSettingData(srcScope))
    using (ManagementObject vm = WmiUtilities.GetVirtualMachine(vmName, srcScope))
    {
        migrationSettingData["MigrationType"] = MigrationType.VirtualSystemAndStorage;
        migrationSettingData["TransportType"] = TransportType.TCP;

        // Get the VHD SASDs
        string[] sasds = null;
        ManagementObject[] vhdList = WmiUtilities.GetVhdSettings(vm);
        if (vhdList != null)
        {
            sasds = new string[vhdList.Length];

            for (uint index = 0; index < vhdList.Length; ++index)
            {
                using (ManagementObject vhd = vhdList[index])
                {
                    // Change the VHD path to an empty string which will force
                    // the system to use resource pools to get the right path at
                    // the destination node.
                    vhd["HostResource"] = new string[] { "" };

                    // Create array of embedded instances.
                    sasds[index] = vhd.GetText(TextFormat.CimDtd20);
                }
            }
        }
        else
        {
            Console.WriteLine("No VHDs found associated with the VM. Skipping VHDs...");
        }

        // Perform migration.
        Console.WriteLine("Performing migration...");
        Migrate(srcScope,
            vmName,
            destinationHost,
            migrationSettingData.GetText(TextFormat.CimDtd20),
            null,
            sasds);
    }
}
```



Le code C# suivant contient l’implémentation de la plupart des méthodes utilitaires appelées à partir de l’exemple ci-dessus.


```CSharp
class MigrationCommon
{
    ///////////////////////////////////////////////////////////////////////
    // Common values and methods for all migration types.
    ///////////////////////////////////////////////////////////////////////

    /// <summary>
    /// Defines the migration types.
    /// </summary>
    public enum MigrationType
    {
        VirtualSystem = 32768,
        Storage = 32769,
        Staged = 32770,
        VirtualSystemAndStorage = 32771
    };

    /// <summary>
    /// Defines migration transport types.
    /// </summary>
    public enum TransportType
    {
        TCP = 5
    };

    /// <summary>
    /// Gets the virtual system migration service.
    /// </summary>
    /// <param name="scope">The scope to use when connecting to WMI.</param>
    /// <returns>The virtual system migration service.</returns>
    public
    ManagementObject
    GetVirtualMachineMigrationService(
        ManagementScope scope)
    {
        using (ManagementClass migrationServiceClass = new ManagementClass("Msvm_VirtualSystemMigrationService"))
        {
            migrationServiceClass.Scope = scope;

            ManagementObject migrationService =
                WmiUtilities.GetFirstObjectFromCollection(migrationServiceClass.GetInstances());

            return migrationService;
        }
    }

    /// <summary>
    /// Returns the instance of
    /// Msvm_VirtualSystemMigrationServiceSettingData
    /// associated with the service.
    /// </summary>
    /// <param name="service">Migration service instance</param>
    /// <returns>
    /// Instance of Msvm_VirtualSystemMigrationServiceSettingData
    /// </returns>
    public
    ManagementObject
    GetMigrationServiceSettings(
        ManagementObject service
        )
    {
        ManagementObject serviceSetting = null;
        using (ManagementObjectCollection settingCollection =
            service.GetRelated("Msvm_VirtualSystemMigrationServiceSettingData"))
        {
            foreach (ManagementObject mgmtObj in settingCollection)
            {
                serviceSetting = mgmtObj;
                break;
            }
        }

        return serviceSetting;
    }

    /// <summary>
    /// Retuns the migration setting data object to be used for
    /// migration.
    /// </summary>
    /// <param name="scope">The namespace to be used.</param>
    /// <returns>Migration setting data object</returns>
    public
    ManagementObject
    GetMigrationSettingData(
        ManagementScope scope
        )
    {
        ManagementObject migrationSettingData = null;
        ManagementPath settingPath =
            new ManagementPath("Msvm_VirtualSystemMigrationSettingData");

        using (ManagementClass migrationSettingDataClass = new ManagementClass(scope, settingPath, null))
        {
            migrationSettingData = migrationSettingDataClass.CreateInstance();
        }

        return migrationSettingData;
    }

    /// <summary>
    /// Performs the migration.
    /// </summary>
    /// <param name="scope">The namespace to be used.</param>
    /// <param name="vmName">The virtual machine name.</param>
    /// <param name="destinationHost">Migration destination host</param>
    /// <param name="migrationSetting">Embedded instance of
    /// Msvm_VirtualSystemMigrationSettingData.</param>
    /// <param name="vssd">Embedded instance of
    /// Msvm_VirtualSystemSettingData.</param>
    /// <param name="rasds">Array of embedded instances of
    /// Msvm_ResourceAllocationSettingData.</param>
    public
    void
    Migrate(
        ManagementScope scope,
        string vmName,
        string destinationHost,
        string migrationSetting,
        string vssd,
        string[] rasds
        )
    {
        using (ManagementObject service = GetVirtualMachineMigrationService(scope))
        using (ManagementBaseObject inParams = service.GetMethodParameters("MigrateVirtualSystemToHost"))
        using (ManagementObject vm = WmiUtilities.GetVirtualMachine(vmName, scope))
        {
            inParams["ComputerSystem"] = vm.Path.Path;
            inParams["DestinationHost"] = destinationHost;
            inParams["MigrationSettingData"] = migrationSetting;
            inParams["NewSystemSettingData"] = vssd;
            inParams["NewResourceSettingData"] = rasds;

            using (ManagementBaseObject outParams =
                service.InvokeMethod("MigrateVirtualSystemToHost", inParams, null))
            {
                WmiUtilities.ValidateOutput(outParams, scope);
            }
        }
    }

    /// <summary>
    /// Performs migratability check.
    /// </summary>
    /// <param name="scope">The namespace to be used.</param>
    /// <param name="vmName">The virtual machine name.</param>
    /// <param name="destinationHost">Migration destination host</param>
    /// <param name="migrationSetting">Embedded instance of
    /// Msvm_VirtualSystemMigrationSettingData.</param>
    /// <param name="vssd">Embedded instance of
    /// Msvm_VirtualSystemSettingData.</param>
    /// <param name="rasds">Array of embedded instances of
    /// Msvm_ResourceAllocationSettingData.</param>
    /// <returns>true if virtual machine is migratable, false otherwise</returns>
    public
    bool
    CheckMigratability(
        ManagementScope scope,
        string vmName,
        string destinationHost,
        string migrationSetting,
        string vssd,
        string[] rasds
        )
    {
        using (ManagementObject service = GetVirtualMachineMigrationService(scope))
        using (ManagementBaseObject inParams =
            service.GetMethodParameters("MigrateVirtualSystemToHost"))
        using (ManagementObject vm = WmiUtilities.GetVirtualMachine(vmName, scope))
        {
            inParams["ComputerSystem"] = vm.Path.Path;
            inParams["DestinationHost"] = destinationHost;
            inParams["MigrationSettingData"] = migrationSetting;
            inParams["NewSystemSettingData"] = vssd;
            inParams["NewResourceSettingData"] = rasds;

            using (ManagementBaseObject outParams =
                service.InvokeMethod("CheckVirtualSystemIsMigratable", inParams, null))
            {
                return WmiUtilities.ValidateOutput(outParams, scope, false, true);
            }
        }
    }

    /// <summary>
    /// Returns array of IP addresses on which the migration destination
    /// host is listening for incoming VM migration request.
    /// </summary>
    /// <param name="destinationHost">
    /// Migration destination hostname
    /// </param>
    /// <returns>Listening IP addresses</returns>
    public
    string[]
    GetMigrationDestinationListenAddresses(
        string destinationHost
        )
    {
        string[] ipAddresses = null;

        ManagementScope scope = new ManagementScope(
            @"\\" + destinationHost + @"\root\virtualization\v2", null);

        using (ManagementObject service = GetVirtualMachineMigrationService(scope))
        using (ManagementObject serviceSetting = GetMigrationServiceSettings(service))
        {
            if (!((bool)serviceSetting["EnableVirtualSystemMigration"]))
            {
                throw new Exception("Destination host does not " +
                    "allow VM migration");
            }

            ipAddresses =
                (string[])service["MigrationServiceListenerIPAddressList"];
            if (ipAddresses == null)
            {
                throw new Exception("Destination host does not have " +
                    "networks set for VM migration");
            }
        }

        return ipAddresses;
    }
}
```



 

 



