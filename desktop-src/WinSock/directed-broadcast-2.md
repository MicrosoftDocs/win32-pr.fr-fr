---
description: Généralement considéré comme plus convivial pour le réseau qu’une diffusion sur tous les itinéraires, une diffusion dirigée se limite au réseau local que vous spécifiez.
ms.assetid: e2358580-5a65-434d-ba4c-a6b0615bccc3
title: Diffusion dirigée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f3a47bd47e9800e1f9c93cffa555b76feb77373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515849"
---
# <a name="directed-broadcast"></a><span data-ttu-id="f34fe-103">Diffusion dirigée</span><span class="sxs-lookup"><span data-stu-id="f34fe-103">Directed Broadcast</span></span>

<span data-ttu-id="f34fe-104">Généralement considéré comme plus convivial pour le réseau qu’une diffusion sur tous les itinéraires, une diffusion dirigée se limite au réseau local que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="f34fe-104">Generally considered more network friendly than an all-routes broadcast, a directed broadcast limits itself to the local network that you specify.</span></span> <span data-ttu-id="f34fe-105">Remplissez **sa \_ netnum** avec le numéro de réseau cible et **sa \_ nodeNum** avec des fichiers binaires.</span><span class="sxs-lookup"><span data-stu-id="f34fe-105">Fill **sa\_netnum** with the target network number and **sa\_nodenum** with binary ones.</span></span> <span data-ttu-id="f34fe-106">Les routeurs transmettent cette demande au réseau de destination où elle devient une diffusion locale.</span><span class="sxs-lookup"><span data-stu-id="f34fe-106">Routers forward this request to the destination network where it becomes a local broadcast.</span></span> <span data-ttu-id="f34fe-107">Les réseaux intermédiaires ne voient pas ce paquet comme une diffusion.</span><span class="sxs-lookup"><span data-stu-id="f34fe-107">Intermediate networks do not see this packet as a broadcast.</span></span>

 

 



