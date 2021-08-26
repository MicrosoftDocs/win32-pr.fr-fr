---
title: Méthode ActiveBasicDevice SetCachedBitrateMeasurement (PlayToDevice. h)
description: Définit le débit binaire mis en cache.
ms.assetid: 53530217-CFF7-4376-B155-E11044621E2D
keywords:
- API de diffusion multimédia en continu de méthode SetCachedBitrateMeasurement
- API de diffusion multimédia en continu de méthode SetCachedBitrateMeasurement, interface ActiveBasicDevice
- API de diffusion multimédia en continu de l’interface ActiveBasicDevice, méthode SetCachedBitrateMeasurement
topic_type:
- apiref
api_name:
- ActiveBasicDevice.SetCachedBitrateMeasurement
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adf79b7e9066aacfcce1f82c998463d6d620f5061fef4af788104a0c01a44ee8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952769"
---
# <a name="activebasicdevicesetcachedbitratemeasurement-method"></a>ActiveBasicDevice :: SetCachedBitrateMeasurement, méthode

Définit le débit binaire mis en cache.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetCachedBitrateMeasurement(
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

Valeur sur laquelle définir le débit binaire.

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

 

