---
title: Méthode IMediaRenderer StopAsync
description: Fait en sorte que le DMR de manière asynchrone arrête la diffusion du contenu actuel. | Méthode IMediaRenderer StopAsync
ms.assetid: B6B0F3F2-E95E-4A58-9CBD-CF4CB24FDAD0
keywords:
- API de diffusion multimédia en continu de méthode StopAsync
- API de diffusion multimédia en continu de méthode StopAsync, interface IMediaRenderer
- API de diffusion multimédia en continu de l’interface IMediaRenderer, méthode StopAsync
topic_type:
- apiref
api_name:
- IMediaRenderer.StopAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a5f73d534fdd786038a242614a981f4915d92c13
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313494"
---
# <a name="imediarendererstopasync-method"></a>IMediaRenderer :: StopAsync, méthode

Fait en sorte que le DMR de manière asynchrone arrête la diffusion du contenu actuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT StopAsync(
  [out] PlaybackOperation **value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Reçoit une référence à un objet [**PlaybackOperation**](playbackoperation.md) qui est utilisé pour obtenir les résultats de l’opération asynchrone.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMediaRenderer**](imediarenderer.md)
</dt> </dl>

 

 





