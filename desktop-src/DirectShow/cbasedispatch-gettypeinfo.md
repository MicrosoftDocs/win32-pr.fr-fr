---
description: La méthode GetTypeInfo récupère les informations de type de l’objet, qui peuvent ensuite être utilisées pour obtenir les informations de type d’une interface.
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
ms.openlocfilehash: 1f63d79327d2f2bf2a60f06e0290aa34891e78ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532862"
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
| <dl> <dt>**\_OK**</dt> </dl>                    | Opération réussie.<br/>                            |
| <dl> <dt>**\_pointeur E**</dt> </dl>               | Argument de pointeur **null** .<br/>          |
| <dl> <dt>**TAPEZ \_ E \_ ELEMENTNOTFOUND**</dt> </dl> | Le paramètre *iTInfo* n’est pas égal à zéro.<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode se comporte comme la méthode **IDispatch :: GetTypeInfo** . Toutefois, il comprend un paramètre supplémentaire, *riid*, qui spécifie l’interface pour laquelle récupérer les informations de type.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseDispatch, classe**](cbasedispatch.md)
</dt> </dl>

 

 




