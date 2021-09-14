---
description: 'Méthode CBaseDispatch. GetTypeInfoCount : la méthode GetTypeInfoCount récupère le nombre d’interfaces d’informations de type fourni par l’objet.'
ms.assetid: e09e6f6c-6ac8-4ce1-8ce1-ee5374d54183
title: Méthode CBaseDispatch. GetTypeInfoCount (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 81e68c94420b3d7715845f8d6bd14e26b770b44f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999761"
---
# <a name="cbasedispatchgettypeinfocount-method"></a>Méthode CBaseDispatch. GetTypeInfoCount

La `GetTypeInfoCount` méthode récupère le nombre d’interfaces d’informations de type fourni par l’objet.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pctinfo* 
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre d’interfaces d’informations de type fournies par l’objet. Lorsque la méthode retourne, la valeur est 1.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs suivantes.



| Code de retour                                                                               | Description                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | Réussite.<br/>                   |
| <dl> <dt>**\_pointeur E**</dt> </dl> | Argument de pointeur **null** .<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseDispatch, classe**](cbasedispatch.md)
</dt> </dl>

 

 




