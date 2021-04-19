---
description: Lors du traitement d’une sauvegarde sous VSS, les demandeurs et les Writers ont collaboré pour produire une image système stable à partir de laquelle sauvegarder des données, ce qui nécessitait une coordination et la création d’un cliché instantané du système actuel.
ms.assetid: 1cefb6ac-f2bb-464b-a62f-05be91ae56f7
title: Vue d’ensemble du traitement d’une restauration sous VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0279888b28af82eb1b4b51093b421b9db5e15d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529784"
---
# <a name="overview-of-processing-a-restore-under-vss"></a>Vue d’ensemble du traitement d’une restauration sous VSS

Lors du traitement d’une sauvegarde sous VSS, les demandeurs et les Writers ont collaboré pour produire une image système stable à partir de laquelle sauvegarder des données, ce qui nécessitait une coordination et la création d’un cliché instantané du système actuel.

Contrairement à une sauvegarde VSS, où l’objectif de la coordination des demandeurs et des Writers consiste à produire une image système stable à partir de laquelle copier des données, l’objectif d’une restauration basée sur VSS est de renvoyer des fichiers sur le disque de la manière la plus utile aux applications (Writers) en cours d’exécution sur le système. Cela ne nécessite pas une image système stable, donc aucun cliché instantané n’est nécessaire.

Au lieu de cela, l’attention est axée sur l’évitement de l’interruption de l’activité de l’enregistreur, ce qui empêche la création de jeux de données incohérents sur le disque et permet aux rédacteurs d’évaluer et de fusionner les données si nécessaire.

À l’instar d’une opération de sauvegarde, une restauration VSS requiert l’accès à un document de composants de sauvegarde et à des documents de métadonnées d’écriture. Ces documents ne sont généralement pas obtenus en interrogeant des applications en cours d’exécution, mais ils sont récupérés à partir de versions stockées en tant que documents XML sur un support de sauvegarde.

Comme c’est le cas pendant les opérations de sauvegarde, les documents de métadonnées de l’enregistreur restent des objets en lecture seule et (une fois récupérés) le document des composants de sauvegarde peut encore être modifié. Les modifications apportées au document composants de sauvegarde permettent aux rédacteurs et aux demandeurs de communiquer sur les éléments suivants :

-   Substitution des [*méthodes de restauration*](vssgloss-r.md) avec les [*cibles de restauration*](vssgloss-r.md)
-   Utilisation de [ *mappages d’emplacements secondaires*](vssgloss-a.md)
-   Restauration des fichiers vers les nouveaux emplacements sur le disque
-   Utilisation de différentes règles de sélection de celles utilisées lors de la sauvegarde

Pour mieux comprendre les tâches de base impliquées dans la réalisation d’une restauration, il est utile de décomposer cette vue d’ensemble selon les étapes suivantes :

-   [Vue d’ensemble de l’initialisation de la restauration](overview-of-restore-initialization.md)
-   [Vue d’ensemble de la préparation pour la restauration](overview-of-preparing-for-restore.md)
-   [Vue d’ensemble de la restauration réelle des fichiers](overview-of-actual-file-restoration.md)
-   [Vue d’ensemble du nettoyage et de l’arrêt de la restauration](overview-of-restore-clean-up-and-termination.md)

 

 



