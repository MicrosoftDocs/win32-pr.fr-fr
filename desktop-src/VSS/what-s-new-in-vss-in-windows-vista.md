---
description: Windows Vista.
ms.assetid: 3b16744d-b9c2-4462-a409-de94d9103c39
title: nouveautés de VSS dans Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc9e0780b092b2bed0235ba62377da9a4f7f0b53bded9e3f7feb5d412f5ab982
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751141"
---
# <a name="whats-new-in-vss-in-windows-vista"></a>nouveautés de VSS dans Windows Vista

Windows Vista introduit les modifications suivantes dans le Service VSS.

notez que toutes les modifications apportées à Windows vista s’appliquent également à Windows Server 2008 et à Windows vista avec Service Pack 1 (SP1).

## <a name="new-vss-interfaces"></a>Nouvelles interfaces VSS

[**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)

[**IVssComponentEx**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex)

[**IVssCreateWriterMetadataEx**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadataex)

[**IVssDifferentialSoftwareSnapshotMgmt2**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt2)

[**IVssExamineWriterMetadataEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadataex2)

## <a name="new-vss-classes"></a>Nouvelles classes VSS

[**CVssWriterEx**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriterex)

## <a name="new-vss-enumerations"></a>Nouvelles énumérations VSS

[**\_type de restauration par progression VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_rollforward_type)

## <a name="existing-vss-enumeration-modifications"></a>Modifications existantes de l’énumération VSS

<dl> <dt>

<span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>Service [**VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) Énumération de schéma de sauvegarde
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valeurs ajoutées :
</dt> <dd>

\_ \_ restauration faisant autorité de VSS BS \_

\_État du \_ \_ système indépendant VSS BS \_

renommage de la \_ restauration VSS BS \_ \_

\_restauration VSS BS \_ restauration par progression \_

</dd> </dl> </dd> </dl>

<dl> <dt>

<span id="VSS_COMPONENT_FLAGS_enumeration"></span><span id="vss_component_flags_enumeration"></span><span id="VSS_COMPONENT_FLAGS_ENUMERATION"></span>Service [**VSS \_ \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags) Énumération des indicateurs de composants
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valeurs ajoutées :
</dt> <dd>

\_État du système de CF \_ non \_ \_

</dd> </dl> </dd> </dl>

<dl> <dt>

<span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>Énumération des [**\_ \_ attributs d' \_ instantané \_ de volume VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valeurs ajoutées :
</dt> <dd>

VSS \_ VOLSNAP \_ attr \_ non- \_ récupération automatique

VSS \_ VOLSNAP \_ attr \_ non \_ traité

</dd> </dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a>Suivi et journalisation des événements VSS

-   Le fichier de trace VSS peut désormais se trouver sur n’importe quel volume local. dans les versions de Windows antérieures à Windows Vista, le fichier de trace VSS n’a pas pu être localisé sur un volume qui se trouvait dans le jeu de clichés instantanés.
-   De nombreuses entrées du journal des événements ont été reformulées pour les rendre plus claires.
-   Toutes les entrées du journal des événements VSS contiennent désormais des informations de contexte.

## <a name="vss-error-reporting"></a>Rapport d’erreurs VSS

-   Les descriptions de tous les codes d’erreur VSS peuvent maintenant être récupérées en appelant la fonction [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) avec l' \_ indicateur format message \_ from \_ HMODULE spécifié dans le paramètre *dwFlags* .
-   Les messages de code d’erreur VSS sont contenus dans vsstrace.dll. Un descripteur de ce module doit être spécifié dans le paramètre *lpSource* .

## <a name="excluding-files-from-shadow-copies"></a>Exclusion de fichiers des clichés instantanés

Les applications ou les services peuvent utiliser la clé de Registre FilesNotToSnapshot pour spécifier les fichiers à supprimer des clichés instantanés nouvellement créés. Pour plus d’informations, consultez [exclusion de fichiers des clichés instantanés](excluding-files-from-shadow-copies.md).

## <a name="backup-and-restore-application-compatibility"></a>Sauvegarde et restauration de la compatibilité des applications

les développeurs d’applications de sauvegarde et de restauration doivent être conscients de certaines nouvelles fonctionnalités de Windows Vista et Windows Server 2008. Pour obtenir une liste de vérification de la compatibilité des applications, consultez [compatibilité des applications pour la sauvegarde et la restauration](application-compatibility-for-backup-and-restore.md).

 

 
