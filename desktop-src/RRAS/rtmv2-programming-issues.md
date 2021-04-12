---
title: Problèmes de programmation RTMv2
description: Les fonctions RTMv2 sont écrites avec les hypothèses suivantes.
ms.assetid: c8c6f553-57cc-4eec-bbc0-b6b50897cc75
keywords:
- Problèmes de programmation, RTMv2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b607adc939ff72a4d9fee99c15f6aa5192fa4c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309962"
---
# <a name="rtmv2-programming-issues"></a><span data-ttu-id="762a9-104">Problèmes de programmation RTMv2</span><span class="sxs-lookup"><span data-stu-id="762a9-104">RTMv2 Programming Issues</span></span>

<span data-ttu-id="762a9-105">Les fonctions RTMv2 sont écrites avec les hypothèses suivantes.</span><span class="sxs-lookup"><span data-stu-id="762a9-105">RTMv2 functions are written with the following assumptions.</span></span>

-   <span data-ttu-id="762a9-106">Les fonctions RTMv2 n’allouent pas de mémoire pour le client.</span><span class="sxs-lookup"><span data-stu-id="762a9-106">RTMv2 functions do not allocate memory for the client.</span></span> <span data-ttu-id="762a9-107">Le client doit toujours allouer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="762a9-107">The client must always allocate memory.</span></span>
-   <span data-ttu-id="762a9-108">Lors de l’annulation de l’inscription d’un client, celui-ci doit effectuer des opérations de nettoyage, telles que la libération de la mémoire allouée.</span><span class="sxs-lookup"><span data-stu-id="762a9-108">When a client is unregistering, it must perform clean-up operations itself, such as releasing all memory allocated.</span></span>
-   <span data-ttu-id="762a9-109">Les clients doivent libérer correctement les handles. des fuites de mémoire peuvent se produire si un client ne respecte pas cette pratique.</span><span class="sxs-lookup"><span data-stu-id="762a9-109">Clients must release handles correctly; memory leaks can occur if a client does not observe this practice.</span></span>

 

 




