---
title: Extraction avec IWMPPlayerServices setTaskPane
description: Extraction avec IWMPPlayerServices setTaskPane
ms.assetid: 0d3efb0e-e8f5-40e3-abb5-6ad22009a4eb
keywords:
- Lecteur Windows Media, extraction de CD
- modèle d’objet Lecteur Windows Media, extraction de CD
- modèle d’objet, extraction de CD
- contrôle de ActiveX Lecteur Windows Media, extraction de CD
- contrôle de ActiveX, extraction de CD
- Lecteur Windows Media contrôle de ActiveX Mobile, extraction de CD
- Lecteur Windows Media Mobile, extraction de CD
- Extraction de CD, interface IWMPPlayerServices setTaskPane
- extraction de CD, interface IWMPPlayerServices setTaskPane
- Interface IWMPPlayerServices setTaskPane
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb1a09d67f310266ae4818bc0b594fe3b74d128
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010886"
---
# <a name="ripping-by-using-iwmpplayerservicessettaskpane"></a>Extraction à l’aide de IWMPPlayerServices :: setTaskPane

> [!Note]  
> cette section documente une fonctionnalité des contrôles de la série Lecteur Windows Media 9 et Lecteur Windows Media 10 ActiveX. Nous vous recommandons d’utiliser l’interface **IWMPCdromRip** avec les versions ultérieures. Voir [interface IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip).

 

vous pouvez utiliser le contrôle Lecteur Windows Media 9 ou version ultérieure pour copier les pistes des CD sur l’ordinateur de l’utilisateur. Ce processus est appelé *extraction*. pour ce faire, vous devez incorporer le contrôle Lecteur Windows Media en mode distant. pour plus d’informations sur le mode distant, consultez communication à distance [du contrôle Lecteur Windows Media](remoting-the-windows-media-player-control.md).

Pour démarrer le processus d’extraction, appelez [IWMPPlayerServices :: setTaskPane](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerservices-settaskpane), en passant le CopyFromCD ? Copie autocopie :*ID* du paramètre *bstrTaskPane* , où *ID* est l’index du lecteur de CD à partir duquel effectuer la copie. Cet index correspond à l’index d’un objet **cdrom** dans l’interface **IWMPCdromCollection** ou l’événement **CdromMediaChange** .

L’exemple de code suivant est une fonction qui démarre le processus d’extraction d’un CD à partir du lecteur de CD identifié par l’index zéro. La fonction utilise la variable de membre suivante :


```C++
CComPtr<IWMPPlayer4>  m_spPlayer;  // Smart pointer to IWMPPlayer4.

```



Le code suivant montre le corps de la fonction :


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



Affichage de l’État pour l’utilisateur

Lors de la copie à partir d’un CD-ROM, vous pouvez récupérer une chaîne contenant des informations d’État sur l’opération de copie. Pour ce faire, vous devez d’abord récupérer une sélection contenant des éléments multimédias représentant les pistes de CD en appelant [IWMPCdrom :: obtenir la \_ sélection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdrom-get_playlist). Comme dans l’exemple précédent, l’exemple de code suivant fonctionne avec l’index de lecteur CD zéro. Elle stocke la sélection récupérée dans la variable de membre suivante :


```C++
CComPtr<IWMPPlaylist>  m_spCDPlaylist;

```



Le code suivant montre le corps de la fonction :


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



Ensuite, gérez l’événement [IWMPEvents :: MediaChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-mediachange) . Cet événement se produit lorsqu’une piste de CD est extraite. Le pointeur **IDispatch** passé au gestionnaire d’événements pointe vers l’interface **IWMPMedia** pour la piste CD. Appelez **QueryInterface** via **IDispatch** pour récupérer le pointeur vers **IWMPMedia**.

Pour détecter la piste CD en cours d’extraction, comparez le pointeur **IWMPMedia** de l’événement aux éléments multimédias de la sélection de CD en appelant [IWMPMedia :: \_ isIdentical](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_isidentical).

Appelez [IWMPMedia :: getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo), en passant la chaîne « Status » comme nom d’élément. l' **état** est un attribut temporaire défini par Lecteur Windows Media sur les éléments multimédias pendant qu’ils sont extraits du CD. elle n’est pas disponible à partir de la bibliothèque.

L’exemple de code suivant montre un gestionnaire d’événements **MediaChange** .


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMPCdrom**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)
</dt> <dt>

[**Interface IWMPCdromCollection**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> <dt>

[**Interface IWMPEvents**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)
</dt> <dt>

[**Interface IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**Interface IWMPPlayerServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)
</dt> <dt>

[**Interface IWMPPlaylist**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[**Guide de contrôle du lecteur**](player-control-guide.md)
</dt> <dt>

[**Extraction à l’aide de l’interface IWMPCdromRip**](ripping-by-using-the-iwmpcdromrip-interface.md)
</dt> </dl>

 

 




