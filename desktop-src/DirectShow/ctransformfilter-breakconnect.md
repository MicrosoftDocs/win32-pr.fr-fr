---
description: La méthode BreakConnect libère un code confidentiel d’une connexion.
ms.assetid: cc384786-9cba-4f68-9c60-740205b35661
title: Méthode CTransformFilter. BreakConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aec60322a4782d84e84dc2030b69f6c385783e98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539585"
---
# <a name="ctransformfilterbreakconnect-method"></a>Méthode CTransformFilter. BreakConnect

La `BreakConnect` méthode libère un code confidentiel d’une connexion.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT BreakConnect(
   PIN_DIRECTION dir
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dir* 
</dt> <dd>

Membre du type énuméré de [**\_ direction du code confidentiel**](/windows/win32/api/strmif/ne-strmif-pin_direction) , spécifiant la connexion de code confidentiel qui a été rompue (entrée ou sortie).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Notes

Les méthodes [**CTransformInputPin :: BreakConnect**](ctransforminputpin-breakconnect.md) et [**CTransformOutputPin :: BreakConnect**](ctransformoutputpin-breakconnect.md) appellent cette méthode lorsqu’une connexion de code confidentiel est interrompue. Cette méthode n’a aucun effet dans la classe de base. Si vous substituez la méthode [**CheckConnect**](ctransformfilter-checkconnect.md) , substituez cette méthode pour libérer toutes les ressources obtenues dans la méthode **CheckConnect** , y compris les pointeurs d’interface.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransformFilter, classe**](ctransformfilter.md)
</dt> </dl>

 

 




