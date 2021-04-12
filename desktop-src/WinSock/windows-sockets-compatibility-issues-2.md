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
# <a name="windows-sockets-compatibility-issues"></a><span data-ttu-id="0bffc-103">Problèmes de compatibilité de Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="0bffc-103">Windows Sockets Compatibility Issues</span></span>

<span data-ttu-id="0bffc-104">Windows Sockets 2 continue à prendre en charge l’ensemble de la sémantique et des appels de fonction Windows Sockets 1,1, à l’exception de ceux qui traitent d’un Pseudo-blocage.</span><span class="sxs-lookup"><span data-stu-id="0bffc-104">Windows Sockets 2 continues to support all of the Windows Sockets 1.1 semantics and function calls except for those dealing with pseudo-blocking.</span></span> <span data-ttu-id="0bffc-105">Étant donné que Windows Sockets 2 s’exécute uniquement dans des environnements de 32 bits et de planification préventive, il n’est pas nécessaire d’implémenter le Pseudo-blocage trouvé dans Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="0bffc-105">Since Windows Sockets 2 runs only in 32-bit, preemptively scheduled environments, there is no need to implement the pseudo-blocking found in Windows Sockets 1.1.</span></span> <span data-ttu-id="0bffc-106">Cela signifie que le code d’erreur WSAEINPROGRESS ne sera jamais indiqué et que les fonctions Windows Sockets 1,1 suivantes ne sont pas disponibles pour les applications Windows Sockets 2 :</span><span class="sxs-lookup"><span data-stu-id="0bffc-106">This means that the WSAEINPROGRESS error code will never be indicated and that the following Windows Sockets 1.1 functions are not available to Windows Sockets 2 applications:</span></span>

-   <span data-ttu-id="0bffc-107">WSACancelBlockingCall</span><span class="sxs-lookup"><span data-stu-id="0bffc-107">WSACancelBlockingCall</span></span>
-   <span data-ttu-id="0bffc-108">WSAIsBlocking</span><span class="sxs-lookup"><span data-stu-id="0bffc-108">WSAIsBlocking</span></span>
-   <span data-ttu-id="0bffc-109">WSASetBlockingHook</span><span class="sxs-lookup"><span data-stu-id="0bffc-109">WSASetBlockingHook</span></span>
-   <span data-ttu-id="0bffc-110">WSAUnhookBlockingHook</span><span class="sxs-lookup"><span data-stu-id="0bffc-110">WSAUnhookBlockingHook</span></span>

<span data-ttu-id="0bffc-111">Les programmes Windows Sockets 1,1 écrits pour utiliser le Pseudo-blocage continuent de fonctionner correctement, car ils sont liés à Winsock.dll ou Wsock32.dll.</span><span class="sxs-lookup"><span data-stu-id="0bffc-111">Windows Sockets 1.1 programs that are written to utilize pseudo-blocking will continue to operate correctly since they link to either Winsock.dll or Wsock32.dll.</span></span> <span data-ttu-id="0bffc-112">Les deux continuent à prendre en charge l’ensemble complet des fonctions Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="0bffc-112">Both continue to support the complete set of Windows Sockets 1.1 functions.</span></span> <span data-ttu-id="0bffc-113">Pour que les programmes deviennent des applications Windows Sockets 2, une modification du code doit se produire.</span><span class="sxs-lookup"><span data-stu-id="0bffc-113">In order for programs to become Windows Sockets 2 applications, some code modification must occur.</span></span> <span data-ttu-id="0bffc-114">Dans la plupart des cas, l’utilisation judicieuse des threads peut être substituée pour prendre en charge le traitement effectué avec une fonction de raccordement de blocage.</span><span class="sxs-lookup"><span data-stu-id="0bffc-114">In most cases, the judicious use of threads can be substituted to accommodate processing that was being accomplished with a blocking hook function.</span></span>

 

 



