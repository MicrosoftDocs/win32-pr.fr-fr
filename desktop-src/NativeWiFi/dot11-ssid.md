---
description: Contient le SSID d’une interface.
ms.assetid: f2b15ef9-99ee-4505-8575-224112024d7a
title: Structure DOT11_SSID (Wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_SSID
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: e319d22db33a627be631f9b6b0ee36591bc7a5bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866033"
---
# <a name="dot11_ssid-structure"></a>\_Structure SSID DOT11

Une structure de **\_ SSID DOT11** contient le SSID d’une interface.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _DOT11_SSID {
  ULONG uSSIDLength;
  UCHAR ucSSID[DOT11_SSID_MAX_LENGTH];
} DOT11_SSID, *PDOT11_SSID;
```



## <a name="members"></a>Membres

<dl> <dt>

**uSSIDLength**
</dt> <dd>

Longueur, en octets, du tableau **ucSSID** .

</dd> <dt>

**ucSSID**
</dt> <dd>

SSID. La \_ longueur maximale des SSID DOT11 \_ \_ est définie sur 32.

</dd> </dl>

## <a name="remarks"></a>Notes

Le SSID spécifié par le membre **ucSSID** n’est pas une chaîne ASCII terminée par le caractère null. La longueur du SSID est déterminée par le membre **uSSIDLength** .

Un SSID générique est un SSID dont le membre **uSSIDLength** a la valeur zéro. Lorsque le SSID souhaité est défini sur le SSID générique, la station 802,11 peut se connecter à n’importe quel réseau BSS (Service Set) de base.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                        |
| Composant redistribuable<br/>          | API de réseau local sans fil pour Windows XP avec SP2<br/>                                                         |
| En-tête<br/>                   | <dl> <dt>Wlantypes. h (inclure Windot11. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_paramètres de connexion WLAN \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> <dt>

[**WlanGetNetworkBssList**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlangetnetworkbsslist)
</dt> <dt>

[**WlanScan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan)
</dt> </dl>

 

 




