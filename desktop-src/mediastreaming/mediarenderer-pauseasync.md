---
title: Méthode MediaRenderer. PauseAsync
description: Ordonne à DMR de suspendre de manière asynchrone la diffusion du contenu actuel. | Méthode MediaRenderer. PauseAsync
ms.assetid: 1bd36349-0551-44e8-9550-3fd80900de9a
keywords:
- API de diffusion multimédia en continu de méthode PauseAsync
- API de diffusion multimédia en continu de méthode PauseAsync, interface MediaRenderer
- API de diffusion multimédia en continu de l’interface MediaRenderer, méthode PauseAsync
topic_type:
- apiref
api_name:
- MediaRenderer.PauseAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5dcb4474f7a7843f2812cf64e0119912eca8ae320b29b9acb0131a65bbbffa19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060249"
---
# <a name="mediarendererpauseasync-method"></a>Méthode MediaRenderer. PauseAsync

Ordonne à DMR de suspendre de manière asynchrone la diffusion du contenu actuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT PauseAsync(
  [out] PlaybackOperation **value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Reçoit une référence à un objet [**PlaybackOperation**](playbackoperation.md) qui est utilisé pour obtenir les résultats de l’opération asynchrone.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MediaRenderer**](mediarenderer.md)
</dt> </dl>

 

 





