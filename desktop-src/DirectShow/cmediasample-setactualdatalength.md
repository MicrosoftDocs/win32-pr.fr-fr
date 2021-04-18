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
ms.openlocfilehash: 825b02f43195424f9ceb5ecd23c4dcf26727ef8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540348"
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
| <dl> <dt>**\_OK**</dt> </dl>                    | Opération réussie.<br/>                                         |
| <dl> <dt>**\_dépassement de \_ mémoire tampon VFW E \_**</dt> </dl> | *lLen* est plus grand que la taille de la mémoire tampon allouée.<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode définit la variable de membre [**CMediaSample :: m \_ lActual**](cmediasample-m-lactual.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaSample, classe**](cmediasample.md)
</dt> </dl>

 

 




