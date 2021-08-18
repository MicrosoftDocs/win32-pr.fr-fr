---
title: Pour modifier les versions de profil système
description: Pour modifier les versions de profil système
ms.assetid: 66bf4041-47b5-41b4-abb4-eb08d05e3b28
keywords:
- profils, système
- profils système, versions
- profils système, modification des versions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c963a142c879242b5e2ae734dedb4073a120a57a9121c3f3f95e5838c15110a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084269"
---
# <a name="to-change-system-profile-versions"></a>Pour modifier les versions de profil système

Chaque fois que vous créez un objet de gestionnaire de profils, il analyse les profils système. Vous pouvez itérer au sein des profils système à l’aide des méthodes [**IWMProfileManager :: GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) et [**IWMProfileManager :: LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) , mais le gestionnaire de profils compte et répertorie uniquement les profils d’une seule version à la fois. Si vous souhaitez utiliser cette méthode pour rechercher des profils système, vous devez vous assurer que le gestionnaire de profils gère la version que vous souhaitez. Utilisez les méthodes de l’interface [**IWMProfileManager2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2) pour définir et récupérer la version du profil système utilisée par le gestionnaire de profils.

Les versions sont spécifiées à l’aide des membres du type d’énumération de [**\_ version WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_version) . Si vous définissez la version du profil système sur WMT \_ ver \_ 9 \_ 0, l’appel échoue, mais le nombre de profils système est égal à zéro. cela est dû au fait qu’aucun profil système prédéfini n’utilise les codecs de série Windows Media Audio et Video 9. Pour plus d’informations sur la mise à jour des profils afin d’utiliser les codecs les plus récents, consultez [réutilisation des configurations de flux](reusing-stream-configurations.md).

Si vous chargez un profil système à l’aide de son identificateur GUID, la version du profil système utilisée par le gestionnaire de profils n’a pas d’importance. Pour plus d’informations sur le chargement des profils système, consultez [pour charger un profil système](to-load-a-system-profile.md).

L’exemple de code suivant montre comment définir et récupérer la version du profil système. Cet exemple utilise printf pour la sortie de la console et doit être inclus stdio. h. Pour plus d’informations sur l’utilisation de ce code, consultez [utilisation des exemples de code](using-the-code-examples.md).


```C++
int main(void)
{
    HRESULT hr = S_OK;

    IWMProfileManager*  pProfileMgr  = NULL;
    IWMProfileManager2* pProfileMgr2 = NULL;

    WMT_VERSION         profileVersion;

    // Initialize COM.
    hr = CoInitialize(NULL);
    if(FAILED(hr))
    {
        printf("Could not initialize COM.");
        return 0;
    }

    // Create a profile manager object.
    hr = WMCreateProfileManager(&pProfileMgr);
    if(FAILED(hr))
    {
        printf("Could not create a profile manager object.");
        return 0;
    }

    // Get the IWMProfileManager2 interface.
    hr = pProfileMgr->QueryInterface(IID_IWMProfileManager2, 
                                     (void**) &pProfileMgr2);
    if(FAILED(hr))
    {
        printf("Could not get the IWMProfileManager2 interface.");
        SAFE_RELEASE(pProfileMgr);
        return 0;
    }

    // Release the old interface.
    SAFE_RELEASE(pProfileMgr);

    // Get the current system profile version.
    hr = pProfileMgr2->GetSystemProfileVersion(&profileVersion);
    if(FAILED(hr))
    {
        printf("Could not retrieve profile version.");
        printf("\nError code: 0x%X\n", hr);
        SAFE_RELEASE(pProfileMgr2);
        return 0;
    }
    
    // Display the current version.
    printf("Current version: ");
    switch(profileVersion)
    {
    case WMT_VER_4_0:
        printf("WMT_VER_4_0\n");
        break;
    case WMT_VER_7_0:
        printf("WMT_VER_7_0\n");
        break;
    case WMT_VER_8_0:
        printf("WMT_VER_8_0\n");
        break;
    case WMT_VER_9_0:
        printf("WMT_VER_9_0\n");
        break;
    }

    // Set the system profile version to 8.
    profileVersion = WMT_VER_8_0;

    hr = pProfileMgr2->SetSystemProfileVersion(profileVersion);
    if(FAILED(hr))
    {
        printf("Could not change profile version.");
        printf("\nError code: 0x%X\n", hr);
        SAFE_RELEASE(pProfileMgr2);
        return 0;
    }

    // Print verification.
    printf("Successfully set version to ");
    switch(profileVersion)
    {
    case WMT_VER_4_0:
        printf("WMT_VER_4_0\n");
        break;
    case WMT_VER_7_0:
        printf("WMT_VER_7_0\n");
        break;
    case WMT_VER_8_0:
        printf("WMT_VER_8_0\n");
        break;
    case WMT_VER_9_0:
        printf("WMT_VER_9_0\n");
        break;
    }

    // Clean up.
    SAFE_RELEASE(pProfileMgr2);
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation des profils système**](using-system-profiles.md)
</dt> </dl>

 

 




