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
# <a name="queryaccept-upstream"></a>QueryAccept (en amont)

Ce mécanisme permet à une broche d’entrée de proposer une modification de format à son homologue en amont. Le filtre en aval doit joindre un type de média à l’exemple que le filtre en amont obtiendra lors de son prochain appel à [**IMemAllocator :: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer). Pour ce faire, toutefois, le filtre en aval doit fournir un allocateur personnalisé pour la connexion. Cet allocateur doit implémenter une méthode privée que le filtre en aval peut utiliser pour définir le type de média sur l’exemple suivant.

Les étapes suivantes se produisent :

1.  Le filtre en aval vérifie si la connexion de code confidentiel utilise l’allocateur personnalisé du filtre. Si le filtre amont est propriétaire de l’Allocator, le filtre en aval ne peut pas modifier le format.
2.  Le filtre en aval appelle [**IPIN :: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sur la broche de sortie en amont (Voir l’illustration, étape A).
3.  Si `QueryAccept` retourne la \_ valeur OK, le filtre en aval appelle la méthode privée sur son allocateur afin de définir le type de média. Dans cette méthode privée, l’allocateur appelle [**IMediaSample :: SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) sur l’exemple suivant disponible (B).
4.  Le filtre amont appelle **GetBuffer** pour obtenir un nouvel exemple (C) et [**IMediaSample :: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) pour obtenir le type de média (D).
5.  Lorsque le filtre en amont remet l’exemple, il doit conserver le type de média associé à cet exemple. De cette façon, le filtre en aval peut vérifier que le type de support a changé (E).

Si le filtre amont accepte le changement de format, il doit également être en mesure de revenir au type de média d’origine, comme indiqué dans le diagramme suivant.

![queryaccept (en amont)](images/dynformat4.png)

Les exemples principaux de ce type de modification de format impliquent les convertisseurs vidéo DirectShow.

-   Le filtre de [convertisseur vidéo](video-renderer-filter.md) d’origine peut basculer entre les types RVB et YUV pendant la diffusion en continu. Lorsque le filtre se connecte, il requiert un format RVB qui correspond aux paramètres d’affichage actuels. Cela garantit qu’il peut revenir sur GDI si nécessaire. Après le début de la diffusion en continu, si DirectDraw est disponible, le convertisseur vidéo demande une modification de format à un type YUV. Plus tard, il peut revenir à RGB s’il perd la surface de DirectDraw pour une raison quelconque.
-   Le filtre de convertisseur de mixage vidéo (VMR) le plus récent se connecte avec n’importe quel format pris en charge par le matériel graphique, y compris les types YUV. Toutefois, le matériel graphique peut modifier le Stride de la surface DirectDraw sous-jacente afin d’optimiser les performances. Le filtre VMR utilise `QueryAccept` pour signaler le nouveau Stride, qui est spécifié dans le membre de la **bichasse** de la structure **BITMAPINFOHEADER** . Les rectangles source et cible dans la structure **VIDEOINFOHEADER** ou **VIDEOINFOHEADER2** identifient la région dans laquelle la vidéo doit être décodée.

**Note d’implémentation**

Il est peu probable que vous écriviez un filtre qui doit demander des modifications de format en amont, car il s’agit principalement d’une fonctionnalité de convertisseurs vidéo. Toutefois, si vous écrivez un filtre de transformation vidéo ou un décodeur vidéo, votre filtre doit répondre correctement aux demandes du convertisseur vidéo.

Un filtre TRANS-in-place qui se situe entre le convertisseur vidéo et le décodeur doit réussir tous les `QueryAccept` appels en amont. Stockez les nouvelles informations de mise en forme lorsqu’elles arrivent.

Un filtre de transformation de copie (autrement dit, un filtre de non-transfert) doit implémenter l’un des comportements suivants :

-   Transmettez les modifications de format en amont et stockez les nouvelles informations de mise en forme lorsqu’elles arrivent. Votre filtre doit utiliser un allocateur personnalisé pour pouvoir attacher le format à l’exemple en amont.
-   Effectuez la conversion de format à l’intérieur du filtre. C’est probablement plus facile que de passer le format en amont. Toutefois, il peut être moins efficace que de laisser le filtre du décodeur décoder dans le format correct.
-   En dernier recours, il suffit de rejeter le changement de format. (Pour plus d’informations, reportez-vous au code source de la méthode [**CTransInPlaceOutputPin :: CheckMediaType**](ctransinplaceoutputpin-checkmediatype.md) dans la bibliothèque de classes de base DirectShow.) Le rejet d’une modification de format peut toutefois réduire les performances, car elle empêche le convertisseur vidéo d’utiliser le format le plus efficace.

Le pseudo-code suivant montre comment vous pouvez implémenter un filtre de transformation de copie (dérivé de **CTransformFilter**) qui peut basculer entre les types de sortie YUV et RGB. Cet exemple part du principe que le filtre effectue la conversion elle-même, au lieu de passer la modification de format en amont.


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



 

 



