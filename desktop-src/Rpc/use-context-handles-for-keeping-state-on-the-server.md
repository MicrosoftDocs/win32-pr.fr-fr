---
title: Utiliser des handles de contexte pour conserver l’État sur le serveur
description: Utiliser des handles de contexte pour conserver l’État sur le serveur
ms.assetid: ee511745-04cf-445d-a02b-41734aabc193
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90bf14632ed1821a1a097a64951f6ca9aef751d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196833"
---
# <a name="use-context-handles-for-keeping-state-on-the-server"></a><span data-ttu-id="d156b-103">Utiliser des handles de contexte pour conserver l’État sur le serveur</span><span class="sxs-lookup"><span data-stu-id="d156b-103">Use Context Handles for Keeping State on the Server</span></span>

<span data-ttu-id="d156b-104">**Bonne pratique :** Chaque fois que l’État est conservé sur le serveur entre les appels, utilisez des handles de contexte.</span><span class="sxs-lookup"><span data-stu-id="d156b-104">**Best practice:** Whenever state is kept on the server between calls, use context handles.</span></span>

<span data-ttu-id="d156b-105">Les handles de contexte sont souvent intimidants pour les nouveaux programmeurs RPC, et la surcharge des handles de contexte d’apprentissage n’est peut-être pas initialement la peine d’être consentie.</span><span class="sxs-lookup"><span data-stu-id="d156b-105">Context handles are often intimidating for new RPC programmers, and the overhead of learning context handles may not initially appear worth the effort.</span></span> <span data-ttu-id="d156b-106">C’est la raison pour laquelle les descripteurs de contexte ont des solutions intégrées pour de nombreux pièges courants rencontrés dans la programmation réseau qui devraient normalement être implémentés à partir de zéro.</span><span class="sxs-lookup"><span data-stu-id="d156b-106">It is worth it because context handles have built-in solutions for many common pitfalls encountered in network programming that otherwise would have to be implemented from scratch.</span></span> <span data-ttu-id="d156b-107">La compréhension des handles de contexte paye les dividendes ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="d156b-107">Understanding context handles pays dividends later.</span></span>

 

 




