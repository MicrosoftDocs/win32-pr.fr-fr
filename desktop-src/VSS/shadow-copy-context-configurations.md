---
description: Les demandeurs contrôlent les fonctionnalités d’un cliché instantané en définissant son contexte. Ce contexte indique si le cliché instantané doit survivre à l’opération en cours, ainsi que le degré de coordination du fournisseur ou du writer.
ms.assetid: adf79bc8-e893-444a-b750-d7ffd09de7c9
title: Configurations du contexte de cliché instantané
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdb41d0e2604dcf92d27f490175cdcbafd49822c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528696"
---
# <a name="shadow-copy-context-configurations"></a>Configurations du contexte de cliché instantané

Les demandeurs contrôlent les fonctionnalités d’un cliché instantané en définissant son contexte. Ce contexte indique si le cliché instantané doit survivre à l’opération en cours, ainsi que le degré de coordination du fournisseur ou du writer.

## <a name="persistence-and-shadow-copy-context"></a>Persistance et contexte de cliché instantané

Un cliché instantané peut être [*persistant*](vssgloss-p.md), c’est-à-dire que le cliché instantané n’est pas supprimé à la suite de l’arrêt d’une opération de sauvegarde ou de la libération d’un objet [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) .

Les clichés instantanés persistants requièrent des contextes de [**\_ \_ \_ contexte de capture instantanée**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) VSS du **\_ client VSS CTX \_ \_ accessible**, de la restauration de l' **\_ \_ application \_ Visual SourceSafe** ou de **VSS \_ \_ \_**. Les clichés instantanés persistants ne peuvent être créés que pour les volumes NTFS.

Les clichés instantanés non persistants sont créés avec des contextes de sauvegarde **VSS \_ CTX \_** ou une **\_ sauvegarde de \_ \_ partage \_ de fichiers CTX VSS**. Les clichés instantanés non persistants peuvent être effectués pour les volumes NTFS et non-NTFS.

## <a name="writer-participation-and-shadow-copies"></a>Participation aux rédacteurs et clichés instantanés

Un contexte de cliché instantané peut être classé comme impliquant des enregistreurs ou ne pas impliquer d’enregistreurs.

Les contextes de clichés instantanés qui impliquent des Writers dans leur création sont les suivants :

-   **restauration de l’application Visual SourceSafe \_ \_ \_**
-   **\_sauvegarde VSS CTX \_**
-   **\_ \_ \_ rédacteurs accessibles par le client CTX VSS \_**

Ceux qui n’impliquent pas de Writers dans leur création sont les suivants :

-   **\_client CTX \_ VSS \_ accessible**
-   **\_sauvegarde du \_ partage de fichiers CTX \_ VSS \_**
-   **\_restauration du \_ NAS \_ CTX VSS**

Un contexte peut être utilisé avec les deux types de clichés instantanés, mais il ne peut pas être utilisé pour créer un cliché instantané :

-   **VSS \_ CTX \_ tout**

La création d’un cliché instantané avec un contexte de l’utilisation de **VSS \_ CTX \_ All** (à l’aide de [**IVssBackupComponents :: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) et [**IVssBackupComponents ::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)) n’est pas prise en charge.

Les opérations qui prennent en charge un contexte de l' **\_ \_ ensemble de la VSS CTX** sont les opérations d’administration [**IVssBackupComponents :: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query), [**IVssBackupComponents ::D Eletesnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots), [**IVssBackupComponents :: BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset)et [**IVssBackupComponents :: ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot).

## <a name="obtaining-shadow-copy-information"></a>Obtention d’informations sur les clichés instantanés

Si un demandeur connaît le GUID d’identification d’un cliché instantané (son **\_ ID VSS**), il peut obtenir des informations sur le contexte d’un cliché instantané spécifique (identifié par **son \_ ID VSS**) en décompactant la structure de l' [**\_ \_ instantané VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) renvoyée par un appel à [**IVssBackupComponents :: GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).

Pour obtenir des informations de contexte sur tous les clichés instantanés d’un système, un demandeur examine le membre **\_ lSnapshotAttributes** du membre **obj. Snap** de la structure de l' [**\_ objet VSS \_ prop**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) (qui est une structure de l' [**\_ instantané \_ VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) ) obtenue à l’aide de [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) pour effectuer une itération au sein de la liste des objets retournés par un appel à [**IVssBackupComponents :: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).

 

 



