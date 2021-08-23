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
ms.openlocfilehash: a6049ad4526d8776b25e81fe4d75b727196f8fa1251a1959662cca71b161fbc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073973"
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

## <a name="remarks"></a>Remarques

Le type de média spécifié par *ppartial* peut avoir la valeur Guid \_ null pour le type principal, le sous-type ou le type de format. Les membres avec des \_ valeurs GUID NULL ne sont pas testés. (En fait, GUID \_ NULL agit comme un caractère générique.) Les membres avec des valeurs autres que le GUID \_ null doivent correspondre pour que le type de média corresponde.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Mtype. h (include Flux. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaType, classe**](cmediatype.md)
</dt> </dl>

 

 




