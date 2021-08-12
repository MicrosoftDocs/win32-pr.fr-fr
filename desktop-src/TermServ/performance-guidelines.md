---
title: Recommandations sur les performances
description: Instructions pour le développement d’applications qui fonctionnent correctement dans un environnement de Services Bureau à distance.
ms.assetid: 50f0c1f6-8046-4ceb-b2c4-6fc1ae86fd73
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97a8211f12e4a89c5dfb309bb4e3c0f998159738b46185aeb5dcee7a5cd29f93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118605311"
---
# <a name="performance-guidelines"></a>Recommandations sur les performances

Les sections suivantes fournissent des instructions pour le développement d’applications qui fonctionnent correctement dans un environnement de Services Bureau à distance.

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[Effets graphiques](graphic-effects.md)
</dt> <dd>

Liste des fonctionnalités qui doivent être désactivées lors de l’exécution en tant que session à distance dans un environnement de Services Bureau à distance.

</dd> <dt>

[Instructions pour les tâches en arrière-plan dans Services Bureau à distance](background-tasks.md)
</dt> <dd>

Pour optimiser la disponibilité du processeur pour tous les utilisateurs, désactivez les tâches en arrière-plan lors de l’exécution dans un environnement Services Bureau à distance ou créez des tâches en arrière-plan efficaces qui ne nécessitent pas beaucoup de ressources.

</dd> <dt>

[Utilisation de threads](thread-usage.md)
</dt> <dd>

Vous devez ajuster et équilibrer l’utilisation des threads d’application pour un environnement multi-utilisateur, multiprocesseur Services Bureau à distance.

</dd> <dt>

[Détection de l’environnement de Services Bureau à distance](detecting-the-terminal-services-environment.md)
</dt> <dd>

Pour optimiser les performances, il est recommandé que les applications détectent si elles s’exécutent dans une session cliente Services Bureau à distance.

</dd> </dl>

Vérifiez les fuites de mémoire de votre application et résolvez les problèmes éventuels. Bien entendu, il s’agit d’un bon conseil pour n’importe quelle application, mais dans un environnement Services Bureau à distance, une application peut être exécutée plusieurs fois par plusieurs utilisateurs, ce qui a pour effet d’agrandir rapidement l’effet d’une fuite de mémoire.

Les animations, les grandes images, l’audio et d’autres services gourmands en bande passante doivent être configurables. Lorsque ces services ne sont pas la fonction principale, ils peuvent être désactivés par défaut pour les sessions à distance, mais activés lorsqu’une session s’exécute localement ou sur une connexion à bande passante élevée. Si l’objectif d’une application est de fournir des services à bande passante élevée, tels que des diffusions vidéo en continu, il n’est pas nécessaire que le service soit désactivé par défaut.

 

 




