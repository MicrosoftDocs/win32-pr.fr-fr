---
description: Signale qu’une source multimédia tente de se reconnecter au serveur.
ms.assetid: c5975279-c710-4046-9152-d1e1c62eb785
title: Événement MEReconnectStart (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d21944e937f52205416b5e6e2b52d18c3a3c768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114626"
---
# <a name="mereconnectstart-event"></a><span data-ttu-id="969c2-103">Événement MEReconnectStart</span><span class="sxs-lookup"><span data-stu-id="969c2-103">MEReconnectStart event</span></span>

<span data-ttu-id="969c2-104">Signale qu’une source multimédia tente de se reconnecter au serveur.</span><span class="sxs-lookup"><span data-stu-id="969c2-104">Signals that a media source is attempting to reconnect to the server.</span></span>

<span data-ttu-id="969c2-105">Déclenché par une source de média au début d’une tentative de reconnexion.</span><span class="sxs-lookup"><span data-stu-id="969c2-105">Raised by a media source at the start of a reconnection attempt.</span></span> <span data-ttu-id="969c2-106">La source réseau déclenche cet événement si elle tente de se reconnecter au serveur.</span><span class="sxs-lookup"><span data-stu-id="969c2-106">The network source raises this event if it attempts to reconnect to the server.</span></span> <span data-ttu-id="969c2-107">La session multimédia transmet cet événement à l’application.</span><span class="sxs-lookup"><span data-stu-id="969c2-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="969c2-108">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="969c2-108">Event values</span></span>

<span data-ttu-id="969c2-109">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="969c2-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="969c2-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="969c2-110">VARTYPE</span></span>              | <span data-ttu-id="969c2-111">Description</span><span class="sxs-lookup"><span data-stu-id="969c2-111">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="969c2-112">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="969c2-112">VT\_EMPTY</span></span><br/> | <span data-ttu-id="969c2-113">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="969c2-113">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="969c2-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="969c2-114">Requirements</span></span>



| <span data-ttu-id="969c2-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="969c2-115">Requirement</span></span> | <span data-ttu-id="969c2-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="969c2-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="969c2-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="969c2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="969c2-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="969c2-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="969c2-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="969c2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="969c2-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="969c2-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="969c2-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="969c2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="969c2-122"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="969c2-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="969c2-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="969c2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="969c2-124">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="969c2-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




