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
ms.openlocfilehash: 4cb900d4de448b59eadb4cfd4de28aebf3ac07845fff6a2769c003d37cac846a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633929"
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

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                            | Description                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Ce code PIN prend en charge ce type de média.<br/>        |
| <dl> <dt>**E \_ échec**</dt> </dl> | Le code PIN ne prend pas en charge ce type de média.<br/> |



 

## <a name="remarks"></a>Remarques

Par défaut, le code PIN prend en charge un seul type de média. Cette méthode récupère le type pris en charge en appelant la version à paramètre unique de la méthode [**CSourceStream :: GetMediaType**](csourcestream-getmediatype.md) et le compare au type proposé. Si votre code PIN prend en charge plusieurs types de média, substituez cette méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceStream, classe**](csourcestream.md)
</dt> </dl>

 

 




