---
title: Méthode IWMDRMDevice IsWMDRMDevice
description: la méthode IsWMDRMDevice détermine si l’appareil prend en charge Windows Media DRM 10 pour les appareils mobiles.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919475"
---
# <a name="iwmdrmdeviceiswmdrmdevice-method"></a>IWMDRMDevice :: IsWMDRMDevice, méthode

la méthode **IsWMDRMDevice** détermine si l’appareil prend en charge Windows Media DRM 10 pour les appareils mobiles.

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

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>WMDDRMSP. idl</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMDevice**](iwmdrmdevice.md)
</dt> </dl>

 

 





