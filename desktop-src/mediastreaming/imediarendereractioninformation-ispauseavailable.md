---
title: Méthode IMediaRendererActionInformation IsPauseAvailable
description: Récupère une valeur qui indique si DMR accepte actuellement la méthode PauseAsync.
ms.assetid: 095A664F-D974-410D-8741-87A171EDD071
keywords:
- API de diffusion multimédia en continu de méthode IsPauseAvailable
- API de diffusion multimédia en continu de méthode IsPauseAvailable, interface IMediaRendererActionInformation
- API de diffusion multimédia en continu de l’interface IMediaRendererActionInformation, méthode IsPauseAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsPauseAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fad69863306a8a937771f16c2ab9a83a2622c571d2cd5ee5658a279bf7564132
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870846"
---
# <a name="imediarendereractioninformationispauseavailable-method"></a>IMediaRendererActionInformation :: IsPauseAvailable, méthode

Récupère une valeur qui indique si DMR accepte actuellement la méthode [**PauseAsync**](imediarenderer-pauseasync.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IsPauseAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Valeur booléenne qui est **true** si DMR accepte actuellement la méthode [**PauseAsync**](imediarenderer-pauseasync.md) et **false** si ce n’est pas le cas.

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

 

