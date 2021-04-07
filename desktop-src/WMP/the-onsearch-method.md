---
title: Méthode OnSearch
description: Méthode OnSearch
ms.assetid: 709bb428-1a5e-4b8d-8622-5fcc816f0a1a
keywords:
- Plug-ins du lecteur Windows Media, méthode OnSearch
- plug-ins, méthode OnSearch
- plug-ins d’interface utilisateur, méthode OnSearch
- Plug-ins d’interface utilisateur, méthode OnSearch
- Méthode OnSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de5c33af434028e6ee72c757c8d71def0d4109fd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029319"
---
# <a name="the-onsearch-method"></a>Méthode OnSearch

La méthode OnSearch est appelée par le lecteur Windows Media quand l’utilisateur clique sur le bouton de **recherche** . Cette méthode récupère l’objet **multimédia** en cours et le passe à la méthode launchpage.

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

 

 




