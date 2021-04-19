---
description: Déclenché par une source de média lorsque les caractéristiques des sources changent.
ms.assetid: df7bb9a3-5949-4a4a-8835-c5b1d01b5cb3
title: Événement MESourceCharacteristicsChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 659e9eea0352d131aac4959b2952e8426ae408a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534163"
---
# <a name="mesourcecharacteristicschanged-event"></a><span data-ttu-id="4bfd0-103">Événement MESourceCharacteristicsChanged</span><span class="sxs-lookup"><span data-stu-id="4bfd0-103">MESourceCharacteristicsChanged event</span></span>

<span data-ttu-id="4bfd0-104">Déclenché par une source de média lorsque les caractéristiques de la source changent.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-104">Raised by a media source when the source's characteristics change.</span></span>

## <a name="event-values"></a><span data-ttu-id="4bfd0-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="4bfd0-105">Event values</span></span>

<span data-ttu-id="4bfd0-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="4bfd0-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="4bfd0-107">VARTYPE</span></span>              | <span data-ttu-id="4bfd0-108">Description</span><span class="sxs-lookup"><span data-stu-id="4bfd0-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="4bfd0-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="4bfd0-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="4bfd0-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="4bfd0-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="4bfd0-111">Attributes</span></span>

<span data-ttu-id="4bfd0-112">Les attributs suivants sont définis pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="4bfd0-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="4bfd0-113">Attribute</span></span>                                                                                                   | <span data-ttu-id="4bfd0-114">Description</span><span class="sxs-lookup"><span data-stu-id="4bfd0-114">Description</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="4bfd0-115">**caractéristiques de la \_ source d’événements MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4bfd0-115">**MF\_EVENT\_SOURCE\_CHARACTERISTICS**</span></span>](mf-event-source-characteristics-attribute.md)<br/>          | <span data-ttu-id="4bfd0-116">Nouvelles caractéristiques de la source du média.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-116">New characteristics of the media source.</span></span><br/> <br/>      |
| [<span data-ttu-id="4bfd0-117">**caractéristiques de la \_ source d’événements MF \_ \_ \_ Old**</span><span class="sxs-lookup"><span data-stu-id="4bfd0-117">**MF\_EVENT\_SOURCE\_CHARACTERISTICS\_OLD**</span></span>](mf-event-source-characteristics-old-attribute.md)<br/> | <span data-ttu-id="4bfd0-118">Caractéristiques précédentes de la source du média.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-118">Previous characteristics of the media source.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="4bfd0-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4bfd0-119">Requirements</span></span>



| <span data-ttu-id="4bfd0-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4bfd0-120">Requirement</span></span> | <span data-ttu-id="4bfd0-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="4bfd0-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bfd0-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4bfd0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4bfd0-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4bfd0-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4bfd0-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4bfd0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4bfd0-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4bfd0-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4bfd0-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="4bfd0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bfd0-127"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4bfd0-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bfd0-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4bfd0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bfd0-129">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="4bfd0-129">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> <dt>

[<span data-ttu-id="4bfd0-130">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4bfd0-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




