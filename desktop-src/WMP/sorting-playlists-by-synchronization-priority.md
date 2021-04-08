---
title: Tri des sélections par priorité de synchronisation
description: Tri des sélections par priorité de synchronisation
ms.assetid: 0f7f1ed3-0639-47bf-bf8e-52ae0a1d7ab2
keywords:
- Lecteur Windows Media, sélections de synchronisation
- Modèle objet du lecteur Windows Media, sélections de synchronisation
- modèle objet, sélections de synchronisation
- Lecteur Windows Media Mobile, sélections de synchronisation
- Contrôle ActiveX du lecteur Windows Media, sélections de synchronisation
- Contrôle ActiveX Windows Media Player Mobile, sélections de synchronisation
- Contrôle ActiveX, sélections de synchronisation
- sélections, synchronisation
- sélections de métafichiers, synchronisation
- Sélections de métafichiers Windows Media, synchronisation
- appareils mobiles, tri des sélections de synchronisation
- sélections de synchronisation, tri
- sélections de synchronisation, priorités
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90624e8e1cab715e8a26e33f40a444d53ab35def
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103841905"
---
# <a name="sorting-playlists-by-synchronization-priority"></a>Tri des sélections par priorité de synchronisation

Le code suivant effectue un simple tri des sélections. Vous pouvez voir comment cette fonction est utilisée dans l’exemple de code dans l' [énumération des sélections de synchronisation](enumerating-synchronization-playlists.md). La fonction accepte les paramètres suivants :

-   *pPlaylist*. Pointeur vers la sélection du lecteur Windows Media à trier. Les éléments multimédias de la liste de lecture doivent pointer vers d’autres sélections, et non vers des fichiers multimédias numériques individuels.
-   *bstrSyncAttribute*. BSTR contenant le nom de l’attribut de partenariat de synchronisation pour l’appareil actuel (« Sync01 », « Sync02 », etc.).
-   *plSelected*. Pointeur vers une variable de **type long** qui reçoit le nombre de sélections de synchronisation.

La fonction inspecte l’attribut de partenariat de synchronisation pour chaque élément multimédia (représentant une sélection) dans la sélection spécifiée par *pPlaylist*. Si l’attribut a une valeur différente de zéro, le code déplace l’élément multimédia au début de la sélection et l’insère dans l’ordre de priorité.

Lorsque vous avez terminé, la fonction retourne le nombre d’éléments multimédias (sélections de synchronisation) ayant une valeur différente de zéro pour l’attribut partenariat de synchronisation.


```C++
STDMETHODIMP CSyncSettings::SortPlaylist(IWMPPlaylist *pPlaylist, BSTR bstrSyncAttribute, long *plSelected)
{
    HRESULT hr = S_OK;
    long lSyncItemCount = 0;

    ATLASSERT (pPlaylist);
    ATLASSERT (plSelected);

    // Local copies of the parameters.
    CComPtr<IWMPPlaylist> spPlaylist(pPlaylist);
    CComBSTR bstrAttribute(bstrSyncAttribute);

    ATLASSERT (bstrAttribute.Length());

    // Get the count of playlist media items.
    long lCount = 0;
    spPlaylist->get_count(&lCount);

    // Walk the playlist.
    for(long i = 0; i < lCount; i++)
    {
        CComPtr<IWMPMedia> spMedia;                 
        CComBSTR bstrVal;            
        long lPriority = 0;
        
        hr = spPlaylist->get_item(i, &spMedia);

        if(SUCCEEDED(hr) && spMedia)
        {      
            // Get the sync priority value as a string.
            hr = spMedia->getItemInfo(bstrAttribute, &bstrVal);
        }

        if(SUCCEEDED(hr) && spMedia)
        {
            // Convert sync priority to a long number.
            lPriority = _wtol(bstrVal);
        }

        // Sort the playlist.
        // Only move the current item if it has a
        // sync priority value.
        if(lPriority > 0)
        {
            lSyncItemCount++;

            // Walk down the list and insert the item
            // in ascending order.
            for(long j = 0; j < lCount; j++)
            {
                CComPtr<IWMPMedia> spMediaCompare;
                CComBSTR bstrValCompare;
                long lPriorityTest = 0;

                hr = spPlaylist->get_item(j, &spMediaCompare);

                if(SUCCEEDED(hr) && spMediaCompare.p)
                {
                    hr = spMediaCompare->getItemInfo(bstrAttribute, &bstrValCompare);
                }
                if(SUCCEEDED(hr) && spMediaCompare.p)
                {
                    lPriorityTest = _wtol(bstrValCompare);
                    
                    if(lPriority <= lPriorityTest || 
                        0 == lPriorityTest)
                    {
                        hr = spPlaylist->moveItem(i, j);
                        break;                            
                    }                        
                } 
            } // for j                       
        } // if(lPriority > 0)          
    } // for i  
  
    // Return the sync item count.
    *plSelected = lSyncItemCount;

    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IWMPMedia :: getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo)
</dt> <dt>

[**IWMPPlaylist :: obtient l' \_ élément**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-get_item)
</dt> <dt>

[**IWMPPlaylist::moveItem**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-moveitem)
</dt> <dt>

[**Gestion des sélections de synchronisation**](managing-synchronization-playlists.md)
</dt> <dt>

[**Attributs de synchronisation**](sync-attributes.md)
</dt> </dl>

 

 




