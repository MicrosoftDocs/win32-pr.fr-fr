---
title: Localité temporelle
description: La localité temporelle est une stratégie d’évitement qui réduit la fenêtre pour les mises à jour partielles.
ms.assetid: 8f454087-46cb-4fa6-b83a-65b2393029c3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceecff05d031875178b6192e7c633f70e4c91c50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462003"
---
# <a name="temporal-locality"></a>Localité temporelle

La *localité temporelle* est une stratégie d’évitement qui réduit la fenêtre pour les mises à jour partielles. La réplication des modifications à partir d’un réplica source donné se poursuit par ordre USN croissant. Les écritures qui se produisent de façon rapprochée dans le temps comportent des USN qui sont « proches » les uns des autres et qui sont propagés de façon rapprochée dans le temps. Les applications qui créent ou mettent à jour plusieurs objets connexes doivent écrire les objets le plus près possible dans le temps. Par exemple, l’application peut collecter toutes les entrées nécessaires de l’utilisateur et les appliquer au répertoire lorsque l’utilisateur clique sur le bouton « appliquer ».

La localité temporelle réduit également les risques de résolution des collisions introduisant des incohérences intra-objets.

 

 




