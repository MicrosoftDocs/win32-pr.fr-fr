---
title: Implémentation du canal Server-Side
description: Les programmes serveur pour les applications distribuées qui utilisent des canaux n’ont pas besoin d’implémenter de fonctions push, pull ou Alloc.
ms.assetid: de733075-5767-4d46-b294-089c7e3cc695
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6927350e10061850c5fac0ab0db7c18570dd2bab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029468"
---
# <a name="server-side-pipe-implementation"></a><span data-ttu-id="5cedd-103">Implémentation du canal Server-Side</span><span class="sxs-lookup"><span data-stu-id="5cedd-103">Server-Side Pipe Implementation</span></span>

<span data-ttu-id="5cedd-104">Les programmes serveur pour les applications distribuées qui utilisent des canaux n’ont pas besoin d’implémenter de fonctions push, pull ou Alloc.</span><span class="sxs-lookup"><span data-stu-id="5cedd-104">Server programs for distributed applications that use pipes need not implement any push, pull, or alloc functions.</span></span> <span data-ttu-id="5cedd-105">Ils doivent contenir des procédures que les clients peuvent appeler à distance pour initier des transferts de données.</span><span class="sxs-lookup"><span data-stu-id="5cedd-105">They do need to contain procedures that clients can invoke remotely to initiate data transfers.</span></span> <span data-ttu-id="5cedd-106">Dans les rubriques suivantes, cette section explique comment implémenter les procédures distantes du serveur.</span><span class="sxs-lookup"><span data-stu-id="5cedd-106">In the following topics, this section explains how the server's remote procedures can be implemented.</span></span>

-   [<span data-ttu-id="5cedd-107">Implémentation de canaux d’entrée sur le serveur</span><span class="sxs-lookup"><span data-stu-id="5cedd-107">Implementing Input Pipes on the Server</span></span>](implementing-input-pipes-on-the-server.md)
-   [<span data-ttu-id="5cedd-108">Implémentation de canaux de sortie sur le serveur</span><span class="sxs-lookup"><span data-stu-id="5cedd-108">Implementing Output Pipes on the Server</span></span>](implementing-output-pipes-on-the-server.md)

 

 




