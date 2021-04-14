---
description: Fréquence d’images d’un type de média vidéo, en images par seconde.
ms.assetid: 8336559c-06f1-478e-b921-e9eae7425230
title: Attribut MF_MT_FRAME_RATE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8df2ef4268bd643d9f65eb16c3f7257bcaceb1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393723"
---
# <a name="mf_mt_frame_rate-attribute"></a><span data-ttu-id="102f0-103">\_Attribut de \_ fréquence d’images MF MF \_</span><span class="sxs-lookup"><span data-stu-id="102f0-103">MF\_MT\_FRAME\_RATE attribute</span></span>

<span data-ttu-id="102f0-104">Fréquence d’images d’un type de média vidéo, en images par seconde.</span><span class="sxs-lookup"><span data-stu-id="102f0-104">Frame rate of a video media type, in frames per second.</span></span>

## <a name="data-type"></a><span data-ttu-id="102f0-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="102f0-105">Data type</span></span>

<span data-ttu-id="102f0-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="102f0-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="102f0-107">Notes</span><span class="sxs-lookup"><span data-stu-id="102f0-107">Remarks</span></span>

<span data-ttu-id="102f0-108">La fréquence d’images est exprimée sous la forme d’un rapport.</span><span class="sxs-lookup"><span data-stu-id="102f0-108">The frame rate is expressed as a ratio.</span></span> <span data-ttu-id="102f0-109">Les 32 bits supérieurs de la valeur de l’attribut contiennent le numérateur et les 32 inférieurs contiennent le dénominateur.</span><span class="sxs-lookup"><span data-stu-id="102f0-109">The upper 32 bits of the attribute value contain the numerator and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="102f0-110">Par exemple, si la fréquence d’images est de 30 images par seconde (FPS), le ratio est de 30/1.</span><span class="sxs-lookup"><span data-stu-id="102f0-110">For example, if the frame rate is 30 frames per second (fps), the ratio is 30/1.</span></span> <span data-ttu-id="102f0-111">Si la fréquence d’images est de 29,97 fps, le ratio est de 30000/1001.</span><span class="sxs-lookup"><span data-stu-id="102f0-111">If the frame rate is 29.97 fps, the ratio is 30,000/1001.</span></span>

<span data-ttu-id="102f0-112">Pour définir la valeur, utilisez la fonction [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) .</span><span class="sxs-lookup"><span data-stu-id="102f0-112">To set the value, use the [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) function.</span></span> <span data-ttu-id="102f0-113">Pour récupérer la valeur, utilisez la fonction [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) .</span><span class="sxs-lookup"><span data-stu-id="102f0-113">To get the value, use the [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) function.</span></span>

<span data-ttu-id="102f0-114">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="102f0-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="102f0-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="102f0-115">Examples</span></span>

<span data-ttu-id="102f0-116">L’exemple suivant définit la fréquence d’images sur un type de média vidéo.</span><span class="sxs-lookup"><span data-stu-id="102f0-116">The following example sets the frame rate on a video media type.</span></span>


```
// Helper function to set the frame rate on a video media type.
inline HRESULT SetFrameRate(
    IMFMediaType *pType, 
    UINT32 numerator, 
    UINT32 denominator
    )
{
    return MFSetAttributeRatio(
        pType, 
        MF_MT_FRAME_RATE, 
        numerator, 
        denominator
        );
}
```



<span data-ttu-id="102f0-117">L’exemple suivant obtient la fréquence d’images à partir d’un type de média vidéo.</span><span class="sxs-lookup"><span data-stu-id="102f0-117">The following example gets the frame rate from a video media type.</span></span>


```
// Helper function to get the frame rate from a video media type.
inline HRESULT GetFrameRate(
    IMFMediaType *pType, 
    UINT32 *pNumerator, 
    UINT32 *pDenominator
    )
{
    return MFGetAttributeRatio(
        pType, 
        MF_MT_FRAME_RATE, 
        pNumerator, 
        pDenominator
        );
}
```



## <a name="requirements"></a><span data-ttu-id="102f0-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="102f0-118">Requirements</span></span>



| <span data-ttu-id="102f0-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="102f0-119">Requirement</span></span> | <span data-ttu-id="102f0-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="102f0-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="102f0-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="102f0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="102f0-122">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="102f0-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="102f0-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="102f0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="102f0-124">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="102f0-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="102f0-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="102f0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="102f0-126"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="102f0-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="102f0-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="102f0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="102f0-128">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="102f0-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="102f0-129">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="102f0-129">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="102f0-130">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="102f0-130">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="102f0-131">**MFAverageTimePerFrameToFrameRate**</span><span class="sxs-lookup"><span data-stu-id="102f0-131">**MFAverageTimePerFrameToFrameRate**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate)
</dt> <dt>

[<span data-ttu-id="102f0-132">**MFFrameRateToAverageTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="102f0-132">**MFFrameRateToAverageTimePerFrame**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe)
</dt> </dl>

 

 




