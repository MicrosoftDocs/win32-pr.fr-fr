---
title: Test et débogage
description: Il y a un \ 0034 ; Echo \ 0034 ; écouteur implémenté par le client Connexion Bureau à distance (RDC), qui est toujours présent et à l’écoute des connexions entrantes.
ms.assetid: ae14af04-7d19-406b-998e-a0579cfe73eb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9028ccf0eea97a8651392baba094ac6dcda242f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512645"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="1f713-103">Test et débogage</span><span class="sxs-lookup"><span data-stu-id="1f713-103">Testing and Debugging</span></span>

<span data-ttu-id="1f713-104">Il existe un écouteur « Echo » implémenté par le client Connexion Bureau à distance (RDC), qui est toujours présent et à l’écoute des connexions entrantes.</span><span class="sxs-lookup"><span data-stu-id="1f713-104">There is an "echo" listener that is implemented by the Remote Desktop Connection (RDC) client, which is always present and listening for incoming connections.</span></span> <span data-ttu-id="1f713-105">Lorsque vous écrivez le côté serveur d’un module de canal virtuel dynamique (DVC), vous pouvez ouvrir un point de terminaison nommé « ECHO » dans le cadre d’un test rapide.</span><span class="sxs-lookup"><span data-stu-id="1f713-105">When you are writing the server side of a dynamic virtual channel (DVC) module, as a quick test you can open an endpoint named "ECHO".</span></span> <span data-ttu-id="1f713-106">Toute écriture sur un canal instancié à partir de ce point de terminaison entraînera la réception des mêmes données.</span><span class="sxs-lookup"><span data-stu-id="1f713-106">Any write to a channel that is instantiated from this endpoint will result in the receipt of the same data.</span></span>

<span data-ttu-id="1f713-107">Vous pouvez utiliser cette technique pour tester une implémentation d’entrée/sortie (e/s) du module côté serveur, pour mesurer le temps de réponse d’un plug-in client Connexion Bureau à distance (RDC) ou pour mesurer le délai réseau pour le client Connexion Bureau à distance (RDC).</span><span class="sxs-lookup"><span data-stu-id="1f713-107">You can use this technique to test an input/output (I/O) implementation of the server-side module, to measure the response time for a Remote Desktop Connection (RDC) client plug-in, or to measure the network delay for the Remote Desktop Connection (RDC) client.</span></span> <span data-ttu-id="1f713-108">Il n’existe aucune limitation quant à la quantité de données qui peuvent être envoyées sur ce canal.</span><span class="sxs-lookup"><span data-stu-id="1f713-108">There is no limitation on the amount of data that can be sent over this channel.</span></span>

 

 




