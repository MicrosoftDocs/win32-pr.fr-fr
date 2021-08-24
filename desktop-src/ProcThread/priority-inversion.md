---
description: Une inversion de priorité se produit lorsque deux threads ou plus avec des priorités différentes sont en conflit pour être planifiés.
ms.assetid: 1cb2f3c9-4641-40d8-892c-768abaf6affb
title: Inversion de priorité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09a891655196b8f7e81c118d39fb8516a244411f1f4f6d9505e2fb40818d71f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031929"
---
# <a name="priority-inversion"></a>Inversion de priorité

Une inversion de priorité se produit lorsque deux threads ou plus avec des priorités différentes sont en conflit pour être planifiés. Prenons un cas simple avec trois threads : thread 1, thread 2 et thread 3. Le thread 1 est prioritaire et est prêt à être planifié. Thread 2, un thread de faible priorité, exécute du code dans une section critique. Thread 1, le thread de priorité élevée, commence à attendre une ressource partagée du thread 2. Le thread 3 a une priorité moyenne. Le thread 3 reçoit tout le temps processeur, car le thread de priorité élevée (thread 1) attend des ressources partagées du thread de faible priorité (thread 2). Le thread 2 ne laisse pas la section critique, car il n’a pas la priorité la plus élevée et n’est pas planifié.

Le planificateur résout ce problème en renforçant de façon aléatoire la priorité des threads prêts (dans ce cas, les détenteurs de verrou basse priorité). Les threads de faible priorité s’exécutent suffisamment longtemps pour quitter la section critique et le thread de priorité élevée peut entrer dans la section critique. Si le thread de faible priorité ne dispose pas de suffisamment de temps processeur pour quitter la section critique la première fois, il obtiendra une autre chance au cours de la prochaine période de planification.

 

 



