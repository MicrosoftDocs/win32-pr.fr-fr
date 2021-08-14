---
description: Le gestionnaire des ressources s’exécute en tant que service approuvé dans un processus unique. Toutes les demandes d’accès par carte à puce sont envoyées au gestionnaire de ressources, qui les achemine vers le lecteur qui contient la carte ciblée.
ms.assetid: 4a62588a-14d9-43dc-9572-25a9cbcd0efd
title: Implémentation de Gestionnaire des ressources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9d0dfd21ed7da466f84e867a6d28b0e826fc5c4733f24d2f5e1f0562f1b4156
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919148"
---
# <a name="resource-manager-implementation"></a>Implémentation de Gestionnaire des ressources

Le [*Gestionnaire des ressources*](../secgloss/r-gly.md) s’exécute en tant que service approuvé dans un processus unique. Toutes les demandes d’accès par [*carte à puce*](../secgloss/s-gly.md) sont envoyées au gestionnaire de ressources, qui les achemine vers le [*lecteur*](../secgloss/r-gly.md) qui contient la carte ciblée.

Les cartes à puce sont souvent utilisées conjointement à la sécurité et à la confidentialité personnelle. Dans la mesure du possible, Resource Manager utilise les mécanismes de sécurité existants dans le système d’exploitation sous-jacent lors de l’accès à un lecteur ou une carte à puce.

 

 
