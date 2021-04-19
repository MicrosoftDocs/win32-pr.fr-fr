---
title: Énumération des éléments multimédias
description: Énumération des éléments multimédias
ms.assetid: 1819b4c3-57ae-48fc-8a01-b699b5802b64
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
ms.openlocfilehash: e8e07148ed6978355056febfb2ad920e4b1380a3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106545735"
---
# <a name="enumerating-the-media-items"></a><span data-ttu-id="6766e-116">Énumération des éléments multimédias</span><span class="sxs-lookup"><span data-stu-id="6766e-116">Enumerating the Media Items</span></span>

<span data-ttu-id="6766e-117">Le code suivant affiche les éléments multimédias contenus dans une sélection individuelle.</span><span class="sxs-lookup"><span data-stu-id="6766e-117">The following code displays the media items contained in an individual playlist.</span></span> <span data-ttu-id="6766e-118">Ce code s’exécute lorsque l’utilisateur clique sur une sélection dans le contrôle ListView identifié par IDC \_ PLVIEW.</span><span class="sxs-lookup"><span data-stu-id="6766e-118">This code runs when the user clicks a playlist in the ListView control identified by IDC\_PLVIEW.</span></span>


```C++
STDMETHODIMP CSyncSettings::ShowMedia(long lIndex)
{
    ATLASSERT(m_pMainDlg != NULL);
    ATLASSERT(m_spPlaylist.p);

    HRESULT hr = S_OK;
    long lCount = 0; // Count of items in the playlist.

    LVITEM lvI;
    ZeroMemory(&lvI, sizeof(LVITEM));
    lvI.mask = LVIF_TEXT;

    CComPtr<IWMPMedia> spPlaylist; // Playlist the user selected.
    CComBSTR bstrSourceURL; // The URL of a digital media file.
    CComPtr<IWMPPlaylist> spNewPlaylist; // Temporary playlist that contains media items.
    ULONG ulOnDevice = 0;
    ULONG ulDidNotFit = 0;

    HCURSOR hCursor = LoadCursor(NULL, IDC_WAIT);
    HCURSOR hCursorOld = SetCursor(hCursor);

    ListView_DeleteAllItems(m_hMediaView);

    // Retrieve the playlist the user selected.
    hr = m_spPlaylist->get_item(lIndex, &spPlaylist);
  
    if(SUCCEEDED(hr) && spPlaylist)
    {
         // Retrieve the source URL (the path).
         hr = spPlaylist->get_sourceURL(&bstrSourceURL);
    }

    if(SUCCEEDED(hr) && bstrSourceURL.Length())
    {
        CComPtr<IWMPCore3> spCore3;
        m_spPlayer.QueryInterface(&spCore3);

        // Create a temporary IWMPPlaylist object from the IWMPMedia 
        // playlist object.
        hr = spCore3->newPlaylist(CComBSTR("Temp"), bstrSourceURL, &spNewPlaylist);
    }

    if(SUCCEEDED(hr) && spNewPlaylist)
    {        
        hr = spNewPlaylist->get_count(&lCount);
    }

    // Walk the playlist.
    if(SUCCEEDED(hr) && lCount > 0)
    {
        for(long i = 0; i < lCount; i++)
        {
            CComPtr<IWMPMedia> spMedia;
            CComBSTR bstrMediaName; 
            CComBSTR bstrOnDevice = "???";
            CComBSTR bstrFit = "???";  

            hr = spNewPlaylist->get_item(i, &spMedia);
   
            if(SUCCEEDED(hr) && spMedia)
            {
                // Get the name.
                hr = spMedia->get_name(&bstrMediaName);                
            }

            if(SUCCEEDED(hr) && bstrMediaName.Length())
            {   
                // Show the media name.
                lvI.iItem = ListView_GetItemCount(m_hMediaView);
                lvI.iSubItem = 0;
                lvI.pszText = COLE2T(bstrMediaName);
                ListView_InsertItem(m_hMediaView, &lvI);
                
                // Retrieve the synchronization state information for 
                // the digital media file.
                hr = GetPartnershipSyncState(spMedia, m_lCurrentPSIndex, &ulOnDevice, &ulDidNotFit);
            }

            if(SUCCEEDED(hr))
            {                
                // Test whether the media is on the device.
                if(ulOnDevice == 1)
                {
                    bstrOnDevice = "Yes";
                    bstrFit = "Yes";
                }
                else
                {
                    bstrOnDevice = "No";
                    // 1 means media did not fit, 
                    // 0 means other reason for failure.
                    bstrFit = ulDidNotFit ? "No" : "Yes"; 
                }                 
            }
   
            ListView_SetItemText(m_hMediaView, lvI.iItem, 1, COLE2T(bstrOnDevice)); 
            ListView_SetItemText(m_hMediaView, lvI.iItem, 2, COLE2T(bstrFit));
        }
    } 

    if(SUCCEEDED(hr) && lCount == 0)
    {
        // Empty playlist.
        lvI.iItem = ListView_GetItemCount(m_hMediaView);
        lvI.iSubItem = 0;
        lvI.pszText = COLE2T(CComBSTR("No items to display."));
        ListView_InsertItem(m_hMediaView, &lvI);
    }
    
    SetCursor(hCursorOld);
    return hr;
}
```



<span data-ttu-id="6766e-119">Pour l’implémentation de la fonction GetPartnershipSyncState, consultez [détermination](determining-playlist-synchronization-state.md)de l’état de synchronisation de la playlist.</span><span class="sxs-lookup"><span data-stu-id="6766e-119">For the implementation of the GetPartnershipSyncState function, see [Determining Playlist Synchronization State](determining-playlist-synchronization-state.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6766e-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6766e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6766e-121">**Interface IWMPMedia**</span><span class="sxs-lookup"><span data-stu-id="6766e-121">**IWMPMedia Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[<span data-ttu-id="6766e-122">**Interface IWMPPlaylist**</span><span class="sxs-lookup"><span data-stu-id="6766e-122">**IWMPPlaylist Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[<span data-ttu-id="6766e-123">**Gestion des sélections de synchronisation**</span><span class="sxs-lookup"><span data-stu-id="6766e-123">**Managing Synchronization Playlists**</span></span>](managing-synchronization-playlists.md)
</dt> </dl>

 

 




