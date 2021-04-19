---
description: Indique s’il faut se connecter à un réseau masqué.
ms.assetid: 31b859e9-adc7-49e2-91d9-4fb63a35addb
title: Élément SSIDConfig (unbroadcast)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nonBroadcast
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 695bede631b19c028a55a2f3ca82ba994ca12ada
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531827"
---
# <a name="nonbroadcast-ssidconfig-element"></a>Élément SSIDConfig (unbroadcast)

L’élément non diffusion (SSIDConfig) indique s’il faut se connecter à un réseau masqué. Si un réseau ne diffuse pas son SSID, il s’agit d’un réseau masqué. Si plusieurs SSID sont définis dans le profil, ils doivent tous avoir la même valeur de dédiffusion.

Si [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) a la valeur **ESS**, cette valeur peut être « true » ou « false ». Si cet élément n’est pas présent, la valeur par défaut est « false ».

Si [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) est défini sur **IBSS**, cette valeur doit être « false ». Si cet élément n’est pas présent, la valeur par défaut est « false ».

**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.

``` syntax
<xs:element name="nonBroadcast"
    type="boolean"
    minOccurs="0"
 />
```

L’élément est défini par l’élément [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) .

## <a name="examples"></a>Exemples

Pour afficher un exemple de profil qui utilise l’élément non **Broadcast** , consultez [exemple de profil de non-diffusion](non-broadcast-profile-sample.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**SSIDConfig (WLANProfile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> </dl>

 

 




