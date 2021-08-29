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
ms.openlocfilehash: a953d024ee0f90f7cb466574b29d7e3cfe150072bf1a3787734f8365916cb2a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972268"
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

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMediaRenderer**](imediarenderer.md)
</dt> </dl>

 

 





