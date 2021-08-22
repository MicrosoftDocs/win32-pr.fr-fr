---
description: Windows sockets 2 continue à prendre en charge tous les Windows sockets 1,1 et les appels de fonction, à l’exception de ceux qui traitent du pseudo-blocage.
ms.assetid: e4dc4019-d421-49b8-825a-faa6d5f5fcae
title: Windows Problèmes de compatibilité des sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3fa7aba32ed74f04b04d717e0b2897dc92e0c78079d2a8c20e2c3bcdd85191
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051467"
---
# <a name="windows-sockets-compatibility-issues"></a>Windows Problèmes de compatibilité des sockets

Windows sockets 2 continue à prendre en charge tous les Windows sockets 1,1 et les appels de fonction, à l’exception de ceux qui traitent du pseudo-blocage. étant donné que les Windows sockets 2 s’exécutent uniquement dans des environnements de 32 bits et préventifs, il n’est pas nécessaire d’implémenter le pseudo-blocage trouvé dans Windows sockets 1,1. cela signifie que le code d’erreur WSAEINPROGRESS ne sera jamais indiqué et que les fonctions Windows sockets 1,1 suivantes ne sont pas disponibles pour les applications Windows sockets 2 :

-   WSACancelBlockingCall
-   WSAIsBlocking
-   WSASetBlockingHook
-   WSAUnhookBlockingHook

Windows Les sockets 1,1 les programmes écrits pour utiliser le Pseudo-blocage continuent de fonctionner correctement, car ils sont liés à Winsock.dll ou Wsock32.dll. les deux continuent à prendre en charge l’ensemble complet de fonctions de Windows sockets 1,1. pour que les programmes deviennent Windows applications sockets 2, une modification du code doit se produire. Dans la plupart des cas, l’utilisation judicieuse des threads peut être substituée pour prendre en charge le traitement effectué avec une fonction de raccordement de blocage.

 

 



