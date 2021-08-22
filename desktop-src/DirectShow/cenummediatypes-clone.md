---
description: 'La méthode Clone effectue une copie de l’énumérateur avec le même état d’énumération. Cette méthode implémente la méthode IEnumMediaTypes :: Clone.'
ms.assetid: 3b4eb29e-48fc-4f00-a5f3-597b9aa94ce1
title: Méthode CEnumMediaTypes. Clone (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Clone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c624ac933228c769248c2980a250a9f89e9ebdaf386aeff951e70ba966311586
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537303"
---
# <a name="cenummediatypesclone-method"></a>CEnumMediaTypes. Clone, méthode

La `Clone` méthode effectue une copie de l’énumérateur avec le même état d’énumération. Cette méthode implémente la méthode [**IEnumMediaTypes :: Clone**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-clone) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Clone(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppEnum* 
</dt> <dd>

Adresse d’une variable qui reçoit un pointeur vers l’interface [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) du nouvel énumérateur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                                                | Description                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                       | Réussite.<br/>                                                                 |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>              | Mémoire insuffisante.<br/>                                                     |
| <dl> <dt>**\_pointeur E**</dt> </dl>                  | Argument de pointeur **null** .<br/>                                               |
| <dl> <dt>**VFW \_ E \_ enum \_ non \_ \_ synchronisé**</dt> </dl> | L’état du pin a changé et est désormais incohérent avec l’énumérateur.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CEnumMediaTypes, classe**](cenummediatypes.md)
</dt> </dl>

 

 




