---
description: Les contextes d’activation sont visibles tout au long du processus.
ms.assetid: 6eda00d5-9dac-4267-bf61-b481814201f8
title: Threads, procédures asynchrones et messages de fenêtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e615eb9795ba32bcf4bd227a4933e890e9b89055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862329"
---
# <a name="using-threads-asynchronous-procedures-and-window-messages"></a>Utilisation de threads, de procédures asynchrones et de messages de fenêtre

Les contextes d’activation sont visibles tout au long du processus. Les piles de contexte d’activation sont toutefois par thread, et deux threads dans le même processus peuvent avoir des piles d’activation différentes. [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread) place automatiquement le contexte d’activation actuel en haut de la pile d’activation du nouveau thread. Cela peut faciliter la mise à niveau du code existant pour utiliser des composants côte à côte, car le nouveau thread peut s’exécuter immédiatement dans le contexte d’activation actuel.

Les appels de procédure asynchrone, les rappels de port de terminaison et tous les autres rappels sur d’autres threads obtiennent automatiquement le contexte d’activation de la source. Lorsque le rappel est appelé, la pile d’activation est nettoyée. Cela signifie que votre application peut utiliser des appels de procédure asynchrones et des rappels sans activer explicitement les contextes, car la gestion du contexte est effectuée par l’infrastructure côte à côte sous-jacente. Pour que d’autres contextes soient actifs pendant un rappel ou un nouveau thread, votre application peut effectuer sa propre gestion de contexte. Dans ce cas, votre programme doit utiliser la séquence correcte des fonctions activation du contexte d’activation et désactiver les fonctions.

Les contextes d’activation sont indépendants du thread. L’activation d’un contexte modifie uniquement la pile du thread actuel et vous ne pouvez pas activer un contexte entre les threads. Le thread A ne peut pas forcer un contexte sur le thread B. Les fonctions de l’API de contexte d’activation prennent également en charge les threads.

Quand vous utilisez [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) ou [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) pour envoyer un message de fenêtre à une autre procédure de fenêtre dans votre processus, le contexte d’activation actuel est activé avant que le message ne soit passé à la procédure cible. Le contexte d’activation actuel est associé au message. Cela permet de s’assurer que les messages qui font référence à des objets COM, aux noms de DLL ou à d’autres ressources côte à côte conservent leurs informations de contexte correctes.

 

 
