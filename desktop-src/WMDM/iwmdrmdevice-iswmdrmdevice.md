---
title: Méthode IWMDRMDevice IsWMDRMDevice
description: La méthode IsWMDRMDevice détermine si l’appareil prend en charge Windows Media DRM 10 pour les appareils mobiles.
ms.assetid: 247e7a77-e805-4848-893f-f5522c161232
keywords:
- Méthode IsWMDRMDevice Gestionnaire de périphériques Windows Media
- Méthode IsWMDRMDevice Gestionnaire de périphériques Windows Media, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gestionnaire de périphériques, méthode IsWMDRMDevice
topic_type:
- apiref
api_name:
- IWMDRMDevice.IsWMDRMDevice
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca9cb79598ea41a996748e383c8fdfc63364dd6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523585"
---
# <a name="iwmdrmdeviceiswmdrmdevice-method"></a>IWMDRMDevice :: IsWMDRMDevice, méthode

La méthode **IsWMDRMDevice** détermine si l’appareil prend en charge Windows Media DRM 10 pour les appareils mobiles.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IsWMDRMDevice(
  [out] DWORD *pdwVersion
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pdwVersion* \[ à\]
</dt> <dd>

Version de Windows Media DRM 10 pour les appareils mobiles, qui a la valeur 0x00010000.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>WMDDRMSP. idl</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMDevice**](iwmdrmdevice.md)
</dt> </dl>

 

 





