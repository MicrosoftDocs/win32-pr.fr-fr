---
title: GUID de cohérence
description: Les GUID de cohérence sont une stratégie de détection qui permet à une application de détecter des mises à jour partielles.
ms.assetid: 3418667f-4d5a-4a4b-b0f5-7744a21608f7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bcfb25d0f04a459217811a2ff0393fac47e3206
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028504"
---
# <a name="consistency-guids"></a>GUID de cohérence

Les GUID de cohérence sont une stratégie de détection qui permet à une application de détecter des mises à jour partielles. Un GUID de cohérence (identificateur global unique) est appliqué à chaque objet dans un ensemble associé. Dans l’implémentation, une application source génère un nouveau GUID et l’applique à chaque objet qu’elle met à jour dans le jeu d’objets connexes. Il applique ensuite le nouveau GUID au reste des objets de l’ensemble, et se termine en appliquant le nouveau GUID à l’objet « Master ». En général, l’objet « maître » est un conteneur qui est le parent des autres objets de l’ensemble.

Quelques points importants à prendre en compte :

-   Les GUID de cohérence combinés avec les nombres d’objets ou les sommes de contrôle sont plus efficaces que les GUID de cohérence seuls, car l’application qui lit les objets peut ne pas savoir combien d’objets avec le GUID doivent être présents.
-   Les applications doivent générer leurs propres GUID (une API Microsoft Win32, UuidCreate, fournit cette fonction) et ne pas utiliser les GUID générés par le système qui se trouvent dans l’attribut **objectGUID** d’un objet. Cela est dû au fait qu’un GUID de cohérence doit changer chaque fois que l’ensemble d’objets est mis à jour. Les GUID d’identité d’objet trouvés dans **objectGUID** ne changent jamais après la création de l’objet.
-   Les GUID de cohérence supposent qu’aucun objet n’est partagé entre les ensembles, donc chaque ensemble peut avoir un GUID de cohérence unique.

 

 




