---
description: Le \_32.dll Ws2 (et les protocoles en couches) appellera WSPCleanup une fois pour chaque appel de WSPStartup.
ms.assetid: c3b7b648-5727-47d6-9ddc-9d9f6511949d
title: Nettoyage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc294183f964d00ae9ebb1d74b90b346c2ce8fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515655"
---
# <a name="cleanup"></a><span data-ttu-id="40986-103">Nettoyage</span><span class="sxs-lookup"><span data-stu-id="40986-103">Cleanup</span></span>

<span data-ttu-id="40986-104">Le \_32.dll Ws2 (et les protocoles en couches) appellera [**WSPCleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85)) une fois pour chaque appel de [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup).</span><span class="sxs-lookup"><span data-stu-id="40986-104">The Ws2\_32.dll (and layered protocols) will call [**WSPCleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85)) once for each invocation of [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup).</span></span> <span data-ttu-id="40986-105">À chaque appel, **WSPCleanup** doit décrémenter un compteur de référence par processus et, lorsque le compteur atteint zéro, le fournisseur de services doit se préparer à être déchargé de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="40986-105">On each invocation, **WSPCleanup** should decrement a per-process reference counter, and when the counter reaches zero, the service provider must prepare itself to be unloaded from memory.</span></span> <span data-ttu-id="40986-106">Le premier ordre d’activité consiste à terminer la transmission de toutes les données non envoyées sur les sockets configurés pour une fermeture normale.</span><span class="sxs-lookup"><span data-stu-id="40986-106">The first order of business is to finish transmitting any unsent data on sockets that are configured for a graceful close.</span></span> <span data-ttu-id="40986-107">Ensuite, toutes les ressources détenues par le fournisseur doivent être libérées.</span><span class="sxs-lookup"><span data-stu-id="40986-107">Thereafter, any and all resources held by the provider are to be freed.</span></span> <span data-ttu-id="40986-108">Le fournisseur de services doit être laissé dans un État où il peut être immédiatement réinitialisé par un appel à **WSPStartup**.</span><span class="sxs-lookup"><span data-stu-id="40986-108">The service provider must be left in a state where it can be immediately reinitialized by a call to **WSPStartup**.</span></span>

 

 
