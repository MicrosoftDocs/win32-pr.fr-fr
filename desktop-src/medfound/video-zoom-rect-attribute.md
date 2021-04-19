---
description: Spécifie le rectangle source pour le mixage vidéo du convertisseur vidéo amélioré (EVR). Le rectangle source est la partie de la trame vidéo que le mixer BLITS à la surface de destination.
ms.assetid: 4364ff87-816e-4b64-b5e9-c53dd6c9bb33
title: Attribut VIDEO_ZOOM_RECT (EVR. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dda4efca5beab844baf3b3f53074d6b3012e8621
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524089"
---
# <a name="video_zoom_rect-attribute"></a><span data-ttu-id="a1cf4-104">IMAGE de l' \_ \_ attribut Rect de zoom</span><span class="sxs-lookup"><span data-stu-id="a1cf4-104">VIDEO\_ZOOM\_RECT attribute</span></span>

<span data-ttu-id="a1cf4-105">Spécifie le rectangle source pour le mixage vidéo du [convertisseur vidéo amélioré](enhanced-video-renderer.md) (EVR).</span><span class="sxs-lookup"><span data-stu-id="a1cf4-105">Specifies the source rectangle for video mixer of the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span> <span data-ttu-id="a1cf4-106">Le rectangle source est la partie de la trame vidéo que le mixer BLITS à la surface de destination.</span><span class="sxs-lookup"><span data-stu-id="a1cf4-106">The source rectangle is the portion of the video frame that the mixer blits to the destination surface.</span></span>

## <a name="data-type"></a><span data-ttu-id="a1cf4-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="a1cf4-107">Data type</span></span>

<span data-ttu-id="a1cf4-108">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="a1cf4-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="a1cf4-109">Notes</span><span class="sxs-lookup"><span data-stu-id="a1cf4-109">Remarks</span></span>

<span data-ttu-id="a1cf4-110">La valeur de cet attribut est une structure [**MFVideoNormalizedRect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) .</span><span class="sxs-lookup"><span data-stu-id="a1cf4-110">The value of this attribute is an [**MFVideoNormalizedRect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) structure.</span></span>

<span data-ttu-id="a1cf4-111">Le rectangle source est défini par rapport à un système de coordonnées normalisé, dans lequel la totalité de la trame vidéo occupe un rectangle avec des coordonnées {0, 0,1, 1}.</span><span class="sxs-lookup"><span data-stu-id="a1cf4-111">The source rectangle is defined relative to a normalized coordinate system, in which the entire video frame occupies a rectangle with coordinates {0, 0, 1, 1}.</span></span> <span data-ttu-id="a1cf4-112">Le rectangle source doit tenir dans le cadre de la vidéo. les coordonnées du rectangle source ont une plage de (0... 1).</span><span class="sxs-lookup"><span data-stu-id="a1cf4-112">The source rectangle must fit within the video frame; the coordinates of the source rectangle have a range of (0...1).</span></span>

<span data-ttu-id="a1cf4-113">Le présentateur EVR standard définit cet attribut sur le mélangeur.</span><span class="sxs-lookup"><span data-stu-id="a1cf4-113">The standard EVR presenter sets this attribute on the mixer.</span></span> <span data-ttu-id="a1cf4-114">Pour définir l’attribut, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="a1cf4-114">To set the attribute, do the following:</span></span>

1.  <span data-ttu-id="a1cf4-115">Appelez [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) sur le mixer pour récupérer le magasin d’attributs du mélangeur.</span><span class="sxs-lookup"><span data-stu-id="a1cf4-115">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the mixer, to get the mixer's attribute store.</span></span>
2.  <span data-ttu-id="a1cf4-116">Appelez [**IMFAttributes :: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob) pour définir l' **attribut \_ \_ Rect de zoom vidéo** sur le mélangeur.</span><span class="sxs-lookup"><span data-stu-id="a1cf4-116">Call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob) to set the **VIDEO\_ZOOM\_RECT** attribute on the mixer.</span></span> <span data-ttu-id="a1cf4-117">La valeur est une structure [**MFVideoNormalizedRect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) .</span><span class="sxs-lookup"><span data-stu-id="a1cf4-117">The value is an [**MFVideoNormalizedRect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) structure.</span></span>

<span data-ttu-id="a1cf4-118">Dans un présentateur EVR personnalisé, vous pouvez utiliser cet attribut pour implémenter la méthode [**IMFVideoDisplayControl :: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) .</span><span class="sxs-lookup"><span data-stu-id="a1cf4-118">In a custom EVR presenter, you can use this attribute to implement the [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) method.</span></span> <span data-ttu-id="a1cf4-119">Pour plus d’informations, consultez [rectangles source et destination](how-to-write-an-evr-presenter.md).</span><span class="sxs-lookup"><span data-stu-id="a1cf4-119">For more information, see [Source and Destination Rectangles](how-to-write-an-evr-presenter.md).</span></span>

<span data-ttu-id="a1cf4-120">La constante GUID de cet attribut est exportée à partir de strmiids. lib.</span><span class="sxs-lookup"><span data-stu-id="a1cf4-120">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="a1cf4-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="a1cf4-121">Examples</span></span>

<span data-ttu-id="a1cf4-122">L’exemple suivant définit le rectangle source sur le mélangeur.</span><span class="sxs-lookup"><span data-stu-id="a1cf4-122">The following example sets the source rectangle on the mixer.</span></span>


```C++
HRESULT SetMixerSourceRect(IMFTransform *pMixer, const MFVideoNormalizedRect& nrcSource)
{
    if (pMixer == NULL)
    {
        return E_POINTER;
    }

    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMixer->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetBlob(VIDEO_ZOOM_RECT, (const UINT8*)&nrcSource, sizeof(nrcSource));
        pAttributes->Release();
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="a1cf4-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1cf4-123">Requirements</span></span>



| <span data-ttu-id="a1cf4-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a1cf4-124">Requirement</span></span> | <span data-ttu-id="a1cf4-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1cf4-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a1cf4-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1cf4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a1cf4-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1cf4-127">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a1cf4-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1cf4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a1cf4-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1cf4-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a1cf4-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="a1cf4-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1cf4-131"><dt>Evr. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1cf4-131"><dt>Evr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1cf4-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1cf4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1cf4-133">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a1cf4-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a1cf4-134">Attributs de convertisseur vidéo améliorés</span><span class="sxs-lookup"><span data-stu-id="a1cf4-134">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="a1cf4-135">Comment écrire un présentateur EVR</span><span class="sxs-lookup"><span data-stu-id="a1cf4-135">How to Write an EVR Presenter</span></span>](how-to-write-an-evr-presenter.md)
</dt> <dt>

[<span data-ttu-id="a1cf4-136">**IMFAttributes :: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="a1cf4-136">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="a1cf4-137">**IMFAttributes :: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="a1cf4-137">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> </dl>

 

 




