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
# <a name="enumerating-synchronization-playlists"></a>Énumération des sélections de synchronisation

L’exemple de code suivant crée une fonction qui remplit un contrôle ListView avec des sélections. Les sélections de synchronisation s’affichent en premier. Les sélections de synchronisation pour l’appareil actuellement sélectionné sont signalées par une coche et sont triées dans l’ordre de priorité de synchronisation. Toutes les autres sélections sont décochées.

Le contrôle ListView a été configuré pour une sélection unique. L’ordre des sélections dans le contrôle ListView détermine leur priorité de synchronisation. L’état activé d’une sélection individuelle détermine s’il s’agit d’une sélection de synchronisation pour l’appareil actuellement sélectionné.

Le paramètre *lPSIndex* spécifie l’index de partenariat pour l’appareil mobile actuellement sélectionné.


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



Pour l’implémentation de la fonction SortPlaylist, consultez [Tri des sélections par priorité de synchronisation](sorting-playlists-by-synchronization-priority.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IWMPMedia :: getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo)
</dt> <dt>

[**IWMPMediaCollection::getByAttribute**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyattribute)
</dt> <dt>

[**Gestion des sélections de synchronisation**](managing-synchronization-playlists.md)
</dt> <dt>

[**Attributs de synchronisation**](sync-attributes.md)
</dt> </dl>

 

 




