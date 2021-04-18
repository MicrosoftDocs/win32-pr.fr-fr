---
description: Hyper-V utilise le Service VSS (VSS) pour sauvegarder et restaurer des machines virtuelles.
ms.assetid: 94C67F22-658D-49DD-9588-6BB4FCF7ADA9
title: Sauvegarde et restauration de machines virtuelles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9cf6d5b80a4c7392fb38e893a4fafad3f90435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519712"
---
# <a name="backing-up-and-restoring-virtual-machines"></a>Sauvegarde et restauration de machines virtuelles

Hyper-V utilise le Service VSS (VSS) pour sauvegarder et restaurer des machines virtuelles. Si les services d’intégration de sauvegarde (Volume Snapshot) sont installés dans le système d’exploitation invité, un demandeur VSS est installé pour permettre aux rédacteurs VSS du système d’exploitation invité de participer à la sauvegarde de la machine virtuelle. Pour plus d’informations, consultez les sections suivantes :

-   [Sauvegarde des machines virtuelles](#backing-up-the-virtual-machines)
-   [Restauration des machines virtuelles](#restoring-the-virtual-machines)
-   [Clustering de basculement et VSS Hyper-V](#failover-clustering-and-hyper-v-vss)
-   [Détails sur l’enregistreur VSS Hyper-V](#details-on-the-hyper-v-vss-writer)
-   [Rubriques connexes](#related-topics)

## <a name="backing-up-the-virtual-machines"></a>Sauvegarde des machines virtuelles

Hyper-V utilise l’un des deux mécanismes pour sauvegarder chaque ordinateur virtuel. Le mécanisme de sauvegarde par défaut est appelé la méthode « état enregistré », où l’ordinateur virtuel est placé dans un état enregistré pendant le traitement de l’événement PrepareForSnapshot, les captures instantanées sont effectuées sur les volumes appropriés et l’ordinateur virtuel est rétabli à l’état précédent pendant le traitement de l’événement PostSnapshot.

L’autre mécanisme de sauvegarde est appelé la méthode « instantané de machine virtuelle enfant », qui utilise VSS à l’intérieur de la machine virtuelle enfant pour participer à la sauvegarde. Pour que la méthode « instantané de machine virtuelle enfant » soit prise en charge, toutes les conditions suivantes doivent être remplies :

-   Le service d’intégration de sauvegarde (Volume Snapshot) est installé et en cours d’exécution sur l’ordinateur virtuel enfant. Le nom du service est « demandeur de cliché instantané du volume Hyper-V ».
-   L’ordinateur virtuel enfant doit être à l’État en cours d’exécution.
-   L’emplacement du fichier d’instantané de l’ordinateur virtuel est défini comme étant le même que celui du système d’exploitation hôte en tant que fichiers VHD pour l’ordinateur virtuel.
-   Tous les volumes sur la machine virtuelle enfant sont des disques de base et il n’y a pas de disques dynamiques.
-   Tous les disques sur l’ordinateur virtuel enfant doivent utiliser un système de fichiers qui prend en charge les instantanés (par exemple, NTFS).

En général, le processus de sauvegarde des machines virtuelles est le même que celui décrit dans [vue d’ensemble du traitement d’une sauvegarde sous VSS](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss). Le comportement unique se produit lorsque l’enregistreur VSS Hyper-V (qui fait partie du service « gestion de l’ordinateur virtuel Hyper-V ») traite l’événement PrepareForSnapshot. Si la sauvegarde a été effectuée à l’aide de la méthode « instantané de machine virtuelle enfant », un traitement supplémentaire est effectué, mais elle n’est pas visible par l’ordinateur virtuel enfant.

La procédure suivante décrit comment sauvegarder des machines virtuelles.

**Pour sauvegarder des machines virtuelles**

1.  Pour chaque machine virtuelle dans les métadonnées du writer, si la méthode « état enregistré » est utilisée, l’ordinateur virtuel est mis dans un état enregistré. Pour les machines virtuelles utilisant la méthode « instantané de machine virtuelle enfant », le service de demande de cliché instantané de volume Hyper-V dans la machine virtuelle enfant traite la sauvegarde comme détaillé dans la [section vue d’ensemble du traitement d’une sauvegarde sous VSS](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss). Tous les événements VSS sur la machine virtuelle enfant se produisent pendant le traitement du système d’exploitation hôte de l’événement PrepareForSnapshot.
2.  Une fois que toutes les machines virtuelles ont été placées dans l’état enregistré ou si des captures instantanées ont été effectuées, l’enregistreur VSS Hyper-V retourne à partir de l’événement PrepareForSnapshot. Aucun traitement n’est effectué par l’enregistreur VSS Hyper-V pendant les événements Freeze et dégeler.
3.  Lorsque l’enregistreur VSS Hyper-V traite l’événement PostSnapshot, les machines virtuelles qui ont été sauvegardées à l’aide de la méthode « état enregistré » et qui ont été placées dans un état enregistré par l’enregistreur VSS Hyper-V sont retournées à l’État dans lequel elles se trouvaient avant le démarrage de la sauvegarde. Pour les machines virtuelles qui ont été sauvegardées à l’aide de la méthode « instantané de machine virtuelle enfant », l’image hôte des fichiers VHD sur lesquels les captures instantanées ont été effectuées est restaurée sur l’instantané pris lors du traitement de l’événement PrepareForSnapshot. Ce traitement s’effectue indépendamment des enregistreurs VSS sur les machines virtuelles enfants, de sorte que les captures instantanées prises doivent être récupérables automatiquement. (**VSS \_ VOLSNAP \_ attr \_ aucune \_ récupération automatique** n’est définie dans le contexte.)

Les sauvegardes partielles ne sont pas prises en charge. Si un ordinateur virtuel ne parvient pas à créer un instantané, aucune machine virtuelle n’est sauvegardée.

> [!Note]  
> Les disques directs et iSCSI ne sont pas visibles par le système d’exploitation hôte et ne sont donc pas sauvegardés par l’enregistreur VSS Hyper-V. Les sauvegardes de ces volumes doivent être effectuées entièrement sur la machine virtuelle.

 

## <a name="restoring-the-virtual-machines"></a>Restauration des machines virtuelles

La restauration des machines virtuelles est entièrement effectuée par le système d’exploitation hôte. les enregistreurs VSS sur les machines virtuelles enfants ne sont pas impliqués.

La procédure suivante décrit comment restaurer des machines virtuelles.

**Pour restaurer des machines virtuelles**

1.  Pendant le traitement de l’événement de prérestauration, l’enregistreur VSS Hyper-V désactive et supprime tous les ordinateurs virtuels qui sont sur le moment d’être restaurés.
2.  Une fois que tous les enregistreurs VSS ont traité l’événement de prérestauration, les fichiers sont restaurés.
3.  Pendant le traitement de l’événement PostRestore, l’enregistreur VSS Hyper-V appelle la méthode [**IVssComponent :: GetFileRestoreStatus**](/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getfilerestorestatus) . Si le retour n’est **pas \_ VSS \_ RS All**, l’enregistreur VSS Hyper-V appelle la méthode [**SetWriterFailure**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure) et retourne **false** à partir de la méthode [**OnPostRestore**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostrestore) .
4.  Pour chaque machine virtuelle restaurée, l’enregistreur VSS Hyper-V inscrit l’ordinateur virtuel auprès du service de gestion Hyper-V. Si la machine virtuelle est restaurée à un emplacement non défini par défaut, un lien symbolique est créé dans l’emplacement par défaut qui est lié à cet emplacement.
5.  Pour chaque disque dur virtuel qui a été restauré, l’emplacement est comparé à celui spécifié pour cet ordinateur virtuel. Si l’emplacement est différent, la configuration est mise à jour avec l’emplacement approprié.
6.  La configuration réseau est mise à jour. Si les commutateurs virtuels auxquels la machine virtuelle était connectée lorsqu’elle a été sauvegardée se ferment, de nouveaux ports sont créés et connectés à la machine virtuelle.

## <a name="failover-clustering-and-hyper-v-vss"></a>Clustering de basculement et VSS Hyper-V

L’enregistreur VSS Hyper-V ne prend pas en compte les ordinateurs virtuels qui font partie d’un cluster de basculement. Pendant les sauvegardes de la méthode « état enregistré » et toutes les restaurations, la machine virtuelle est placée dans l’état enregistré ou entièrement supprimée. Cela est considéré comme un échec du service de clustering et entraîne le basculement des applications sur ces nœuds vers d’autres nœuds. Pour éviter cette situation lors des sauvegardes « état enregistré », l’état de l’ordinateur virtuel doit être enregistré à l’aide du service de clustering. Pour éviter cette erreur lors d’une restauration, les ressources sur l’ordinateur virtuel doivent être mises hors connexion.

## <a name="details-on-the-hyper-v-vss-writer"></a>Détails sur l’enregistreur VSS Hyper-V

Nom de l’enregistreur : Microsoft Hyper-V l’enregistreur VSS

ID de l’enregistreur : 66841CD4-6DED-4F4B-8F17-FD23F8DDC3DE

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble du traitement d’une sauvegarde sous VSS](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss)
</dt> <dt>

[Vue d’ensemble du traitement d’une restauration sous VSS](/windows/desktop/VSS/overview-of-processing-a-restore-under-vss)
</dt> </dl>

 

 
