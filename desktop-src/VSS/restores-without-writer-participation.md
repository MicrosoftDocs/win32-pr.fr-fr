---
description: La participation de l’enregistreur dans une sauvegarde VSS est conçue pour permettre aux applications de contrôler l’utilisation de leurs données de restauration.
ms.assetid: 076b2e6f-c2ca-4129-8827-1b18a655d634
title: Restaurations sans participation au rédacteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f89fd5ea855d2d91701d351e860bf966148be587
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414590"
---
# <a name="restores-without-writer-participation"></a>Restaurations sans participation au rédacteur

La participation de l’enregistreur dans une sauvegarde VSS est conçue pour permettre aux applications de contrôler l’utilisation de leurs données de restauration.

En général, si un enregistreur est disponible sur un système, il n’est jamais conseillé de restaurer les données à leur emplacement d’origine sans participation au rédacteur. Une telle restauration rencontre probablement des fichiers de destination verrouillés et risque de corrompre les données.

Toutefois, il existe des raisons pour lesquelles une application de sauvegarde peut vouloir restaurer une sauvegarde VSS sans participation au rédacteur :

-   Les données sont gérées par des applications qui ne prennent pas en charge VSS. Presque tous les systèmes disposent de certaines applications : les éditeurs de texte, les lecteurs de messagerie, les traitements de texte, etc., qui ne sont pas compatibles avec VSS. Ces données ne peuvent pas être restaurées à l’aide de la participation de l’auteur.

    En règle générale, ce type de données n’est pas critique pour le système ou le service, et la restauration ne doit pas être problématique, ou au moins plus problématiques que lors d’une restauration conventionnelle.

    Comme avec les préparations pour les restaurations conventionnelles, si possible, les opérateurs de restauration doivent tenter d’interrompre ou de mettre fin à ces applications avant de démarrer une restauration VSS.

-   Enregistreurs VSS manquants. Cette situation peut être relativement courante lors de la restauration de l’état d’un système endommagé. Une opération de sauvegarde doit déterminer s’il est souhaitable de restaurer des fichiers pour les enregistreurs manquants. Si la restauration est souhaitable, les fichiers peuvent être restaurés de la même manière qu’une sauvegarde conventionnelle les restaure.
-   Restauration privée des données d’un enregistreur. Un demandeur peut choisir de restaurer les données d’un enregistreur en cours d’exécution sur un emplacement privé sans en avertir l’enregistreur. Par exemple, il peut s’agir de la restauration des données du writer pour prendre en charge la comparaison hors connexion. Dans ce type de situation, un demandeur ne souhaite pas utiliser le [*nouvel emplacement cible*](vssgloss-n.md) lors de la restauration, car il ne souhaite pas que le writer accède aux données.
-   Un enregistreur ne doit pas être impliqué lors de la restauration. Un enregistreur indique cela en transmettant VSS \_ WRE \_ jamais pour le paramètre *writerRestore* de [**IVssCreateWriterMetadata :: SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod).
-   Un enregistreur requiert une méthode de restauration personnalisée. Un enregistreur indique qu’il requiert une restauration personnalisée en passant dans VSS \_ RME \_ personnalisé pour le paramètre de *méthode* de [**IVssCreateWriterMetadata :: SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod). Dans ce cas, ce writer ne doit pas être impliqué dans le processus de restauration, sauf si la documentation de restauration personnalisée pour ce writer indique un autre cas.

Un demandeur implique un enregistreur dans le processus de restauration en spécifiant l’un des composants de ce writer dans un appel à [**IVssBackupComponents :: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore). Les données d’un enregistreur peuvent être restaurées sans impliquer l’enregistreur en ne spécifiant simplement aucun des composants de ce writer dans un appel à **IVssBackupComponents :: SetSelectedForRestore**. Si un enregistreur n’attend pas d’événement de restauration, l’implication de cet enregistreur dans le processus de restauration peut entraîner le signalement d’erreurs erronées pour ce writer.

 

 



