---
title: Problèmes de programmation RTMv2
description: Les fonctions RTMv2 sont écrites avec les hypothèses suivantes.
ms.assetid: c8c6f553-57cc-4eec-bbc0-b6b50897cc75
keywords:
- Problèmes de programmation, RTMv2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 584568fc3c4e7a46a2a2114781b81465d893b80978471aa3149d93d38f0c8c5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035589"
---
# <a name="rtmv2-programming-issues"></a>Problèmes de programmation RTMv2

Les fonctions RTMv2 sont écrites avec les hypothèses suivantes.

-   Les fonctions RTMv2 n’allouent pas de mémoire pour le client. Le client doit toujours allouer de la mémoire.
-   Lors de l’annulation de l’inscription d’un client, celui-ci doit effectuer des opérations de nettoyage, telles que la libération de la mémoire allouée.
-   Les clients doivent libérer correctement les handles. des fuites de mémoire peuvent se produire si un client ne respecte pas cette pratique.

 

 




