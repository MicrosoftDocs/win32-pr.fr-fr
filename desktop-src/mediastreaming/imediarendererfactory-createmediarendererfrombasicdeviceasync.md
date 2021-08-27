---
title: Méthode IMediaRendererFactory CreateMediaRendererFromBasicDeviceAsync
description: Crée de façon asynchrone une nouvelle instance d’un objet qui implémente l’interface IMediaRenderer à l’aide de l’interface IBasicDevice spécifiée.
ms.assetid: 14A83789-0F3C-467B-8EFD-3BB421C54217
keywords:
- API de diffusion multimédia en continu de méthode CreateMediaRendererFromBasicDeviceAsync
- API de diffusion multimédia en continu de méthode CreateMediaRendererFromBasicDeviceAsync, interface IMediaRendererFactory
- API de diffusion multimédia en continu de l’interface IMediaRendererFactory, méthode CreateMediaRendererFromBasicDeviceAsync
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererFromBasicDeviceAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b9ee80a4f681bb57d62f84d35cf3a254e38982a10f642a35e35187f6af9e48e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092289"
---
# <a name="imediarendererfactorycreatemediarendererfrombasicdeviceasync-method"></a>IMediaRendererFactory :: CreateMediaRendererFromBasicDeviceAsync, méthode

Crée de façon asynchrone une nouvelle instance d’un objet qui implémente l’interface [**IMediaRenderer**](imediarenderer.md) à l’aide de l’interface [**IBasicDevice**](ibasicdevice.md) spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateMediaRendererFromBasicDeviceAsync(
  [in]          IBasicDevice                 *basicDevice,
  [out, retval] CreateMediaRendererOperation **value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*basicDevice* \[ dans\]
</dt> <dd>

Pointeur vers une interface [**IBasicDevice**](ibasicdevice.md) représentant l’appareil pour lequel une instance de [**IMediaRenderer**](imediarenderer.md) sera créée.

</dd> <dt>

*valeur* \[ out, retval\]
</dt> <dd>

Reçoit une référence à un objet [**CreateMediaRendererOperation**](createmediarendereroperation.md) qui est utilisé pour obtenir les résultats de l’opération asynchrone.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMediaRendererFactory**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)
</dt> </dl>

 

