---
description: Windows Server 2008.
ms.assetid: 2f7b62f8-ba1e-42d2-8872-38d4475e4a2a
title: Nouveautés de VSS dans Windows Server 2008 et Windows Vista SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f053e327a7a54a9597bc06836b37c00effc62f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113162"
---
# <a name="whats-new-in-vss-in-windows-server-2008-and-windows-vista-sp1"></a><span data-ttu-id="22904-103">Nouveautés de VSS dans Windows Server 2008 et Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="22904-103">What's New in VSS in Windows Server 2008 and Windows Vista SP1</span></span>

<span data-ttu-id="22904-104">Windows Server 2008 et Windows Vista avec Service Pack 1 (SP1) introduisent les modifications suivantes dans le Service VSS.</span><span class="sxs-lookup"><span data-stu-id="22904-104">Windows Server 2008 and Windows Vista with Service Pack 1 (SP1) introduce the following changes to the Volume Shadow Copy Service.</span></span>

> [!Note]  
> <span data-ttu-id="22904-105">Toutes les modifications apportées à Windows Vista s’appliquent à Windows Server 2008 et Windows Vista avec SP1.</span><span class="sxs-lookup"><span data-stu-id="22904-105">All changes for Windows Vista apply to Windows Server 2008 and Windows Vista with SP1.</span></span> <span data-ttu-id="22904-106">Pour plus d’informations sur ces modifications, consultez [Nouveautés de VSS dans Windows Vista](what-s-new-in-vss-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="22904-106">For details on those changes, see [What's New in VSS in Windows Vista](what-s-new-in-vss-in-windows-vista.md).</span></span>

 

-   [<span data-ttu-id="22904-107">Nouvelles interfaces VSS</span><span class="sxs-lookup"><span data-stu-id="22904-107">New VSS Interfaces</span></span>](#new-vss-interfaces)
-   [<span data-ttu-id="22904-108">Nouvelles énumérations VSS</span><span class="sxs-lookup"><span data-stu-id="22904-108">New VSS Enumerations</span></span>](#new-vss-enumerations)
-   [<span data-ttu-id="22904-109">Nouvelles structures VSS</span><span class="sxs-lookup"><span data-stu-id="22904-109">New VSS Structures</span></span>](#new-vss-structures)
-   [<span data-ttu-id="22904-110">Modifications existantes de l’énumération VSS</span><span class="sxs-lookup"><span data-stu-id="22904-110">Existing VSS Enumeration Modifications</span></span>](#existing-vss-enumeration-modifications)
-   [<span data-ttu-id="22904-111">Modifications existantes de l’interface VSS</span><span class="sxs-lookup"><span data-stu-id="22904-111">Existing VSS Interface Modifications</span></span>](#existing-vss-interface-modifications)
-   [<span data-ttu-id="22904-112">Nouveaux enregistreurs VSS</span><span class="sxs-lookup"><span data-stu-id="22904-112">New VSS Writers</span></span>](#new-vss-writers)

## <a name="new-vss-interfaces"></a><span data-ttu-id="22904-113">Nouvelles interfaces VSS</span><span class="sxs-lookup"><span data-stu-id="22904-113">New VSS Interfaces</span></span>

<dl>

[<span data-ttu-id="22904-114">**IVssDifferentialSoftwareSnapshotMgmt3**</span><span class="sxs-lookup"><span data-stu-id="22904-114">**IVssDifferentialSoftwareSnapshotMgmt3**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3)  
[<span data-ttu-id="22904-115">**IVssHardwareSnapshotProviderEx**</span><span class="sxs-lookup"><span data-stu-id="22904-115">**IVssHardwareSnapshotProviderEx**</span></span>](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)  
</dl>

## <a name="new-vss-enumerations"></a><span data-ttu-id="22904-116">Nouvelles énumérations VSS</span><span class="sxs-lookup"><span data-stu-id="22904-116">New VSS Enumerations</span></span>

<dl>

[<span data-ttu-id="22904-117">**\_\_options matérielles VSS \_**</span><span class="sxs-lookup"><span data-stu-id="22904-117">**\_VSS\_HARDWARE\_OPTIONS**</span></span>](/windows/desktop/api/Vss/ne-vss-vss_hardware_options)  
[<span data-ttu-id="22904-118">**\_erreur de protection VSS \_**</span><span class="sxs-lookup"><span data-stu-id="22904-118">**VSS\_PROTECTION\_FAULT**</span></span>](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_fault)  
[<span data-ttu-id="22904-119">**\_niveau de protection VSS \_**</span><span class="sxs-lookup"><span data-stu-id="22904-119">**VSS\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_level)  
</dl>

## <a name="new-vss-structures"></a><span data-ttu-id="22904-120">Nouvelles structures VSS</span><span class="sxs-lookup"><span data-stu-id="22904-120">New VSS Structures</span></span>

<dl>

[<span data-ttu-id="22904-121">**\_ \_ informations sur la protection du volume VSS \_**</span><span class="sxs-lookup"><span data-stu-id="22904-121">**VSS\_VOLUME\_PROTECTION\_INFO**</span></span>](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_protection_info)  
</dl>

## <a name="existing-vss-enumeration-modifications"></a><span data-ttu-id="22904-122">Modifications existantes de l’énumération VSS</span><span class="sxs-lookup"><span data-stu-id="22904-122">Existing VSS Enumeration Modifications</span></span>

<dl> <dt>

<span data-ttu-id="22904-123"><span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>Service [**VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) Énumération de schéma de sauvegarde</span><span class="sxs-lookup"><span data-stu-id="22904-123"><span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS\_BACKUP\_SCHEMA**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="22904-124"><span id="Added_value_"></span><span id="added_value_"></span><span id="ADDED_VALUE_"></span>Valeur ajoutée :</span><span class="sxs-lookup"><span data-stu-id="22904-124"><span id="Added_value_"></span><span id="added_value_"></span><span id="ADDED_VALUE_"></span>Added value:</span></span>
</dt> <dd>

<span data-ttu-id="22904-125">VSS \_ BS \_ writer \_ prend en charge les \_ \_ restaurations parallèles</span><span class="sxs-lookup"><span data-stu-id="22904-125">VSS\_BS\_WRITER\_SUPPORTS\_PARALLEL\_RESTORES</span></span>

</dd> </dl> </dd> </dl>

<dl> <dt>

<span data-ttu-id="22904-126"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>Énumération des [**\_ \_ attributs d' \_ instantané \_ de volume VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)</span><span class="sxs-lookup"><span data-stu-id="22904-126"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>[**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="22904-127"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valeurs ajoutées :</span><span class="sxs-lookup"><span data-stu-id="22904-127"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="22904-128">VSS \_ VOLSNAP \_ attr \_ \_ POSTSNAPSHOT différé</span><span class="sxs-lookup"><span data-stu-id="22904-128">VSS\_VOLSNAP\_ATTR\_DELAYED\_POSTSNAPSHOT</span></span>

<span data-ttu-id="22904-129">VSS \_ VOLSNAP \_ attr \_ \_ récupération TxF</span><span class="sxs-lookup"><span data-stu-id="22904-129">VSS\_VOLSNAP\_ATTR\_TXF\_RECOVERY</span></span>

</dd> </dl> </dd> </dl>

## <a name="existing-vss-interface-modifications"></a><span data-ttu-id="22904-130">Modifications existantes de l’interface VSS</span><span class="sxs-lookup"><span data-stu-id="22904-130">Existing VSS Interface Modifications</span></span>

<dl> <dt>

<span data-ttu-id="22904-131"><span id="IVssBackupComponentsEx2_interface"></span><span id="ivssbackupcomponentsex2_interface"></span><span id="IVSSBACKUPCOMPONENTSEX2_INTERFACE"></span>Interface [**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)</span><span class="sxs-lookup"><span data-stu-id="22904-131"><span id="IVssBackupComponentsEx2_interface"></span><span id="ivssbackupcomponentsex2_interface"></span><span id="IVSSBACKUPCOMPONENTSEX2_INTERFACE"></span>[**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="22904-132"><span id="Added_method_"></span><span id="added_method_"></span><span id="ADDED_METHOD_"></span>Méthode ajoutée :</span><span class="sxs-lookup"><span data-stu-id="22904-132"><span id="Added_method_"></span><span id="added_method_"></span><span id="ADDED_METHOD_"></span>Added method:</span></span>
</dt> <dd>

[<span data-ttu-id="22904-133">**BreakSnapshotSetEx**</span><span class="sxs-lookup"><span data-stu-id="22904-133">**BreakSnapshotSetEx**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)

</dd> </dl> </dd> </dl>

## <a name="new-vss-writers"></a><span data-ttu-id="22904-134">Nouveaux enregistreurs VSS</span><span class="sxs-lookup"><span data-stu-id="22904-134">New VSS Writers</span></span>

<span data-ttu-id="22904-135">Windows Server 2008 et Windows Vista avec SP1 introduisent les enregistreurs VSS suivants :</span><span class="sxs-lookup"><span data-stu-id="22904-135">Windows Server 2008 and Windows Vista with SP1 introduce the following VSS writers:</span></span>

-   <span data-ttu-id="22904-136">Rédacteur de configuration IIS</span><span class="sxs-lookup"><span data-stu-id="22904-136">IIS Configuration Writer</span></span>
-   <span data-ttu-id="22904-137">Enregistreur de la métabase IIS</span><span class="sxs-lookup"><span data-stu-id="22904-137">IIS Metabase Writer</span></span>
-   <span data-ttu-id="22904-138">Enregistreur VSS NPS</span><span class="sxs-lookup"><span data-stu-id="22904-138">NPS VSS Writer</span></span>
-   <span data-ttu-id="22904-139">Enregistreur VSS de la passerelle Services Bureau à distance (services Terminal Server)</span><span class="sxs-lookup"><span data-stu-id="22904-139">Remote Desktop Services (Terminal Services) Gateway VSS Writer</span></span>
-   <span data-ttu-id="22904-140">Enregistreur VSS du gestionnaire de licences des Services Bureau à distance (services Terminal Server)</span><span class="sxs-lookup"><span data-stu-id="22904-140">Remote Desktop Services (Terminal Services) Licensing VSS Writer</span></span>

<span data-ttu-id="22904-141">Ces Writers sont documentés dans les [enregistreurs VSS](in-box-vss-writers.md).</span><span class="sxs-lookup"><span data-stu-id="22904-141">These writers are documented in [In-Box VSS Writers](in-box-vss-writers.md).</span></span>

 

 



