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
ms.openlocfilehash: d15b38ba2730d2023b09c2fa0352ade1f1532724
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509190"
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

 

