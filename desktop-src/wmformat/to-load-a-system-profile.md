---
title: Pour charger un profil système
description: Pour charger un profil système
ms.assetid: 2398a44d-c5c7-4fa2-b0ed-1cfb75d8822c
keywords:
- profils, système
- profils système, chargement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e745cb2fed32d650a22febef827ed7662f4448
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381512"
---
# <a name="to-load-a-system-profile"></a>Pour charger un profil système

Pour apporter des modifications à un profil système, vous devez le charger dans un objet de profil. Le gestionnaire de profils fournit deux options pour le chargement des profils système : par identificateur et par index.

Un identificateur de profil système est une valeur GUID affectée au profil système lors de sa création. Pour obtenir la liste des constantes GUID associées aux profils système de la version 8, consultez [profils système](system-profiles.md). Vous pouvez trouver les constantes GUID pour les versions précédentes dans le fichier d’en-tête WMSysPrf. h. Pour plus d’informations à ce sujet et sur les autres fichiers d’en-tête inclus dans le kit de développement logiciel (SDK) Windows Media format, consultez [fichiers de bibliothèque et paramètres du compilateur](library-files-and-compiler-settings.md).

L’exemple de code suivant montre comment charger un profil système à l’aide de l’identificateur de profil système. Pour que ce code fonctionne, vous devez inclure WMSysPrf. h et stdio. h. Pour plus d’informations sur l’utilisation de ce code, consultez [utilisation des exemples de code](using-the-code-examples.md).


```C++
IWMProfileManager* pProfileMgr = NULL;
IWMProfile*        pProfile    = NULL;

HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a profile manager.
hr = WMCreateProfileManager(&pProfileMgr);

// Retrieve the data for the general-purpose broadband video profile.
hr = pProfileMgr->LoadProfileByID(WMProfile_V80_100Video, &pProfile);

// TODO: Perform whatever customizations are needed. For details about
// editing profiles, see Using Custom Profiles.

// Clean up.
pProfile->Release();
pProfile = NULL;
pProfileMgr->Release();
pProfileMgr = NULL;
```



Si vous ne connaissez pas le profil que vous souhaitez utiliser, vous pouvez effectuer une itération dans tous les profils système d’une version particulière à l’aide des méthodes [**GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) et [**LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) de l’interface [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) . Ces méthodes traitent uniquement une version des profils système à la fois. Pour plus d’informations sur la modification de la version du profil système, consultez [pour modifier les versions de profil système](to-change-system-profile-versions.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation des profils système**](using-system-profiles.md)
</dt> </dl>

 

 




