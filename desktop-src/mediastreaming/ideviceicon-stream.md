---
title: IDeviceIcon, méthode de flux
description: Récupère l’icône sous la forme d’un flux.
ms.assetid: 0B9E852F-4F72-4721-8F88-24A850A088C4
keywords:
- API de diffusion multimédia en continu de méthode de flux
- API de diffusion multimédia en continu de méthode de flux, interface IDeviceIcon
- API de diffusion multimédia en continu de l’interface IDeviceIcon, méthode Stream
topic_type:
- apiref
api_name:
- IDeviceIcon.Stream
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 75163836c2722156ec4bf6cd8b763a7c1b0f43b35a087c9dbdce6aef1ec99541
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117871184"
---
# <a name="ideviceiconstream-method"></a>IDeviceIcon :: Stream, méthode

Récupère l’icône sous la forme d’un flux.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Stream(
  [out] IRandomAccessStreamWithContentType **value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Reçoit une référence à un [**IRandomAccessStreamWithContentType**](/uwp/api/Windows.Storage.Streams.IRandomAccessStreamWithContentType) qui peut être utilisé pour récupérer les données d’image.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

