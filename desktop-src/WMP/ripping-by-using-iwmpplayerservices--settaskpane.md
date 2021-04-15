---
title: Extraction avec IWMPPlayerServices setTaskPane
description: Extraction avec IWMPPlayerServices setTaskPane
ms.assetid: 0d3efb0e-e8f5-40e3-abb5-6ad22009a4eb
keywords:
- Lecteur Windows Media, extraction de CD
- Modèle d’objet du lecteur Windows Media, extraction de CD
- modèle d’objet, extraction de CD
- Contrôle Windows Media Player ActiveX, extraction de CD
- Contrôle ActiveX, extraction de CD
- Windows Media Player Mobile contrôle ActiveX, extraction de CD
- Windows Media Player Mobile, extraction de CD
- Extraction de CD, interface IWMPPlayerServices setTaskPane
- extraction de CD, interface IWMPPlayerServices setTaskPane
- Interface IWMPPlayerServices setTaskPane
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb1a09d67f310266ae4818bc0b594fe3b74d128
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104462778"
---
# <a name="ripping-by-using-iwmpplayerservicessettaskpane"></a><span data-ttu-id="e411e-113">Extraction à l’aide de IWMPPlayerServices :: setTaskPane</span><span class="sxs-lookup"><span data-stu-id="e411e-113">Ripping by Using IWMPPlayerServices::setTaskPane</span></span>

> [!Note]  
> <span data-ttu-id="e411e-114">Cette section décrit une fonctionnalité des contrôles ActiveX du lecteur Windows Media série 9 et de Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="e411e-114">This section documents a feature of the Windows Media Player 9 Series and Windows Media Player 10 ActiveX controls.</span></span> <span data-ttu-id="e411e-115">Nous vous recommandons d’utiliser l’interface **IWMPCdromRip** avec les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e411e-115">It is recommended that you use the **IWMPCdromRip** interface with later versions.</span></span> <span data-ttu-id="e411e-116">Voir [interface IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip).</span><span class="sxs-lookup"><span data-stu-id="e411e-116">See [IWMPCdromRip Interface](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip).</span></span>

 

<span data-ttu-id="e411e-117">Vous pouvez utiliser le contrôle Windows Media Player 9 ou une version ultérieure pour copier les pistes des CD sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e411e-117">You can use the Windows Media Player 9 Series or later control to copy CD tracks to the user's computer.</span></span> <span data-ttu-id="e411e-118">Ce processus est appelé *extraction*.</span><span class="sxs-lookup"><span data-stu-id="e411e-118">This process is called *ripping*.</span></span> <span data-ttu-id="e411e-119">Pour ce faire, vous devez incorporer le contrôle du lecteur Windows Media en mode distant.</span><span class="sxs-lookup"><span data-stu-id="e411e-119">To do this, you must embed the Windows Media Player control in remote mode.</span></span> <span data-ttu-id="e411e-120">Pour plus d’informations sur le mode distant, consultez communication à distance [du contrôle du lecteur Windows Media](remoting-the-windows-media-player-control.md).</span><span class="sxs-lookup"><span data-stu-id="e411e-120">For more information about remote mode, see [Remoting the Windows Media Player Control](remoting-the-windows-media-player-control.md).</span></span>

<span data-ttu-id="e411e-121">Pour démarrer le processus d’extraction, appelez [IWMPPlayerServices :: setTaskPane](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerservices-settaskpane), en passant le CopyFromCD ? Copie autocopie :*ID* du paramètre *bstrTaskPane* , où *ID* est l’index du lecteur de CD à partir duquel effectuer la copie.</span><span class="sxs-lookup"><span data-stu-id="e411e-121">To start the ripping process, call [IWMPPlayerServices::setTaskPane](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerservices-settaskpane), passing the CopyFromCD?AutoCopy:*id* value for the *bstrTaskPane* parameter, where *id* is the index of the CD drive from which to copy.</span></span> <span data-ttu-id="e411e-122">Cet index correspond à l’index d’un objet **cdrom** dans l’interface **IWMPCdromCollection** ou l’événement **CdromMediaChange** .</span><span class="sxs-lookup"><span data-stu-id="e411e-122">This index corresponds to the index of a **Cdrom** object in the **IWMPCdromCollection** interface or the **CdromMediaChange** event.</span></span>

<span data-ttu-id="e411e-123">L’exemple de code suivant est une fonction qui démarre le processus d’extraction d’un CD à partir du lecteur de CD identifié par l’index zéro.</span><span class="sxs-lookup"><span data-stu-id="e411e-123">The following example code is a function that starts the process of ripping a CD from the CD drive identified by index zero.</span></span> <span data-ttu-id="e411e-124">La fonction utilise la variable de membre suivante :</span><span class="sxs-lookup"><span data-stu-id="e411e-124">The function uses the following member variable:</span></span>


```C++
CComPtr<IWMPPlayer4>  m_spPlayer;  // Smart pointer to IWMPPlayer4.

```



<span data-ttu-id="e411e-125">Le code suivant montre le corps de la fonction :</span><span class="sxs-lookup"><span data-stu-id="e411e-125">The following code shows the body of the function:</span></span>


```C++
HRESULT CMyApp::StartRip()
{
    CComPtr<IWMPPlayerApplication>  spPlayerApp;
    CComPtr<IWMPPlayerServices>     spPlayerServices;
    CComBSTR bstrParam;  // Contains the parameter string.

    ATLASSERT(m_spPlayer.p);

    HRESULT hr = m_spPlayer->QueryInterface(&spPlayerServices);

    if(SUCCEEDED(hr))
    {
        // Create the parameter string.
        hr = bstrParam.Append(_T("CopyFromCD?AutoCopy:0"));
    }

    if(SUCCEEDED(hr))
    {
        // Rip the CD in drive 0.
        hr = spPlayerServices->setTaskPane(bstrParam);
    }

    return hr;
}

```



<span data-ttu-id="e411e-126">Affichage de l’État pour l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="e411e-126">Displaying Status to the User</span></span>

<span data-ttu-id="e411e-127">Lors de la copie à partir d’un CD-ROM, vous pouvez récupérer une chaîne contenant des informations d’État sur l’opération de copie.</span><span class="sxs-lookup"><span data-stu-id="e411e-127">When copying from a CD, you can retrieve a string containing status information about the copy operation.</span></span> <span data-ttu-id="e411e-128">Pour ce faire, vous devez d’abord récupérer une sélection contenant des éléments multimédias représentant les pistes de CD en appelant [IWMPCdrom :: obtenir la \_ sélection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdrom-get_playlist).</span><span class="sxs-lookup"><span data-stu-id="e411e-128">To do this, you must first retrieve a playlist containing media items that represent the CD tracks by calling [IWMPCdrom::get\_playlist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdrom-get_playlist).</span></span> <span data-ttu-id="e411e-129">Comme dans l’exemple précédent, l’exemple de code suivant fonctionne avec l’index de lecteur CD zéro.</span><span class="sxs-lookup"><span data-stu-id="e411e-129">Like the previous example, the following example code works with CD drive index zero.</span></span> <span data-ttu-id="e411e-130">Elle stocke la sélection récupérée dans la variable de membre suivante :</span><span class="sxs-lookup"><span data-stu-id="e411e-130">It stores the retrieved playlist in the following member variable:</span></span>


```C++
CComPtr<IWMPPlaylist>  m_spCDPlaylist;

```



<span data-ttu-id="e411e-131">Le code suivant montre le corps de la fonction :</span><span class="sxs-lookup"><span data-stu-id="e411e-131">The following code shows the body of the function:</span></span>


```C++
HRESULT CMyApp::GetCDPlaylist()
{
    HRESULT hr = S_OK;

    // Release any existing playlist instance.
    m_spCDPlaylist.Release();

    CComPtr<IWMPCdromCollection> spCDDrives;
    CComPtr<IWMPCdrom>  spDrive;
    long lCount = 0;  // Count of CD drives.

    ATLASSERT(m_spPlayer);

    hr = m_spPlayer->get_cdromCollection(&spCDDrives);

    // Test to make sure there is at least one drive.
    if(SUCCEEDED(hr))
    {
        hr = spCDDrives->get_count(&lCount);
    }

    if(SUCCEEDED(hr) && lCount < 1)
    {
        MessageBox(_T("No CD drive detected"), 
                   _T("CD Rip Error"), MB_OK);
        hr = NS_E_CD_READ_ERROR;
    }

    if(SUCCEEDED(hr))
    {
        // Retrieve the first drive.
        hr = spCDDrives->item(0, &spDrive);
    }
    
    if(SUCCEEDED(hr))
    {
        // Get the playlist.
        hr = spDrive->get_playlist(&m_spCDPlaylist);
    }
   
    return hr;
}

```



<span data-ttu-id="e411e-132">Ensuite, gérez l’événement [IWMPEvents :: MediaChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-mediachange) .</span><span class="sxs-lookup"><span data-stu-id="e411e-132">Next, handle the [IWMPEvents::MediaChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-mediachange) event.</span></span> <span data-ttu-id="e411e-133">Cet événement se produit lorsqu’une piste de CD est extraite.</span><span class="sxs-lookup"><span data-stu-id="e411e-133">This event occurs when a CD track is being ripped.</span></span> <span data-ttu-id="e411e-134">Le pointeur **IDispatch** passé au gestionnaire d’événements pointe vers l’interface **IWMPMedia** pour la piste CD. Appelez **QueryInterface** via **IDispatch** pour récupérer le pointeur vers **IWMPMedia**.</span><span class="sxs-lookup"><span data-stu-id="e411e-134">The **IDispatch** pointer passed to the event handler points to the **IWMPMedia** interface for the CD track. Call **QueryInterface** through **IDispatch** to retrieve the pointer to **IWMPMedia**.</span></span>

<span data-ttu-id="e411e-135">Pour détecter la piste CD en cours d’extraction, comparez le pointeur **IWMPMedia** de l’événement aux éléments multimédias de la sélection de CD en appelant [IWMPMedia :: \_ isIdentical](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_isidentical).</span><span class="sxs-lookup"><span data-stu-id="e411e-135">To detect which CD track is being ripped, compare the **IWMPMedia** pointer from the event to the media items in the CD playlist by calling [IWMPMedia::get\_isIdentical](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_isidentical).</span></span>

<span data-ttu-id="e411e-136">Appelez [IWMPMedia :: getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo), en passant la chaîne « Status » comme nom d’élément.</span><span class="sxs-lookup"><span data-stu-id="e411e-136">Call [IWMPMedia::getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo), passing the string "Status" as the item name.</span></span> <span data-ttu-id="e411e-137">L' **État** est un attribut temporaire défini par le lecteur Windows Media sur les éléments multimédias pendant qu’ils sont extraits du CD. elle n’est pas disponible à partir de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="e411e-137">**Status** is a temporary attribute set by Windows Media Player on media items while they are being ripped from CD; it is not available from the library.</span></span>

<span data-ttu-id="e411e-138">L’exemple de code suivant montre un gestionnaire d’événements **MediaChange** .</span><span class="sxs-lookup"><span data-stu-id="e411e-138">The following example code shows a **MediaChange** event handler.</span></span>


```C++
void CMyApp::MediaChange(IDispatch * Item)
{
    // Test whether the CD playlist exists.
    if(!m_spCDPlaylist)
    {
        return;
    }

    // Declare and initialize variables.
    CComPtr<IWMPMedia> spMedia;
    HRESULT hr = S_OK;
    VARIANT_BOOL vbIdentical = VARIANT_FALSE;
    CComBSTR bstrVal;
    CComBSTR bstrName;
    long lCount = 0;  

    // Create the attribute value string.
    hr = bstrName.Append(_T("Status"));

    if(SUCCEEDED(hr))
    { 
        // Retrieve the IWMPMedia pointer from IDispatch.
        hr = Item->QueryInterface(__uuidof(IWMPMedia),(void**)&spMedia);
    }

    if(SUCCEEDED(hr))
    {
        // Get the value of the Status attribute.
        hr = spMedia->getItemInfo(bstrName, &bstrVal);
    }

    if(SUCCEEDED(hr))
    {
        // If the attribute is empty, set a failure code
        // to simply exit the function.
        if(bstrVal.Length() == 0)
        {
            hr = E_PENDING;
        }
    }
      
    if(SUCCEEDED(hr))
    {
        // Retrieve the count of items in the CD playlist.
        hr = m_spCDPlaylist->get_count(&lCount);
    }

    if(lCount < 1)
    {
        // Exit if the playlist is empty.
        hr = E_PENDING;
    }    

    if(SUCCEEDED(hr) && spMedia)
    {
        // Iterate through the playlist.
        // Compare the media item that raised the event
        // to each CD track. This detects which track
        // has a new status.
        for(long i = 0; i < lCount; i++)
        {
            CComPtr<IWMPMedia> spTrack;

            // Retrieve the CD track as a media object.
            hr = m_spCDPlaylist->get_item(i, &spTrack);

            if(SUCCEEDED(hr))
            {
                // Do the comparison.
                hr = spMedia->get_isIdentical(spTrack, &vbIdentical);
            }

            if(SUCCEEDED(hr) && VARIANT_TRUE == vbIdentical)
            {
                 // spTrack represents a track with changed status.
                 // bstrVal contains a status string. For example:
                 // "Ripping (10%)"
                 //
                 // TODO: Retrieve metadata about the track, and then
                 // display the status to the user.
            }
        }
    }

    return;
}

```



## <a name="related-topics"></a><span data-ttu-id="e411e-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e411e-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e411e-140">**Interface IWMPCdrom**</span><span class="sxs-lookup"><span data-stu-id="e411e-140">**IWMPCdrom Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)
</dt> <dt>

[<span data-ttu-id="e411e-141">**Interface IWMPCdromCollection**</span><span class="sxs-lookup"><span data-stu-id="e411e-141">**IWMPCdromCollection Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> <dt>

[<span data-ttu-id="e411e-142">**Interface IWMPEvents**</span><span class="sxs-lookup"><span data-stu-id="e411e-142">**IWMPEvents Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)
</dt> <dt>

[<span data-ttu-id="e411e-143">**Interface IWMPMedia**</span><span class="sxs-lookup"><span data-stu-id="e411e-143">**IWMPMedia Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[<span data-ttu-id="e411e-144">**Interface IWMPPlayerServices**</span><span class="sxs-lookup"><span data-stu-id="e411e-144">**IWMPPlayerServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)
</dt> <dt>

[<span data-ttu-id="e411e-145">**Interface IWMPPlaylist**</span><span class="sxs-lookup"><span data-stu-id="e411e-145">**IWMPPlaylist Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[<span data-ttu-id="e411e-146">**Guide de contrôle du lecteur**</span><span class="sxs-lookup"><span data-stu-id="e411e-146">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> <dt>

[<span data-ttu-id="e411e-147">**Extraction à l’aide de l’interface IWMPCdromRip**</span><span class="sxs-lookup"><span data-stu-id="e411e-147">**Ripping by Using the IWMPCdromRip Interface**</span></span>](ripping-by-using-the-iwmpcdromrip-interface.md)
</dt> </dl>

 

 




