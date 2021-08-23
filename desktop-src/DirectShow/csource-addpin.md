---
description: La méthode AddPin ajoute une nouvelle broche de sortie au filtre.
ms.assetid: 48850a1f-ecb7-460c-9bfc-ce1d1103a00b
title: Méthode CSource. AddPin (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.AddPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a1c221d2fd032445587b52b0d0ae7f7744889254983fab82c7b282d06fee195e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953778"
---
# <a name="csourceaddpin-method"></a>Méthode CSource. AddPin

La `AddPin` méthode ajoute une nouvelle broche de sortie au filtre.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AddPin(
   CSourceStream *pStream
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pStream* 
</dt> <dd>

Pointeur vers l’objet [**CSourceStream**](csourcestream.md) qui implémente le code confidentiel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                                   | Description                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Succès<br/>             |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante<br/> |



 

## <a name="remarks"></a>Remarques

Lorsque vous créez un nouveau code confidentiel dérivé de **CSourceStream**, le constructeur **CSourceStream** appelle automatiquement cette méthode pour ajouter la broche de sortie au filtre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSource, classe**](csource.md)
</dt> </dl>

 

 




