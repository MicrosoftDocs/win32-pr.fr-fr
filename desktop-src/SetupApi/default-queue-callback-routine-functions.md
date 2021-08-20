---
description: Les fonctions suivantes sont utilisées avec la routine de rappel de file d’attente par défaut.
ms.assetid: 2122c1cf-3ea9-4601-8a2e-dd991b09edc2
title: Fonctions de routine de rappel de file d’attente par défaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11e1999ccbeee3e98d87ea1461df843522310f44fefd198a22ffd6694ab49552
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117966006"
---
# <a name="default-queue-callback-routine-functions"></a>Fonctions de routine de rappel de file d’attente par défaut

Les fonctions suivantes sont utilisées avec la routine de rappel de file d’attente par défaut.



| Fonction                                                                   | Description                                                                                                                                                                            |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)             | Routine de rappel de file d’attente par défaut.                                                                                                                                                    |
| [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback)     | Initialise les informations de contexte nécessaires à la routine de rappel de file d’attente par défaut.                                                                                                          |
| [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) | Initialise les informations de contexte nécessaires à la routine de rappel de file d’attente par défaut et spécifie une autre fenêtre pour afficher les messages de progression.                                           |
| [**SetupTermDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback)     | Libère les ressources allouées par [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) et [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex). |



 

 

 



