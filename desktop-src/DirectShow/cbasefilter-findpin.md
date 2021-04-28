---
description: 'Méthode CBaseFilter. FindPin : la méthode FindPin récupère le code confidentiel avec l’identificateur spécifié. Cette méthode implémente la méthode IBaseFilter :: FindPin.'
ms.assetid: 152e4ff3-2809-4c57-b9c8-f51fc50b3703
title: Méthode CBaseFilter. FindPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2bbef9b051a42597b2585a432f544eead4e2e0a1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099817"
---
# <a name="cbasefilterfindpin-method"></a>Méthode CBaseFilter. FindPin

La `FindPin` méthode récupère le code confidentiel avec l’identificateur spécifié. Cette méthode implémente la méthode [**IBaseFilter :: FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Id* 
</dt> <dd>

Pointeur vers une chaîne Unicode de constante, terminée par un caractère null, qui identifie le code confidentiel.

</dd> <dt>

*ppPin* 
</dt> <dd>

Adresse d’une variable qui reçoit un pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) du pin.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne l’une des valeurs **HRESULT** suivantes.



| Code de retour                                                                                       | Description                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>              | Réussite.<br/>                       |
| <dl> <dt>**\_pointeur E**</dt> </dl>         | Argument de pointeur **null** .<br/>     |
| <dl> <dt>**VFW \_ E \_ \_ introuvable**</dt> </dl> | Impossible de trouver un code PIN correspondant.<br/> |



 

## <a name="remarks"></a>Notes 

Cette méthode appelle la méthode [**CBasePin :: Name**](cbasepin-name.md) pour comparer le nom de chaque pin à la chaîne spécifiée par le paramètre *ID* .

Si la méthode est réussie, l’interface **IPIN** a un nombre de références en attente. Veillez à le libérer lorsque vous avez terminé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseFilter, classe**](cbasefilter.md)
</dt> </dl>

 

 




