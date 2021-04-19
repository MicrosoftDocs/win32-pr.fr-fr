---
description: L’interface IScanProfileMgr fournit des méthodes pour créer, ouvrir, supprimer et gérer des profils d’analyse.
ms.assetid: f57a71b7-750c-42a8-be73-229f0145d9d5
title: Interface IScanProfileMgr (Scanprofilemgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 9f0762befdda272b91451dcca67c3f9560ad354e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514227"
---
# <a name="iscanprofilemgr-interface"></a>Interface IScanProfileMgr

L’interface **IScanProfileMgr** fournit des méthodes pour créer, ouvrir, supprimer et gérer des profils d’analyse.

## <a name="members"></a>Membres

L’interface **IScanProfileMgr** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IScanProfileMgr** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IScanProfileMgr** possède ces méthodes.



| Méthode                                                                              | Description                                                                                                            |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**CreateProfile**](-wia-iscanprofilemgr-createprofile.md)                         | Crée un profil de numérisation vide et l’associe à un scanneur ou à un autre élément WIA 2,0.<br/>                       |
| [**DeleteAllProfiles**](-wia-iscanprofilemgr-deleteallprofiles.md)                 | Supprime tous les profils d’analyse associés à l’appareil spécifié.<br/>                                         |
| [**DeleteAllProfilesForUser**](-wia-iscanprofilemgr-deleteallprofilesforuser.md)   | Supprime tous les profils d’analyse disponibles pour l’utilisateur dans le système sous lequel votre application s’exécute. <br/> |
| [**DeleteProfile**](-wia-iscanprofilemgr-deleteprofile.md)                         | Supprime le profil de numérisation spécifié.<br/>                                                                         |
| [**GetDefaultProfile**](-wia-iscanprofilemgr-getdefaultprofile.md)                 | Obtient le profil de numérisation par défaut.<br/>                                                                              |
| [**GetNumProfiles**](-wia-iscanprofilemgr-getnumprofiles.md)                       | Obtient le nombre de profils d’analyse créés pour l’utilisateur dans le système sous lequel votre application s’exécute.<br/> |
| [**GetNumProfilesforDeviceID**](-wia-iscanprofilemgr-getnumprofilesfordeviceid.md) | Obtient le nombre de profils de numérisation pour l’appareil.<br/>                                                            |
| [**GetProfiles**](-wia-iscanprofilemgr-getprofiles.md)                             | Obtient tous les profils d’analyse disponibles pour l’utilisateur dans le système sous lequel votre application s’exécute.<br/>     |
| [**GetProfilesforDeviceID**](-wia-iscanprofilemgr-getprofilesfordeviceid.md)       | Obtient tous les profils d’analyse associés à un appareil.<br/>                                                        |
| [**OpenProfile**](-wia-iscanprofilemgr-openprofile.md)                             | Ouvre un profil de numérisation enregistré sur le disque sous la forme d’un fichier XML.<br/>                                            |
| [**Générer**](-wia-iscanprofilemgr-refresh.md)                                     | Énumère à nouveau tous les profils d’analyse dans le système.<br/>                                                          |
| [**SetDefault**](-wia-iscanprofilemgr-setdefault.md)                               | Définit le profil d’analyse spécifié comme profil par défaut.<br/>                                                     |



 

## <a name="remarks"></a>Notes

Pour créer un objet **IScanProfileMgr** , utilisez la méthode [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) avec les paramètres suivants :

``` syntax
CoCreateInstance(CLSID_ScanProfileMgr, NULL, CLSCTX_LOCAL_SERVER, IID_IScanProfileMgr, ppv)
```

Si un profil de numérisation est enregistré à l’aide de la méthode [**IScanProfile :: Save**](-wia-iscanprofile-save.md) , il est stocké sous la forme d’un fichier XML dans% UserProfile%, \\ données d’application \\ Microsoft \\ document Center \\ UserScanProfiles.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                        |
| En-tête<br/>                   | <dl> <dt>Scanprofilemgr. h</dt> </dl> |
| MIDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Analyser le schéma de profil](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
