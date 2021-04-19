---
description: Spécifie la durée d’une présentation, en unités de 100 nanosecondes.
ms.assetid: abc21696-ea97-41ff-9341-6d9e9dcb19ec
title: Attribut MF_PD_DURATION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace7bd4f897de0220c2c449ce4fa891ac52eb200
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521823"
---
# <a name="mf_pd_duration-attribute"></a><span data-ttu-id="0af7b-103">\_ \_ Attribut durée MF PD</span><span class="sxs-lookup"><span data-stu-id="0af7b-103">MF\_PD\_DURATION attribute</span></span>

<span data-ttu-id="0af7b-104">Spécifie la durée d’une présentation, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="0af7b-104">Specifies the duration of a presentation, in 100-nanosecond units.</span></span>

## <a name="data-type"></a><span data-ttu-id="0af7b-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="0af7b-105">Data type</span></span>

<span data-ttu-id="0af7b-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="0af7b-106">**UINT64**</span></span>

<span data-ttu-id="0af7b-107">Traiter en tant que valeur **LongLong** .</span><span class="sxs-lookup"><span data-stu-id="0af7b-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0af7b-108">Notes</span><span class="sxs-lookup"><span data-stu-id="0af7b-108">Remarks</span></span>

<span data-ttu-id="0af7b-109">Les sources multimédias peuvent définir cet attribut sur un descripteur de présentation pour indiquer la durée de la présentation.</span><span class="sxs-lookup"><span data-stu-id="0af7b-109">Media sources can set this attribute on a presentation descriptor to indicate the duration of the presentation.</span></span>

<span data-ttu-id="0af7b-110">Cet attribut est une valeur signée, bien qu’il soit stocké en tant que **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="0af7b-110">This attribute is a signed value, although it is stored as a **UINT64**.</span></span> <span data-ttu-id="0af7b-111">Toutefois, l’attribut ne doit jamais contenir une valeur négative.</span><span class="sxs-lookup"><span data-stu-id="0af7b-111">However, the attribute should never contain a negative value.</span></span>

<span data-ttu-id="0af7b-112">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="0af7b-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="0af7b-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="0af7b-113">Examples</span></span>

<span data-ttu-id="0af7b-114">L’exemple suivant montre comment obtenir la durée d’une présentation à partir d’une source multimédia.</span><span class="sxs-lookup"><span data-stu-id="0af7b-114">The following example shows how to get the presentation duration from a media source.</span></span>


```C++
HRESULT GetSourceDuration(IMFMediaSource *pSource, MFTIME *pDuration)
{
    *pDuration = 0;

    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_DURATION, (UINT64*)pDuration);
        pPD->Release();
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="0af7b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0af7b-115">Requirements</span></span>



| <span data-ttu-id="0af7b-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0af7b-116">Requirement</span></span> | <span data-ttu-id="0af7b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="0af7b-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0af7b-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0af7b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0af7b-119">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="0af7b-119">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="0af7b-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0af7b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0af7b-121">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="0af7b-121">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="0af7b-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="0af7b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0af7b-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0af7b-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0af7b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0af7b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0af7b-125">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0af7b-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0af7b-126">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="0af7b-126">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="0af7b-127">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="0af7b-127">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="0af7b-128">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="0af7b-128">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="0af7b-129">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="0af7b-129">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="0af7b-130">Descripteurs de présentation</span><span class="sxs-lookup"><span data-stu-id="0af7b-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




