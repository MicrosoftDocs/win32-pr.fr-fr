---
title: Récupération de l’état d’avancement
description: Récupération de l’état d’avancement
ms.assetid: 63b6525d-00be-4c68-8473-3bc1a58fde15
keywords:
- Lecteur Windows Media, gravure de CD
- Windows Media Player Object Model, gravage de CD
- modèle d’objet, gravage de CD
- Contrôle ActiveX du lecteur Windows Media, gravure de CD
- Contrôle ActiveX, gravage de CD
- Windows Media Player Mobile contrôle ActiveX, gravure de CD
- Lecteur Windows Media Mobile, gravure de CD
- Gravage de CD, récupération de l’état de gravure
- gravure de CD, récupération de l’état d’avancement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9b9ab1d865b728c3a23b9b77f45ab022226605
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103940699"
---
# <a name="retrieving-the-burn-status"></a><span data-ttu-id="a9bda-112">Récupération de l’état d’avancement</span><span class="sxs-lookup"><span data-stu-id="a9bda-112">Retrieving the Burn Status</span></span>

<span data-ttu-id="a9bda-113">Dans l’exemple de code qui suit, les contrôles de boîte de dialogue suivants sont définis :</span><span class="sxs-lookup"><span data-stu-id="a9bda-113">In the code example that follows, the following dialog controls are defined:</span></span>



| <span data-ttu-id="a9bda-114">ID du contrôle</span><span class="sxs-lookup"><span data-stu-id="a9bda-114">Control ID</span></span>           | <span data-ttu-id="a9bda-115">Description</span><span class="sxs-lookup"><span data-stu-id="a9bda-115">Description</span></span>                                                                    |
|----------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="a9bda-116">\_État de gravure IDC \_</span><span class="sxs-lookup"><span data-stu-id="a9bda-116">IDC\_BURN\_STATE</span></span>     | <span data-ttu-id="a9bda-117">Texte statique qui représente l’état de l’opération de gravure de CD.</span><span class="sxs-lookup"><span data-stu-id="a9bda-117">Static text that represents the state of the CD burning operation.</span></span>             |
| <span data-ttu-id="a9bda-118">progression d’IDC \_</span><span class="sxs-lookup"><span data-stu-id="a9bda-118">IDC\_PROGRESS</span></span>        | <span data-ttu-id="a9bda-119">Barre de progression avec une plage comprise entre 0 et 100 qui représente la progression totale de la gravure.</span><span class="sxs-lookup"><span data-stu-id="a9bda-119">Progress bar with a range of 0 to 100 that represents the total burn progress.</span></span> |
| <span data-ttu-id="a9bda-120">\_texte de progression IDC \_</span><span class="sxs-lookup"><span data-stu-id="a9bda-120">IDC\_PROGRESS\_TEXT</span></span>  | <span data-ttu-id="a9bda-121">Texte statique qui représente la progression totale de la gravure sous la forme d’un nombre compris entre 0 et 100.</span><span class="sxs-lookup"><span data-stu-id="a9bda-121">Static text that represents the total burn progress as a number from 0 to 100.</span></span> |
| <span data-ttu-id="a9bda-122">\_heure disponible d’IDC \_</span><span class="sxs-lookup"><span data-stu-id="a9bda-122">IDC\_AVAILABLE\_TIME</span></span> | <span data-ttu-id="a9bda-123">Texte statique pour afficher l’heure disponible sur le CD, en secondes.</span><span class="sxs-lookup"><span data-stu-id="a9bda-123">Static text to display the time available on the CD, in seconds.</span></span>               |
| <span data-ttu-id="a9bda-124">\_espace libre \_ IDC</span><span class="sxs-lookup"><span data-stu-id="a9bda-124">IDC\_FREE\_SPACE</span></span>     | <span data-ttu-id="a9bda-125">Texte statique pour afficher l’espace libre sur le CD, en octets.</span><span class="sxs-lookup"><span data-stu-id="a9bda-125">Static text to display the free space on the CD, in bytes.</span></span>                     |
| <span data-ttu-id="a9bda-126">\_espace total \_ IDC</span><span class="sxs-lookup"><span data-stu-id="a9bda-126">IDC\_TOTAL\_SPACE</span></span>    | <span data-ttu-id="a9bda-127">Texte statique pour afficher la capacité totale du CD, en octets.</span><span class="sxs-lookup"><span data-stu-id="a9bda-127">Static text to display the total capacity of the CD, in bytes.</span></span>                 |



 

<span data-ttu-id="a9bda-128">Vous pouvez surveiller la progression de l’opération de gravure en appelant régulièrement [IWMPCdromBurn :: obten \_ burnProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress) pendant la gravure du CD.</span><span class="sxs-lookup"><span data-stu-id="a9bda-128">You can monitor the progress of the burning operation by periodically calling [IWMPCdromBurn::get\_burnProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress) while the CD is being burned.</span></span> <span data-ttu-id="a9bda-129">Cette méthode récupère une valeur de progression pour l’ensemble de l’opération de gravure.</span><span class="sxs-lookup"><span data-stu-id="a9bda-129">This method retrieves a progress value for the entire burning operation.</span></span> <span data-ttu-id="a9bda-130">La valeur récupérée est un nombre qui représente le pourcentage de brûlures terminées, de 0 à 100.</span><span class="sxs-lookup"><span data-stu-id="a9bda-130">The value retrieved is a number that represents the percentage of burning completed, from 0 to 100.</span></span>


```C++
// Update the progress bar IDC_PROGRESS
// and the corresponding text string IDC_PROGRESS_TEXT.
long lProgress = 0;
hr = m_spCdromBurn->get_burnProgress(&lProgress);
if (SUCCEEDED(hr))
{
    SendMessage(GetDlgItem(IDC_PROGRESS),
        PBM_SETPOS, lProgress, 0);
    SetDlgItemInt(IDC_PROGRESS_TEXT, lProgress);
}

```



<span data-ttu-id="a9bda-131">Vous pouvez récupérer l’état actuel de l’opération de gravure en appelant [IWMPCdromBurn :: obten \_ burnState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnstate).</span><span class="sxs-lookup"><span data-stu-id="a9bda-131">You can get the current state of the burning operation by calling [IWMPCdromBurn::get\_burnState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnstate).</span></span> <span data-ttu-id="a9bda-132">Cette méthode récupère une énumération spécifiant l’opération en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a9bda-132">This method retrieves an enumeration specifying the current operation being performed.</span></span>


```C++
// Retrieve the burn state.
WMPBurnState wmpbs = wmpbsUnknown;
HRESULT hr = m_spCdromBurn->get_burnState(&wmpbs);

if (SUCCEEDED(hr))
{
    // Set the burn state string.
    CComBSTR bstrState;
    switch (wmpbs)
    {
        case wmpbsUnknown:
        default:
            hr = bstrState.Append("Unknown state.");
            break;
        case wmpbsBusy:
            hr = bstrState.Append("Windows Media Player is Busy.");
            break;
        case wmpbsReady:
            hr = bstrState.Append("Ready to begin burning.");
            break;
        case wmpbsWaitingForDisc:
            hr = bstrState.Append("Waiting for disc.");
            break;
        case wmpbsRefreshStatusPending:
            hr = bstrState.Append("The burn playlist has changed.");
            m_spCdromBurn->refreshStatus();
            break;
        case wmpbsPreparingToBurn:
            hr = bstrState.Append("Preparing to burn the CD.");
            break;
        case wmpbsBurning:
            hr = bstrState.Append("The CD is being burned.");
            break;
        case wmpbsStopped:
            hr = bstrState.Append("The burning operation is stopped.");
            break;
        case wmpbsErasing:
            hr = bstrState.Append("Erasing the CD.");
            break;
    }
    if (SUCCEEDED(hr))
    {
        SetDlgItemTextW(IDC_BURN_STATE, bstrState.m_str);
    }
}

```



<span data-ttu-id="a9bda-133">Pour récupérer le nombre de secondes que le CD peut contenir, appelez [IWMPCdromBurn :: getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-getiteminfo) avec « AvailableTime » comme premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="a9bda-133">To retrieve the number of seconds of audio the CD can hold, call [IWMPCdromBurn::getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-getiteminfo) with "AvailableTime" as the first parameter.</span></span> <span data-ttu-id="a9bda-134">La valeur récupérée par cette fonction est représentée par une chaîne.</span><span class="sxs-lookup"><span data-stu-id="a9bda-134">The value retrieved by this function is represented by a string.</span></span>


```C++
// Set "AvailableTime" string
CComBSTR bstrTime;
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("AvailableTime");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->getItemInfo(bstrItem, &bstrTime);
}
if (SUCCEEDED(hr))
{
    hr = bstrTime.Append(" seconds");
}
if (SUCCEEDED(hr))
{
    SetDlgItemTextW(IDC_AVAILABLE_TIME, bstrTime.m_str);
}

```



<span data-ttu-id="a9bda-135">Pour récupérer la quantité d’espace libre sur un disque, appelez **IWMPCdromBurn :: getItemInfo** avec « FreeSpace » comme premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="a9bda-135">To retrieve the amount of free space on a disc, call **IWMPCdromBurn::getItemInfo** with "FreeSpace" as the first parameter.</span></span> <span data-ttu-id="a9bda-136">La valeur récupérée par cette fonction est une chaîne qui représente le nombre d’octets libres disponibles sur le disque.</span><span class="sxs-lookup"><span data-stu-id="a9bda-136">The value retrieved by this function is a string that represents the number of free bytes available on the disc.</span></span>


```C++
// Set "FreeSpace" string
CComBSTR bstrFreeSpace;
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("FreeSpace");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->getItemInfo(bstrItem, &bstrFreeSpace);
}
if (SUCCEEDED(hr))
{
    hr = bstrFreeSpace.Append(" bytes");
}
if (SUCCEEDED(hr))
{
    SetDlgItemTextW(IDC_FREE_SPACE, bstrFreeSpace.m_str);
}

```



<span data-ttu-id="a9bda-137">Pour récupérer la capacité totale d’un disque, appelez **IWMPCdromBurn :: getItemInfo** avec « TotalSpace » comme premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="a9bda-137">To retrieve the total capacity of a disc, call **IWMPCdromBurn::getItemInfo** with "TotalSpace" as the first parameter.</span></span> <span data-ttu-id="a9bda-138">La valeur récupérée par cette fonction est une chaîne qui correspond au nombre total d’octets sur le disque.</span><span class="sxs-lookup"><span data-stu-id="a9bda-138">The value retrieved by this function is a string that corresponds to the total number of bytes on the disc.</span></span>


```C++
// Set "TotalSpace" string.
CComBSTR bstrTotalSpace;
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("TotalSpace");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->getItemInfo(bstrItem, &bstrTotalSpace);
}
if (SUCCEEDED(hr))
{
    hr = bstrTotalSpace.Append(" bytes");
}
if (SUCCEEDED(hr))
{
    SetDlgItemTextW(IDC_TOTAL_SPACE, bstrTotalSpace.m_str);
}

```



## <a name="related-topics"></a><span data-ttu-id="a9bda-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a9bda-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9bda-140">**Gravure d’un CD**</span><span class="sxs-lookup"><span data-stu-id="a9bda-140">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="a9bda-141">**Récupération de l’interface de gravure de CD**</span><span class="sxs-lookup"><span data-stu-id="a9bda-141">**Retrieving the CD Burning Interface**</span></span>](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[<span data-ttu-id="a9bda-142">**Démarrage du processus de gravure**</span><span class="sxs-lookup"><span data-stu-id="a9bda-142">**Starting the Burn Process**</span></span>](starting-the-burn-process.md)
</dt> <dt>

[<span data-ttu-id="a9bda-143">**Effacement d’un CD réinscriptible**</span><span class="sxs-lookup"><span data-stu-id="a9bda-143">**Erasing a Rewritable CD**</span></span>](erasing-a-rewritable-cd.md)
</dt> <dt>

[<span data-ttu-id="a9bda-144">**Récupération de l’état du lecteur et du disque**</span><span class="sxs-lookup"><span data-stu-id="a9bda-144">**Retrieving the Drive and Disc Status**</span></span>](retrieving-the-drive-and-disc-status.md)
</dt> </dl>

 

 




