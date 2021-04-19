---
title: IMsRdpClientAdvancedSettings7 propriété NetworkConnectionType
description: Obtient ou définit le type de connexion réseau utilisé entre le client et le serveur. Les informations sur le type de connexion réseau transmises au serveur permettent au serveur d’ajuster plusieurs paramètres en fonction du type de connexion réseau.
ms.assetid: 4dd4fa17-f121-412d-a30d-1c01f4c892b0
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété NetworkConnectionType
- Services Bureau à distance de la propriété NetworkConnectionType, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété NetworkConnectionType
- Services Bureau à distance de la propriété NetworkConnectionType, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété NetworkConnectionType
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.NetworkConnectionType
- IMsRdpClientAdvancedSettings7.get_NetworkConnectionType
- IMsRdpClientAdvancedSettings7.put_NetworkConnectionType
- IMsRdpClientAdvancedSettings8.NetworkConnectionType
- IMsRdpClientAdvancedSettings8.get_NetworkConnectionType
- IMsRdpClientAdvancedSettings8.put_NetworkConnectionType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5df4c1e944920759f56f5d4b493b9cd47e7ebc29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509726"
---
# <a name="imsrdpclientadvancedsettings7networkconnectiontype-property"></a>IMsRdpClientAdvancedSettings7 :: NetworkConnectionType, propriété

Obtient ou définit le type de connexion réseau utilisé entre le client et le serveur. Les informations sur le type de connexion réseau transmises au serveur permettent au serveur d’ajuster plusieurs paramètres en fonction du type de connexion réseau.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_NetworkConnectionType(
  [in]          UINT connectionType
);

HRESULT get_NetworkConnectionType(
  [out, retval] UINT *pConnectionType
);
```



## <a name="property-value"></a>Valeur de la propriété

Type de connexion réseau.

<dt>

<span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>

<span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>**Connexion \_ TAPEZ \_ modem** (1 (0x1))


</dt> <dd>

Modem (56 Kbits/s)

</dd> <dt>

<span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>

<span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>**Connexion \_ TAPEZ \_ haut débit \_ bas** (2 (0X2))


</dt> <dd>

Bande passante basse vitesse (256 kbits/s à 2 Mbits/s)

</dd> <dt>

<span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>

<span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>**Connexion \_ TYPE \_ satellite** (3 (0x3))


</dt> <dd>

Satellite (2 Mbits/s à 16 Mbits/s, avec une latence élevée)

</dd> <dt>

<span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>

<span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>**Connexion \_ TYPE haut \_ débit \_ élevé** (4 (0x4))


</dt> <dd>

Haut débit haute vitesse (2 Mbits/s à 10 Mbits/s)

</dd> <dt>

<span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>

<span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>**Connexion \_ TYPE \_ WAN** (5 (0x5))


</dt> <dd>

Réseau étendu (WAN) (10 Mbits/s ou plus, avec une latence élevée)

</dd> <dt>

<span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>

<span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>**Connexion \_ TAPEZ \_ LAN** (6 (0x6))


</dt> <dd>

Réseau local (LAN) (10 Mbits/s ou plus)

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7<br/>                                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                                |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 est défini en tant que 26036036-4010-4578-8091-0db9a1edf9c3<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





