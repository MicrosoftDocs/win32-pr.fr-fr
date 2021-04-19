---
title: Instructions pour les tâches en arrière-plan dans Services Bureau à distance
description: Pour optimiser la disponibilité du processeur pour tous les utilisateurs, désactivez les tâches en arrière-plan lors de l’exécution dans un environnement Services Bureau à distance ou créez des tâches en arrière-plan efficaces qui ne nécessitent pas beaucoup de ressources.
ms.assetid: c3688319-dbe7-4be5-8895-622a8f8797d2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b93169b248fb086b7ccad88aa57c0feae171f91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106544136"
---
# <a name="guidelines-for-background-tasks-in-remote-desktop-services"></a>Instructions pour les tâches en arrière-plan dans Services Bureau à distance

Les tâches en arrière-plan (tâches effectuées lorsque la boucle de message d’une application est inactive) fournissent un mécanisme permettant de gérer les tâches de faible priorité dans un environnement à utilisateur unique. Toutefois, dans un environnement Services Bureau à distance, la tâche en arrière-plan d’un utilisateur est en concurrence pour les cycles de processeur avec les tâches de premier plan d’un autre utilisateur. Lorsque plusieurs utilisateurs exécutent des tâches de premier plan et d’arrière-plan, les demandes d’UC sont plus élevées que lorsque tous les utilisateurs exécutent uniquement des tâches de premier plan. Pour optimiser la disponibilité du processeur pour tous les utilisateurs, désactivez les tâches en arrière-plan lors de l’exécution dans un environnement Services Bureau à distance ou créez des tâches en arrière-plan efficaces qui ne nécessitent pas beaucoup de ressources.

Pour plus d’informations, consultez [détection de l’environnement de services Bureau à distance](detecting-the-terminal-services-environment.md). Après avoir détecté l’environnement Services Bureau à distance, vous pouvez désactiver ou reconfigurer des tâches en arrière-plan pour l’application à l’aide du même ensemble d’API que celui utilisé pour gérer les tâches.

 

 




