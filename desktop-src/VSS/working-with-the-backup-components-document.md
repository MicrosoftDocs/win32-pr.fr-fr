---
description: Un demandeur crée un document de composants de sauvegarde au début de l’exécution d’une sauvegarde.
ms.assetid: 5e40e45d-6afa-401a-a6b4-7bec460cb9ec
title: Utilisation du document sur les composants de sauvegarde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40d5d3c97696b85d589501f6d3af0b6c7d0e6d47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519304"
---
# <a name="working-with-the-backup-components-document"></a>Utilisation du document sur les composants de sauvegarde

Un demandeur crée un document de composants de sauvegarde au début de l’exécution d’une sauvegarde. Le document ne contient initialement qu’une description de l’état de l’opération de sauvegarde. Pendant la restauration, le document doit fournir des instructions sur la façon dont un demandeur doit effectuer la copie des fichiers sur le disque. Au cours de l’opération de restauration, le document composants de sauvegarde est modifié et contient l’état de cette opération.

Contrairement au document de métadonnées de l’enregistreur, qui est en lecture seule, il existe une fenêtre dans laquelle le document des composants de sauvegarde peut être modifié par les demandeurs et les rédacteurs. Le document peut être mis à jour jusqu’à la génération d’un événement [*BackupComplete*](vssgloss-b.md) ou [*BackupShutdown*](vssgloss-b.md) pendant les opérations de sauvegarde et jusqu’à un événement [*postRestore*](vssgloss-p.md) lors de la restauration.

Pour utiliser le document des composants de sauvegarde d’un demandeur, vous devez comprendre les sujets suivants :

-   [Cycle de vie des documents des composants de sauvegarde](backup-components-document-life-cycle.md)
-   [Contenu du document des composants de sauvegarde](backup-components-document-contents.md)

 

 



