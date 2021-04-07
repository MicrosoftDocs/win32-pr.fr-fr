---
title: Modification de la priorité de synchronisation
description: Modification de la priorité de synchronisation
ms.assetid: 992781cb-5018-4b88-aa93-2f8a86468a42
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
- périphériques portables, modification des priorités des sélections de synchronisation
- sélections de synchronisation, priorités
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327f211282e2e3b35c21dce721a17f99dcb6583d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723610"
---
# <a name="changing-synchronization-priority"></a><span data-ttu-id="d11dd-115">Modification de la priorité de synchronisation</span><span class="sxs-lookup"><span data-stu-id="d11dd-115">Changing Synchronization Priority</span></span>

<span data-ttu-id="d11dd-116">L’exemple de code suivant spécifie une valeur de priorité pour chaque élément dans le contrôle ListView identifié par IDC \_ PLVIEW.</span><span class="sxs-lookup"><span data-stu-id="d11dd-116">The following example code specifies a priority value for each item in the ListView control identified by IDC\_PLVIEW.</span></span> <span data-ttu-id="d11dd-117">Les éléments marqués avec une coche reçoivent une valeur de priorité en fonction de leur ordre dans la liste.</span><span class="sxs-lookup"><span data-stu-id="d11dd-117">Items that are marked with a check mark are assigned a priority value based on their order in the list.</span></span> <span data-ttu-id="d11dd-118">La valeur de priorité zéro est affectée aux éléments qui ne sont pas vérifiés.</span><span class="sxs-lookup"><span data-stu-id="d11dd-118">Items that are not checked are assigned a priority value of zero.</span></span>


```C++
void CSyncSettings::SetPriorities()
{
    ATLASSERT(m_spPlaylist.p);
    
    long lCount = 0;
    CComBSTR bstrAttribute(g_szSyncAttributeNames[m_lCurrentPSIndex]); 
    long lPriorityCount = 0; // Tracks the next priority value to be assigned.
    long lNewPriority = 0; // Contains the new priority value for the playlist.

    HRESULT hr = m_spPlaylist->get_count(&lCount);

    if(SUCCEEDED(hr) && lCount > 0)
    {
        HCURSOR hCursor = LoadCursor(NULL, IDC_WAIT);
        HCURSOR hCursorOld = SetCursor(hCursor);

        // Walk the list.
        for(long i = 0; i < lCount; i++)
        {
            CComPtr<IWMPMedia> spMedia;
            BOOL bChecked = ListView_GetCheckState(m_hPlView, i);

            if(TRUE == bChecked)
            {
                // Assign a priority value.
                lNewPriority = ++lPriorityCount;
            }
            else
            {
                // Not a sync playlist.
                lNewPriority = 0;
            }

            // Set the attribute on the playlist.
            hr = m_spPlaylist->get_item(i, &spMedia);

            if(SUCCEEDED(hr))
            {     
                WCHAR buffer[30];
                _ltow(lNewPriority, buffer, 10);
                CComBSTR bstrPriority(buffer);
                hr = spMedia->setItemInfo(bstrAttribute, bstrPriority);
            }
        }
        SetCursor(hCursorOld);
    }       
}
```



## <a name="related-topics"></a><span data-ttu-id="d11dd-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d11dd-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d11dd-120">**Interface IWMPMedia**</span><span class="sxs-lookup"><span data-stu-id="d11dd-120">**IWMPMedia Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[<span data-ttu-id="d11dd-121">**Interface IWMPPlaylist**</span><span class="sxs-lookup"><span data-stu-id="d11dd-121">**IWMPPlaylist Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[<span data-ttu-id="d11dd-122">**Gestion des sélections de synchronisation**</span><span class="sxs-lookup"><span data-stu-id="d11dd-122">**Managing Synchronization Playlists**</span></span>](managing-synchronization-playlists.md)
</dt> </dl>

 

 




