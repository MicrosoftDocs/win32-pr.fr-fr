---
title: Méthode ActiveBasicDevice GetCachedSinkProtocolInfo (PlayToDevice. h)
description: Obtient les informations de protocole du récepteur mis en cache pour l’appareil. | Méthode ActiveBasicDevice GetCachedSinkProtocolInfo (PlayToDevice. h)
ms.assetid: C6A3C4B5-1883-4E71-83D2-11E378A4FBCA
keywords:
- API de diffusion multimédia en continu de méthode GetCachedSinkProtocolInfo
- API de diffusion multimédia en continu de méthode GetCachedSinkProtocolInfo, interface ActiveBasicDevice
- API de diffusion multimédia en continu de l’interface ActiveBasicDevice, méthode GetCachedSinkProtocolInfo
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1a9ebda71f59dc4bd887479b5ff9e763844b32985736f8cf224ed4981f04b34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736395"
---
# <a name="activebasicdevicegetcachedsinkprotocolinfo-method"></a>ActiveBasicDevice :: GetCachedSinkProtocolInfo, méthode

Obtient les informations de protocole du récepteur mis en cache pour l’appareil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCachedSinkProtocolInfo(
  [out, retval] HSTRING *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ out, retval\]
</dt> <dd>

Informations de protocole du récepteur mis en cache pour l’appareil.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>PlayToDevice. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>PlayToDevice. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

