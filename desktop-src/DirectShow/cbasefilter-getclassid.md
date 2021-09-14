---
description: 'La méthode GetClassID récupère l’identificateur de classe du filtre. Cette méthode implémente la méthode IPersist :: GetClassID.'
ms.assetid: c3a8b6ab-b36f-493e-9436-6784e25e2511
title: Méthode CBaseFilter. GetClassID (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 02dfe8452da6366454dcc1cfeeed93c379c89bd1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010132"
---
# <a name="cbasefiltergetclassid-method"></a>Méthode CBaseFilter. GetClassID

La `GetClassID` méthode récupère l’identificateur de classe du filtre. Cette méthode implémente la méthode **IPersist :: GetClassID** .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pClsID* 
</dt> <dd>

Pointeur vers une variable qui reçoit l’identificateur de classe.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne le \_ pointeur S ou OK \_ .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseFilter, classe**](cbasefilter.md)
</dt> </dl>

 

 




