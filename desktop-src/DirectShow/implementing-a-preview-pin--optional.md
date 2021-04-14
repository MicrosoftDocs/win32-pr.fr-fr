---
description: Cette rubrique décrit comment implémenter un pin d’aperçu sur un filtre de capture DirectShow.
ms.assetid: 60306702-97d4-4627-8fbe-e7c8750f3902
title: Implémentation d’un pin d’aperçu (facultatif)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d1e09d070be2aa154428cb8684ff1c405fac959
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392740"
---
# <a name="implementing-a-preview-pin-optional"></a><span data-ttu-id="41f47-103">Implémentation d’un pin d’aperçu (facultatif)</span><span class="sxs-lookup"><span data-stu-id="41f47-103">Implementing a Preview Pin (Optional)</span></span>

<span data-ttu-id="41f47-104">Cette rubrique décrit comment implémenter un pin d’aperçu sur un filtre de capture DirectShow.</span><span class="sxs-lookup"><span data-stu-id="41f47-104">This topic describes how to implement a preview pin on a DirectShow capture filter.</span></span>

<span data-ttu-id="41f47-105">Si votre filtre a une broche d’aperçu, le code confidentiel de l’aperçu doit envoyer une copie des données fournies par le code confidentiel de capture.</span><span class="sxs-lookup"><span data-stu-id="41f47-105">If your filter has a preview pin, the preview pin must send a copy of the data delivered by the capture pin.</span></span> <span data-ttu-id="41f47-106">L’envoi de données uniquement à partir du code pin d’aperçu n’entraîne pas la suppression des frames par le code confidentiel de capture.</span><span class="sxs-lookup"><span data-stu-id="41f47-106">Only send data from the preview pin when doing so will not cause the capture pin to drop frames.</span></span> <span data-ttu-id="41f47-107">Le code PIN de capture a toujours priorité sur la pin de la préversion.</span><span class="sxs-lookup"><span data-stu-id="41f47-107">The capture pin always has priority over the preview pin.</span></span>

<span data-ttu-id="41f47-108">Le code confidentiel de capture et le code PIN de la préversion doivent envoyer des données avec le même format.</span><span class="sxs-lookup"><span data-stu-id="41f47-108">The capture pin and the preview pin must send data with the same format.</span></span> <span data-ttu-id="41f47-109">Par conséquent, ils doivent se connecter à l’aide de types de média identiques.</span><span class="sxs-lookup"><span data-stu-id="41f47-109">Therefore, they must connect using identical media types.</span></span> <span data-ttu-id="41f47-110">Si la broche de capture se connecte en premier, le code confidentiel de l’aperçu doit offrir le même type de média et rejeter tous les autres types.</span><span class="sxs-lookup"><span data-stu-id="41f47-110">If the capture pin connects first, the preview pin should offer the same media type, and reject any others types.</span></span> <span data-ttu-id="41f47-111">Si la broche de préversion se connecte en premier et que la broche de capture se connecte avec un autre type de média, le code confidentiel de l’aperçu doit se reconnecter à l’aide du nouveau type de média.</span><span class="sxs-lookup"><span data-stu-id="41f47-111">If the preview pin connects first, and the capture pin connects with a different media type, the preview pin should reconnect using the new media type.</span></span> <span data-ttu-id="41f47-112">Si le filtre en aval de la broche d’aperçu rejette le nouveau type, le code PIN de capture doit également rejeter le type.</span><span class="sxs-lookup"><span data-stu-id="41f47-112">If the filter downstream from the preview pin rejects the new type, the capture pin should also reject the type.</span></span> <span data-ttu-id="41f47-113">Utilisez la méthode [**IPIN :: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) pour interroger le filtre en aval de la broche d’aperçu et utilisez la méthode [**IFilterGraph :: reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect) pour reconnecter le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="41f47-113">Use the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method to query the filter downstream from the preview pin, and use the [**IFilterGraph::Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect) method to reconnect the pin.</span></span> <span data-ttu-id="41f47-114">Ces règles s’appliquent également si le gestionnaire de graphique de filtre reconnecte le code confidentiel de capture.</span><span class="sxs-lookup"><span data-stu-id="41f47-114">These rules also apply if the Filter Graph Manager reconnects the capture pin.</span></span>

<span data-ttu-id="41f47-115">L’exemple suivant illustre un plan de ce processus :</span><span class="sxs-lookup"><span data-stu-id="41f47-115">The following example shows an outline of this process:</span></span>


```C++
// Override CBasePin::CheckMediaType.
CCapturePin::CheckMediaType(CMediaType *pmt)
{
    if (m_pMyPreviewPin->IsConnected()) 
    {
        // The preview pin is already connected, so query the pin it is
        // connected to. If the other pin rejects it, so do we.
        hr = m_pMyPreviewPin->GetConnected()->QueryAccept(pmt);
        if (hr != S_OK) 
        {
            // The preview pin cannot reconnect with this media type.
            return E_INVALIDARG;
        }
        // The preview pin will reconnect when SetMediaType is called.
    }
    // Decide whether the capture pin accepts the format. 
    BOOL fAcceptThisType = ...  // (Not shown.)
    return (fAcceptThisType? S_OK : E_FAIL);
}

// Override CBasePin::SetMediaType.
CCapturePin::SetMediaType(CMediaType *pmt);
{
    if (m_pMyPreviewPin->IsConnected()) 
    {
        // The preview pin is already connected, so it must reconnect.
        if (m_pMyPreviewPin->GetConnected()->QueryAccept(pmt) == S_OK)
        {
            // The downstream pin will accept the new type, so it's safe
            // to reconnect. 
            m_pFilter->m_pGraph->Reconnect(m_pMyPreviewPin);
        }
        else
        {
            return VFW_E_INVALIDMEDIATYPE;
        }
    }
    // Now do anything that the capture pin needs to set the type.
    hr = MyInternalSetMediaType(pmt);

    // And finally, call the base-class method.
    return CBasePin::SetMediaType(pmt);
}

CPreviewPin::CheckMediaType(CMediaType *pmt)
{
    if (m_pMyCapturePin->IsConnected())
    {
       // The preview pin must connect with the same type.
       CMediaType cmt = m_pMyCapturePin->m_mt;
       return (*pmt == cmt ? S_OK : VFW_E_INVALIDMEDIATYPE);
    }
    // Decide whether the preview pin accepts the format. You can use your 
    // knowledge of which types the capture pin will accept. Regardless,
    // when the capture pin connects, the preview pin will reconnect.
    return (fAcceptThisType? S_OK : E_FAIL);
}
```



## <a name="related-topics"></a><span data-ttu-id="41f47-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="41f47-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41f47-117">Connexion des filtres</span><span class="sxs-lookup"><span data-stu-id="41f47-117">How Filters Connect</span></span>](how-filters-connect.md)
</dt> <dt>

[<span data-ttu-id="41f47-118">Écriture de filtres de capture</span><span class="sxs-lookup"><span data-stu-id="41f47-118">Writing Capture Filters</span></span>](writing-capture-filters.md)
</dt> </dl>

 

 



