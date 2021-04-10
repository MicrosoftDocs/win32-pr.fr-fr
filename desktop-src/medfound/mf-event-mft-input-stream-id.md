---
description: Spécifie un flux d’entrée sur une transformation de Media Foundation (MFT).
ms.assetid: 2922af62-3fcc-4153-a26a-aba3c4121a0b
title: Attribut MF_EVENT_MFT_INPUT_STREAM_ID (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59d3966c33dc563fc9e38ad367cc675ba6616c03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201610"
---
# <a name="mf_event_mft_input_stream_id-attribute"></a><span data-ttu-id="ad7d8-103">\_ \_ \_ Attribut d’ID de \_ flux d’entrée MFT d’événement \_ MF</span><span class="sxs-lookup"><span data-stu-id="ad7d8-103">MF\_EVENT\_MFT\_INPUT\_STREAM\_ID attribute</span></span>

<span data-ttu-id="ad7d8-104">Spécifie un flux d’entrée sur une transformation de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="ad7d8-104">Specifies an input stream on a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="ad7d8-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="ad7d8-105">Data type</span></span>

<span data-ttu-id="ad7d8-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ad7d8-106">**UINT32**</span></span>

<span data-ttu-id="ad7d8-107">La valeur est un identificateur de flux d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ad7d8-107">The value is an input stream identifier.</span></span>

## <a name="getset"></a><span data-ttu-id="ad7d8-108">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="ad7d8-108">Get/set</span></span>

<span data-ttu-id="ad7d8-109">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="ad7d8-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="ad7d8-110">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="ad7d8-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="ad7d8-111">S’applique à</span><span class="sxs-lookup"><span data-stu-id="ad7d8-111">Applies to</span></span>

[<span data-ttu-id="ad7d8-112">**IMFMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="ad7d8-112">**IMFMediaEvent**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)

## <a name="remarks"></a><span data-ttu-id="ad7d8-113">Notes</span><span class="sxs-lookup"><span data-stu-id="ad7d8-113">Remarks</span></span>

<span data-ttu-id="ad7d8-114">Cet attribut est utilisé avec les événements suivants :</span><span class="sxs-lookup"><span data-stu-id="ad7d8-114">This attribute is used with the following events:</span></span>

-   [<span data-ttu-id="ad7d8-115">METransformDrainComplete</span><span class="sxs-lookup"><span data-stu-id="ad7d8-115">METransformDrainComplete</span></span>](metransformdraincomplete.md)
-   [<span data-ttu-id="ad7d8-116">METransformNeedInput</span><span class="sxs-lookup"><span data-stu-id="ad7d8-116">METransformNeedInput</span></span>](metransformneedinput.md)

<span data-ttu-id="ad7d8-117">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ad7d8-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad7d8-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad7d8-118">Requirements</span></span>



| <span data-ttu-id="ad7d8-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad7d8-119">Requirement</span></span> | <span data-ttu-id="ad7d8-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad7d8-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ad7d8-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad7d8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ad7d8-122">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ad7d8-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="ad7d8-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad7d8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ad7d8-124">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ad7d8-124">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="ad7d8-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="ad7d8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad7d8-126"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad7d8-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad7d8-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad7d8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad7d8-128">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ad7d8-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ad7d8-129">MFTs asynchrone</span><span class="sxs-lookup"><span data-stu-id="ad7d8-129">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="ad7d8-130">Attributs d'événement</span><span class="sxs-lookup"><span data-stu-id="ad7d8-130">Event Attributes</span></span>](event-attributes.md)
</dt> </dl>

 

 




