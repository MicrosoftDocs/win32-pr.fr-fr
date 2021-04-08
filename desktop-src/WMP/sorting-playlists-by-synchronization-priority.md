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
# <a name="sorting-playlists-by-synchronization-priority"></a><span data-ttu-id="f8a09-116">Tri des sélections par priorité de synchronisation</span><span class="sxs-lookup"><span data-stu-id="f8a09-116">Sorting Playlists by Synchronization Priority</span></span>

<span data-ttu-id="f8a09-117">Le code suivant effectue un simple tri des sélections.</span><span class="sxs-lookup"><span data-stu-id="f8a09-117">The following code performs a simple sort of playlists.</span></span> <span data-ttu-id="f8a09-118">Vous pouvez voir comment cette fonction est utilisée dans l’exemple de code dans l' [énumération des sélections de synchronisation](enumerating-synchronization-playlists.md).</span><span class="sxs-lookup"><span data-stu-id="f8a09-118">You can see how this function is used in the example code in [Enumerating Synchronization Playlists](enumerating-synchronization-playlists.md).</span></span> <span data-ttu-id="f8a09-119">La fonction accepte les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="f8a09-119">The function takes the following parameters:</span></span>

-   <span data-ttu-id="f8a09-120">*pPlaylist*.</span><span class="sxs-lookup"><span data-stu-id="f8a09-120">*pPlaylist*.</span></span> <span data-ttu-id="f8a09-121">Pointeur vers la sélection du lecteur Windows Media à trier.</span><span class="sxs-lookup"><span data-stu-id="f8a09-121">The pointer to the Windows Media Player playlist to sort.</span></span> <span data-ttu-id="f8a09-122">Les éléments multimédias de la liste de lecture doivent pointer vers d’autres sélections, et non vers des fichiers multimédias numériques individuels.</span><span class="sxs-lookup"><span data-stu-id="f8a09-122">The media items in the playlist must point to other playlists, not individual digital media files.</span></span>
-   <span data-ttu-id="f8a09-123">*bstrSyncAttribute*.</span><span class="sxs-lookup"><span data-stu-id="f8a09-123">*bstrSyncAttribute*.</span></span> <span data-ttu-id="f8a09-124">BSTR contenant le nom de l’attribut de partenariat de synchronisation pour l’appareil actuel (« Sync01 », « Sync02 », etc.).</span><span class="sxs-lookup"><span data-stu-id="f8a09-124">A BSTR containing the name of the synchronization partnership attribute for the current device ("Sync01", "Sync02", and so on).</span></span>
-   <span data-ttu-id="f8a09-125">*plSelected*.</span><span class="sxs-lookup"><span data-stu-id="f8a09-125">*plSelected*.</span></span> <span data-ttu-id="f8a09-126">Pointeur vers une variable de **type long** qui reçoit le nombre de sélections de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="f8a09-126">Pointer to a **long** variable that receives the count of synchronization playlists.</span></span>

<span data-ttu-id="f8a09-127">La fonction inspecte l’attribut de partenariat de synchronisation pour chaque élément multimédia (représentant une sélection) dans la sélection spécifiée par *pPlaylist*.</span><span class="sxs-lookup"><span data-stu-id="f8a09-127">The function inspects the synchronization partnership attribute for each media item (representing a playlist) in the playlist specified by *pPlaylist*.</span></span> <span data-ttu-id="f8a09-128">Si l’attribut a une valeur différente de zéro, le code déplace l’élément multimédia au début de la sélection et l’insère dans l’ordre de priorité.</span><span class="sxs-lookup"><span data-stu-id="f8a09-128">If the attribute has a nonzero value, the code moves the media item to the beginning of the playlist and inserts it in priority order.</span></span>

<span data-ttu-id="f8a09-129">Lorsque vous avez terminé, la fonction retourne le nombre d’éléments multimédias (sélections de synchronisation) ayant une valeur différente de zéro pour l’attribut partenariat de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="f8a09-129">When finished, the function returns the count of media items (synchronization playlists) that had a nonzero value for the synchronization partnership attribute.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="f8a09-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f8a09-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8a09-131">**IWMPMedia :: getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="f8a09-131">**IWMPMedia::getItemInfo**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo)
</dt> <dt>

[<span data-ttu-id="f8a09-132">**IWMPPlaylist :: obtient l' \_ élément**</span><span class="sxs-lookup"><span data-stu-id="f8a09-132">**IWMPPlaylist::get\_item**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-get_item)
</dt> <dt>

[<span data-ttu-id="f8a09-133">**IWMPPlaylist::moveItem**</span><span class="sxs-lookup"><span data-stu-id="f8a09-133">**IWMPPlaylist::moveItem**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-moveitem)
</dt> <dt>

[<span data-ttu-id="f8a09-134">**Gestion des sélections de synchronisation**</span><span class="sxs-lookup"><span data-stu-id="f8a09-134">**Managing Synchronization Playlists**</span></span>](managing-synchronization-playlists.md)
</dt> <dt>

[<span data-ttu-id="f8a09-135">**Attributs de synchronisation**</span><span class="sxs-lookup"><span data-stu-id="f8a09-135">**Sync Attributes**</span></span>](sync-attributes.md)
</dt> </dl>

 

 




