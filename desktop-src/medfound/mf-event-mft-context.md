---
description: Contient une valeur définie par l’appelant pour un événement METransformMarker.
ms.assetid: c6ab20d9-c2bc-43ba-a018-2c6682bf0485
title: Attribut MF_EVENT_MFT_CONTEXT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d61e8920c119da151df1215e8de8ce0d526220e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034210"
---
# <a name="mf_event_mft_context-attribute"></a><span data-ttu-id="96ae3-103">\_Attribut de \_ \_ contexte MFT de l’événement MF</span><span class="sxs-lookup"><span data-stu-id="96ae3-103">MF\_EVENT\_MFT\_CONTEXT attribute</span></span>

<span data-ttu-id="96ae3-104">Contient une valeur définie par l’appelant pour un événement [METransformMarker](metransformmarker.md) .</span><span class="sxs-lookup"><span data-stu-id="96ae3-104">Contains a caller-defined value for an [METransformMarker](metransformmarker.md) event.</span></span>

## <a name="data-type"></a><span data-ttu-id="96ae3-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="96ae3-105">Data type</span></span>

<span data-ttu-id="96ae3-106">**ULong \_ PTR** stocké comme **UINT64**</span><span class="sxs-lookup"><span data-stu-id="96ae3-106">**ULONG\_PTR** stored as **UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="96ae3-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="96ae3-107">Get/set</span></span>

<span data-ttu-id="96ae3-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="96ae3-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="96ae3-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="96ae3-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="96ae3-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="96ae3-110">Applies to</span></span>

[<span data-ttu-id="96ae3-111">**IMFMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="96ae3-111">**IMFMediaEvent**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)

## <a name="remarks"></a><span data-ttu-id="96ae3-112">Notes</span><span class="sxs-lookup"><span data-stu-id="96ae3-112">Remarks</span></span>

<span data-ttu-id="96ae3-113">Cet attribut est utilisé avec l’événement [METransformMarker](metransformmarker.md) .</span><span class="sxs-lookup"><span data-stu-id="96ae3-113">This attribute is used with the [METransformMarker](metransformmarker.md) event.</span></span> <span data-ttu-id="96ae3-114">La valeur de l’attribut est extraite du paramètre *ulParam* de la méthode [**IMFTransform ::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) .</span><span class="sxs-lookup"><span data-stu-id="96ae3-114">The value of the attribute is taken from the *ulParam* parameter of the [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) method.</span></span>

<span data-ttu-id="96ae3-115">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="96ae3-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="96ae3-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="96ae3-116">Requirements</span></span>



| <span data-ttu-id="96ae3-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="96ae3-117">Requirement</span></span> | <span data-ttu-id="96ae3-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="96ae3-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="96ae3-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="96ae3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="96ae3-120">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="96ae3-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="96ae3-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="96ae3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="96ae3-122">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="96ae3-122">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="96ae3-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="96ae3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="96ae3-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="96ae3-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96ae3-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96ae3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96ae3-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="96ae3-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="96ae3-127">MFTs asynchrone</span><span class="sxs-lookup"><span data-stu-id="96ae3-127">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="96ae3-128">Attributs d'événement</span><span class="sxs-lookup"><span data-stu-id="96ae3-128">Event Attributes</span></span>](event-attributes.md)
</dt> </dl>

 

 




