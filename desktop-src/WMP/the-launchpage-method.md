---
title: Méthode LaunchPage
description: Méthode LaunchPage
ms.assetid: f0f93535-5afc-4777-9188-5bbac63ddc6b
keywords:
- plug-ins Lecteur Windows Media, méthode LaunchPage
- plug-ins, méthode LaunchPage
- plug-ins d’interface utilisateur, méthode LaunchPage
- Plug-ins d’interface utilisateur, méthode LaunchPage
- Méthode LaunchPage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11a22e1f4b136711a6f4336fbe54d6d90e4bb18b24a88645587311a0b4046f6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762719"
---
# <a name="the-launchpage-method"></a>Méthode LaunchPage

La méthode LaunchPage fournit la fonctionnalité principale du plug-in, qui consiste à lancer une page de recherche contenant des informations sur l’artiste de l’élément multimédia transmis à la méthode.

Cette méthode est appelée par la méthode OnSearch à l’aide de l’objet **média** actuel.

Le code suivant est utilisé pour implémenter cette méthode :


```C++
void LaunchPage(IWMPMedia *pMedia)
{
    USES_CONVERSION;

    HRESULT hr;
    CComBSTR bstrType;
    CComBSTR bstrArtist;

    // Get the name of the artist.
    bstrType = _T("artist");
    hr = pMedia->getItemInfo(bstrType, &bstrArtist);
    if (SUCCEEDED(hr)) 
    {
        // Create the search URL.
        TCHAR szSearch[MAX_PATH];
        _stprintf_s(szSearch, MAX_PATH, _T("https://search.msn.com/results.asp?q=%s"), OLE2T(bstrArtist));
        CComBSTR bstrURL = szSearch;

        // Launch the search page.
        m_pPlugin->m_spCore->launchURL(bstrURL);
    }
    else
    {
        MessageBox(_T("Failed to get artist information from media."), _T("Warn"), MB_OK | MB_ICONWARNING);
    }
}

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation de CPluginWindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




