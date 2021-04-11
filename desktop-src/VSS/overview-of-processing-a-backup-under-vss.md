---
description: Lors du traitement d’une sauvegarde, le demandeur et les rédacteurs coordonnent la mise en place d’une image système stable à partir de laquelle sauvegarder des données (le volume des clichés instantanés), pour regrouper des fichiers en fonction de leur utilisation et pour stocker des informations sur les données enregistrées.
ms.assetid: d7acb2a2-bb58-47e3-a950-d32f663ae36d
title: Vue d’ensemble du traitement d’une sauvegarde sous VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a11aeab87b503241acefdd15a153c9e417e537
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318985"
---
# <a name="overview-of-processing-a-backup-under-vss"></a>Vue d’ensemble du traitement d’une sauvegarde sous VSS

Lors du traitement d’une sauvegarde, le demandeur et les rédacteurs coordonnent la mise en place d’une image système stable à partir de laquelle sauvegarder des données (le volume des clichés instantanés), pour regrouper des fichiers en fonction de leur utilisation et pour stocker des informations sur les données enregistrées. Cela doit être effectué lors de la création d’une interruption minimale du workflow de travail normal de l’enregistreur.

Un demandeur interroge les enregistreurs pour ses métadonnées, traite ces données, notifie les enregistreurs avant le début du cliché instantané et des opérations de sauvegarde, puis notifie à nouveau les Writers après la fin des opérations de sauvegarde et de cliché instantané.

En réponse à ces notifications, le writer fournit des informations sur les fichiers à sauvegarder, y compris la spécification de groupes de fichiers à coordonner ([*composants*](vssgloss-c.md)) — interrompt les opérations d’e/s avant le cliché instantané, puis revient au fonctionnement normal après l’achèvement d’un cliché instantané ou à la fin de la sauvegarde.

Au cours du traitement de la sauvegarde, un enregistreur spécifie les fichiers dont il est responsable par le biais de ses métadonnées en lecture seule : le document de métadonnées de l’enregistreur (voir [métadonnées VSS : utilisation du document de métadonnées de l’enregistreur](working-with-the-writer-metadata-document.md)). Le demandeur interprète ensuite ces métadonnées, choisit les éléments à sauvegarder et stocke ces décisions dans son propre objet de métadonnées, le document sur les composants de sauvegarde (voir [métadonnées VSS : utilisation du document sur les composants de sauvegarde](working-with-the-backup-components-document.md)). Ce document sur les composants de sauvegarde est disponible à des fins d’inspection et de modification du writer au cours des opérations de sauvegarde et de restauration.

Ce diagramme illustre les interactions entre le demandeur, le service VSS, la prise en charge du noyau VSS, tous les enregistreurs VSS impliqués et tous les fournisseurs de matériel VSS.

![interactions entre le demandeur, les composants de sauvegarde, les rédacteurs et les fournisseurs](images/vssimpl.png)

Pour mieux comprendre les tâches de base impliquées dans la réalisation d’une sauvegarde, il est utile de décomposer cette vue d’ensemble dans les rubriques suivantes :

-   [Vue d’ensemble de l’initialisation de la sauvegarde](overview-of-backup-initialization.md)
-   [Vue d’ensemble de la phase de découverte de sauvegarde](overview-of-the-backup-discovery-phase.md)
-   [Vue d’ensemble des tâches de pré-sauvegarde](overview-of-pre-backup-tasks.md)
-   [Vue d’ensemble de la sauvegarde réelle des fichiers](overview-of-actual-backup-of-files.md)
-   [Vue d’ensemble de l’arrêt de la sauvegarde](overview-of-backup-termination.md)

 

 



