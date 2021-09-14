---
description: 'La méthode CheckMediaType détermine si le code PIN accepte un type de média spécifique. Cette méthode implémente la méthode CBasePin :: CheckMediaType virtuelle pure.'
ms.assetid: 3db7c74c-a6aa-4b49-b2a5-9bf8db35fd7e
title: Méthode CSourceStream. CheckMediaType (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62f8b6c18613f5c187fc637febd08b74260a1e44
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012246"
---
# <a name="csourcestreamcheckmediatype-method"></a>Méthode CSourceStream. CheckMediaType

La `CheckMediaType` méthode détermine si le code PIN accepte un type de média spécifique. Cette méthode implémente la méthode [**CBasePin :: CheckMediaType**](cbasepin-checkmediatype.md) virtuelle pure.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pMediaType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMediaType* 
</dt> <dd>

Pointeur vers un objet [**CMediaType**](cmediatype.md) qui contient le type de média proposé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                            | Description                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Ce code PIN prend en charge ce type de média.<br/>        |
| <dl> <dt>**E \_ échec**</dt> </dl> | Le code PIN ne prend pas en charge ce type de média.<br/> |



 

## <a name="remarks"></a>Notes

Par défaut, le code PIN prend en charge un seul type de média. Cette méthode récupère le type pris en charge en appelant la version à paramètre unique de la méthode [**CSourceStream :: GetMediaType**](csourcestream-getmediatype.md) et le compare au type proposé. Si votre code PIN prend en charge plusieurs types de média, substituez cette méthode.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceStream, classe**](csourcestream.md)
</dt> </dl>

 

 




