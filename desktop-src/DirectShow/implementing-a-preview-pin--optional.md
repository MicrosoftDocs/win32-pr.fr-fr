---
description: cette rubrique décrit comment implémenter un pin d’aperçu sur un filtre de capture DirectShow.
ms.assetid: 60306702-97d4-4627-8fbe-e7c8750f3902
title: Implémentation d’un pin d’aperçu (facultatif)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7de47b86df70500c83c794fe1074dc927622d571e78ef6175b944702277da492
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015557"
---
# <a name="implementing-a-preview-pin-optional"></a>Implémentation d’un pin d’aperçu (facultatif)

cette rubrique décrit comment implémenter un pin d’aperçu sur un filtre de capture DirectShow.

Si votre filtre a une broche d’aperçu, le code confidentiel de l’aperçu doit envoyer une copie des données fournies par le code confidentiel de capture. L’envoi de données uniquement à partir du code pin d’aperçu n’entraîne pas la suppression des frames par le code confidentiel de capture. Le code PIN de capture a toujours priorité sur la pin de la préversion.

Le code confidentiel de capture et le code PIN de la préversion doivent envoyer des données avec le même format. Par conséquent, ils doivent se connecter à l’aide de types de média identiques. Si la broche de capture se connecte en premier, le code confidentiel de l’aperçu doit offrir le même type de média et rejeter tous les autres types. Si la broche de préversion se connecte en premier et que la broche de capture se connecte avec un autre type de média, le code confidentiel de l’aperçu doit se reconnecter à l’aide du nouveau type de média. Si le filtre en aval de la broche d’aperçu rejette le nouveau type, le code PIN de capture doit également rejeter le type. Utilisez la méthode [**IPIN :: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) pour interroger le filtre en aval de la broche d’aperçu et utilisez la méthode [**IFilterGraph :: reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect) pour reconnecter le code confidentiel. ces règles s’appliquent également si le gestionnaire de Graph de filtre reconnecte le code confidentiel de capture.

L’exemple suivant illustre un plan de ce processus :


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Connecter des filtres](how-filters-connect.md)
</dt> <dt>

[Écriture de filtres de capture](writing-capture-filters.md)
</dt> </dl>

 

 



