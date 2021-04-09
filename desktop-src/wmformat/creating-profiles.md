---
title: Création de profils
description: Création de profils
ms.assetid: af4a8efe-d797-4d19-961d-b917e4c7c81a
keywords:
- Windows Media Format SDK, profils
- profils, création
- profils, interface IWMProfileManager
- IWMProfileManager, création de profils
- profils, fonction WMCreateProfileManager
- WMCreateProfileManager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45eeca9e99e09bd709b7e9fdf1aeffe8d35ca14a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030775"
---
# <a name="creating-profiles"></a>Création de profils

Dans de nombreux cas, vous souhaiterez peut-être créer un profil vide pour configurer vos besoins. Dans d’autres cas, il est plus facile de modifier un profil existant, comme un profil système. Pour plus d’informations sur l’utilisation des profils système, consultez [utilisation des profils système](using-system-profiles.md).

La création d’un profil vide, prêt à être configuré, nécessite un objet gestionnaire de profils. Pour obtenir l’interface [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) d’un objet de gestionnaire de profils, appelez la fonction [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .

Pour créer un profil vide, appelez [**IWMProfileManager :: CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile). Lorsque vous créez un profil vide, la seule chose que vous spécifiez est la version du kit de développement logiciel (SDK) de format Windows Media avec laquelle le profil est conforme. À moins que vous n’ayez besoin d’utiliser une version antérieure, vous devez toujours utiliser la version la plus récente. La version dicte la structure du profil ; les versions précédentes ne prenaient pas en charge certaines propriétés.

L’exemple de code suivant montre comment créer un nouveau profil. Pour compiler ce code dans votre application, incluez stdio. h. Pour plus d’informations sur l’utilisation de ce code, consultez [utilisation des exemples de code](using-the-code-examples.md).


```C++
HRESULT CreateProfile(IWMProfileManager* pProfileMgr, IWMProfile** ppProfile)
{
    HRESULT hr = S_OK;

    // Create the empty profile.
    hr = pProfileMgr->CreateEmptyProfile(WMT_VER_9_0, ppProfile);
    if(FAILED(hr))
    {
        printf("Could not create the profile.\n");
        return hr;
    }

    return S_OK;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMProfile**](iwmprofile.md)
</dt> <dt>

[**Interface IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**Utilisation des profils**](working-with-profiles.md)
</dt> </dl>

 

 




