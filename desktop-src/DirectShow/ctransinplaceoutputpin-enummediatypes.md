---
description: 'Méthode CTransInPlaceOutputPin. EnumMediaTypes : la méthode EnumMediaTypes énumère les types de média préférés du pin. Cette méthode implémente la méthode IPin :: EnumMediaTypes.'
ms.assetid: 942c6594-3053-484a-a0f7-286dcd3f7550
title: Méthode CTransInPlaceOutputPin. EnumMediaTypes (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 26dd58f23dc18a086c6c59f6f8a6a098e3449fea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084633"
---
# <a name="ctransinplaceoutputpinenummediatypes-method"></a>Méthode CTransInPlaceOutputPin. EnumMediaTypes

La `EnumMediaTypes` méthode énumère les types de média préférés du pin. Cette méthode implémente la méthode [**IPIN :: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppEnum* 
</dt> <dd>

Reçoit un pointeur vers l’interface [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                           | Description                                         |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Réussite.<br/>                                 |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>         | Mémoire insuffisante.<br/>                     |
| <dl> <dt>**\_pointeur E**</dt> </dl>             | Pointeur **null** .<br/>                        |
| <dl> <dt>**VFW \_ E \_ non \_ connecté**</dt> </dl> | La broche d’entrée du filtre n’est pas connectée.<br/> |



 

## <a name="remarks"></a>Notes 

Cette méthode retourne l’interface **IEnumMediaTypes** à partir de la broche de sortie en amont.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transip. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransInPlaceOutputPin, classe**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




