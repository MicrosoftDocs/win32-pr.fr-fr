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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527789"
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

Pour Windows XP avec Service Pack 3 (SP3) et l’API de réseau local sans fil pour Windows XP avec Service Pack 2 (SP2), l’élément Name est ignoré lorsque le profil est enregistré dans le magasin de profils. Le nom du profil est dérivé du SSID du réseau. Pour les profils réseau d’infrastructure, le nom du profil correspond à l’identificateur SSID du réseau. Pour les profils réseau ad hoc, le nom du profil correspond à l’identificateur SSID du réseau ad hoc suivi de `-adhoc` . Les caractères d’échappement XML, tels que les &, ne sont pas affichés. Évitez d’utiliser des caractères d’échappement XML dans des noms SSID pour les profils déployés sur Windows XP avec SP3 ou l’API LAN sans fil pour Windows XP avec SP2.

Pour tout profil réseau destiné à être utilisé uniquement sur Windows Vista ou Windows Server 2008, le nom peut être n’importe quelle chaîne.

## <a name="examples"></a>Exemples

Pour afficher des exemples de profils qui utilisent l’élément **Name** , consultez Exemples de profils [sans fil](wireless-profile-samples.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                |
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

 

 




