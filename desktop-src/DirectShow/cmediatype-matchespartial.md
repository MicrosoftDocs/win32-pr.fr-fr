---
description: La méthode MatchesPartial détermine si ce type de média correspond à un type de média partiellement spécifié.
ms.assetid: 62d531f3-5aa2-4af2-b951-584a49a849fc
title: Méthode CMediaType. MatchesPartial (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.MatchesPartial
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f4d2d4232b64857ca209e6b43cd7081a42495fee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526791"
---
# <a name="cmediatypematchespartial-method"></a>Méthode CMediaType. MatchesPartial

La `MatchesPartial` méthode détermine si ce type de média correspond à un type de média partiellement spécifié.

## <a name="syntax"></a>Syntaxe


```C++
BOOL MatchesPartial(
   const CMediaType *ppartial
) const;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppartial* 
</dt> <dd>

Pointeur vers le type de média à faire correspondre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si les types de média correspondent. Sinon, retourne **false**.

## <a name="remarks"></a>Notes

Le type de média spécifié par *ppartial* peut avoir la valeur Guid \_ null pour le type principal, le sous-type ou le type de format. Les membres avec des \_ valeurs GUID NULL ne sont pas testés. (En fait, GUID \_ NULL agit comme un caractère générique.) Les membres avec des valeurs autres que le GUID \_ null doivent correspondre pour que le type de média corresponde.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Mtype. h (include streams. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaType, classe**](cmediatype.md)
</dt> </dl>

 

 




