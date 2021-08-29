---
description: Les fonctions d’assistance suivantes peuvent être appelées uniquement par des experts qui exportent la fonction exécuter ou configurer.
ms.assetid: 6890087c-7c94-41ff-bb5c-4bf88a4e07cc
title: Fonctions d’experts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b189f0af3b748bc6ad162342ae23d98cbf0e381232193c114d245fa6aadb77c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779379"
---
# <a name="expert-functions"></a>Fonctions d’experts

Les fonctions d’assistance suivantes peuvent être appelées uniquement par des experts qui exportent la fonction [exécuter](run.md) ou [configurer](configure.md) .



| Fonction                                         | Description                                                                             |
|--------------------------------------------------|-----------------------------------------------------------------------------------------|
| [ExpertGetFrame](expertgetframe.md)             | Récupère un frame donné de la capture.                                               |
| [ExpertIndicateStatus](expertindicatestatus.md) | Indique le pourcentage d’achèvement de l’analyse de capture de l’expert.             |
| [ExpertGetStartupInfo](expertgetstartupinfo.md) | Récupère les informations de démarrage de l’expert.                                       |
| [ExpertMemorySize](expertmemorysize.md)         | Récupère la taille de la mémoire allouée par un appel à la fonction **ExpertAllocMemory** . |
| [ExpertSubmitEvent](expertsubmitevent.md)       | Indique un problème et récupère des informations sur le problème, le cas échéant.          |
| [ExpertAllocMemory](expertallocmemory.md)       | Alloue de la mémoire à l’expert.                                                        |
| [ExpertReallocMemory](expertreallocmemory.md)   | Modifie la taille de la mémoire allouée par la fonction **ExpertAllocMemory** .         |
| [ExpertFreeMemory](expertfreememory.md)         | Libère de la mémoire allouée par l’expert.                                                   |



 

Pour plus d’informations sur les fonctions d’exportation, les fonctions d’assistance qui peuvent être appelées par des experts et des analyseurs, des structures et des énumérations, consultez les rubriques suivantes :



| Pour obtenir des informations sur                                             | Consultez                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------|
| Fonctions exportées par des experts                            | [Fonctions d’exportation de DLL d’experts](expert-dll-export-functions.md)               |
| Structures utilisées par les fonctions d’experts                      | [Structures d’experts](expert-structures.md)                                   |
| Énumérations utilisées par les structures et fonctions d’experts              | [Énumérations d’experts](expert-enumerations.md)                               |
| Fonctions d’assistance courantes qui peuvent être appelées par des experts et des analyseurs | [Fonctions courantes des experts et de l’analyseur](expert-and-parser-common-functions.md) |



 

 

 



