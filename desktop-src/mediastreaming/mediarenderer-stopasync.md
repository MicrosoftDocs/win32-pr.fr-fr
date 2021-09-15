---
title: Méthode MediaRenderer. StopAsync
description: Fait en sorte que le DMR de manière asynchrone arrête la diffusion du contenu actuel. | Méthode MediaRenderer. StopAsync
ms.assetid: 04cf6d5a-8aa5-4821-8117-f250bfaf7ebd
keywords:
- API de diffusion multimédia en continu de méthode StopAsync
- API de diffusion multimédia en continu de méthode StopAsync, interface MediaRenderer
- API de diffusion multimédia en continu de l’interface MediaRenderer, méthode StopAsync
topic_type:
- apiref
api_name:
- MediaRenderer.StopAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 205c69a83572539974c1b8ad2cf45159c45335cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521452"
---
# <a name="mediarendererstopasync-method"></a>Méthode MediaRenderer. StopAsync

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

[**MediaRenderer**](mediarenderer.md)
</dt> </dl>

 

 





