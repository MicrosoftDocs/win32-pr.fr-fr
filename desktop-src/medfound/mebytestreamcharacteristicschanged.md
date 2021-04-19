---
description: Envoyé par un flux d’octets lorsque les caractéristiques du flux d’octets ont changé.
ms.assetid: EC34A7A3-BF01-4F9E-BA79-131B76D4C58F
title: Événement MEByteStreamCharacteristicsChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e626f510927970aad3c51182fca3a6dfddb0009
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527771"
---
# <a name="mebytestreamcharacteristicschanged-event"></a><span data-ttu-id="cb681-103">Événement MEByteStreamCharacteristicsChanged</span><span class="sxs-lookup"><span data-stu-id="cb681-103">MEByteStreamCharacteristicsChanged event</span></span>

<span data-ttu-id="cb681-104">Envoyé par un flux d’octets lorsque les caractéristiques du flux d’octets ont changé.</span><span class="sxs-lookup"><span data-stu-id="cb681-104">Sent by a byte stream when the characteristics of the byte stream have changed.</span></span>

## <a name="event-values"></a><span data-ttu-id="cb681-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="cb681-105">Event values</span></span>

<span data-ttu-id="cb681-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="cb681-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="cb681-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cb681-107">VARTYPE</span></span>               | <span data-ttu-id="cb681-108">Description</span><span class="sxs-lookup"><span data-stu-id="cb681-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="cb681-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="cb681-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="cb681-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="cb681-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="cb681-111">Notes</span><span class="sxs-lookup"><span data-stu-id="cb681-111">Remarks</span></span>

<span data-ttu-id="cb681-112">Cet événement indique qu’une ou plusieurs des caractéristiques suivantes ont été modifiées :</span><span class="sxs-lookup"><span data-stu-id="cb681-112">This event indicates that one or more of the following characteristics has changed:</span></span>

-   <span data-ttu-id="cb681-113">Indicateurs de capacité ([**IMFByteStream :: GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities))</span><span class="sxs-lookup"><span data-stu-id="cb681-113">Capability flags ([**IMFByteStream::GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities))</span></span>
-   <span data-ttu-id="cb681-114">Indicateur de fin de flux ([**IMFByteStream :: IsEndOfStream**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-isendofstream))</span><span class="sxs-lookup"><span data-stu-id="cb681-114">End-of-stream flag ([**IMFByteStream::IsEndOfStream**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-isendofstream))</span></span>
-   <span data-ttu-id="cb681-115">Longueur ([**IMFByteStream :: GetLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getlength))</span><span class="sxs-lookup"><span data-stu-id="cb681-115">Length ([**IMFByteStream::GetLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getlength))</span></span>

<span data-ttu-id="cb681-116">Toutes les implémentations de [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) ne prennent pas en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="cb681-116">Not all [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) implementations support this event.</span></span> <span data-ttu-id="cb681-117">Pour recevoir l’événement, interrogez l’objet de flux d’octets de l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="cb681-117">To receive the event, query the byte-stream object for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb681-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb681-118">Requirements</span></span>



| <span data-ttu-id="cb681-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb681-119">Requirement</span></span> | <span data-ttu-id="cb681-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb681-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb681-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb681-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cb681-122">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb681-122">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="cb681-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb681-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cb681-124">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb681-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cb681-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="cb681-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb681-126"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb681-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb681-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb681-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb681-128">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cb681-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




