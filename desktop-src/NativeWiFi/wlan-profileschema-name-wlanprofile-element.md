---
description: Contient le nom d’un profil de réseau local sans fil.
ms.assetid: b8977183-7b5d-4c79-9065-ade85ed45716
title: Élément Name (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- name
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 79174d1cb24fff1841b3022fa06e201794415ce5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194728"
---
# <a name="name-wlanprofile-element"></a>Élément Name (WLANProfile)

L’élément Name (WLANProfile) contient le nom d’un profil de réseau local sans fil.

``` syntax
<xs:element name="name"
    type="nameType"
 />
```

L’élément **Name** est défini par l’élément [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .

## <a name="remarks"></a>Notes

Les noms respectent la casse.

pour Windows xp avec service pack 3 (SP3) et l’API de réseau local sans fil pour Windows XP avec service pack 2 (SP2), l’élément name est ignoré lorsque le profil est enregistré dans le magasin de profils. Le nom du profil est dérivé du SSID du réseau. Pour les profils réseau d’infrastructure, le nom du profil correspond à l’identificateur SSID du réseau. Pour les profils réseau ad hoc, le nom du profil correspond à l’identificateur SSID du réseau ad hoc suivi de `-adhoc` . Les caractères d’échappement XML, tels que les &, ne sont pas affichés. évitez d’utiliser des caractères d’échappement XML dans des noms SSID pour les profils déployés sur Windows xp avec SP3 ou une API de réseau local sans fil pour Windows XP avec SP2.

pour tout profil réseau destiné à être utilisé uniquement sur Windows Vista ou Windows Server 2008, le nom peut être n’importe quelle chaîne.

## <a name="examples"></a>Exemples

Pour afficher des exemples de profils qui utilisent l’élément **Name** , consultez Exemples de profils [sans fil](wireless-profile-samples.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                |
| Composant redistribuable<br/>          | API de réseau local sans fil pour Windows XP avec SP2<br/>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




