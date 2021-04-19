---
title: Interface IWMProfile
description: L’interface IWMProfile est l’interface principale d’un objet de profil.
ms.assetid: 00f28d6b-d27d-4268-960e-c8ea25e5359e
keywords:
- Format Windows Media de l’interface IWMProfile
- Interface IWMProfile format Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location:
- wmsdkidl.h
ms.openlocfilehash: f814df820bd50a36abf2ee8e453549f46c9c5c9e
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "106511328"
---
# <a name="iwmprofile-interface"></a>Interface IWMProfile

L’interface **IWMProfile** est l’interface principale d’un objet de [*Profil*](wmformat-glossary.md) . Un objet de profil est utilisé pour configurer des profils personnalisés. Vous pouvez utiliser **IWMProfile** pour créer, supprimer ou modifier des objets de configuration de flux et des objets d’exclusion mutuelle. Vous pouvez également définir et récupérer des informations générales sur le profil. Pour accéder à toutes les fonctionnalités de l’objet profil, vous devez utiliser [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3), qui hérite de **IWMProfile** et [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2).

**IWMProfile** est également accessible via l’objet Reader, où vous pouvez l’utiliser pour obtenir des informations sur les flux d’un fichier chargé dans le lecteur. Lors de l’accès à **IWMProfile** à partir du lecteur, vous pouvez apporter des modifications au profil, mais aucune des modifications ne peut être enregistrée dans le fichier. Il est souvent pratique d’utiliser le profil d’un fichier existant comme base d’un nouveau profil. Le lecteur synchrone prend en charge **IWMProfile** de la même façon que le lecteur.

Les informations de profil obtenues via le lecteur ou le lecteur synchrone ne proviennent pas d’un fichier. prx. Le lecteur utilise les informations du fichier ASF pour assembler les configurations de flux. Ainsi, certaines informations de profil, telles que le nom et la description, ne sont pas disponibles via le lecteur.

Il existe plusieurs façons d’obtenir un pointeur vers une interface **IWMProfile** . Le gestionnaire de profils a des méthodes pour créer un nouveau profil et accéder aux profils existants. Toutes ces méthodes définissent un pointeur **IWMProfile** . Lors de la lecture d’un fichier, un pointeur vers **IWMProfile** peut être obtenu en appelant la méthode **QueryInterface** de toute interface de lecteur. De même, toute interface de l’objet de lecteur synchrone peut obtenir un pointeur avec un appel à **QueryInterface**[**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3).

## <a name="members"></a>Membres

L’interface **IWMProfile** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMProfile** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWMProfile** possède ces méthodes.



| Méthode                                                                  | Description                                                                                 |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion)             | Ajoute un objet d’exclusion mutuelle au profil.<br/>                                   |
| [**AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream)                               | Ajoute un flux au profil.<br/>                                                    |
| [**CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) | Crée un objet d’exclusion mutuelle pour le profil.<br/>                               |
| [**CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)                   | Crée un objet de configuration de flux pour le profil.<br/>                           |
| [**GetDescription**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getdescription)                     | Récupère la description du profil.<br/>                                        |
| [**GetMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)             | Récupère un objet d’exclusion mutuelle à partir du profil.<br/>                            |
| [**GetMutualExclusionCount**](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusioncount)   | Récupère le nombre d’objets d’exclusion mutuelle dans le profil.<br/>                 |
| [**GetName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getname)                                   | Récupère le nom du profil.<br/>                                               |
| [**GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)                               | Récupère un flux, à l’aide d’un numéro d’index, à partir du profil.<br/>                     |
| [**GetStreamByNumber**](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreambynumber)               | Récupère un flux, à l’aide du numéro du flux, à partir du profil.<br/>            |
| [**GetStreamCount**](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount)                     | Récupère le nombre de flux dans le profil.<br/>                                  |
| [**GetVersion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getversion)                             | Récupère le numéro de version de Microsoft Windows Media Services dans le profil.<br/> |
| [**ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream)                     | Permet d’inclure les modifications apportées à une configuration de flux dans le profil.<br/>    |
| [**RemoveMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removemutualexclusion)       | Supprime un objet d’exclusion mutuelle du profil.<br/>                              |
| [**RemoveStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removestream)                         | Supprime un flux du profil.<br/>                                               |
| [**RemoveStreamByNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removestreambynumber)         | Supprime un flux du profil.<br/>                                               |
| [**SetDescription**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-setdescription)                     | Spécifie la description du profil.<br/>                                        |
| [**SetName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-setname)                                   | Spécifie le nom du profil.<br/>                                               |



 

Pour plus d’informations sur les interfaces pouvant être obtenues à l’aide de la méthode QueryInterface de cette interface, consultez la rubrique relative à l’objet sur lequel cette interface est implémentée.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces**](interfaces.md)
</dt> <dt>

[**Interface IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**Gestionnaire de profils, objet**](profile-manager-object.md)
</dt> <dt>

[**Lecteur, objet**](reader-object.md)
</dt> <dt>

[**Lecteur synchrone, objet**](synchronous-reader-object.md)
</dt> <dt>

[**Utilisation des profils**](working-with-profiles.md)
</dt> </dl>

 

