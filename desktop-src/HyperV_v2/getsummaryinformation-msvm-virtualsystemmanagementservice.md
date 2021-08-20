---
description: Retourne les informations de résumé de la machine virtuelle.
ms.assetid: CDDC2B5A-8172-4E6D-A206-CEAB9E54C69A
title: Méthode GetSummaryInformation de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetSummaryInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: efa879cd3da0f5e8a4cc8cf1e9873390c94a94bae0eef3dd8d36c59c9e1680e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253649"
---
# <a name="getsummaryinformation-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Méthode GetSummaryInformation de la \_ classe VirtualSystemManagementService MSVM

Retourne les informations de résumé de la machine virtuelle.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetSummaryInformation(
  [in]  CIM_VirtualSystemSettingData REF SettingData[],
  [in]  uint32                           RequestedInformation[],
  [out] Msvm_SummaryInformationBase      SummaryInformation[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SettingData* \[ dans\]
</dt> <dd>

Type : **CIM \_ VirtualSystemSettingData \[ \]**

Tableau d’instances [**de \_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)) qui spécifient les ordinateurs virtuels ou les captures instantanées dont les informations doivent être récupérées. Si ce paramètre a la **valeur null**, les informations de toutes les machines virtuelles sont récupérées.

</dd> <dt>

*RequestedInformation* \[ dans\]
</dt> <dd>

Type : **UInt32 \[ \]**

Tableau de valeurs d’énumération, qui correspondent aux propriétés de la classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) , qui spécifient les données à récupérer pour les machines virtuelles et les instantanés spécifiés dans le tableau *SettingData* .

<dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nom** (0)


</dt> <dd>

Cela correspond à la propriété **Name** de la classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>

<span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>**Nom** de l’élément (1)


</dt> <dd>

Cela correspond à la propriété **ElementName** de la classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>

<span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>**Heure de création** (2)


</dt> <dd>

Cela correspond à la propriété **CreationTime** de la classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>

<span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>**Remarques** (3)


</dt> <dd>

Cela correspond à la propriété **Notes** de la classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>

<span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>**Nombre de processeurs** (4)


</dt> <dd>

Cela correspond à la propriété **NumberOfProcessors** de la classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>

<span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>**Petite image miniature (80x60)** (5)


</dt> <dd>

Cela correspond à la propriété **ThumbnailImage** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) . Une image miniature avec les dimensions 80 60 sera récupérée.

</dd> <dt>

<span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>

<span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>**Image miniature moyenne (160x120)** (6)


</dt> <dd>

Cela correspond à la propriété **ThumbnailImage** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) . Une image miniature avec les dimensions 160 120 sera récupérée.

</dd> <dt>

<span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>

<span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>**Grande image miniature (320x240)** (7)


</dt> <dd>

Cela correspond à la propriété **ThumbnailImage** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) . Une image miniature avec les dimensions 320 240 sera récupérée.

</dd> <dt>

<span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>

<span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>**AllocatedGPU** (8)


</dt> <dd>

Cela correspond à la propriété **AllocatedGPU** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>

<span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>**VirtualSwitchNames** (9)


</dt> <dd></dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version** (10)


</dt> <dd>

> [!Note]  
> ajouté dans Windows 10 et Windows Server 2016.

 

</dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Protégé** (11)


</dt> <dd>

> [!Note]  
> ajouté dans Windows 10, version 1703 et Windows Server 2016.

 

</dd> <dt>

<span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>

<span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>**EnabledState** (100)


</dt> <dd>

Cela correspond à la propriété **EnabledState** de la classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>

<span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>**ProcessorLoad** (101)


</dt> <dd>

Cela correspond à la propriété **ProcessorLoad** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>

<span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>**ProcessorLoadHistory** (102)


</dt> <dd>

Cela correspond à la propriété **ProcessorLoadHistory** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>

<span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>**MemoryUsage** (103)


</dt> <dd>

Cela correspond à la propriété **MemoryUsage** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>

<span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>**Pulsation** (104)


</dt> <dd>

Cela correspond à la propriété **Heartbeat** de la classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>

<span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>**Temps d’activité** (105)


</dt> <dd>

Cela correspond à la propriété **Uptime** de la classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>

<span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>**GuestOperatingSystem** (106)


</dt> <dd>

Cela correspond à la propriété **GuestOperatingSystem** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>

<span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>**Instantanés** (107)


</dt> <dd>

Cela correspond à la propriété d' **instantanés** de la classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>

<span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>**AsynchronousTasks** (108)


</dt> <dd>

Cela correspond à la propriété **AsynchronousTasks** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>

<span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>**HealthState** (109)


</dt> <dd>

Cela correspond à la propriété **HealthState** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>

<span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>**OperationalStatus** (110)


</dt> <dd>

Cela correspond à la propriété **OperationalStatus** de la classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>

<span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>**StatusDescriptions** (111)


</dt> <dd>

Cela correspond à la propriété **StatusDescriptions** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>

<span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>**MemoryAvailable** (112)


</dt> <dd>

Cela correspond à la propriété **MemoryAvailable** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>

<span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>**AvailableMemoryBuffer** (113)


</dt> <dd>

Cela correspond à la propriété **AvailableMemoryBuffer** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>

<span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>**Mode de réplication** (114)


</dt> <dd>

Cela correspond à la propriété **ReplicationMode** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>

<span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>**État de réplication** (115)


</dt> <dd>

Cela correspond à la propriété **ReplicationState** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>

<span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>**Système de réplication HealthTest réplica** (116)


</dt> <dd>

Cela correspond à la propriété **ReplicationHealth** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>

<span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>**Intégrité** de l’Application (117)


</dt> <dd></dd> <dt>

<span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>

<span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>**ReplicationStateEx** (118)


</dt> <dd>

Cela correspond à la propriété **ReplicationState** de la [**classe \_ ReplicationRelationship MSVM**](msvm-replicationrelationship.md) . Il s’agit d’un tableau pour toutes les valeurs d’état de réplication sur les relations principales et étendues. 0 la valeur d’index est toujours pour la relation principale, et si la réplication étendue est activée, elle est retournée dans l’index 1.

</dd> <dt>

<span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>

<span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>**ReplicationHealthEx** (119)


</dt> <dd>

Cela correspond à la propriété **ReplicationHealth** de la [**classe \_ ReplicationRelationship MSVM**](msvm-replicationrelationship.md) . Il s’agit d’un tableau pour toutes les valeurs d’intégrité de réplication entre les relations principale et étendue. 0 la valeur d’index est toujours pour la relation principale, et si la réplication étendue est activée, elle est retournée dans l’index 1.

</dd> <dt>

<span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>

<span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>**SwapFilesInUse** (120)


</dt> <dd>

Cela correspond à la propriété **SwapFilesInUse** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (121)


</dt> <dd></dd> <dt>

<span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>

<span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>**ReplicationProviderId** (122)


</dt> <dd>

Cela correspond à la propriété **Name** de la classe [**MSVM \_ ReplicationProvider**](msvm-replicationprovider.md) .

</dd> <dt>

<span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>

<span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>**MemorySpansPhysicalNumaNodes** (123)


</dt> <dd></dd> <dt>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (132)


</dt> <dd>

Cela correspond à la propriété **IntegrationServicesVersionState** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>

<span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>**OtherEnabledState** (132)


</dt> <dd>

Cela correspond à la propriété **OtherEnabledState** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .

</dd> <dt>



 (133)


</dt> <dd></dd> </dl> </dd> <dt>

*SummaryInformation* \[ à\]
</dt> <dd>

Type : **[ **MSVM \_ SummaryInformationBase**](msvm-summaryinformationbase.md)\[\]**

Tableau d’instances [**de \_ SummaryInformationBase MSVM**](msvm-summaryinformationbase.md) contenant les informations demandées pour les ordinateurs virtuels et/ou les instantanés spécifiés dans le tableau *SettingData* . Ce tableau aura le même nombre d’éléments que le tableau *SettingData* . Chacune de ces entrées contient la propriété **Name** , même si cette propriété n’a pas été demandée. Si la machine virtuelle ou la capture instantanée est introuvable ou n’est pas disponible, la propriété **nom** de l’entrée de résumé correspondante est vide.

Les propriétés non spécifiées dans le paramètre *RequestedInformation* auront une valeur **null** .

> [!Note]  
> type de données mis à jour à partir de dans Windows 10, version 1703 à partir de [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md).

 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’une des valeurs suivantes.

<dl> <dt>

**Terminé sans erreur** (0)
</dt> <dt>

**Paramètres de méthode activés-tâche démarrée** (4096)
</dt> <dt>

**Échec** (32768)
</dt> <dt>

**Accès refusé** (32769)
</dt> <dt>

**Non pris en charge** (32770)
</dt> <dt>

**État inconnu** (32771)
</dt> <dt>

**Délai d’expiration** (32772)
</dt> <dt>

**Paramètre non valide** (32773)
</dt> <dt>

Le **système est en cours d’utilisation** (32774)
</dt> <dt>

**État non valide pour cette opération** (32775)
</dt> <dt>

**Type de données incorrect** (32776)
</dt> <dt>

Le **système n’est pas disponible** (32777)
</dt> <dt>

**Mémoire insuffisante** (32778)
</dt> </dl>

## <a name="remarks"></a>Remarques

L’accès à la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Exemples

L’exemple C# suivant affiche des informations de synthèse. Les utilitaires référencés se trouvent dans [les utilitaires courants pour les exemples de virtualisation (v2)](common-utilities-for-the-virtualization-samples-v2.md).

> [!IMPORTANT]
> Pour fonctionner correctement, le code suivant doit être exécuté sur le serveur hôte de l’ordinateur virtuel et doit être exécuté avec des privilèges d’administrateur.

 


```CSharp
public class GetSummaryInformationClassV2
{
    public static void GetSummaryInformation(string[] vmNames)
    {
        ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
        ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");
        ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("GetSummaryInformation");

        ManagementObject[] virtualSystemSettings = new ManagementObject[vmNames.Length];

        for (int i = 0; i < vmNames.Length; i++)
        {
            virtualSystemSettings[i] = GetVirtualSystemSetting(vmNames[i], scope);
        }

        UInt32[] requestedInformation = new UInt32[4];
        requestedInformation[0] = 1;    // ElementName
        requestedInformation[2] = 103;  // MemoryUsage
        requestedInformation[3] = 112;  // MemoryAvailable

        inParams["SettingData"] = virtualSystemSettings;
        inParams["RequestedInformation"] = requestedInformation;

        ManagementBaseObject outParams = virtualSystemService.InvokeMethod("GetSummaryInformation", inParams, null);

        if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
        {
            Console.WriteLine("Summary information was retrieved successfully.");

            ManagementBaseObject[] summaryInformationArray = 
                (ManagementBaseObject[])outParams["SummaryInformation"];

            foreach (ManagementBaseObject summaryInformation in summaryInformationArray)
            {
                Console.WriteLine("\nVirtual System Summary Information:");
                if ((null == summaryInformation["Name"]) || 
                    (summaryInformation["Name"].ToString().Length == 0))
                {
                    Console.WriteLine("\tThe VM or snapshot could not be found.");
                }
                else
                {
                    Console.WriteLine("\tName: {0}", summaryInformation["Name"].ToString());
                    foreach (UInt32 requested in requestedInformation)
                    {
                        switch (requested)
                        {
                            case 1:
                                Console.WriteLine("\tElementName: {0}", summaryInformation["ElementName"].ToString());
                                break;

                            case 103:
                                Console.WriteLine("\tMemoryUsage: {0}", summaryInformation["MemoryUsage"].ToString());
                                break;

                            case 112:
                                Console.WriteLine("\tMemoryAvailable: {0}", summaryInformation["MemoryAvailable"].ToString());
                                break;
                        }
                    }
                }
            }
        }
        else
        {
            Console.WriteLine("Failed to retrieve virtual system summary information");
        }

        inParams.Dispose();
        outParams.Dispose();
        virtualSystemService.Dispose();
    }

    public static ManagementObject GetVirtualSystemSetting(string vmName, ManagementScope scope)
    {
        ManagementObject virtualSystem = Utility.GetTargetComputer(vmName, scope);

        ManagementObjectCollection virtualSystemSettings = virtualSystem.GetRelated
         (
             "Msvm_VirtualSystemSettingData",
             "Msvm_SettingsDefineState",
             null,
             null,
             "SettingData",
             "ManagedElement",
             false,
             null
         );

        ManagementObject virtualSystemSetting = null;

        foreach (ManagementObject instance in virtualSystemSettings)
        {
            virtualSystemSetting = instance;
            break;
        }

        return virtualSystemSetting;

    }
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> <dt>

[**\_VIRTUALSYSTEMSETTINGDATA CIM**](/previous-versions//cc136954(v=vs.85))
</dt> <dt>

[**MSVM \_ SummaryInformation**](msvm-summaryinformation.md)
</dt> </dl>

 

