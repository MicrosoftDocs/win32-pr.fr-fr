---
description: Énumération des types de média
ms.assetid: 7878885f-c285-4744-8eab-445678dcfd49
title: Énumération des types de média
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4e2f063fc243d081b930a1bf47f85904dfbc2fc7eef00fb595d5f0fb3a451ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102799"
---
# <a name="enumerating-media-types"></a>Énumération des types de média

Les codes confidentiels prennent en charge la méthode [**IPIN :: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) , qui énumère les types de média préférés d’un pin. Elle retourne un pointeur vers l’interface [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) . La méthode [**IEnumMediaTypes :: Next**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next) récupère les pointeurs vers des structures de [**\_ \_ type de média**](/windows/win32/api/strmif/ns-strmif-am_media_type) qui décrivent les types de média.

l’énumérateur de type de média existe principalement pour aider le filtre Graph Manager à établir des connexions intelligentes et vos applications ne l’utiliseront probablement pas. Un code confidentiel ne retourne pas nécessairement tous les types de média préférés. En outre, les types de média qu’il retourne peuvent dépendre de l’état de la connexion du filtre. Par exemple, la broche de sortie d’un filtre peut retourner un ensemble différent de types de médias en fonction du type de média défini pour la broche d’entrée du filtre.

L’exemple suivant recherche un type de média préféré qui correspond à un type, un sous-type ou un type de format principal spécifié.


```C++
// Given a pin, find a preferred media type 
//
// pPin         Pointer to the pin.
// majorType    Preferred major type (GUID_NULL = don't care).
// subType      Preferred subtype (GUID_NULL = don't care).
// formatType   Preferred format type (GUID_NULL = don't care).
// ppmt         Receives a pointer to the media type. Can be NULL.
//
// Note: If you want to check whether a pin supports a desired media type,
//       but do not need the format details, set ppmt to NULL.
//
//       If ppmt is not NULL and the method succeeds, the caller must
//       delete the media type, including the format block. 

HRESULT GetPinMediaType(
    IPin *pPin,             // pointer to the pin
    REFGUID majorType,      // desired major type, or GUID_NULL = don't care
    REFGUID subType,        // desired subtype, or GUID_NULL = don't care
    REFGUID formatType,     // desired format type, of GUID_NULL = don't care
    AM_MEDIA_TYPE **ppmt    // Receives a pointer to the media type. (Can be NULL)
    )
{
    *ppmt = NULL;

    IEnumMediaTypes *pEnum = NULL;
    AM_MEDIA_TYPE *pmt = NULL;
    BOOL bFound = FALSE;
    
    HRESULT hr = pPin->EnumMediaTypes(&pEnum);
    if (FAILED(hr))
    {
        return hr;
    }

    while (hr = pEnum->Next(1, &pmt, NULL), hr == S_OK)
    {
        if ((majorType == GUID_NULL) || (majorType == pmt->majortype))
        {
            if ((subType == GUID_NULL) || (subType == pmt->subtype))
            {
                if ((formatType == GUID_NULL) || 
                    (formatType == pmt->formattype))
                {
                    // Found a match. 
                    if (ppmt)
                    {
                        *ppmt = pmt;  // Return it to the caller
                    }
                    else
                    {
                        _DeleteMediaType(pmt);
                    }
                    bFound = TRUE;
                    break;
                }
            }
        }
        _DeleteMediaType(pmt);
    }

    SafeRelease(&pEnum);
    if (SUCCEEDED(hr))
    {
        if (!bFound)
        {
            hr = VFW_E_NOT_FOUND;
        }
    }
    return hr;
}
```



> [!Note]  
> Cet exemple utilise la fonction [SafeRelease](/windows/desktop/medfound/saferelease) pour libérer des pointeurs d’interface.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Énumération d’objets dans un filtre Graph](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes)
</dt> </dl>

 

 
