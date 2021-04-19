---
description: Méthode de constructeur.
ms.assetid: 35c9ac07-8756-42b1-beeb-5f0e79466742
title: Constructeur CAMEvent. CAMEvent (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.CAMEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a01d9d1f592675f58d19e81b800c966dddaca1c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528609"
---
# <a name="cameventcamevent-constructor"></a>Constructeur CAMEvent. CAMEvent

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CAMEvent(
   BOOL    fManualReset,
   HRESULT *phr
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fManualReset* 
</dt> <dd>

Valeur booléenne qui spécifie si l’objet est un événement de réinitialisation manuelle ou un événement de réinitialisation automatique. Si la **valeur est true**, l’objet est un événement de réinitialisation manuelle. Dans le cas contraire, il s’agit d’un événement de réinitialisation automatique.

</dd> <dt>

*phr* 
</dt> <dd>

Pointeur vers une valeur **HRESULT** . Si le constructeur échoue, ce paramètre reçoit un code d’erreur. Si cela se produit, l’état de l’objet n’est pas valide.

Pour la compatibilité descendante avec les versions antérieures de strmbase. lib, la valeur par défaut de ce paramètre est **null**. Toutefois, le passage d’une valeur non **null** est préférable, afin que l’appelant puisse vérifier l’état de l’objet.

</dd> </dl>

## <a name="remarks"></a>Notes

L’événement commence dans un État non signalé.

Avec un événement de réinitialisation automatique, la méthode [**CAMEvent :: wait**](camevent-wait.md) réinitialise l’événement à l’état non signalé lorsque la méthode est retournée. Avec un événement de réinitialisation manuelle, l’événement reste signalé jusqu’à ce que vous appeliez la méthode [**CAMEvent :: Reset**](camevent-reset.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMEvent, classe**](camevent.md)
</dt> </dl>

 

 




