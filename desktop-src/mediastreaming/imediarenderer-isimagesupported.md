---
title: Méthode IMediaRenderer IsImageSupported
description: Récupère une valeur qui indique si DMR est capable d’afficher des images.
ms.assetid: 3941789B-0FFF-4F00-B63C-2586B39B6546
keywords:
- API de diffusion multimédia en continu de méthode IsImageSupported
- API de diffusion multimédia en continu de méthode IsImageSupported, interface IMediaRenderer
- API de diffusion multimédia en continu de l’interface IMediaRenderer, méthode IsImageSupported
topic_type:
- apiref
api_name:
- IMediaRenderer.IsImageSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1fae20b6b5486586e305723a1d6a29a885bf0db8b8741ab9e6881fb292f35d6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461639"
---
# <a name="imediarendererisimagesupported-method"></a>IMediaRenderer :: IsImageSupported, méthode

Récupère une valeur qui indique si DMR est capable d’afficher des images.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IsImageSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Valeur booléenne qui est **true** si DMR est capable d’afficher des images et **false** si ce n’est pas le cas.

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

 

 





