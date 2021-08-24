---
description: 'La méthode SetActualDataLength définit la longueur des données valides dans la mémoire tampon. Cette méthode implémente la méthode IMediaSample :: SetActualDataLength.'
ms.assetid: a80a67ef-e490-4874-a123-f2d193cec4d7
title: Méthode CMediaSample. SetActualDataLength (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetActualDataLength
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: db090ad96f6c53f725aef7864e729b8083bfd1a02b30f0d699d30b5c6f8f71aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634374"
---
# <a name="cmediasamplesetactualdatalength-method"></a>Méthode CMediaSample. SetActualDataLength

La `SetActualDataLength` méthode définit la longueur des données valides dans la mémoire tampon. Cette méthode implémente la méthode [**IMediaSample :: SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetActualDataLength(
   long lLen
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lLen* 
</dt> <dd>

Longueur des données valides, en octets.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                                             | Description                                                 |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                    | Réussite.<br/>                                         |
| <dl> <dt>**\_dépassement de \_ mémoire tampon VFW E \_**</dt> </dl> | *lLen* est plus grand que la taille de la mémoire tampon allouée.<br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode définit la variable de membre [**CMediaSample :: m \_ lActual**](cmediasample-m-lactual.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaSample, classe**](cmediasample.md)
</dt> </dl>

 

 




