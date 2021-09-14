---
description: Le gestionnaire des ressources s’exécute en tant que service approuvé dans un processus unique. Toutes les demandes d’accès par carte à puce sont envoyées au gestionnaire de ressources, qui les achemine vers le lecteur qui contient la carte ciblée.
ms.assetid: 4a62588a-14d9-43dc-9572-25a9cbcd0efd
title: Implémentation de Gestionnaire des ressources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04ec653f999b74bb9851893b11e1fa49120a7bd6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229061"
---
# <a name="resource-manager-implementation"></a>Implémentation de Gestionnaire des ressources

Le [*Gestionnaire des ressources*](../secgloss/r-gly.md) s’exécute en tant que service approuvé dans un processus unique. Toutes les demandes d’accès par [*carte à puce*](../secgloss/s-gly.md) sont envoyées au gestionnaire de ressources, qui les achemine vers le [*lecteur*](../secgloss/r-gly.md) qui contient la carte ciblée.

Les cartes à puce sont souvent utilisées conjointement à la sécurité et à la confidentialité personnelle. Dans la mesure du possible, Resource Manager utilise les mécanismes de sécurité existants dans le système d’exploitation sous-jacent lors de l’accès à un lecteur ou une carte à puce.

 

 
