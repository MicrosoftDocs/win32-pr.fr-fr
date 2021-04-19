---
description: Comme les doublons sont les descripteurs de socket et non les sockets sous-jacents, tous les États associés à un socket sont communs à tous les descripteurs.
ms.assetid: f3a2cd5a-bc3a-4aeb-8606-7b8aa6afb105
title: Plusieurs descripteurs sur un seul socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2356f24a69d132f87e0f6543f61509ff12acba5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515023"
---
# <a name="multiple-handles-to-a-single-socket"></a><span data-ttu-id="61872-103">Plusieurs descripteurs sur un seul socket</span><span class="sxs-lookup"><span data-stu-id="61872-103">Multiple Handles to a Single Socket</span></span>

<span data-ttu-id="61872-104">Comme les doublons sont les descripteurs de socket et non les sockets sous-jacents, tous les États associés à un socket sont communs à tous les descripteurs.</span><span class="sxs-lookup"><span data-stu-id="61872-104">Since what are duplicated are the socket descriptors and not the underlying sockets, all of the states associated with a socket are held in common across all the descriptors.</span></span> <span data-ttu-id="61872-105">Par exemple, une opération [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) effectuée à l’aide d’un descripteur est visible par la suite à l’aide d’un [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) à partir d’un ou de tous les descripteurs.</span><span class="sxs-lookup"><span data-stu-id="61872-105">For example a [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) operation performed using one descriptor is subsequently visible using a [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) from any or all descriptors.</span></span>

<span data-ttu-id="61872-106">La notification sur les sockets partagés est soumise aux contraintes habituelles de [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) et de [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="61872-106">Notification on shared sockets is subject to the usual constraints of [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) and [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span></span> <span data-ttu-id="61872-107">L’émission de l’un de ces appels à l’aide de l’un des descripteurs partagés annule toute inscription d’événement précédente pour le socket, quel que soit le descripteur utilisé pour effectuer cette inscription.</span><span class="sxs-lookup"><span data-stu-id="61872-107">Issuing either of these calls using any of the shared descriptors cancels any previous event registration for the socket, regardless of which descriptor was used to make that registration.</span></span> <span data-ttu-id="61872-108">Par exemple, il n’est pas possible d’avoir des événements de lecture de lecture FD de réception \_ et de traitement B pour les événements d' \_ écriture FD.</span><span class="sxs-lookup"><span data-stu-id="61872-108">Thus, for example, it would not be possible to have process A receive FD\_READ events and process B receive FD\_WRITE events.</span></span> <span data-ttu-id="61872-109">Dans les situations où une étroite coordination est nécessaire, il est préférable que les développeurs envisagent d’utiliser des threads plutôt que des processus distincts.</span><span class="sxs-lookup"><span data-stu-id="61872-109">For situations when such tight coordination is required, it is suggested that developers consider using threads instead of separate processes.</span></span>

 

 
