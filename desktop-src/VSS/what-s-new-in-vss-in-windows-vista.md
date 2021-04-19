---
description: Windows Vista.
ms.assetid: 3b16744d-b9c2-4462-a409-de94d9103c39
title: Nouveautés de VSS dans Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 122caa350ede984d5b05eb7eedd6039d82a76f1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515859"
---
# <a name="whats-new-in-vss-in-windows-vista"></a><span data-ttu-id="2f2e5-103">Nouveautés de VSS dans Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f2e5-103">What's New in VSS in Windows Vista</span></span>

<span data-ttu-id="2f2e5-104">Windows Vista apporte les modifications suivantes au Service VSS.</span><span class="sxs-lookup"><span data-stu-id="2f2e5-104">Windows Vista introduces the following changes to the Volume Shadow Copy Service.</span></span>

<span data-ttu-id="2f2e5-105">Notez que toutes les modifications apportées à Windows Vista s’appliquent également à Windows Server 2008 et Windows Vista avec Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="2f2e5-105">Note that all changes for Windows Vista also apply to Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

## <a name="new-vss-interfaces"></a><span data-ttu-id="2f2e5-106">Nouvelles interfaces VSS</span><span class="sxs-lookup"><span data-stu-id="2f2e5-106">New VSS Interfaces</span></span>

[<span data-ttu-id="2f2e5-107">**IVssBackupComponentsEx2**</span><span class="sxs-lookup"><span data-stu-id="2f2e5-107">**IVssBackupComponentsEx2**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)

[<span data-ttu-id="2f2e5-108">**IVssComponentEx**</span><span class="sxs-lookup"><span data-stu-id="2f2e5-108">**IVssComponentEx**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex)

[<span data-ttu-id="2f2e5-109">**IVssCreateWriterMetadataEx**</span><span class="sxs-lookup"><span data-stu-id="2f2e5-109">**IVssCreateWriterMetadataEx**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadataex)

[<span data-ttu-id="2f2e5-110">**IVssDifferentialSoftwareSnapshotMgmt2**</span><span class="sxs-lookup"><span data-stu-id="2f2e5-110">**IVssDifferentialSoftwareSnapshotMgmt2**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt2)

[<span data-ttu-id="2f2e5-111">**IVssExamineWriterMetadataEx2**</span><span class="sxs-lookup"><span data-stu-id="2f2e5-111">**IVssExamineWriterMetadataEx2**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadataex2)

## <a name="new-vss-classes"></a><span data-ttu-id="2f2e5-112">Nouvelles classes VSS</span><span class="sxs-lookup"><span data-stu-id="2f2e5-112">New VSS Classes</span></span>

[<span data-ttu-id="2f2e5-113">**CVssWriterEx**</span><span class="sxs-lookup"><span data-stu-id="2f2e5-113">**CVssWriterEx**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriterex)

## <a name="new-vss-enumerations"></a><span data-ttu-id="2f2e5-114">Nouvelles énumérations VSS</span><span class="sxs-lookup"><span data-stu-id="2f2e5-114">New VSS Enumerations</span></span>

[<span data-ttu-id="2f2e5-115">**\_type de restauration par progression VSS \_**</span><span class="sxs-lookup"><span data-stu-id="2f2e5-115">**VSS\_ROLLFORWARD\_TYPE**</span></span>](/windows/desktop/api/Vss/ne-vss-vss_rollforward_type)

## <a name="existing-vss-enumeration-modifications"></a><span data-ttu-id="2f2e5-116">Modifications existantes de l’énumération VSS</span><span class="sxs-lookup"><span data-stu-id="2f2e5-116">Existing VSS Enumeration Modifications</span></span>

<dl> <dt>

<span data-ttu-id="2f2e5-117"><span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>Service [**VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) Énumération de schéma de sauvegarde</span><span class="sxs-lookup"><span data-stu-id="2f2e5-117"><span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS\_BACKUP\_SCHEMA**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="2f2e5-118"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valeurs ajoutées :</span><span class="sxs-lookup"><span data-stu-id="2f2e5-118"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="2f2e5-119">\_ \_ restauration faisant autorité de VSS BS \_</span><span class="sxs-lookup"><span data-stu-id="2f2e5-119">VSS\_BS\_AUTHORITATIVE\_RESTORE</span></span>

<span data-ttu-id="2f2e5-120">\_État du \_ \_ système indépendant VSS BS \_</span><span class="sxs-lookup"><span data-stu-id="2f2e5-120">VSS\_BS\_INDEPENDENT\_SYSTEM\_STATE</span></span>

<span data-ttu-id="2f2e5-121">renommage de la \_ restauration VSS BS \_ \_</span><span class="sxs-lookup"><span data-stu-id="2f2e5-121">VSS\_BS\_RESTORE\_RENAME</span></span>

<span data-ttu-id="2f2e5-122">\_restauration VSS BS \_ restauration par progression \_</span><span class="sxs-lookup"><span data-stu-id="2f2e5-122">VSS\_BS\_ROLLFORWARD\_RESTORE</span></span>

</dd> </dl> </dd> </dl>

<dl> <dt>

<span data-ttu-id="2f2e5-123"><span id="VSS_COMPONENT_FLAGS_enumeration"></span><span id="vss_component_flags_enumeration"></span><span id="VSS_COMPONENT_FLAGS_ENUMERATION"></span>Service [**VSS \_ \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags) Énumération des indicateurs de composants</span><span class="sxs-lookup"><span data-stu-id="2f2e5-123"><span id="VSS_COMPONENT_FLAGS_enumeration"></span><span id="vss_component_flags_enumeration"></span><span id="VSS_COMPONENT_FLAGS_ENUMERATION"></span>[**VSS\_COMPONENT\_FLAGS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="2f2e5-124"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valeurs ajoutées :</span><span class="sxs-lookup"><span data-stu-id="2f2e5-124"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="2f2e5-125">\_État du système de CF \_ non \_ \_</span><span class="sxs-lookup"><span data-stu-id="2f2e5-125">VSS\_CF\_NOT\_SYSTEM\_STATE</span></span>

</dd> </dl> </dd> </dl>

<dl> <dt>

<span data-ttu-id="2f2e5-126"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>Énumération des [**\_ \_ attributs d' \_ instantané \_ de volume VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)</span><span class="sxs-lookup"><span data-stu-id="2f2e5-126"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>[**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="2f2e5-127"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valeurs ajoutées :</span><span class="sxs-lookup"><span data-stu-id="2f2e5-127"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="2f2e5-128">VSS \_ VOLSNAP \_ attr \_ non- \_ récupération automatique</span><span class="sxs-lookup"><span data-stu-id="2f2e5-128">VSS\_VOLSNAP\_ATTR\_NO\_AUTORECOVERY</span></span>

<span data-ttu-id="2f2e5-129">VSS \_ VOLSNAP \_ attr \_ non \_ traité</span><span class="sxs-lookup"><span data-stu-id="2f2e5-129">VSS\_VOLSNAP\_ATTR\_NOT\_TRANSACTED</span></span>

</dd> </dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a><span data-ttu-id="2f2e5-130">Suivi et journalisation des événements VSS</span><span class="sxs-lookup"><span data-stu-id="2f2e5-130">VSS Event Tracing and Logging</span></span>

-   <span data-ttu-id="2f2e5-131">Le fichier de trace VSS peut désormais se trouver sur n’importe quel volume local.</span><span class="sxs-lookup"><span data-stu-id="2f2e5-131">The VSS trace file can now be located on any local volume.</span></span> <span data-ttu-id="2f2e5-132">Dans les versions de Windows antérieures à Windows Vista, le fichier de trace VSS n’a pas pu être localisé sur un volume qui se trouvait dans le jeu de clichés instantanés.</span><span class="sxs-lookup"><span data-stu-id="2f2e5-132">On versions of Windows prior to Windows Vista, the VSS trace file could not be located on a volume that was in the shadow copy set.</span></span>
-   <span data-ttu-id="2f2e5-133">De nombreuses entrées du journal des événements ont été reformulées pour les rendre plus claires.</span><span class="sxs-lookup"><span data-stu-id="2f2e5-133">Many event log entries have been reworded to make them clearer.</span></span>
-   <span data-ttu-id="2f2e5-134">Toutes les entrées du journal des événements VSS contiennent désormais des informations de contexte.</span><span class="sxs-lookup"><span data-stu-id="2f2e5-134">All VSS event log entries now contain context information.</span></span>

## <a name="vss-error-reporting"></a><span data-ttu-id="2f2e5-135">Rapport d’erreurs VSS</span><span class="sxs-lookup"><span data-stu-id="2f2e5-135">VSS Error Reporting</span></span>

-   <span data-ttu-id="2f2e5-136">Les descriptions de tous les codes d’erreur VSS peuvent maintenant être récupérées en appelant la fonction [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) avec l' \_ indicateur format message \_ from \_ HMODULE spécifié dans le paramètre *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="2f2e5-136">Descriptions of all VSS error codes can now be retrieved by calling the [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_HMODULE flag specified in the *dwFlags* parameter.</span></span>
-   <span data-ttu-id="2f2e5-137">Les messages de code d’erreur VSS sont contenus dans vsstrace.dll.</span><span class="sxs-lookup"><span data-stu-id="2f2e5-137">The VSS error code messages are contained in vsstrace.dll.</span></span> <span data-ttu-id="2f2e5-138">Un descripteur de ce module doit être spécifié dans le paramètre *lpSource* .</span><span class="sxs-lookup"><span data-stu-id="2f2e5-138">A handle to this module must be specified in the *lpSource* parameter.</span></span>

## <a name="excluding-files-from-shadow-copies"></a><span data-ttu-id="2f2e5-139">Exclusion de fichiers des clichés instantanés</span><span class="sxs-lookup"><span data-stu-id="2f2e5-139">Excluding Files from Shadow Copies</span></span>

<span data-ttu-id="2f2e5-140">Les applications ou les services peuvent utiliser la clé de Registre FilesNotToSnapshot pour spécifier les fichiers à supprimer des clichés instantanés nouvellement créés.</span><span class="sxs-lookup"><span data-stu-id="2f2e5-140">Applications or services can use the FilesNotToSnapshot registry key to specify files to be deleted from newly created shadow copies.</span></span> <span data-ttu-id="2f2e5-141">Pour plus d’informations, consultez [exclusion de fichiers des clichés instantanés](excluding-files-from-shadow-copies.md).</span><span class="sxs-lookup"><span data-stu-id="2f2e5-141">For more information, see [Excluding Files from Shadow Copies](excluding-files-from-shadow-copies.md).</span></span>

## <a name="backup-and-restore-application-compatibility"></a><span data-ttu-id="2f2e5-142">Sauvegarde et restauration de la compatibilité des applications</span><span class="sxs-lookup"><span data-stu-id="2f2e5-142">Backup and Restore Application Compatibility</span></span>

<span data-ttu-id="2f2e5-143">Les développeurs d’applications de sauvegarde et de restauration doivent être conscients de certaines nouvelles fonctionnalités de Windows Vista et de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="2f2e5-143">Developers of backup and restore applications need to be aware of certain new features in Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="2f2e5-144">Pour obtenir une liste de vérification de la compatibilité des applications, consultez [compatibilité des applications pour la sauvegarde et la restauration](application-compatibility-for-backup-and-restore.md).</span><span class="sxs-lookup"><span data-stu-id="2f2e5-144">For an application compatibility checklist, see [Application Compatibility for Backup and Restore](application-compatibility-for-backup-and-restore.md).</span></span>

 

 
