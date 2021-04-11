---
description: La restauration de fichiers sur un système en cours d’exécution peut être problématique. Il est important que les applications en cours d’exécution (Writers) indiquent ce qu’il faut faire lorsque des problèmes surviennent pendant les restaurations, par exemple, si le fichier en cours de restauration est en cours d’utilisation.
ms.assetid: 2cb963a8-7077-4419-96d8-cba0fd011e4f
title: Configurations de restauration VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f13acfc59f250a859e9c62f2df2e1b1b982608ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113178"
---
# <a name="vss-restore-configurations"></a>Configurations de restauration VSS

La restauration de fichiers sur un système en cours d’exécution peut être problématique. Il est important que les applications en cours d’exécution (Writers) indiquent ce qu’il faut faire lorsque des problèmes surviennent pendant les restaurations, par exemple, si le fichier en cours de restauration est en cours d’utilisation.

Sous VSS, les rédacteurs disposent de deux méthodes complémentaires pour gérer les restaurations : les [*méthodes de restauration*](vssgloss-r.md) et les [*cibles de restauration*](vssgloss-r.md).

En outre, les demandeurs peuvent choisir de restaurer les fichiers aux emplacements précédemment non spécifiés et de notifier les enregistreurs (voir [**IVssBackupComponents :: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)).

La méthode Restore (également appelée cible de restauration d’origine) est spécifiée par un enregistreur à l’heure de la sauvegarde et définit une définition à l’aide de l’enregistreur de la méthode à utiliser pour restaurer tous ses composants à l’avenir. Tous les fichiers et les composants gérés par un enregistreur partagent la même méthode de restauration.

Les cibles de restauration permettent aux rédacteurs de modifier le mode de restauration des composants spécifiques au moment de la restauration. Contrairement aux méthodes de restauration, les cibles de restauration sont définies pour un jeu de composants.

Une présentation détaillée de l’utilisation des méthodes de restauration et des cibles de restauration se trouve dans les rubriques ci-dessous :

-   [État de restauration VSS](vss-restore-state.md)
-   [Définition des méthodes de restauration VSS](setting-vss-restore-methods.md)
-   [Définition des cibles de restauration VSS](setting-vss-restore-targets.md)
-   [Définition des options de restauration VSS](setting-vss-restore-options.md)

(Pour plus d’informations sur les restaurations qui n’utilisent pas ces mécanismes, consultez [restaurations sans participation au rédacteur](restores-without-writer-participation.md).)

 

 



