---
description: Fonctions de débogage d’attente
ms.assetid: 784ef76e-3c17-45e0-9a0b-656c11c71322
title: Fonctions de débogage d’attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f8f1de3d19ce7408625a5ab42f230d23ce401728e9fa7cf060edae62e19fcfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049199"
---
# <a name="wait-debugging-functions"></a>Fonctions de débogage d’attente

Microsoft DirectShow fournit plusieurs fonctions pour déboguer des attentes infinies.

dans les versions commerciales, les fonctions [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) et [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) fonctionnent comme leurs équivalents API Windows, **WaitForMultipleObjects** et **WaitForSingleObject**, avec des intervalles de délai d’attente infinis.

Dans les versions Debug, ces fonctions utilisent une valeur de délai d’attente globale. Si le délai d’attente expire, la fonction déclenche une assertion. La clé de Registre suivante spécifie la valeur du délai d’attente, en millisecondes :

**% \_ \_ \\ <DebugRoot> \\ <Module Name> \\ d’expiration de l’ordinateur local**

où *<DebugRoot>* est le chemin d’accès au registre décrit dans la rubrique [fonctions de sortie de débogage](debug-output-functions.md).

Si la clé n’existe pas, la valeur du délai d’attente est définie par défaut sur Infinite. Vous pouvez utiliser la fonction [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) pour remplacer l’entrée de registre.



| Fonction                                                       | Description                                                     |
|----------------------------------------------------------------|-----------------------------------------------------------------|
| [**DbgSetWaitTimeout**](dbgsetwaittimeout.md)                 | Définit la valeur du délai d’attente du débogage.                              |
| [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) | Attend qu’un ou plusieurs des objets spécifiés soient signalés. |
| [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md)       | Attend qu’un objet soit signalé.                         |



 

 

 



