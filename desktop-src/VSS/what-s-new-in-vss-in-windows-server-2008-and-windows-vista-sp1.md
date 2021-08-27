---
description: Windows Server 2008.
ms.assetid: 2f7b62f8-ba1e-42d2-8872-38d4475e4a2a
title: nouveautés de VSS dans Windows Server 2008 et Windows Vista SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ee109eec31c084dc43fb9e0cc6341f443a16e6aa06ac989a7f328d9bb3011f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006119"
---
# <a name="whats-new-in-vss-in-windows-server-2008-and-windows-vista-sp1"></a>nouveautés de VSS dans Windows Server 2008 et Windows Vista SP1

Windows le serveur 2008 et Windows Vista avec Service Pack 1 (SP1) introduisent les modifications suivantes dans le Service VSS.

> [!Note]  
> toutes les modifications apportées à Windows vista s’appliquent à Windows Server 2008 et à Windows vista avec SP1. pour plus d’informations sur ces modifications, consultez [nouveautés de VSS dans Windows Vista](what-s-new-in-vss-in-windows-vista.md).

 

-   [Nouvelles interfaces VSS](#new-vss-interfaces)
-   [Nouvelles énumérations VSS](#new-vss-enumerations)
-   [Nouvelles structures VSS](#new-vss-structures)
-   [Modifications existantes de l’énumération VSS](#existing-vss-enumeration-modifications)
-   [Modifications existantes de l’interface VSS](#existing-vss-interface-modifications)
-   [Nouveaux enregistreurs VSS](#new-vss-writers)

## <a name="new-vss-interfaces"></a>Nouvelles interfaces VSS

<dl>

[**IVssDifferentialSoftwareSnapshotMgmt3**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3)  
[**IVssHardwareSnapshotProviderEx**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)  
</dl>

## <a name="new-vss-enumerations"></a>Nouvelles énumérations VSS

<dl>

[**\_\_options matérielles VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_hardware_options)  
[**\_erreur de protection VSS \_**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_fault)  
[**\_niveau de protection VSS \_**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_level)  
</dl>

## <a name="new-vss-structures"></a>Nouvelles structures VSS

<dl>

[**\_ \_ informations sur la protection du volume VSS \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_protection_info)  
</dl>

## <a name="existing-vss-enumeration-modifications"></a>Modifications existantes de l’énumération VSS

<dl> <dt>

<span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>Service [**VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) Énumération de schéma de sauvegarde
</dt> <dd>

<dl> <dt>

<span id="Added_value_"></span><span id="added_value_"></span><span id="ADDED_VALUE_"></span>Valeur ajoutée :
</dt> <dd>

VSS \_ BS \_ writer \_ prend en charge les \_ \_ restaurations parallèles

</dd> </dl> </dd> </dl>

<dl> <dt>

<span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>Énumération des [**\_ \_ attributs d' \_ instantané \_ de volume VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valeurs ajoutées :
</dt> <dd>

VSS \_ VOLSNAP \_ attr \_ \_ POSTSNAPSHOT différé

VSS \_ VOLSNAP \_ attr \_ \_ récupération TxF

</dd> </dl> </dd> </dl>

## <a name="existing-vss-interface-modifications"></a>Modifications existantes de l’interface VSS

<dl> <dt>

<span id="IVssBackupComponentsEx2_interface"></span><span id="ivssbackupcomponentsex2_interface"></span><span id="IVSSBACKUPCOMPONENTSEX2_INTERFACE"></span>Interface [**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)
</dt> <dd>

<dl> <dt>

<span id="Added_method_"></span><span id="added_method_"></span><span id="ADDED_METHOD_"></span>Méthode ajoutée :
</dt> <dd>

[**BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)

</dd> </dl> </dd> </dl>

## <a name="new-vss-writers"></a>Nouveaux enregistreurs VSS

Windows le serveur 2008 et Windows Vista avec SP1 introduisent les enregistreurs VSS suivants :

-   Rédacteur de configuration IIS
-   Enregistreur de la métabase IIS
-   Enregistreur VSS NPS
-   Enregistreur VSS de la passerelle Services Bureau à distance (services Terminal Server)
-   Enregistreur VSS du gestionnaire de licences des Services Bureau à distance (services Terminal Server)

Ces Writers sont documentés dans les [enregistreurs VSS](in-box-vss-writers.md).

 

 



