---
title: Méthode OnSearch
description: Méthode OnSearch
ms.assetid: 709bb428-1a5e-4b8d-8622-5fcc816f0a1a
keywords:
- plug-ins Lecteur Windows Media, méthode OnSearch
- plug-ins, méthode OnSearch
- plug-ins d’interface utilisateur, méthode OnSearch
- Plug-ins d’interface utilisateur, méthode OnSearch
- Méthode OnSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ab5cb4b26d291a940ed329e2422240e6fc36e5ba980431af169d58f1398fdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117999"
---
# <a name="the-onsearch-method"></a>Méthode OnSearch

la méthode OnSearch est appelée par Lecteur Windows Media lorsque l’utilisateur clique sur le bouton de **recherche** . Cette méthode récupère l’objet **multimédia** en cours et le passe à la méthode launchpage.

Le code suivant est utilisé pour implémenter cette méthode :


```C++
LRESULT OnSearch(WORD wNotifyCode, WORD wID, HWND hwndCtl, BOOL& fHandled)
{
    HRESULT hr;
    CComPtr<IWMPMedia> spMedia;

    if( m_pPlugin && m_pPlugin->m_spCore )
    {
        // Get a pointer to the current media item.
        hr = m_pPlugin->m_spCore->get_currentMedia(&spMedia);
        if (SUCCEEDED(hr) && spMedia)
        {
            LaunchPage(spMedia);
        }
    else
        {
            MessageBox(_T("There is no media loaded."), _T("Warn"), MB_OK | MB_ICONWARNING);
        }
    }
    return 0;
}

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation de CPluginWindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




