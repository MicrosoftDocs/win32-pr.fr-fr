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
ms.openlocfilehash: 3c4e77e28548c1f181cb5f8a6c106572d243314c5afd9d9126024e9b84fbe02a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053809"
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

## <a name="remarks"></a>Remarques

Les méthodes [**CTransformInputPin :: BreakConnect**](ctransforminputpin-breakconnect.md) et [**CTransformOutputPin :: BreakConnect**](ctransformoutputpin-breakconnect.md) appellent cette méthode lorsqu’une connexion de code confidentiel est interrompue. Cette méthode n’a aucun effet dans la classe de base. Si vous substituez la méthode [**CheckConnect**](ctransformfilter-checkconnect.md) , substituez cette méthode pour libérer toutes les ressources obtenues dans la méthode **CheckConnect** , y compris les pointeurs d’interface.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransformFilter, classe**](ctransformfilter.md)
</dt> </dl>

 

 




