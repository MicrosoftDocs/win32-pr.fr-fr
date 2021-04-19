---
description: La méthode IsPartiallySpecified détermine si le type de média est partiellement défini. Un type de média est partiel si le type principal, le sous-type ou le type de format est le GUID \_ null.
ms.assetid: 26dd7a2b-b2f8-485f-a9af-31c3a9eb1def
title: Méthode CMediaType. IsPartiallySpecified (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.IsPartiallySpecified
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32c39942ab3f97d45ecf71ba841d56b7afd4be62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539983"
---
# <a name="cmediatypeispartiallyspecified-method"></a>Méthode CMediaType. IsPartiallySpecified

La `IsPartiallySpecified` méthode détermine si le type de média est partiellement défini. Un type de média est *partiel* si le type principal, le sous-type ou le type de format est le GUID \_ null.

## <a name="syntax"></a>Syntaxe


```C++
BOOL IsPartiallySpecified() const;
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si le type de média est partiellement spécifié. Sinon, retourne **false**.

## <a name="remarks"></a>Notes

La méthode [**IPIN :: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) peut accepter des types de média partiels.

L’implémentation de ne teste pas réellement le sous-type. S’il existe un type de format spécifié, le type de média n’est pas considéré comme partiel, même si le sous-type est un GUID \_ null.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Mtype. h (include streams. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaType, classe**](cmediatype.md)
</dt> </dl>

 

 




