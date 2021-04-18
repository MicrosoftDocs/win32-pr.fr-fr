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
ms.openlocfilehash: dd8c040d9804cd822b17e7caad8a8cfb5e5854c4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106529066"
---
# <a name="working-with-localized-system-profiles"></a><span data-ttu-id="9b5f4-108">Utilisation des profils système localisés</span><span class="sxs-lookup"><span data-stu-id="9b5f4-108">Working with Localized System Profiles</span></span>

<span data-ttu-id="9b5f4-109">Le kit de développement logiciel (SDK) du format Windows Media comprend des profils système avec des noms et des descriptions dans plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="9b5f4-109">The Windows Media Format SDK includes system profiles with names and descriptions in several languages.</span></span> <span data-ttu-id="9b5f4-110">Les fichiers. prx du profil système localisé sont installés dans le \[ \] \\ dossier SDKRoot WMSDK \\ WMFSDK9 \\ LocalizedProfiles</span><span class="sxs-lookup"><span data-stu-id="9b5f4-110">The localized system profile .prx files are installed into the \[SDKRoot\]\\WMSDK\\WMFSDK9\\LocalizedProfiles folder.</span></span> <span data-ttu-id="9b5f4-111">Pour accéder à un fichier particulier avec les méthodes **IWMProfileManagerLanguage** , vous devez le déplacer dans le répertoire racine système avec les autres fichiers de profil système.</span><span class="sxs-lookup"><span data-stu-id="9b5f4-111">To access a particular file with the **IWMProfileManagerLanguage** methods, you must move it into the system root directory along with the other system profile files.</span></span> <span data-ttu-id="9b5f4-112">Pour obtenir la liste des fichiers de profil système localisés, consultez [profils système localisés](localized-system-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f4-112">For a list of the localized system profile files, see [Localized System Profiles](localized-system-profiles.md).</span></span>

<span data-ttu-id="9b5f4-113">Vous pouvez définir ou récupérer la langue du profil système à l’aide des méthodes de l’interface [**IWMProfileManagerLanguage**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) .</span><span class="sxs-lookup"><span data-stu-id="9b5f4-113">You can set or retrieve the system profile language using the methods of the [**IWMProfileManagerLanguage**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) interface.</span></span> <span data-ttu-id="9b5f4-114">La langue est spécifiée en tant que valeur LANGID, qui se compose d’un identificateur de langue primaire et d’un identificateur de langue secondaire.</span><span class="sxs-lookup"><span data-stu-id="9b5f4-114">The language is specified as a LANGID value, which consists of a primary language identifier and a secondary language identifier.</span></span> <span data-ttu-id="9b5f4-115">Le code suivant montre comment récupérer le langage actuel.</span><span class="sxs-lookup"><span data-stu-id="9b5f4-115">The following code demonstrates how to retrieve the current language.</span></span> <span data-ttu-id="9b5f4-116">La langue par défaut est anglais (États-Unis) (0x40C).</span><span class="sxs-lookup"><span data-stu-id="9b5f4-116">The default language is U.S. English (0x409).</span></span> <span data-ttu-id="9b5f4-117">Pour plus d’informations sur l’utilisation de ce code, consultez [utilisation des exemples de code](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f4-117">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="9b5f4-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9b5f4-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b5f4-119">**Utilisation des profils système**</span><span class="sxs-lookup"><span data-stu-id="9b5f4-119">**Using System Profiles**</span></span>](using-system-profiles.md)
</dt> </dl>

 

 




