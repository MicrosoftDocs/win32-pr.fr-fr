---
description: Déclenché par un flux multimédia lorsque le type de média du flux change.
ms.assetid: 14786a9b-413e-4fb4-b267-bfd0ccd4631b
title: Événement MEStreamFormatChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd48e7abc8121707b150af5bc8968a50c1eb44e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863602"
---
# <a name="mestreamformatchanged-event"></a><span data-ttu-id="032db-103">Événement MEStreamFormatChanged</span><span class="sxs-lookup"><span data-stu-id="032db-103">MEStreamFormatChanged event</span></span>

<span data-ttu-id="032db-104">Déclenché par un flux multimédia lorsque le type de média du flux change.</span><span class="sxs-lookup"><span data-stu-id="032db-104">Raised by a media stream when the media type of the stream changes.</span></span>

## <a name="event-values"></a><span data-ttu-id="032db-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="032db-105">Event values</span></span>

<span data-ttu-id="032db-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="032db-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="032db-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="032db-107">VARTYPE</span></span>                | <span data-ttu-id="032db-108">Description</span><span class="sxs-lookup"><span data-stu-id="032db-108">Description</span></span>                                                                                                 |
|------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="032db-109">VT \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="032db-109">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="032db-110">Pointeur vers l’interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) du nouveau type de média.</span><span class="sxs-lookup"><span data-stu-id="032db-110">Pointer to the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface of the new media type.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="032db-111">Notes</span><span class="sxs-lookup"><span data-stu-id="032db-111">Remarks</span></span>

<span data-ttu-id="032db-112">Utilisez cet événement pour signaler les modifications de format dans le flux.</span><span class="sxs-lookup"><span data-stu-id="032db-112">Use this event to signal format changes in the stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="032db-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="032db-113">Requirements</span></span>



| <span data-ttu-id="032db-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="032db-114">Requirement</span></span> | <span data-ttu-id="032db-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="032db-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="032db-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="032db-116">Minimum supported client</span></span><br/> | <span data-ttu-id="032db-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="032db-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="032db-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="032db-118">Minimum supported server</span></span><br/> | <span data-ttu-id="032db-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="032db-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="032db-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="032db-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="032db-121"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="032db-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="032db-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="032db-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="032db-123">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="032db-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




