---
description: L’interface IScanProfile représente un profil de numérisation unique et permet aux applications de définir et d’obtenir les propriétés du profil.
ms.assetid: 5cd76256-d64e-4934-8cc2-0a467c7e34a9
title: Interface IScanProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile
api_type:
- COM
api_location:
- Scanprofiles.idl
ms.openlocfilehash: 1de80ac23ffa3e2687e2e6d0449f7a273067d5899204c479f9b62e8571190d61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450829"
---
# <a name="iscanprofile-interface"></a>Interface IScanProfile

L’interface **IScanProfile** représente un profil de numérisation unique et permet aux applications de définir et d’obtenir les propriétés du profil.

## <a name="members"></a>Membres

L’interface **IScanProfile** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IScanProfile** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IScanProfile** possède ces méthodes.



| Méthode                                                     | Description                                                                                                                                         |
|:-----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAllPropIDs**](-wia-iscanprofile-getallpropids.md)   | Obtient tous les ID de propriété disponibles dans un profil.<br/>                                                                                            |
| [**GetDeviceID**](-wia-iscanprofile-getdeviceid.md)       | Retourne l’ID de l’appareil.<br/>                                                                                                            |
| [**GetGUID**](-wia-iscanprofile-getguid.md)               | Retourne le GUID du profil.<br/>                                                                                                         |
| [**GetItem**](-wia-iscanprofile-getitem.md)               | Obtient le GUID de la catégorie de l’élément WIA 2,0 auquel le profil est associé.<br/>                                                   |
| [**GetName**](-wia-iscanprofile-getname.md)               | Obtient le nom convivial du profil.<br/>                                                                                                   |
| [**GetNumPropIDS**](-wia-iscanprofile-getnumpropids.md)   | Obtient le nombre d’ID de propriété dans un profil.<br/>                                                                                            |
| [**GetProperty**](-wia-iscanprofile-getproperty.md)       | Obtient la valeur des propriétés enfants spécifiées dans l' `<Properties>` élément d’un profil de numérisation.<br/>                                            |
| [**IsDefault**](-wia-iscanprofile-isdefault.md)           | Obtient une valeur qui indique si le profil est le profil de numérisation par défaut d’un appareil [**IWiaItem2**](-wia-iwiaitem2.md) associé.<br/> |
| [**RemoveProperty**](-wia-iscanprofile-removeproperty.md) | Supprime une liste spécifiée de propriétés enfants dans l' `<Properties>` élément d’un profil de numérisation.<br/>                                            |
| [**Enregistrer**](-wia-iscanprofile-save.md)                     | Enregistre les modifications apportées à un profil sur le disque.<br/>                                                                                                      |
| [**SetItem**](-wia-iscanprofile-setitem.md)               | Définit le GUID de la catégorie de l’élément WIA 2,0 auquel le profil est associé.<br/>                                                       |
| [**SetName**](-wia-iscanprofile-setname.md)               | Définit le nom convivial du profil.<br/>                                                                                                   |
| [**SetProperty**](-wia-iscanprofile-setproperty.md)       | Définit la valeur des propriétés enfants spécifiées dans l' `<Properties>` élément d’un profil de numérisation.<br/>                                            |



 

## <a name="remarks"></a>Remarques

Tout appareil [**IWiaItem2**](-wia-iwiaitem2.md) peut avoir un profil de numérisation. Toutefois, les éléments **IWiaItem2** de type WIA la \_ catégorie \_ \_ fichier fini et la racine de catégorie WIA \_ \_ ne peuvent pas avoir de profils.

Si un profil de numérisation est enregistré à l’aide de la méthode [**IScanProfile :: Save**](-wia-iscanprofile-save.md) , il est stocké sous la forme d’un fichier XML dans% UserProfile%, \\ données d’application \\ Microsoft \\ document Center \\ UserScanProfiles.

Pour créer une instance d’un objet **IScanProfile** , utilisez la méthode [**IScanProfileMgr :: CreateProfile**](-wia-iscanprofilemgr-createprofile.md) . Pour obtenir une référence à un profil de numérisation qui a déjà été enregistré sur le disque, utilisez la méthode [**IScanProfileMgr :: OpenProfile**](-wia-iscanprofilemgr-openprofile.md) .

Tous les profils d’analyse comportent les éléments suivants : `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` et `<Properties>` . Le profil par défaut d’un appareil possède également un `<Default>` élément.

Les `<ProfileGUID>` `<DeviceID>` éléments et ne peuvent pas être modifiés une fois le profil créé. Les valeurs de l' `<ProfileName>` élément et de l' `<WiaItem>` élément peuvent être modifiées après la création du profil. L' `<Default>` élément peut être ajouté ou supprimé. Cela peut être effectué par programmation avec les méthodes [**IScanProfile :: SetName**](-wia-iscanprofile-setname.md), [**IScanProfile :: SetItem**](-wia-iscanprofile-setitem.md)et [**IScanProfileMgr :: SetDefault**](-wia-iscanprofilemgr-setdefault.md) . Ces propriétés peuvent également être modifiées par les utilisateurs par le biais de la méthode [**IScanProfileUI :: ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .

L' `<Properties>` élément contient des `<Property>` enfants. Utilisez-les pour ajouter n’importe quel élément ou propriété d’appareil WIA 2,0 au profil. Vous pouvez également développer votre propre image acquisition `<Property>` Children. Cela rend le schéma de profil d’analyse extensible. (Pour plus d’informations sur l’extension du schéma, consultez [définition des propriétés personnalisées](-wia-defining-custom-properties.md), [**IScanProfile :: GetProperty**](-wia-iscanprofile-getproperty.md)et [**IScanProfile :: SetProperty**](-wia-iscanprofile-setproperty.md).)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                        |
| MIDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Analyser le schéma de profil](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
