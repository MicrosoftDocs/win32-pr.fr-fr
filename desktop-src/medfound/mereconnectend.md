---
description: Signale qu’une source de média a terminé une tentative de reconnexion au serveur.
ms.assetid: 228e069a-a26b-472e-915e-ff9aec5ee9c1
title: Événement MEReconnectEnd (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3477abd5d4413faa6b2d965f7ace2d19c48dd786
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528269"
---
# <a name="mereconnectend-event"></a><span data-ttu-id="89655-103">Événement MEReconnectEnd</span><span class="sxs-lookup"><span data-stu-id="89655-103">MEReconnectEnd event</span></span>

<span data-ttu-id="89655-104">Signale qu’une source de média a terminé une tentative de reconnexion au serveur.</span><span class="sxs-lookup"><span data-stu-id="89655-104">Signals that a media source has completed an attempt to reconnect to the server.</span></span>

<span data-ttu-id="89655-105">Déclenché par une source de média à la fin d’une tentative de reconnexion.</span><span class="sxs-lookup"><span data-stu-id="89655-105">Raised by a media source at the end of a reconnection attempt.</span></span> <span data-ttu-id="89655-106">La source réseau déclenche cet événement s’il se reconnecte au serveur.</span><span class="sxs-lookup"><span data-stu-id="89655-106">The network source raises this event if it reconnects to the server.</span></span> <span data-ttu-id="89655-107">La session multimédia transmet cet événement à l’application.</span><span class="sxs-lookup"><span data-stu-id="89655-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="89655-108">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="89655-108">Event values</span></span>

<span data-ttu-id="89655-109">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="89655-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="89655-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="89655-110">VARTYPE</span></span>              | <span data-ttu-id="89655-111">Description</span><span class="sxs-lookup"><span data-stu-id="89655-111">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="89655-112">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="89655-112">VT\_EMPTY</span></span><br/> | <span data-ttu-id="89655-113">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="89655-113">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="89655-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89655-114">Requirements</span></span>



| <span data-ttu-id="89655-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89655-115">Requirement</span></span> | <span data-ttu-id="89655-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="89655-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89655-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89655-117">Minimum supported client</span></span><br/> | <span data-ttu-id="89655-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="89655-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="89655-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89655-119">Minimum supported server</span></span><br/> | <span data-ttu-id="89655-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="89655-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="89655-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="89655-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="89655-122"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89655-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89655-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89655-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89655-124">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="89655-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




