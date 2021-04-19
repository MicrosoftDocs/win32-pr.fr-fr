---
description: Déclenché par la session multimédia lorsque les fonctionnalités de session changent.
ms.assetid: d59fd3a0-29db-434c-b6ba-d9beb33bd965
title: Événement MESessionCapabilitiesChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0612b705571c50a6adcbde4afe93b42a524a950
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524963"
---
# <a name="mesessioncapabilitieschanged-event"></a><span data-ttu-id="41849-103">Événement MESessionCapabilitiesChanged</span><span class="sxs-lookup"><span data-stu-id="41849-103">MESessionCapabilitiesChanged event</span></span>

<span data-ttu-id="41849-104">Déclenché par la session multimédia lorsque les fonctionnalités de session changent.</span><span class="sxs-lookup"><span data-stu-id="41849-104">Raised by the Media Session when the session capabilities change.</span></span>

## <a name="event-values"></a><span data-ttu-id="41849-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="41849-105">Event values</span></span>

<span data-ttu-id="41849-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="41849-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="41849-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="41849-107">VARTYPE</span></span>              | <span data-ttu-id="41849-108">Description</span><span class="sxs-lookup"><span data-stu-id="41849-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="41849-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="41849-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="41849-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="41849-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="41849-111">Notes</span><span class="sxs-lookup"><span data-stu-id="41849-111">Remarks</span></span>

<span data-ttu-id="41849-112">L’événement contient les attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="41849-112">The event contains the following attributes.</span></span>



| <span data-ttu-id="41849-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="41849-113">Attribute</span></span>                                                                     | <span data-ttu-id="41849-114">Description</span><span class="sxs-lookup"><span data-stu-id="41849-114">Description</span></span>                                      |
|-------------------------------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="41849-115">**\_SESSIONCAPS d’événements MF \_**</span><span class="sxs-lookup"><span data-stu-id="41849-115">**MF\_EVENT\_SESSIONCAPS**</span></span>](mf-event-sessioncaps-attribute.md)              | <span data-ttu-id="41849-116">Nouveaux indicateurs de fonctionnalités de session.</span><span class="sxs-lookup"><span data-stu-id="41849-116">New session capabilities flags.</span></span>                  |
| [<span data-ttu-id="41849-117">**\_ \_ SESSIONCAPS Delta d’événement MF \_**</span><span class="sxs-lookup"><span data-stu-id="41849-117">**MF\_EVENT\_SESSIONCAPS\_DELTA**</span></span>](mf-event-sessioncaps-delta-attribute.md) | <span data-ttu-id="41849-118">Indique les indicateurs de fonctionnalités qui ont été modifiés.</span><span class="sxs-lookup"><span data-stu-id="41849-118">Indicates which capabilities flags have changed.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="41849-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41849-119">Requirements</span></span>



| <span data-ttu-id="41849-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41849-120">Requirement</span></span> | <span data-ttu-id="41849-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="41849-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41849-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41849-122">Minimum supported client</span></span><br/> | <span data-ttu-id="41849-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="41849-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="41849-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41849-124">Minimum supported server</span></span><br/> | <span data-ttu-id="41849-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="41849-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="41849-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="41849-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="41849-127"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="41849-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41849-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41849-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41849-129">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="41849-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




