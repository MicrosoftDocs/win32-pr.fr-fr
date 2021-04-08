---
description: COM+ tente d’éviter les situations dans lesquelles ces chemins d’erreurs doivent être exécutés sur un serveur.
ms.assetid: 0de125a2-2e91-49b9-a903-6c2e173e22a2
title: Concepts de la passerelle d’activation COM+ Low-Memory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d844a0492301ef067f5b3cd0e0749ec3a21779
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "103953303"
---
# <a name="com-low-memory-activation-gates-concepts"></a>Concepts de la passerelle d’activation COM+ Low-Memory

En règle générale, la synchronisation n’est pas requise lorsque vous avez un thread cloisonné (STA, Single-Threaded Apartment) car le cloisonnement fournit la synchronisation pour vous. La synchronisation devient importante lorsque vous avez un cloisonnement multithread (MTA) et un objet à thread libre. Dans le passé, les objets à thread libre devaient gérer le verrouillage. Vous pouvez éliminer la nécessité d’utiliser le verrouillage en définissant l’attribut de synchronisation d’un composant.

Les problèmes de fiabilité se produisent souvent lorsque les ressources d’un serveur ne peuvent pas réagir efficacement aux pics de charge. Lorsqu’un serveur ne dispose pas de suffisamment de ressources physiques pour répondre aux pics de demande, il peut épuiser la mémoire virtuelle. Cela devient problématique si le code utilisateur ou le code système ne gère pas correctement les échecs d’allocation de mémoire. Le serveur commence à ralentir et, comme la mémoire est épuisée, les allocations de mémoire échouent. Le serveur exécute les chemins d’accès d’erreur pour gérer les échecs d’allocation. Si un chemin d’accès d’erreur contient un bogue dans le code système ou utilisateur s’exécutant sur le serveur, il est extrêmement difficile de l’intercepter et de le gérer en toute sécurité.

COM+ tente d’éviter les situations dans lesquelles ces chemins d’erreurs doivent être exécutés sur un serveur. Grâce à la fonctionnalité des portes d’activation de faible mémoire, COM+ surveille de manière proactive la charge mémoire dans le système et s’assure qu’une quantité raisonnable de mémoire est disponible avant l’exécution du code utilisateur. Si le pourcentage de mémoire virtuelle disponible pour l’application passe sous un seuil fixe, l’activation échoue avant la création d’une application ou d’un objet serveur COM+ (comme indiqué dans l’illustration ci-dessous). En faisant échouer ces activations normalement exécutées, les portes d’activation de faible mémoire réduisent les problèmes liés aux allocations de mémoire dans le code utilisateur, ce qui améliore considérablement la fiabilité du système.

![Diagramme qui montre la relation entre une application COM+ et une porte d’activation de faible mémoire.](images/ada5ef02-f2b1-46bb-b0fc-fe7d65f31b43.png)

La fonctionnalité des portes d’activation de faible mémoire s’applique uniquement aux composants COM configurés qui sont installés dans une application COM+.

## <a name="how-the-low-memory-activation-gates-feature-works"></a>Fonctionnement de la fonctionnalité portes d’activation Low-Memory

La fonctionnalité des portes d’activation de faible mémoire utilise un niveau de seuil fixe différent selon le type d’activation. Lors de la création d’une application serveur COM+, COM+ autorise l’activation si plus de 10% de la mémoire virtuelle est disponible. Si moins de 10% sont disponibles, COM+ effectue une allocation de test pour déterminer si le fichier d’échange peut s’étendre pour s’adapter à la nouvelle charge mémoire. Si le fichier d’échange est développé, l’application serveur est créée. Si le fichier d’échange ne peut pas être développé, l’activation échoue et la mémoire n’est pas allouée.

Le processus est similaire lors de la création d’un objet. Dans ce cas, COM+ autorise l’activation si plus de 5% de la mémoire virtuelle est disponible. Si moins de 5% sont disponibles, COM+ effectue une allocation de test. Là encore, si l’allocation de test développe le fichier d’échange, l’objet est créé. Si ce n’est pas le cas, l’activation échoue.

Les niveaux de seuil fixe pour les portes d’activation de faible mémoire ne sont pas configurables actuellement. Pour cette raison, aucune tâche n’est associée à cette fonctionnalité.

 

 



