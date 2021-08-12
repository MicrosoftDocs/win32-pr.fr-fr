---
description: 'La méthode Skip ignore un nombre spécifié de types de médias. Cette méthode implémente la méthode IEnumMediaTypes :: Skip.'
ms.assetid: a01fb084-b227-4ca6-b5ca-c57d56e8b1aa
title: CEnumMediaTypes. Skip, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Skip
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a9930472b5c8a2873ca0a7f3280565bd41ac6b0aac7e1e33303464d3a2c1ca3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656444"
---
# <a name="cenummediatypesskip-method"></a>CEnumMediaTypes. Skip, méthode

La `Skip` méthode ignore un nombre spécifié de types de médias. Cette méthode implémente la méthode [**IEnumMediaTypes :: Skip**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-skip) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Skip(
   ULONG cMediaTypes
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cMediaTypes* 
</dt> <dd>

Nombre de types de médias à ignorer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                                                | Description                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                    | Ignorée au-delà de la fin de la séquence.<br/>                                    |
| <dl> <dt>**\_OK**</dt> </dl>                       | Réussite.<br/>                                                                 |
| <dl> <dt>**VFW \_ E \_ enum \_ non \_ \_ synchronisé**</dt> </dl> | L’état du pin a changé et est désormais incohérent avec l’énumérateur.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CEnumMediaTypes, classe**](cenummediatypes.md)
</dt> </dl>

 

 




