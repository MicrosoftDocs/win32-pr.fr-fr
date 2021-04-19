---
description: Opérations de Pseudo-blocage Pseudoblocking dans Windows Sockets (Winsock).
ms.assetid: fa8f29f1-bb4f-4814-ab8a-52d3c83232bb
title: Pseudo-blocage et blocage réel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 082992aba884aebec30d35bc65d2cb6c49e29051
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518612"
---
# <a name="pseudo-blocking-and-true-blocking"></a>Pseudo-blocage et blocage réel

Dans 16 environnements Windows, le blocage réel n’est pas pris en charge par le système d’exploitation. par conséquent, une opération de blocage qui ne peut pas être effectuée immédiatement est gérée comme suit :

-   Le fournisseur de services lance l’opération, puis entre une boucle au cours de laquelle il distribue les messages Windows (ce qui produit le processeur à un autre thread si nécessaire)
-   Il vérifie ensuite la fin de la fonction Windows Sockets.
-   Si la fonction est terminée, ou si [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) a été appelé, la boucle est arrêtée et la fonction de blocage se termine avec un résultat approprié.

C’est ce que signifie le terme Pseudo-blocage, et la boucle mentionnée ci-dessus est connue sous le nom de hook de blocage par défaut.

 

 
