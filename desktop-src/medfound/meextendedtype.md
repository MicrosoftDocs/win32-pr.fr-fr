---
description: Type d’événement personnalisé.
ms.assetid: a54a446c-0e96-467b-90f6-0f64a7c1727d
title: Événement MEExtendedType (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d5551110fc3637a40834a7bf9251826f151ec62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518605"
---
# <a name="meextendedtype-event"></a><span data-ttu-id="696d5-103">Événement MEExtendedType</span><span class="sxs-lookup"><span data-stu-id="696d5-103">MEExtendedType event</span></span>

<span data-ttu-id="696d5-104">Type d’événement personnalisé.</span><span class="sxs-lookup"><span data-stu-id="696d5-104">Custom event type.</span></span> <span data-ttu-id="696d5-105">Vous pouvez utiliser ce type d’événement pour définir des événements personnalisés pour votre composant.</span><span class="sxs-lookup"><span data-stu-id="696d5-105">You can use this event type to define custom events for your component.</span></span> <span data-ttu-id="696d5-106">Utilisez le type d’événement étendu pour identifier l’événement.</span><span class="sxs-lookup"><span data-stu-id="696d5-106">Use the extended event type to identify the event.</span></span> <span data-ttu-id="696d5-107">Le type d’événement étendu est une valeur GUID associée à l’événement.</span><span class="sxs-lookup"><span data-stu-id="696d5-107">The extended event type is a GUID value associated with the event.</span></span> <span data-ttu-id="696d5-108">Pour plus d’informations, consultez [**IMFMediaEvent :: GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).</span><span class="sxs-lookup"><span data-stu-id="696d5-108">For more information, see [**IMFMediaEvent::GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).</span></span>

## <a name="event-values"></a><span data-ttu-id="696d5-109">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="696d5-109">Event values</span></span>

<span data-ttu-id="696d5-110">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="696d5-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="696d5-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="696d5-111">VARTYPE</span></span>              | <span data-ttu-id="696d5-112">Description</span><span class="sxs-lookup"><span data-stu-id="696d5-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="696d5-113">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="696d5-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="696d5-114">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="696d5-114">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="696d5-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="696d5-115">Requirements</span></span>



| <span data-ttu-id="696d5-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="696d5-116">Requirement</span></span> | <span data-ttu-id="696d5-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="696d5-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="696d5-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="696d5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="696d5-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="696d5-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="696d5-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="696d5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="696d5-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="696d5-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="696d5-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="696d5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="696d5-123"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="696d5-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="696d5-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="696d5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="696d5-125">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="696d5-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




