---
title: Méthode IMediaRenderer PauseAsync
description: Ordonne à DMR de suspendre de manière asynchrone la diffusion du contenu actuel. | Méthode IMediaRenderer PauseAsync
ms.assetid: 2EADD9BE-2306-4CDA-AD5C-8342C06EAF1B
keywords:
- API de diffusion multimédia en continu de méthode PauseAsync
- API de diffusion multimédia en continu de méthode PauseAsync, interface IMediaRenderer
- API de diffusion multimédia en continu de l’interface IMediaRenderer, méthode PauseAsync
topic_type:
- apiref
api_name:
- IMediaRenderer.PauseAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8713fa4b2fe46a694024c2873cd50a0ec89ce898
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106538305"
---
# <a name="imediarendererpauseasync-method"></a>IMediaRenderer ::P méthode auseAsync

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

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMediaRenderer**](imediarenderer.md)
</dt> </dl>

 

 





