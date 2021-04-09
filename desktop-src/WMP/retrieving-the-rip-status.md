---
title: Récupération de l’État RIP
description: Récupération de l’État RIP
ms.assetid: 9907bfdd-eae7-4ca2-b488-5a6ad11416f5
keywords:
- Lecteur Windows Media, extraction de CD
- Modèle d’objet du lecteur Windows Media, extraction de CD
- modèle d’objet, extraction de CD
- Contrôle Windows Media Player ActiveX, extraction de CD
- Contrôle ActiveX, extraction de CD
- Windows Media Player Mobile contrôle ActiveX, extraction de CD
- Windows Media Player Mobile, extraction de CD
- Extraction de CD, récupération de l’État RIP
- extraction de CD, récupération de l’État RIP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be1fce1a46f9cc2d8477cabcc12a3a1b5bd159d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030844"
---
# <a name="retrieving-the-rip-status"></a><span data-ttu-id="02b94-112">Récupération de l’État RIP</span><span class="sxs-lookup"><span data-stu-id="02b94-112">Retrieving the Rip Status</span></span>

<span data-ttu-id="02b94-113">Vous pouvez surveiller la progression de l’opération d’extraction en appelant périodiquement [IWMPCdromRip :: obten \_ ripProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress).</span><span class="sxs-lookup"><span data-stu-id="02b94-113">You can monitor the progress of the ripping operation by periodically calling [IWMPCdromRip::get\_ripProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress).</span></span> <span data-ttu-id="02b94-114">Cette méthode récupère une valeur de progression pour l’opération d’extraction entière.</span><span class="sxs-lookup"><span data-stu-id="02b94-114">This method retrieves a progress value for the entire ripping operation.</span></span> <span data-ttu-id="02b94-115">La valeur récupérée est un nombre qui représente le pourcentage d’extraction terminé, de 0 à 100.</span><span class="sxs-lookup"><span data-stu-id="02b94-115">The value retrieved is a number that represents the percentage of ripping completed, from 0 to 100.</span></span>

<span data-ttu-id="02b94-116">La valeur de progression représente le pourcentage terminé de l’ensemble du processus d’extraction.</span><span class="sxs-lookup"><span data-stu-id="02b94-116">The progress value represents the completed percentage of the entire ripping process.</span></span> <span data-ttu-id="02b94-117">Pour déterminer la progression d’une piste spécifique, utilisez [IWMPMedia :: getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo) avec « RipProgress » comme nom d’attribut.</span><span class="sxs-lookup"><span data-stu-id="02b94-117">To determine the progress of a specific track, use [IWMPMedia::getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo) with "RipProgress" as the attribute name.</span></span> <span data-ttu-id="02b94-118">Pour déterminer l’index de la piste actuellement extraite, appelez **IWMPPlaylist :: getItemInfo** avec « CurrentRipTrackIndex » comme nom d’attribut.</span><span class="sxs-lookup"><span data-stu-id="02b94-118">To determine the index of the track currently being ripped, call **IWMPPlaylist::getItemInfo** with "CurrentRipTrackIndex" as the attribute name.</span></span>

<span data-ttu-id="02b94-119">Vous pouvez surveiller l’état de l’opération d’extraction en appelant périodiquement [IWMPCdromRip :: obten \_ ripState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate).</span><span class="sxs-lookup"><span data-stu-id="02b94-119">You can monitor the state of the ripping operation by periodically calling [IWMPCdromRip::get\_ripState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate).</span></span> <span data-ttu-id="02b94-120">Cette méthode récupère une valeur d’énumération [WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) qui indique si l’opération est en cours ou arrêtée.</span><span class="sxs-lookup"><span data-stu-id="02b94-120">This method retrieves a [WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) enumeration value that indicates whether the operation is in progress or stopped.</span></span> <span data-ttu-id="02b94-121">Vous pouvez également surveiller l’état de l’opération d’extraction en gérant l’événement [IWMPEvents3 :: CdromRipStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) .</span><span class="sxs-lookup"><span data-stu-id="02b94-121">You can also monitor the state of the ripping operation by handling the [IWMPEvents3::CdromRipStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) event.</span></span> <span data-ttu-id="02b94-122">(Consultez [gestion des événements en C++](handling-events-in-c.md).) Veillez à comparer le pointeur **IWMPCdromRip** (fourni par l’événement) au pointeur qui représente votre opération d’extraction, pour vous assurer que l’événement a été déclenché par votre opération.</span><span class="sxs-lookup"><span data-stu-id="02b94-122">(See [Handling Events in C++](handling-events-in-c.md).) Be careful to compare the **IWMPCdromRip** pointer (provided by the event) to the pointer that represents your ripping operation, to ensure that the event was raised by your operation.</span></span>

<span data-ttu-id="02b94-123">L’exemple de code suivant montre comment utiliser ces fonctions pour récupérer l’état d’une opération d’extraction.</span><span class="sxs-lookup"><span data-stu-id="02b94-123">The following example code shows how to use these functions to retrieve the status of a ripping operation.</span></span>

<span data-ttu-id="02b94-124">Les contrôles de boîte de dialogue suivants sont définis pour l’exemple de code.</span><span class="sxs-lookup"><span data-stu-id="02b94-124">The following dialog controls are defined for the code example.</span></span>



| <span data-ttu-id="02b94-125">ID du contrôle</span><span class="sxs-lookup"><span data-stu-id="02b94-125">Control ID</span></span>                   | <span data-ttu-id="02b94-126">Description</span><span class="sxs-lookup"><span data-stu-id="02b94-126">Description</span></span>                                                                                                        |
|------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02b94-127">\_suivi actuel \_ IDC</span><span class="sxs-lookup"><span data-stu-id="02b94-127">IDC\_CURRENT\_TRACK</span></span>          | <span data-ttu-id="02b94-128">Texte statique qui représente l’index de la piste actuellement extraite.</span><span class="sxs-lookup"><span data-stu-id="02b94-128">Static text that represents the index of the track currently being ripped.</span></span>                                         |
| <span data-ttu-id="02b94-129">IDC \_ suivre \_ le \_ texte de progression</span><span class="sxs-lookup"><span data-stu-id="02b94-129">IDC\_TRACK\_PROGRESS\_TEXT</span></span>   | <span data-ttu-id="02b94-130">Texte statique qui représente la progression de la piste en cours d’extraction en tant que pourcentage.</span><span class="sxs-lookup"><span data-stu-id="02b94-130">Static text that represents the progress of the track currently being ripped as a percentage.</span></span>                      |
| <span data-ttu-id="02b94-131">\_suivi de progression IDC \_</span><span class="sxs-lookup"><span data-stu-id="02b94-131">IDC\_PROGRESS\_TRACK</span></span>         | <span data-ttu-id="02b94-132">Barre de progression avec une plage comprise entre 0 et 100 qui représente la progression de la piste en cours d’extraction en tant que pourcentage.</span><span class="sxs-lookup"><span data-stu-id="02b94-132">Progress bar with range 0 to 100 that represents the progress of the track currently being ripped as a percentage.</span></span> |
| <span data-ttu-id="02b94-133">\_texte de \_ progression \_ général IDC</span><span class="sxs-lookup"><span data-stu-id="02b94-133">IDC\_OVERALL\_PROGRESS\_TEXT</span></span> | <span data-ttu-id="02b94-134">Texte statique qui représente la progression du processus d’extraction total sous la forme d’un pourcentage.</span><span class="sxs-lookup"><span data-stu-id="02b94-134">Static text that represents the progress of the total ripping process as a percentage.</span></span>                             |
| <span data-ttu-id="02b94-135">\_progression IDC \_ globale</span><span class="sxs-lookup"><span data-stu-id="02b94-135">IDC\_PROGRESS\_OVERALL</span></span>       | <span data-ttu-id="02b94-136">Barre de progression avec une plage comprise entre 0 et 100 qui représente la progression du processus d’extraction total sous la forme d’un pourcentage.</span><span class="sxs-lookup"><span data-stu-id="02b94-136">Progress bar with range 0 to 100 that represents the progress of the total ripping process as a percentage.</span></span>        |
| <span data-ttu-id="02b94-137">\_État RIP \_ IDC</span><span class="sxs-lookup"><span data-stu-id="02b94-137">IDC\_RIP\_STATE</span></span>              | <span data-ttu-id="02b94-138">Texte statique qui affiche l’opération en cours d’exécution (« extraction », « arrêt » ou « inconnu »)</span><span class="sxs-lookup"><span data-stu-id="02b94-138">Static text that displays the operation currently being performed ("Ripping", "Stopped", or "Unknown")</span></span>             |



 


```C++
HRESULT CMainDlg::UpdateStatus (void)
{
    // bstrItemName and bstrVal are used for getItemInfo.
    CComBSTR bstrItemName;
    CComBSTR bstrVal;

    // Get the current track index.
    HRESULT hr = bstrItemName.Append("CurrentRipTrackIndex");
    if (SUCCEEDED(hr))
    {
        hr = m_spPlaylist->getItemInfo(bstrItemName, &bstrVal);
    }

    // Update the dialog text with the track number.
    if (SUCCEEDED(hr))
    {
        SetDlgItemTextW(IDC_CURRENT_TRACK, bstrVal.m_str);
    }

    // Get an IWMPMedia interface from the Playlist.
    CComPtr<IWMPMedia> spMedia;
    if (SUCCEEDED(hr))
    {
        long lIndex = _wtol(bstrVal.m_str);
        hr = m_spPlaylist->get_item(lIndex, &spMedia);
    }

    // Update the current track progress bar and progress text.
    if (SUCCEEDED(hr))
    {
        bstrItemName.Empty();
        hr = bstrItemName.Append("RipProgress");
    }
    if (SUCCEEDED(hr))
    {
        hr = spMedia->getItemInfo(bstrItemName, &bstrVal);
    }

    if (SUCCEEDED(hr))
    {
        // Update the text corresponding to the percentage.
        SetDlgItemTextW(IDC_TRACK_PROGRESS_TEXT, bstrVal.m_str);

        // Obtain a numerical value from the progress string.
        long lTrackPosition = _wtol(bstrVal.m_str);

        // Update the progress bar showing the percentage.
        SendMessage(GetDlgItem(IDC_PROGRESS_TRACK),
            PBM_SETPOS, lTrackPosition, 0);
    }

    // Update the total progress bar and progress text.
    long lTotalPosition = 0;
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromRip->get_ripProgress(&lTotalPosition);
    }
    if (SUCCEEDED(hr))
    {
        // Update the text corresponding to the percentage.
        SetDlgItemInt(IDC_OVERALL_PROGRESS_TEXT, lTotalPosition);

        // Update the progress bar showing the percentage.
        SendMessage(GetDlgItem(IDC_PROGRESS_OVERALL),
            PBM_SETPOS, lTotalPosition, 0);
    }

    // Update the ripping state.
    CComBSTR bstrState;
    WMPRipState wmprs = wmprsUnknown;
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromRip->get_ripState(&wmprs);
    }
    if (SUCCEEDED(hr))
    {
        switch (wmprs)
        {
            case wmprsUnknown:
            default:
                hr = bstrState.Append("Unknown");
                break;
            case wmprsRipping:
                hr = bstrState.Append("Ripping");
                break;
            case wmprsStopped:
                hr = bstrState.Append("Stopped");
                break;
        }
    }
    if (SUCCEEDED(hr))
    {
        SetDlgItemTextW(IDC_RIP_STATE, bstrState.m_str);
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="02b94-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="02b94-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02b94-140">**Extraction d’un CD**</span><span class="sxs-lookup"><span data-stu-id="02b94-140">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> <dt>

[<span data-ttu-id="02b94-141">**Récupération de l’interface d’extraction**</span><span class="sxs-lookup"><span data-stu-id="02b94-141">**Retrieving the Ripping Interface**</span></span>](retrieving-the-ripping-interface.md)
</dt> <dt>

[<span data-ttu-id="02b94-142">**Démarrage du processus RIP**</span><span class="sxs-lookup"><span data-stu-id="02b94-142">**Starting the Rip Process**</span></span>](starting-the-rip-process.md)
</dt> <dt>

[<span data-ttu-id="02b94-143">**Sélection d’éléments pour l’extraction**</span><span class="sxs-lookup"><span data-stu-id="02b94-143">**Selecting Items for Ripping**</span></span>](selecting-items-for-ripping.md)
</dt> </dl>

 

 




