---
title: Méthode ActiveBasicDevice SetCachedSinkProtocolInfo (PlayToDevice. h)
description: Obtient les informations de protocole du récepteur mis en cache pour l’appareil. | Méthode ActiveBasicDevice SetCachedSinkProtocolInfo (PlayToDevice. h)
ms.assetid: C4856B97-89F9-43EC-B778-9E0CDAAF2C47
keywords:
- API de diffusion multimédia en continu de méthode SetCachedSinkProtocolInfo
- API de diffusion multimédia en continu de méthode SetCachedSinkProtocolInfo, interface ActiveBasicDevice
- API de diffusion multimédia en continu de l’interface ActiveBasicDevice, méthode SetCachedSinkProtocolInfo
topic_type:
- apiref
api_name:
- ActiveBasicDevice.SetCachedSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9100cb8faeb685a0cc7a8b7b73deb11afca29a3e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106545251"
---
# <a name="activebasicdevicesetcachedsinkprotocolinfo-method"></a>ActiveBasicDevice :: SetCachedSinkProtocolInfo, méthode

Obtient les informations de protocole du récepteur mis en cache pour l’appareil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetCachedSinkProtocolInfo(
  [in] GUID   physicalNetworkInterface,
  [in] UINT64 bitrate
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*physicalNetworkInterface* \[ dans\]
</dt> <dd>

Spécifie l’interface réseau physique.

</dd> <dt>

*débit binaire* \[ dans\]
</dt> <dd>

Valeur de la vitesse de transmission.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>PlayToDevice. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>PlayToDevice. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

