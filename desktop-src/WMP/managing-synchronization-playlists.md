---
title: Gestion des sélections de synchronisation
description: Gestion des sélections de synchronisation
ms.assetid: 5891ada0-37a6-4256-9885-8aa9dbe98b7c
keywords:
- Lecteur Windows Media, appareils mobiles
- Modèle objet du lecteur Windows Media, appareils mobiles
- modèle objet, appareils mobiles
- Contrôle ActiveX du lecteur Windows Media, appareils mobiles
- Contrôle ActiveX, appareils mobiles
- Windows Media Player Mobile contrôle ActiveX, appareils mobiles
- Windows Media Player Mobile, appareils mobiles
- périphériques portables, gestion des sélections de synchronisation
- synchronisation des appareils, sélections
- synchronisation des appareils, des sélections
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
- sélections de synchronisation, gestion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be0fe084918c0b69b827dbb941388246cbd177ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512474"
---
# <a name="managing-synchronization-playlists"></a><span data-ttu-id="33cfa-124">Gestion des sélections de synchronisation</span><span class="sxs-lookup"><span data-stu-id="33cfa-124">Managing Synchronization Playlists</span></span>

<span data-ttu-id="33cfa-125">Le lecteur Windows Media 10 ou version ultérieure utilise des sélections pour synchroniser les fichiers multimédias numériques avec les périphériques portables.</span><span class="sxs-lookup"><span data-stu-id="33cfa-125">Windows Media Player 10 or later uses playlists to synchronize digital media files with portable devices.</span></span> <span data-ttu-id="33cfa-126">Cette section explique comment utiliser les sélections de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="33cfa-126">This section explains how to work with synchronization playlists.</span></span>

<span data-ttu-id="33cfa-127">L’exemple de code dans cette section utilise deux contrôles ListView pour afficher des informations.</span><span class="sxs-lookup"><span data-stu-id="33cfa-127">The example code in this section uses two ListView controls to display information.</span></span> <span data-ttu-id="33cfa-128">Le premier contrôle ListView (IDC \_ PLVIEW) affiche toutes les sélections dans la bibliothèque du lecteur Windows Media, les sélections de synchronisation apparaissant en premier.</span><span class="sxs-lookup"><span data-stu-id="33cfa-128">The first ListView control (IDC\_PLVIEW) displays all of the playlists in the Windows Media Player library, with synchronization playlists appearing first.</span></span> <span data-ttu-id="33cfa-129">Les sélections de synchronisation pour l’appareil actuellement sélectionné sont signalées par une coche et sont triées dans l’ordre de priorité de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="33cfa-129">Synchronization playlists for the currently selected device are marked with a check mark and are sorted in synchronization priority order.</span></span> <span data-ttu-id="33cfa-130">Toutes les autres sélections sont décochées.</span><span class="sxs-lookup"><span data-stu-id="33cfa-130">All other playlists are unchecked.</span></span> <span data-ttu-id="33cfa-131">Le contrôle ListView a été configuré pour une sélection unique.</span><span class="sxs-lookup"><span data-stu-id="33cfa-131">The ListView control was configured for single selection.</span></span> <span data-ttu-id="33cfa-132">L’ordre des sélections dans le contrôle ListView détermine leur priorité de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="33cfa-132">The order of playlists in the ListView control determines their synchronization priority.</span></span> <span data-ttu-id="33cfa-133">L’état activé d’une sélection individuelle détermine s’il s’agit d’une sélection de synchronisation pour l’appareil actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="33cfa-133">The checked state of an individual playlist determines whether it is a synchronization playlist for the currently selected device.</span></span>

<span data-ttu-id="33cfa-134">Le deuxième contrôle ListView (IDC \_ MEDIAVIEW) affiche les éléments multimédias dans la sélection sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="33cfa-134">The second ListView control (IDC\_MEDIAVIEW) displays the media items in the selected playlist.</span></span> <span data-ttu-id="33cfa-135">Deux colonnes supplémentaires affichent du texte indiquant si le fichier multimédia numérique a été copié sur l’appareil et, en cas de défaillance, si la copie a échoué parce que le fichier multimédia numérique n’est pas adapté.</span><span class="sxs-lookup"><span data-stu-id="33cfa-135">Two additional columns display text indicating whether the digital media file was copied to the device and, in the case of a failure, whether the copy failed because the digital media file did not fit.</span></span>

<span data-ttu-id="33cfa-136">L’exemple de code suivant montre comment les contrôles ListView sont initialisés :</span><span class="sxs-lookup"><span data-stu-id="33cfa-136">The following example code shows how the ListView controls are initialized:</span></span>


```C++
STDMETHODIMP CSyncSettings::InitListView()
{
    m_hPlView = GetDlgItem(IDC_PLVIEW);
    m_hMediaView = GetDlgItem(IDC_MEDIAVIEW); 

    ATLASSERT(m_hPlView);
    ATLASSERT(m_hMediaView);

    // Sync playlist information.
    // Selection highlights all rows.
    // Show checkboxes.
    ListView_SetExtendedListViewStyleEx(m_hPlView, 0, LVS_EX_CHECKBOXES | LVS_EX_FULLROWSELECT);
   
    // Add headers.
    LVCOLUMN lvc;
    ZeroMemory(&lvc, sizeof(LVCOLUMN));
    lvc.mask = LVCF_WIDTH | LVCF_TEXT | LVCF_SUBITEM; 
    lvc.iSubItem = 0;
    
    lvc.pszText = _T("Sync");
    lvc.cx = 40;
    ListView_InsertColumn(m_hPlView, lvc.iSubItem, &lvc);

    lvc.iSubItem++;
    lvc.pszText = _T("Playlist Name");
    lvc.cx = 300;
    ListView_InsertColumn(m_hPlView, lvc.iSubItem, &lvc); 

    // Media information.
    // Selection highlights all rows.
    ListView_SetExtendedListViewStyleEx(m_hMediaView, 0, LVS_EX_FULLROWSELECT);

    // Add headers
    ZeroMemory(&lvc, sizeof(LVCOLUMN));
    lvc.mask = LVCF_WIDTH | LVCF_TEXT | LVCF_SUBITEM; 
    lvc.iSubItem = 0;
    
    lvc.pszText = _T("Media name");
    lvc.cx = 150;
    ListView_InsertColumn(m_hMediaView, lvc.iSubItem, &lvc);

    lvc.iSubItem++;
    lvc.pszText = _T("On Device");
    lvc.cx = 69;
    ListView_InsertColumn(m_hMediaView, lvc.iSubItem, &lvc);  

    lvc.iSubItem++;
    lvc.pszText = _T("Fit?");
    lvc.cx = 40;
    ListView_InsertColumn(m_hMediaView, lvc.iSubItem, &lvc);  
   
    return S_OK;
}
```



<span data-ttu-id="33cfa-137">Le tableau de chaînes suivant contient les noms des attributs de synchronisation utilisés dans les exemples :</span><span class="sxs-lookup"><span data-stu-id="33cfa-137">The following array of strings contains the names of the synchronization attributes used in the examples:</span></span>


```C++
static const TCHAR *g_szSyncAttributeNames[17] = {
        _T("Not used"), // Do not access this one.
        _T("Sync01"),
        _T("Sync02"),
        _T("Sync03"),
        _T("Sync04"),
        _T("Sync05"),
        _T("Sync06"),
        _T("Sync07"),
        _T("Sync08"),
        _T("Sync09"),
        _T("Sync10"),
        _T("Sync11"),
        _T("Sync12"),
        _T("Sync13"),
        _T("Sync14"),
        _T("Sync15"),
        _T("Sync16")};
```



<span data-ttu-id="33cfa-138">La variable membre suivante contient une sélection contenant toutes les sélections de la bibliothèque du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="33cfa-138">The following member variable contains a playlist containing all playlists in the Windows Media Player library.</span></span> <span data-ttu-id="33cfa-139">Chaque sélection est représentée comme un élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="33cfa-139">Each playlist is represented as a media item.</span></span>


```C++
CComPtr<IWMPPlaylist> m_spPlaylist;
```



<span data-ttu-id="33cfa-140">Les sections suivantes fournissent un exemple de code :</span><span class="sxs-lookup"><span data-stu-id="33cfa-140">The following sections provide example code:</span></span>

-   [<span data-ttu-id="33cfa-141">Énumération des sélections de synchronisation</span><span class="sxs-lookup"><span data-stu-id="33cfa-141">Enumerating Synchronization Playlists</span></span>](enumerating-synchronization-playlists.md)
-   [<span data-ttu-id="33cfa-142">Tri des sélections par priorité de synchronisation</span><span class="sxs-lookup"><span data-stu-id="33cfa-142">Sorting Playlists by Synchronization Priority</span></span>](sorting-playlists-by-synchronization-priority.md)
-   [<span data-ttu-id="33cfa-143">Énumération des éléments multimédias</span><span class="sxs-lookup"><span data-stu-id="33cfa-143">Enumerating the Media Items</span></span>](enumerating-the-media-items.md)
-   [<span data-ttu-id="33cfa-144">Détermination de l’état de synchronisation des sélections</span><span class="sxs-lookup"><span data-stu-id="33cfa-144">Determining Playlist Synchronization State</span></span>](determining-playlist-synchronization-state.md)
-   [<span data-ttu-id="33cfa-145">Modification de la priorité de synchronisation</span><span class="sxs-lookup"><span data-stu-id="33cfa-145">Changing Synchronization Priority</span></span>](changing-synchronization-priority.md)

## <a name="related-topics"></a><span data-ttu-id="33cfa-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="33cfa-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33cfa-147">**Utilisation d’appareils mobiles**</span><span class="sxs-lookup"><span data-stu-id="33cfa-147">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




