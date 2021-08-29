---
title: Utilisation des profils système localisés
description: Utilisation des profils système localisés
ms.assetid: d911baf6-0731-4f02-9001-d04464a03f56
keywords:
- profils, système
- profils système, localisés
- profils système, interface IWMProfileManagerLanguage
- profils système localisés, à propos de
- IWMProfileManagerLanguage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9525ae51334b14b467324fa393438a9ad52106f4c7519c5ad9b0d00af9e3084
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083713"
---
# <a name="working-with-localized-system-profiles"></a>Utilisation des profils système localisés

le kit de développement logiciel (SDK) Windows Media Format comprend des profils système avec des noms et des descriptions dans plusieurs langues. Les fichiers. prx du profil système localisé sont installés dans le \[ \] \\ dossier SDKRoot WMSDK \\ WMFSDK9 \\ LocalizedProfiles Pour accéder à un fichier particulier avec les méthodes **IWMProfileManagerLanguage** , vous devez le déplacer dans le répertoire racine système avec les autres fichiers de profil système. Pour obtenir la liste des fichiers de profil système localisés, consultez [profils système localisés](localized-system-profiles.md).

Vous pouvez définir ou récupérer la langue du profil système à l’aide des méthodes de l’interface [**IWMProfileManagerLanguage**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) . La langue est spécifiée en tant que valeur LANGID, qui se compose d’un identificateur de langue primaire et d’un identificateur de langue secondaire. Le code suivant montre comment récupérer le langage actuel. La langue par défaut est anglais (États-Unis) (0x40C). Pour plus d’informations sur l’utilisation de ce code, consultez [utilisation des exemples de code](using-the-code-examples.md).


```C++
HRESULT GetCurrentSystemProfileLanguage(IMWProfilManager* pProfileMgr)
{
    HRESULT hr = S_OK;

    IWMProfileManagerLanguage* pProfileMgrLang = NULL;

    // Get the profile manager language interface.
    hr = pProfileMgr->QueryInterface(IID_IWMProfileManagerLanguage,
                                     (void **) &pProfileMgrLang);
    if(FAILED(hr))
    {
        printf("Couldn't get IWMProfileManagerLanguage.\n");
        SAFE_RELEASE(pProfileMgrLang);
        return hr;
    }

    // Retrieve the current language (as a LANGID value)
    WORD wLangID = 0;
    hr = pProfileMgrLang->GetUserLanguageID(&wLangID);
    if(FAILED(hr))
    {
        printf("Could not get the current language.\n");
        SAFE_RELEASE(pProfileMgrLang);
        return hr;
    }

    printf("The current language ID is 0x%X\n", wLangID);

    SAFE_RELEASE(pProfileMgrLang);
    return S_OK;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation des profils système**](using-system-profiles.md)
</dt> </dl>

 

 




