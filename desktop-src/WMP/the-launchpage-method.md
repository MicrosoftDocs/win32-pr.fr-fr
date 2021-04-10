---
title: Méthode LaunchPage
description: Méthode LaunchPage
ms.assetid: f0f93535-5afc-4777-9188-5bbac63ddc6b
keywords:
- Plug-ins du lecteur Windows Media, méthode LaunchPage
- plug-ins, méthode LaunchPage
- plug-ins d’interface utilisateur, méthode LaunchPage
- Plug-ins d’interface utilisateur, méthode LaunchPage
- Méthode LaunchPage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f04974eba1ba5c86300de44acd2ba6e2920954f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029421"
---
# <a name="the-launchpage-method"></a><span data-ttu-id="a6b62-108">Méthode LaunchPage</span><span class="sxs-lookup"><span data-stu-id="a6b62-108">The LaunchPage Method</span></span>

<span data-ttu-id="a6b62-109">La méthode LaunchPage fournit la fonctionnalité principale du plug-in, qui consiste à lancer une page de recherche contenant des informations sur l’artiste de l’élément multimédia transmis à la méthode.</span><span class="sxs-lookup"><span data-stu-id="a6b62-109">The LaunchPage method provides the primary functionality of the plug-in, which is to launch a search page containing information about the artist of the media item passed to the method.</span></span>

<span data-ttu-id="a6b62-110">Cette méthode est appelée par la méthode OnSearch à l’aide de l’objet **média** actuel.</span><span class="sxs-lookup"><span data-stu-id="a6b62-110">This method is called by the OnSearch method using the current **Media** object.</span></span>

<span data-ttu-id="a6b62-111">Le code suivant est utilisé pour implémenter cette méthode :</span><span class="sxs-lookup"><span data-stu-id="a6b62-111">The following code is used to implement this method:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a6b62-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a6b62-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6b62-113">**Implémentation de CPluginWindow**</span><span class="sxs-lookup"><span data-stu-id="a6b62-113">**Implementing CPluginWindow**</span></span>](implementing-cpluginwindow.md)
</dt> </dl>

 

 




