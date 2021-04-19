---
title: Énumération des sélections de synchronisation
description: Énumération des sélections de synchronisation
ms.assetid: 830c3ea5-2937-48b5-b89f-ef68a6649ca3
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
- sélections de synchronisation, énumération
- appareils mobiles, énumération
- énumérations, sélections de synchronisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29679380cec1844e9a790ac4ff047bfa4bf05288
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106509635"
---
# <a name="enumerating-synchronization-playlists"></a><span data-ttu-id="e694b-116">Énumération des sélections de synchronisation</span><span class="sxs-lookup"><span data-stu-id="e694b-116">Enumerating Synchronization Playlists</span></span>

<span data-ttu-id="e694b-117">L’exemple de code suivant crée une fonction qui remplit un contrôle ListView avec des sélections.</span><span class="sxs-lookup"><span data-stu-id="e694b-117">The following example code creates a function that fills a ListView control with playlists.</span></span> <span data-ttu-id="e694b-118">Les sélections de synchronisation s’affichent en premier.</span><span class="sxs-lookup"><span data-stu-id="e694b-118">Synchronization playlists appear first.</span></span> <span data-ttu-id="e694b-119">Les sélections de synchronisation pour l’appareil actuellement sélectionné sont signalées par une coche et sont triées dans l’ordre de priorité de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="e694b-119">Synchronization playlists for the currently selected device are marked with a check mark and are sorted in synchronization priority order.</span></span> <span data-ttu-id="e694b-120">Toutes les autres sélections sont décochées.</span><span class="sxs-lookup"><span data-stu-id="e694b-120">All other playlists are unchecked.</span></span>

<span data-ttu-id="e694b-121">Le contrôle ListView a été configuré pour une sélection unique.</span><span class="sxs-lookup"><span data-stu-id="e694b-121">The ListView control was configured for single selection.</span></span> <span data-ttu-id="e694b-122">L’ordre des sélections dans le contrôle ListView détermine leur priorité de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="e694b-122">The order of playlists in the ListView control determines their synchronization priority.</span></span> <span data-ttu-id="e694b-123">L’état activé d’une sélection individuelle détermine s’il s’agit d’une sélection de synchronisation pour l’appareil actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="e694b-123">The checked state of an individual playlist determines whether it is a synchronization playlist for the currently selected device.</span></span>

<span data-ttu-id="e694b-124">Le paramètre *lPSIndex* spécifie l’index de partenariat pour l’appareil mobile actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="e694b-124">The parameter *lPSIndex* specifies the partnership index for the currently selected portable device.</span></span>


```C++
STDMETHODIMP CSyncSettings::ShowPlaylists(long lPSIndex)
{ 
    HRESULT hr = S_OK; 
    ATLASSERT(m_pMainDlg);
   
    CComPtr<IWMPMediaCollection> spMediaCollection;
    CComPtr<IWMPPlaylist> spPlaylist; // Contains a playlist of all playlists.
    long lSyncItemCount= 0; // Count of items selected for synchronization. 

    ListView_DeleteAllItems(m_hPlView);

    m_spPlaylist.Release();
   
    if(lPSIndex == 0)
    {
        return S_OK;
    } 

    HCURSOR hCursor = LoadCursor(NULL, IDC_WAIT);
    HCURSOR hCursorOld = SetCursor(hCursor);

    if(SUCCEEDED(hr))
    {
        // Retrieve a pointer to IWMPMediaCollection.
        hr = m_spPlayer->get_mediaCollection(&spMediaCollection);
    }

    if(SUCCEEDED(hr) && spMediaCollection)
    {
        // Retrieve a playlist filled with IWMPMedia items.
        // Each IWMPMedia represents an individual playlist 
        // in the library.
        hr = spMediaCollection->getByAttribute(CComBSTR("MediaType"), CComBSTR("playlist"), &spPlaylist);
    }
 
    if(SUCCEEDED(hr) && spPlaylist)
    {  
        // Get the sync attribute name for the current device.
        CComBSTR bstrAttribute(g_szSyncAttributeNames[lPSIndex]);

        // Sort the playlist.
        // lSyncItemCount is the count of synchronization playlists.
        hr = SortPlaylist(spPlaylist, bstrAttribute, &lSyncItemCount);
     
        if(SUCCEEDED(hr))
        {
            m_spPlaylist = spPlaylist;  // Cache the playlist.

            long lCount = 0;
            spPlaylist->get_count(&lCount);
             
            // Fill the ListView control.
            for(long i = 0; i < lCount; i++)
            {
                CComPtr<IWMPMedia> spMedia;
                CComBSTR bstrPlaylistName;
                CComBSTR bstrVal; // Value of the SyncXX attribute.

                // Retrieve a playlist.
                hr = spPlaylist->get_item(i, &spMedia);

                if(SUCCEEDED(hr) && spMedia)
                {
                    // Get the name.
                    hr = spMedia->get_name(&bstrPlaylistName);
                }  
                if(SUCCEEDED(hr) && spMedia)
                {      
                    // Get the SyncXX attribute value.
                    hr = spMedia->getItemInfo(bstrAttribute, &bstrVal);
                }

                if(SUCCEEDED(hr) && bstrPlaylistName.Length())
                {
                    // Insert the item in the ListView control.
                    LVITEM lvI;
                    ZeroMemory(&lvI, sizeof(LVITEM));
                    lvI.mask = LVIF_TEXT; 
                    lvI.lParam = _wtol(bstrVal);
                    lvI.iItem = ListView_GetItemCount(m_hPlView);
                    lvI.pszText = "";
                    ListView_InsertItem(m_hPlView, &lvI);

                    // If this is a sync playlist, mark the check box.
                    if(i < lSyncItemCount)
                    {
                        ListView_SetCheckState(m_hPlView, i, TRUE);
                    }

                    // Display the playlist name.
                    lvI.iSubItem = 1;
                    lvI.pszText = COLE2T(bstrPlaylistName);
                    ListView_SetItem(m_hPlView, &lvI);
                }
            }
        }        
    }

    SetCursor(hCursorOld);
    return hr;
}
```



<span data-ttu-id="e694b-125">Pour l’implémentation de la fonction SortPlaylist, consultez [Tri des sélections par priorité de synchronisation](sorting-playlists-by-synchronization-priority.md).</span><span class="sxs-lookup"><span data-stu-id="e694b-125">For the implementation of the SortPlaylist function, see [Sorting Playlists by Synchronization Priority](sorting-playlists-by-synchronization-priority.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e694b-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e694b-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e694b-127">**IWMPMedia :: getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="e694b-127">**IWMPMedia::getItemInfo**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo)
</dt> <dt>

[<span data-ttu-id="e694b-128">**IWMPMediaCollection::getByAttribute**</span><span class="sxs-lookup"><span data-stu-id="e694b-128">**IWMPMediaCollection::getByAttribute**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyattribute)
</dt> <dt>

[<span data-ttu-id="e694b-129">**Gestion des sélections de synchronisation**</span><span class="sxs-lookup"><span data-stu-id="e694b-129">**Managing Synchronization Playlists**</span></span>](managing-synchronization-playlists.md)
</dt> <dt>

[<span data-ttu-id="e694b-130">**Attributs de synchronisation**</span><span class="sxs-lookup"><span data-stu-id="e694b-130">**Sync Attributes**</span></span>](sync-attributes.md)
</dt> </dl>

 

 




