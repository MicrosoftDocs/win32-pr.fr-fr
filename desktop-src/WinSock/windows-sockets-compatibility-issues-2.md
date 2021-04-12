---
description: Windows Sockets 2 continue à prendre en charge l’ensemble de la sémantique et des appels de fonction Windows Sockets 1,1, à l’exception de ceux qui traitent d’un Pseudo-blocage.
ms.assetid: e4dc4019-d421-49b8-825a-faa6d5f5fcae
title: Problèmes de compatibilité de Windows Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58495db7ff504b68d0db41104fe0fff79b93f985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201827"
---
# <a name="windows-sockets-compatibility-issues"></a>Problèmes de compatibilité de Windows Sockets

Windows Sockets 2 continue à prendre en charge l’ensemble de la sémantique et des appels de fonction Windows Sockets 1,1, à l’exception de ceux qui traitent d’un Pseudo-blocage. Étant donné que Windows Sockets 2 s’exécute uniquement dans des environnements de 32 bits et de planification préventive, il n’est pas nécessaire d’implémenter le Pseudo-blocage trouvé dans Windows Sockets 1,1. Cela signifie que le code d’erreur WSAEINPROGRESS ne sera jamais indiqué et que les fonctions Windows Sockets 1,1 suivantes ne sont pas disponibles pour les applications Windows Sockets 2 :

-   WSACancelBlockingCall
-   WSAIsBlocking
-   WSASetBlockingHook
-   WSAUnhookBlockingHook

Les programmes Windows Sockets 1,1 écrits pour utiliser le Pseudo-blocage continuent de fonctionner correctement, car ils sont liés à Winsock.dll ou Wsock32.dll. Les deux continuent à prendre en charge l’ensemble complet des fonctions Windows Sockets 1,1. Pour que les programmes deviennent des applications Windows Sockets 2, une modification du code doit se produire. Dans la plupart des cas, l’utilisation judicieuse des threads peut être substituée pour prendre en charge le traitement effectué avec une fonction de raccordement de blocage.

 

 



