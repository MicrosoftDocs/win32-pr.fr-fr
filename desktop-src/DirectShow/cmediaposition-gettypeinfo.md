---
description: 'Méthode CMediaPosition. GetTypeInfo : la méthode GetTypeInfo récupère les informations de type de l’objet, qui peuvent ensuite être utilisées pour obtenir les informations de type d’une interface.'
ms.assetid: 0a04c43d-8b4b-4780-b02f-04053c405c77
title: Méthode CMediaPosition. GetTypeInfo (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7827a3599f05061b5760084bed46cd2554b45f9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099137"
---
# <a name="cmediapositiongettypeinfo-method"></a>Méthode CMediaPosition. GetTypeInfo

La `GetTypeInfo` méthode récupère les informations de type de l’objet, qui peuvent ensuite être utilisées pour obtenir les informations de type d’une interface.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

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

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes.



| Code de retour                                                                                             | Description                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                    | Réussite.<br/>                            |
| <dl> <dt>**\_pointeur E**</dt> </dl>               | Argument de pointeur **null** .<br/>          |
| <dl> <dt>**TAPEZ \_ E \_ ELEMENTNOTFOUND**</dt> </dl> | Le paramètre *iTInfo* n’est pas égal à zéro.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaPosition, classe**](cmediaposition.md)
</dt> </dl>

 

 




