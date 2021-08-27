---
description: Fonctions de débogage d’attente
ms.assetid: 784ef76e-3c17-45e0-9a0b-656c11c71322
title: Fonctions de débogage d’attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f2aabec60a14ff36d74298a21d31c91b4bc6d94
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884026"
---
# <a name="wait-debugging-functions"></a>Fonctions de débogage d’attente

Microsoft DirectShow fournit plusieurs fonctions pour déboguer des attentes infinies.

dans les versions commerciales, les fonctions [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) et [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) fonctionnent comme leurs équivalents API Windows, **WaitForMultipleObjects** et **WaitForSingleObject**, avec des intervalles de délai d’attente infinis.

Dans les versions Debug, ces fonctions utilisent une valeur de délai d’attente globale. Si le délai d’attente expire, la fonction déclenche une assertion. La clé de Registre suivante spécifie la valeur du délai d’attente, en millisecondes :

**\_ \_ \\ &lt; DebugRoot &gt; \\ <Module Name> \\ du délai d’expiration de la machine locale HKEY**

où *&lt; DebugRoot &gt;* est le chemin d’accès au registre décrit dans la rubrique [fonctions de sortie de débogage](debug-output-functions.md).

Si la clé n’existe pas, la valeur du délai d’attente est définie par défaut sur Infinite. Vous pouvez utiliser la fonction [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) pour remplacer l’entrée de registre.



| Fonction                                                       | Description                                                     |
|----------------------------------------------------------------|-----------------------------------------------------------------|
| [**DbgSetWaitTimeout**](dbgsetwaittimeout.md)                 | Définit la valeur du délai d’attente du débogage.                              |
| [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) | Attend qu’un ou plusieurs des objets spécifiés soient signalés. |
| [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md)       | Attend qu’un objet soit signalé.                         |



 

 

 



