---
title: Méthode IMediaRenderer IsVideoSupported
description: Récupère une valeur qui indique si DMR peut lire du contenu vidéo.
ms.assetid: AE9A14D0-A7A2-4A71-9454-06A05C7D85F9
keywords:
- API de diffusion multimédia en continu de méthode IsVideoSupported
- API de diffusion multimédia en continu de méthode IsVideoSupported, interface IMediaRenderer
- API de diffusion multimédia en continu de l’interface IMediaRenderer, méthode IsVideoSupported
topic_type:
- apiref
api_name:
- IMediaRenderer.IsVideoSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c1f6fa149c6c5025d3fd2c785dc2f4a8451fabed3906b559674d8038662c21d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972308"
---
# <a name="imediarendererisvideosupported-method"></a>IMediaRenderer :: IsVideoSupported, méthode

Récupère une valeur qui indique si DMR peut lire du contenu vidéo.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IsVideoSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Valeur booléenne qui est **true** si DMR est capable de visionner du contenu vidéo et **false** si ce n’est pas le cas.

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

 

 





