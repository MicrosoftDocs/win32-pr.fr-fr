---
title: IBasicDevice, méthode d’icônes
description: Retourne un vecteur d’interfaces IDeviceIcon.
ms.assetid: 0C083AF3-FE22-4A8E-87B7-0FFA7B65ADBD
keywords:
- Méthode d’icônes API de diffusion multimédia en continu
- Icon Method Media Streaming API, IBasicDevice interface
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode Icons
topic_type:
- apiref
api_name:
- IBasicDevice.Icons
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6fdb514b2f6ab09a2c0024d37ed32e9968fe08dd7f16aefe40298ac2ba5497c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060439"
---
# <a name="ibasicdeviceicons-method"></a>IBasicDevice :: icons, méthode

Retourne un vecteur d’interfaces [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Icons(
  [out] IVector< IDeviceIcon > **value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Reçoit une collection énumérable de pointeurs d’interface [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

