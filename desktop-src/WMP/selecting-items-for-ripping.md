---
title: Sélection d’éléments pour l’extraction
description: Sélection d’éléments pour l’extraction
ms.assetid: 94bc765a-8318-4715-82e0-e7a9b93e99e0
keywords:
- Lecteur Windows Media, extraction de CD
- Modèle d’objet du lecteur Windows Media, extraction de CD
- modèle d’objet, extraction de CD
- Contrôle Windows Media Player ActiveX, extraction de CD
- Contrôle ActiveX, extraction de CD
- Windows Media Player Mobile contrôle ActiveX, extraction de CD
- Windows Media Player Mobile, extraction de CD
- Extraction de CD, sélection d’éléments
- extraction de CD, sélection d’éléments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc18ded43b609be6c7ac1f16833b0c8a33505ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940097"
---
# <a name="selecting-items-for-ripping"></a>Sélection d’éléments pour l’extraction

Parfois, un utilisateur ne souhaite pas extraire chaque piste sur un CD. Le lecteur Windows Media fournit une interface permettant de spécifier les pistes sélectionnées pour l’extraction. En général, dans une application d’extraction de CD, il existe une interface utilisateur qui permet à l’utilisateur de sélectionner des cases à cocher dans une liste de pistes sur le CD.

Certaines pistes peuvent ne pas être sélectionnées pour l’extraction par défaut. Si une piste figure déjà dans la bibliothèque du lecteur Windows Media, elle ne sera pas automatiquement sélectionnée pour l’extraction. Le deuxième exemple de code de cette section montre comment ignorer la valeur par défaut et sélectionner manuellement une piste d’extraction si elle a déjà été extraite.

L’exemple de code suivant montre comment déterminer si une piste est sélectionnée pour l’extraction :


```C++
HRESULT CMainDlg::IsTrackSelected(long lIndex, bool &bSelected)
{
    // The track is selected unless the
    // "SelectedForRip" attribute is true.
    bSelected = true;

    // bstrItemName and bstrVal are used for getItemInfo.
    CComBSTR bstrItemName;
    CComBSTR bstrVal;

    // Get an IWMPMedia from the Playlist.
    CComPtr<IWMPMedia> spMedia;
    HRESULT hr = m_spPlaylist->get_item(lIndex, &spMedia);

    // Check whether it is selected for ripping.
    if (SUCCEEDED(hr))
    {
        hr = bstrItemName.Append("SelectedForRip");
    }
    if (SUCCEEDED(hr))
    {
        hr = spMedia->getItemInfo(
            bstrItemName,
            &bstrVal);
    }
    if (SUCCEEDED(hr))
    {
        // If getItemInfo("SelectedForRip") is not "True"
        // then the track is not selected.
        if (wcscmp(bstrVal.m_str, L"True"))
            bSelected = false;
    }

    return hr;
}

```



L’exemple de code suivant montre comment spécifier si une piste est sélectionnée pour l’extraction.


```C++
HRESULT CMainDlg::SelectTrack (long lIndex, bool bSelected)
{
    // bstrItemName and bstrVal are used for setItemInfo.
    CComBSTR bstrItemName;
    CComBSTR bstrVal;

    // Get an IWMPMedia from the Playlist.
    CComPtr<IWMPMedia> spMedia;
    HRESULT hr = m_spPlaylist->get_item(lIndex, &spMedia);

    // Select the track for ripping.
    if (SUCCEEDED(hr))
    {
        hr = bstrItemName.Append("SelectedForRip");
    }
    if (SUCCEEDED(hr))
    {
        if (bSelected)
        {
            hr = bstrVal.Append("True");
        }
        else
        {
            hr = bstrVal.Append("False");
        }
    }
    if (SUCCEEDED(hr))
    {
        hr = spMedia->setItemInfo(
            bstrItemName,
            bstrVal);
    }

    return hr;
}

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Extraction d’un CD**](ripping-a-cd.md)
</dt> <dt>

[**Récupération de l’interface d’extraction**](retrieving-the-ripping-interface.md)
</dt> <dt>

[**Démarrage du processus RIP**](starting-the-rip-process.md)
</dt> <dt>

[**Récupération de l’État RIP**](retrieving-the-rip-status.md)
</dt> </dl>

 

 




