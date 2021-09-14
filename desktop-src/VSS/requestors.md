---
description: Un demandeur est une application qui utilise l’API VSS (plus précisément l’interface IVssBackupComponents) pour demander les services de la Service VSS de créer et gérer des clichés instantanés et des jeux de clichés instantanés d’un ou de plusieurs volumes.
ms.assetid: e49920d0-5b66-4aa1-b3ca-641629df5f8a
title: Requesters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b676b8cd287365b257e3b6ee85a7e47a70f88ef3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414591"
---
# <a name="requesters"></a>Requesters

Un [*demandeur*](vssgloss-r.md) est une application qui utilise l’API VSS (plus précisément l’interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) ) pour demander les services de la service VSS de créer et gérer des clichés instantanés et des jeux de clichés instantanés d’un ou de plusieurs volumes.

L’exemple le plus courant d’un demandeur (et le seul qui est traité dans cette documentation) est une application de sauvegarde/restauration prenant en charge VSS, qui utilise des données copiées en miroir comme source stable pour ses opérations de sauvegarde.

En plus d’initier des clichés instantanés, les applications de demandeurs de sauvegarde/récupération communiquent avec les producteurs de données (rédacteurs) pour collecter des informations sur le système et pour signaler aux rédacteurs de préparer leurs données pour la sauvegarde.

## <a name="requester-state"></a>État du demandeur

Un demandeur conserve ses informations d’État dans un objet de métadonnées XML appelé le document sur les composants de sauvegarde. Les métadonnées du demandeur sont nécessaires, mais pas suffisantes pour permettre à un demandeur de sauvegarder, puis de restaurer un système de fichiers. Les raisons sont les suivantes :

-   Au cours d’une opération de sauvegarde, seul un sous-ensemble de tous les composants impliqués dans la sauvegarde (non [*sélectionnables pour*](vssgloss-s.md) les composants de sauvegarde sans sélectionnable pour les ancêtres de sauvegarde et sélectionnables pour les composants de sauvegarde [*inclus explicitement*](vssgloss-e.md) dans la sauvegarde) a vu leurs informations ajoutées au document des composants de sauvegarde du demandeur.
-   Les informations, même pour les composants ajoutés au document des composants de sauvegarde sont incomplètes, les spécifications de fichier et de chemin d’accès ne sont pas incluses.
-   Pendant les opérations de restauration, un composant [*inclus implicitement*](vssgloss-i.md) dans la sauvegarde peut être [*sélectionnable pour la restauration*](vssgloss-s.md) et peut donc être inclus explicitement dans la restauration. Cela nécessite la mise à jour du document des composants de sauvegarde du demandeur avec les informations des copies stockées du document des métadonnées de l’enregistreur d’un writer.

Pour permettre la spécification complète d’une opération de sauvegarde ou de restauration, l’API VSS permet au demandeur d’interroger les métadonnées des enregistreurs en cours d’exécution (pendant les sauvegardes) ou d’examiner les métadonnées de l’enregistreur stocké (pendant les restaurations). En outre, un enregistreur peut modifier les informations sur les composants dans le document des composants de sauvegarde au cours d’une opération de sauvegarde ou de restauration.

À l’aide des informations sur les composants qui ont été sélectionnés pour la sauvegarde et la restauration et les règles relatives à la sélection des composants (pour plus d’informations, voir Configuration de l' [Organisation des composants](definition-of-components-by-writers.md) et [utilisation de la sélectivité et des chemins logiques](working-with-selectability-and-logical-paths.md)), un demandeur peut déterminer les fichiers dont il a besoin pour la sauvegarde ou la restauration, et où il peut trouver ces fichiers.

Dans le cadre d’une sauvegarde, les métadonnées du demandeur et de l’enregistreur doivent être stockées pour pouvoir être utilisées dans la restauration. Inversement, les opérations de restauration requièrent la récupération des anciens composants de sauvegarde et des documents de métadonnées d’écriture pour obtenir des instructions complètes sur la restauration des fichiers.

## <a name="requester-interprocess-communication"></a>Communication interprocessus du demandeur

Le demandeur conserve le contrôle des opérations de sauvegarde et de restauration VSS en générant des événements COM via différents appels dans l’API du demandeur. Ces appels peuvent effectuer les opérations suivantes :

-   Effectuer des demandes des fournisseurs, par exemple, [**IVssBackupComponents ::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) oblige le fournisseur à créer un cliché instantané du volume sélectionné.
-   Déclenchez les enregistreurs pour retourner des informations, par exemple, [**IVssBackupComponents :: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) permet au demandeur d’obtenir le document de métadonnées d’écriture de chaque Writer.
-   Demandez aux rédacteurs de préparer ou de gérer les différentes phases du cliché instantané et des opérations de sauvegarde, par exemple, [**IVssBackupComponents ::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) signale les Writers à configurer pour le gel des e/s.

Un demandeur reçoit des informations des enregistreurs par le biais de documents de métadonnées de l’enregistreur en direct ou stocké et à l’aide de l’interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , que l’enregistreur peut mettre à jour.

## <a name="life-cycle-of-a-requester-during-backup"></a>Cycle de vie d’un demandeur pendant la sauvegarde

Voici un résumé du cycle de vie du demandeur pour la sauvegarde :

1.  Instancier et initialiser des interfaces API VSS.
2.  Contacter les auteurs et récupérer leurs informations.
3.  Choisissez les données à sauvegarder.
4.  Demandez un cliché instantané du fournisseur.
5.  Sauvegardez les données.
6.  Libérez l’interface et le cliché instantané.

## <a name="life-cycle-of-a-requester-during-restore"></a>Cycle de vie d’un demandeur pendant la restauration

Le cycle de vie de restauration ne nécessite pas de cliché instantané, mais nécessite toujours la coopération de l’enregistreur :

1.  Instanciez les interfaces API VSS.
2.  Initialisez le demandeur pour l’opération de restauration en chargeant un document de composants de sauvegarde stocké.
3.  Récupérez les métadonnées de l’enregistreur stocké et les documents des composants de sauvegarde.
4.  Contactez les rédacteurs pour initialiser la coopération.
5.  Recherchez les mises à jour de l’enregistreur dans le document sur les composants de sauvegarde.
6.  Restaurer les données.

 

 



