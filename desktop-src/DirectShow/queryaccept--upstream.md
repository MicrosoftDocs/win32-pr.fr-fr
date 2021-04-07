---
description: QueryAccept (en amont)
ms.assetid: 3153e3a4-2227-4fdd-b2b0-218763013d2d
title: QueryAccept (en amont)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7707c52d36c3d065c4a7277939f724aabdb73e46
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747093"
---
# <a name="queryaccept-upstream"></a><span data-ttu-id="d1fe1-103">QueryAccept (en amont)</span><span class="sxs-lookup"><span data-stu-id="d1fe1-103">QueryAccept (Upstream)</span></span>

<span data-ttu-id="d1fe1-104">Ce mécanisme permet à une broche d’entrée de proposer une modification de format à son homologue en amont.</span><span class="sxs-lookup"><span data-stu-id="d1fe1-104">This mechanism enables an input pin to propose a format change to its upstream peer.</span></span> <span data-ttu-id="d1fe1-105">Le filtre en aval doit joindre un type de média à l’exemple que le filtre en amont obtiendra lors de son prochain appel à [**IMemAllocator :: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer).</span><span class="sxs-lookup"><span data-stu-id="d1fe1-105">The downstream filter must attach a media type to the sample that the upstream filter will obtain in its next call to [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer).</span></span> <span data-ttu-id="d1fe1-106">Pour ce faire, toutefois, le filtre en aval doit fournir un allocateur personnalisé pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="d1fe1-106">In order to do this, however, the downstream filter must provide a custom allocator for the connection.</span></span> <span data-ttu-id="d1fe1-107">Cet allocateur doit implémenter une méthode privée que le filtre en aval peut utiliser pour définir le type de média sur l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="d1fe1-107">This allocator must implement a private method that the downstream filter can use to set the media type on the next sample.</span></span>

<span data-ttu-id="d1fe1-108">Les étapes suivantes se produisent :</span><span class="sxs-lookup"><span data-stu-id="d1fe1-108">The following steps occur:</span></span>

1.  <span data-ttu-id="d1fe1-109">Le filtre en aval vérifie si la connexion de code confidentiel utilise l’allocateur personnalisé du filtre.</span><span class="sxs-lookup"><span data-stu-id="d1fe1-109">The downstream filter checks whether the pin connection uses the filter's custom allocator.</span></span> <span data-ttu-id="d1fe1-110">Si le filtre amont est propriétaire de l’Allocator, le filtre en aval ne peut pas modifier le format.</span><span class="sxs-lookup"><span data-stu-id="d1fe1-110">If the upstream filter owns the allocator, the downstream filter cannot change the format.</span></span>
2.  <span data-ttu-id="d1fe1-111">Le filtre en aval appelle [**IPIN :: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sur la broche de sortie en amont (Voir l’illustration, étape A).</span><span class="sxs-lookup"><span data-stu-id="d1fe1-111">The downstream filter calls [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) on the upstream output pin (see illustration, step A).</span></span>
3.  <span data-ttu-id="d1fe1-112">Si `QueryAccept` retourne la \_ valeur OK, le filtre en aval appelle la méthode privée sur son allocateur afin de définir le type de média.</span><span class="sxs-lookup"><span data-stu-id="d1fe1-112">If `QueryAccept` returns S\_OK, the downstream filter calls the private method on its allocator in order to set the media type.</span></span> <span data-ttu-id="d1fe1-113">Dans cette méthode privée, l’allocateur appelle [**IMediaSample :: SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) sur l’exemple suivant disponible (B).</span><span class="sxs-lookup"><span data-stu-id="d1fe1-113">Within this private method, the allocator calls [**IMediaSample::SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) on the next available sample (B).</span></span>
4.  <span data-ttu-id="d1fe1-114">Le filtre amont appelle **GetBuffer** pour obtenir un nouvel exemple (C) et [**IMediaSample :: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) pour obtenir le type de média (D).</span><span class="sxs-lookup"><span data-stu-id="d1fe1-114">The upstream filter calls **GetBuffer** to get a new sample (C) and [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) to get the media type (D).</span></span>
5.  <span data-ttu-id="d1fe1-115">Lorsque le filtre en amont remet l’exemple, il doit conserver le type de média associé à cet exemple.</span><span class="sxs-lookup"><span data-stu-id="d1fe1-115">When the upstream filter delivers the sample, it should leave the media type attached to that sample.</span></span> <span data-ttu-id="d1fe1-116">De cette façon, le filtre en aval peut vérifier que le type de support a changé (E).</span><span class="sxs-lookup"><span data-stu-id="d1fe1-116">That way, the downstream filter can confirm that the media type has changed (E).</span></span>

<span data-ttu-id="d1fe1-117">Si le filtre amont accepte le changement de format, il doit également être en mesure de revenir au type de média d’origine, comme indiqué dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="d1fe1-117">If the upstream filter accepts the format change, it must also be able to switch back to the original media type, as shown in the following diagram.</span></span>

![queryaccept (en amont)](images/dynformat4.png)

<span data-ttu-id="d1fe1-119">Les exemples principaux de ce type de modification de format impliquent les convertisseurs vidéo DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d1fe1-119">The main examples of this kind of format change involve the DirectShow video renderers.</span></span>

-   <span data-ttu-id="d1fe1-120">Le filtre de [convertisseur vidéo](video-renderer-filter.md) d’origine peut basculer entre les types RVB et YUV pendant la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="d1fe1-120">The original [Video Renderer](video-renderer-filter.md) filter can switch between RGB and YUV types during streaming.</span></span> <span data-ttu-id="d1fe1-121">Lorsque le filtre se connecte, il requiert un format RVB qui correspond aux paramètres d’affichage actuels.</span><span class="sxs-lookup"><span data-stu-id="d1fe1-121">When the filter connects, it requires an RGB format that matches the current display settings.</span></span> <span data-ttu-id="d1fe1-122">Cela garantit qu’il peut revenir sur GDI si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d1fe1-122">This guarantees that it can fall back on GDI if it needs to.</span></span> <span data-ttu-id="d1fe1-123">Après le début de la diffusion en continu, si DirectDraw est disponible, le convertisseur vidéo demande une modification de format à un type YUV.</span><span class="sxs-lookup"><span data-stu-id="d1fe1-123">After streaming begins, if DirectDraw is available, the Video Renderer requests a format change to a YUV type.</span></span> <span data-ttu-id="d1fe1-124">Plus tard, il peut revenir à RGB s’il perd la surface de DirectDraw pour une raison quelconque.</span><span class="sxs-lookup"><span data-stu-id="d1fe1-124">Later, it might switch back to RGB if it loses the DirectDraw surface for any reason.</span></span>
-   <span data-ttu-id="d1fe1-125">Le filtre de convertisseur de mixage vidéo (VMR) le plus récent se connecte avec n’importe quel format pris en charge par le matériel graphique, y compris les types YUV.</span><span class="sxs-lookup"><span data-stu-id="d1fe1-125">The newer Video Mixing Renderer (VMR) filter will connect with any format that is supported by the graphics hardware, including YUV types.</span></span> <span data-ttu-id="d1fe1-126">Toutefois, le matériel graphique peut modifier le Stride de la surface DirectDraw sous-jacente afin d’optimiser les performances.</span><span class="sxs-lookup"><span data-stu-id="d1fe1-126">However, the graphics hardware might change the stride of the underlying DirectDraw surface in order to optimize performance.</span></span> <span data-ttu-id="d1fe1-127">Le filtre VMR utilise `QueryAccept` pour signaler le nouveau Stride, qui est spécifié dans le membre de la **bichasse** de la structure **BITMAPINFOHEADER** .</span><span class="sxs-lookup"><span data-stu-id="d1fe1-127">The VMR filter uses `QueryAccept` to report the new stride, which is specified in the **biWidth** member of the **BITMAPINFOHEADER** structure.</span></span> <span data-ttu-id="d1fe1-128">Les rectangles source et cible dans la structure **VIDEOINFOHEADER** ou **VIDEOINFOHEADER2** identifient la région dans laquelle la vidéo doit être décodée.</span><span class="sxs-lookup"><span data-stu-id="d1fe1-128">The source and target rectangles in the **VIDEOINFOHEADER** or **VIDEOINFOHEADER2** structure identify the region where the video should be decoded.</span></span>

<span data-ttu-id="d1fe1-129">**Note d’implémentation**</span><span class="sxs-lookup"><span data-stu-id="d1fe1-129">**Implementation Note**</span></span>

<span data-ttu-id="d1fe1-130">Il est peu probable que vous écriviez un filtre qui doit demander des modifications de format en amont, car il s’agit principalement d’une fonctionnalité de convertisseurs vidéo.</span><span class="sxs-lookup"><span data-stu-id="d1fe1-130">It is unlikely that you will write a filter that needs to request upstream format changes, since this is mainly a feature of video renderers.</span></span> <span data-ttu-id="d1fe1-131">Toutefois, si vous écrivez un filtre de transformation vidéo ou un décodeur vidéo, votre filtre doit répondre correctement aux demandes du convertisseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="d1fe1-131">However, if you write a video transform filter or a video decoder, your filter must respond correctly to requests from the video renderer.</span></span>

<span data-ttu-id="d1fe1-132">Un filtre TRANS-in-place qui se situe entre le convertisseur vidéo et le décodeur doit réussir tous les `QueryAccept` appels en amont.</span><span class="sxs-lookup"><span data-stu-id="d1fe1-132">A trans-in-place filter that sits between the video renderer and the decoder should pass all `QueryAccept` calls upstream.</span></span> <span data-ttu-id="d1fe1-133">Stockez les nouvelles informations de mise en forme lorsqu’elles arrivent.</span><span class="sxs-lookup"><span data-stu-id="d1fe1-133">Store the new format information when it arrives.</span></span>

<span data-ttu-id="d1fe1-134">Un filtre de transformation de copie (autrement dit, un filtre de non-transfert) doit implémenter l’un des comportements suivants :</span><span class="sxs-lookup"><span data-stu-id="d1fe1-134">A copy-transform filter (that is, a non-trans-in-place filter) should implement one of the following behaviors:</span></span>

-   <span data-ttu-id="d1fe1-135">Transmettez les modifications de format en amont et stockez les nouvelles informations de mise en forme lorsqu’elles arrivent.</span><span class="sxs-lookup"><span data-stu-id="d1fe1-135">Pass format changes upstream and store the new format information when it arrives.</span></span> <span data-ttu-id="d1fe1-136">Votre filtre doit utiliser un allocateur personnalisé pour pouvoir attacher le format à l’exemple en amont.</span><span class="sxs-lookup"><span data-stu-id="d1fe1-136">Your filter must use a custom allocator so that it can attach the format to the upstream sample.</span></span>
-   <span data-ttu-id="d1fe1-137">Effectuez la conversion de format à l’intérieur du filtre.</span><span class="sxs-lookup"><span data-stu-id="d1fe1-137">Perform the format conversion inside the filter.</span></span> <span data-ttu-id="d1fe1-138">C’est probablement plus facile que de passer le format en amont.</span><span class="sxs-lookup"><span data-stu-id="d1fe1-138">This is probably easier than passing the format change upstream.</span></span> <span data-ttu-id="d1fe1-139">Toutefois, il peut être moins efficace que de laisser le filtre du décodeur décoder dans le format correct.</span><span class="sxs-lookup"><span data-stu-id="d1fe1-139">However, it might be less efficient than letting the decoder filter decode into the correct format.</span></span>
-   <span data-ttu-id="d1fe1-140">En dernier recours, il suffit de rejeter le changement de format.</span><span class="sxs-lookup"><span data-stu-id="d1fe1-140">As a last resort, simply reject the format change.</span></span> <span data-ttu-id="d1fe1-141">(Pour plus d’informations, reportez-vous au code source de la méthode [**CTransInPlaceOutputPin :: CheckMediaType**](ctransinplaceoutputpin-checkmediatype.md) dans la bibliothèque de classes de base DirectShow.) Le rejet d’une modification de format peut toutefois réduire les performances, car elle empêche le convertisseur vidéo d’utiliser le format le plus efficace.</span><span class="sxs-lookup"><span data-stu-id="d1fe1-141">(For more information, refer to the source code for the [**CTransInPlaceOutputPin::CheckMediaType**](ctransinplaceoutputpin-checkmediatype.md) method in the DirectShow base class library.) Rejecting a format change can reduce performance, however, because it prevents the video renderer from using the most efficient format.</span></span>

<span data-ttu-id="d1fe1-142">Le pseudo-code suivant montre comment vous pouvez implémenter un filtre de transformation de copie (dérivé de **CTransformFilter**) qui peut basculer entre les types de sortie YUV et RGB.</span><span class="sxs-lookup"><span data-stu-id="d1fe1-142">The following pseudo-code shows how you might implement a copy-transform filter (derived from **CTransformFilter**) that can switch between YUV and RGB output types.</span></span> <span data-ttu-id="d1fe1-143">Cet exemple part du principe que le filtre effectue la conversion elle-même, au lieu de passer la modification de format en amont.</span><span class="sxs-lookup"><span data-stu-id="d1fe1-143">This example assumes that the filter does the conversion itself, rather than passing the format change upstream.</span></span>


```C++
HRESULT CMyTransform::CheckInputType(const CMediaType *pmt)
{
    if (pmt is a YUV type that you support) {
        return S_OK;
    }
    else {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
}

HRESULT CMyTransform::CheckTransform(
    const CMediaType *mtIn, const CMediaType *mtOut)
{
    if (mtOut is a YUV or RGB type that you support)
    {
        if ((mtIn has the same video dimensions as mtOut) &&
            (you support the mtIn-to-mtOut transform))
        {
            return S_OK;
        }
    }
    // otherwise
    return VFW_E_TYPE_NOT_ACCEPTED;
}

// GetMediaType: Return a preferred output type.
HRESULT CMyTransform::GetMediaType(int iPosition, CMediaType *pMediaType)
{
    if (iPosition < 0) {
        return E_INVALIDARG;
    }
    switch (iPosition)
    {
    case 0:
        Copy the input type (YUV) to pMediaType
        return S_OK;
    case 1:
        Construct an RGB type that matches the input type.
        return S_OK;
    default:
        return VFW_S_NO_MORE_ITEMS;
    }
}

// SetMediaType: Override from CTransformFilter. 
HRESULT CMyTransform::SetMediaType(
    PIN_DIRECTION direction, const CMediaType *pmt)
{
    // Capture this information...
    if (direction == PINDIR_OUTPUT)
    {
       m_bYuv = (pmt->subtype == MEDIASUBTYPE_UYVY);
    }
    return S_OK;
}

HRESULT CMyTransform::Transform(
    IMediaSample *pSource, IMediaSample *pDest)
{
    // Look for format changes from downstream.
    CMediaType *pMT = NULL;
    HRESULT hr = pDest->GetMediaType((AM_MEDIA_TYPE**)&pMT);
    if (hr == S_OK)
    {
        hr = m_pOutput->CheckMediaType(pMT);
        if(FAILED(hr))
        {
            DeleteMediaType(pMT);
            return E_FAIL;
        }
        // Notify our own output pin about the new type.
        m_pOutput->SetMediaType(pMT);
        DeleteMediaType(pMT);
    }
    // Process the buffers
    if (m_bYuv) {
        return ProcessFrameYUV(pSource, pDest);
    }
    else {
        return ProcessFrameRGB(pSource, pDest);
    }
}
```



 

 



