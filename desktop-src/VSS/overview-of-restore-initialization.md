---
description: Lors de l’initialisation d’une opération de restauration VSS, un demandeur doit récupérer le document du composant de sauvegarde et chaque document de métadonnées de l’enregistreur approprié créé et enregistré pendant l’opération de sauvegarde.
ms.assetid: 0a087125-c9d4-460a-8153-3e2e26633ac2
title: Vue d’ensemble de l’initialisation de la restauration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb62e5282a74e38cd53d36c8ba004f4b8069746
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413365"
---
# <a name="overview-of-restore-initialization"></a>Vue d’ensemble de l’initialisation de la restauration

Lors de l’initialisation d’une opération de restauration VSS, un demandeur doit récupérer le document du composant de sauvegarde et chaque document de métadonnées de l’enregistreur approprié créé et enregistré pendant l’opération de sauvegarde. L’état actuel de l’enregistreur est interrogé dans le traitement de l' [*événement d’identification*](vssgloss-i.md) généré par le demandeur. Pour plus d’informations, consultez [vue d’ensemble du traitement d’une restauration sous VSS](overview-of-processing-a-restore-under-vss.md).

Le tableau suivant présente la séquence des actions et des événements qui sont requis pour initialiser une opération de restauration.



| Action du demandeur                                                                                                                                                                                                                                                                                                       | Événement                                                     | Action d’écriture                                                                                                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Créez une interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) , initialisez-la pour gérer une restauration et chargez les métadonnées du demandeur stocké (consultez [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents), [**IVssBackupComponents :: InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore)). | None                                                      | None                                                                                                                                                                                                                                                                                                                      |
| Appelez [**CreateVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssexaminewritermetadata) pour créer des interfaces [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) et les charger avec les métadonnées de l’enregistreur stocké.                                                                                                           | None                                                      | None                                                                                                                                                                                                                                                                                                                      |
| Lancer un contact asynchrone avec des enregistreurs (consultez [**IVssBackupComponents :: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).)                                                                                                                                                                      | [*Repérer*](vssgloss-i.md) | L’enregistreur commence la gestion des événements à la prise en charge de la restauration. Crée le document de métadonnées de l’enregistreur (consultez [utilisation du document de métadonnées de l’enregistreur](working-with-the-writer-metadata-document.md), [**CVssWriter :: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify), [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)). |
| Le demandeur attend que les Writers s’initialisent en appelant [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync).                                                                                                                                                                                                                               | None                                                      | None                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requester-actions-during-restore-initialization"></a>Actions du demandeur pendant l’initialisation de la restauration

Pendant la phase d’initialisation d’une restauration, le demandeur doit avoir accès au document des composants de sauvegarde stockés et à tous les documents de métadonnées de l’enregistreur.

En fonction de l’implémentation, cela signifie soit que le demandeur exige que le support de sauvegarde soit monté et lisible, soit qu’un autre mécanisme d’accès aux métadonnées stockées soit disponible.

Le demandeur utilise le document XML stocké contenant le document des composants de sauvegarde du demandeur qui a effectué la sauvegarde pour initialiser son document de composants de sauvegarde à l’aide de [**IVssBackupComponents :: InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) peut accéder aux informations.

Comme c’était le cas lors de la sauvegarde, le document sur les composants de sauvegarde ne dispose pas d’informations suffisantes pour prendre en charge une restauration. par conséquent, le demandeur a besoin d’accéder aux documents de métadonnées de l’enregistreur stockés pendant la sauvegarde (consultez [utilisation des composants par le demandeur](use-of-components-by-the-requestor.md)).

Le demandeur récupère les métadonnées de l’enregistreur stocké en appelant [**CreateVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssexaminewritermetadata) pour chaque enregistreur dont les données ont été sauvegardées et doit maintenant être restauré. Cette fonction crée un objet [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) pour chaque Writer et charge le document de métadonnées de l’enregistreur du writer dans l’objet.

Comme c’était le cas lors de la sauvegarde, pour initier la coopération entre lui-même et les rédacteurs du système, un demandeur doit générer un événement d' [*identification*](vssgloss-i.md) en appelant [**IVssBackupComponents :: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata). Il n’est pas nécessaire d’appeler [**IVssBackupComponents :: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) après l’achèvement de [**GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata). Les enregistreurs qui ne parviennent pas à traiter l’événement d' [*identification*](vssgloss-i.md) ne seront pas inclus dans la liste des enregistreurs fournissant les métadonnées à retourner par [**IVssBackupComponents :: GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) et [**IVssBackupComponents :: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) (consultez Détermination de l’état de l' [enregistreur](determining-writer-status.md)).

Comme pour l’opération de sauvegarde, un demandeur devra interroger et analyser les informations contenues dans le document sur les composants de sauvegarde et les comparer aux données dans les documents de métadonnées de l’enregistreur pour déterminer les composants qui ont été sauvegardés et choisir ceux à restaurer (voir [vue d’ensemble de la préparation à la restauration](overview-of-preparing-for-restore.md)). En outre, le demandeur doit générer une liste détaillée contenant des informations sur les fichiers sur le support de sauvegarde sélectionné pour la restauration, ainsi que sur la manière et l’emplacement de restauration. (Voir [génération d’un jeu de restauration](generating-a-restore-set.md).)

Par conséquent, certaines applications de sauvegarde peuvent être utiles à stocker sur le support de sauvegarde leur propre liste (dans leur propre format optimisé) des fichiers et leur auteur, composant, procédure de restauration et informations d’emplacement associés. Cette liste peut être utilisée pour réduire la quantité d’analyses et de comparaison des documents de métadonnées de l’enregistreur et les documents du composant de sauvegarde nécessaires à la prise en charge d’une restauration.

## <a name="writer-actions-during-restore-initialization"></a>Actions d’écriture pendant l’initialisation de la restauration

Comme c’est le cas lors d’une opération de restauration, en réponse à l’événement d’identification, VSS appelle la méthode de gestionnaire virtuelle [**CVssWriter :: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)de chaque enregistreur.

Notez que les applications autres que le demandeur actuel (par exemple, les applications système) peuvent générer des événements d’identification, qui doivent être gérés par le writer. En outre, il n’existe aucun moyen pour un writer de déterminer à partir de [**CVssWriter :: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) l’application qui a généré l’événement d’identification.

Étant donné qu’un writer peut recevoir plusieurs événements d’identification lors du traitement d’une opération de restauration, les enregistreurs ne doivent jamais définir d’informations d’État dans le gestionnaire [**CVssWriter :: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) . Au lieu de cela, ils doivent utiliser le même algorithme pour créer le document de métadonnées de l’enregistreur que lors des opérations de sauvegarde (pour plus d’informations, consultez [actions de l’enregistreur pendant l’initialisation](overview-of-backup-initialization.md) de la sauvegarde).

 

 



