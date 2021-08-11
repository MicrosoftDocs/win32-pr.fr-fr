---
title: Méthode ActiveBasicDevice GetCachedBitrateMeasurement (PlayToDevice. h)
description: Obtient le débit binaire mis en cache.
ms.assetid: 78C3C5D7-C46B-413D-BC18-C3861E5FDAA5
keywords:
- API de diffusion multimédia en continu de méthode GetCachedBitrateMeasurement
- API de diffusion multimédia en continu de méthode GetCachedBitrateMeasurement, interface ActiveBasicDevice
- API de diffusion multimédia en continu de l’interface ActiveBasicDevice, méthode GetCachedBitrateMeasurement
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedBitrateMeasurement
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 031d77595298651be11c793f8fd96471808ab1aef3f5a2b6398be9c1ff10de02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236864"
---
# <a name="activebasicdevicegetcachedbitratemeasurement-method"></a>ActiveBasicDevice :: GetCachedBitrateMeasurement, méthode

Obtient le débit binaire mis en cache.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCachedBitrateMeasurement(
  [in]          GUID   physicalNetworkInterface,
  [out, retval] UINT64 *bitrate
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*physicalNetworkInterface* \[ dans\]
</dt> <dd>

Spécifie l’interface réseau physique.

</dd> <dt>

*débit binaire* \[ out, retval\]
</dt> <dd>

Reçoit la valeur de débit binaire.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

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

 

