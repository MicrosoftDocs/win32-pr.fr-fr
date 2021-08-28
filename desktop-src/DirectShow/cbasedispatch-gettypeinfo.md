---
description: 'Méthode CBaseDispatch. GetTypeInfo : la méthode GetTypeInfo récupère les informations de type de l’objet, qui peuvent ensuite être utilisées pour obtenir les informations de type d’une interface.'
ms.assetid: aa06b97c-541b-44fc-bdef-97fd1f014e85
title: Méthode CBaseDispatch. GetTypeInfo (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 294b9758aa79ab033c1e3cf8932056ca10e7bf2424de97a1cf9f3b509f1906bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076679"
---
# <a name="cbasedispatchgettypeinfo-method"></a>Méthode CBaseDispatch. GetTypeInfo

La `GetTypeInfo` méthode récupère les informations de type de l’objet, qui peuvent ensuite être utilisées pour obtenir les informations de type d’une interface.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetTypeInfo(
   REFIID    riid,
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*riid* 
</dt> <dd>

Référence à un identificateur d’interface (IID) qui spécifie l’interface.

</dd> <dt>

*itinfo* 
</dt> <dd>

Informations de type à retourner. Doit être zéro.

</dd> <dt>

*lcid* 
</dt> <dd>

Identificateur de paramètres régionaux.

</dd> <dt>

*ppTInfo* 
</dt> <dd>

Adresse d’une variable qui reçoit un pointeur **ITypeInfo** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes.



| Code de retour                                                                                             | Description                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                    | Réussite.<br/>                            |
| <dl> <dt>**\_pointeur E**</dt> </dl>               | Argument de pointeur **null** .<br/>          |
| <dl> <dt>**TAPEZ \_ E \_ ELEMENTNOTFOUND**</dt> </dl> | Le paramètre *iTInfo* n’est pas égal à zéro.<br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode se comporte comme la méthode **IDispatch :: GetTypeInfo** . Toutefois, il comprend un paramètre supplémentaire, *riid*, qui spécifie l’interface pour laquelle récupérer les informations de type.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseDispatch, classe**](cbasedispatch.md)
</dt> </dl>

 

 




