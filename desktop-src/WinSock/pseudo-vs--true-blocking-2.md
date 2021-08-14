---
description: opérations de pseudo-blocage Pseudoblocking dans les sockets de Windows (Winsock).
ms.assetid: fa8f29f1-bb4f-4814-ab8a-52d3c83232bb
title: Pseudo-blocage et blocage réel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371935a2f8984ebd080da48492807b3f5ffa9286b991b16b516244ccf26ee093
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740941"
---
# <a name="pseudo-blocking-and-true-blocking"></a>Pseudo-blocage et blocage réel

dans 16 environnements Windows, le blocage réel n’est pas pris en charge par le système d’exploitation. par conséquent, une opération de blocage qui ne peut pas être effectuée immédiatement est gérée comme suit :

-   le fournisseur de services lance l’opération, puis entre une boucle au cours de laquelle il distribue les messages d’Windows (en générant le processeur à un autre thread si nécessaire)
-   il vérifie ensuite la fin de la fonction Windows sockets.
-   Si la fonction est terminée, ou si [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) a été appelé, la boucle est arrêtée et la fonction de blocage se termine avec un résultat approprié.

C’est ce que signifie le terme Pseudo-blocage, et la boucle mentionnée ci-dessus est connue sous le nom de hook de blocage par défaut.

 

 
