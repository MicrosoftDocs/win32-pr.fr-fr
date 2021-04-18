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
# <a name="managing-synchronization-playlists"></a>Gestion des sélections de synchronisation

Le lecteur Windows Media 10 ou version ultérieure utilise des sélections pour synchroniser les fichiers multimédias numériques avec les périphériques portables. Cette section explique comment utiliser les sélections de synchronisation.

L’exemple de code dans cette section utilise deux contrôles ListView pour afficher des informations. Le premier contrôle ListView (IDC \_ PLVIEW) affiche toutes les sélections dans la bibliothèque du lecteur Windows Media, les sélections de synchronisation apparaissant en premier. Les sélections de synchronisation pour l’appareil actuellement sélectionné sont signalées par une coche et sont triées dans l’ordre de priorité de synchronisation. Toutes les autres sélections sont décochées. Le contrôle ListView a été configuré pour une sélection unique. L’ordre des sélections dans le contrôle ListView détermine leur priorité de synchronisation. L’état activé d’une sélection individuelle détermine s’il s’agit d’une sélection de synchronisation pour l’appareil actuellement sélectionné.

Le deuxième contrôle ListView (IDC \_ MEDIAVIEW) affiche les éléments multimédias dans la sélection sélectionnée. Deux colonnes supplémentaires affichent du texte indiquant si le fichier multimédia numérique a été copié sur l’appareil et, en cas de défaillance, si la copie a échoué parce que le fichier multimédia numérique n’est pas adapté.

L’exemple de code suivant montre comment les contrôles ListView sont initialisés :


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



Le tableau de chaînes suivant contient les noms des attributs de synchronisation utilisés dans les exemples :


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



La variable membre suivante contient une sélection contenant toutes les sélections de la bibliothèque du lecteur Windows Media. Chaque sélection est représentée comme un élément multimédia.


```C++
CComPtr<IWMPPlaylist> m_spPlaylist;
```



Les sections suivantes fournissent un exemple de code :

-   [Énumération des sélections de synchronisation](enumerating-synchronization-playlists.md)
-   [Tri des sélections par priorité de synchronisation](sorting-playlists-by-synchronization-priority.md)
-   [Énumération des éléments multimédias](enumerating-the-media-items.md)
-   [Détermination de l’état de synchronisation des sélections](determining-playlist-synchronization-state.md)
-   [Modification de la priorité de synchronisation](changing-synchronization-priority.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation d’appareils mobiles**](working-with-portable-devices.md)
</dt> </dl>

 

 




