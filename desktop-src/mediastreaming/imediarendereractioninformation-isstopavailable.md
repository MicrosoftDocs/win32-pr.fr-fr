---
title: Méthode IMediaRendererActionInformation IsStopAvailable
description: Récupère une valeur qui indique si DMR accepte actuellement la méthode StopAsync.
ms.assetid: 6EE8F56D-2A5A-49B0-A9B2-0A7EE57D03FD
keywords:
- API de diffusion multimédia en continu de méthode IsStopAvailable
- API de diffusion multimédia en continu de méthode IsStopAvailable, interface IMediaRendererActionInformation
- API de diffusion multimédia en continu de l’interface IMediaRendererActionInformation, méthode IsStopAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsStopAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c177c46c62309525d9362f985075cec293105a80678b3b857eafa0524179d17e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712889"
---
# <a name="imediarendereractioninformationisstopavailable-method"></a>IMediaRendererActionInformation :: IsStopAvailable, méthode

Récupère une valeur qui indique si DMR accepte actuellement la méthode [**StopAsync**](imediarenderer-stopasync.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IsStopAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Valeur booléenne qui est **true** si DMR accepte actuellement la méthode [**StopAsync**](imediarenderer-stopasync.md) et **false** si ce n’est pas le cas.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

