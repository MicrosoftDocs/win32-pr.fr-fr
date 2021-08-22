---
description: 'La méthode GetClassID récupère l’identificateur de classe (CLSID) de l’objet. Cette méthode implémente la méthode IPersist :: GetClassID.'
ms.assetid: 3d2cc6a3-67d1-4dd9-916b-7c350ce6a542
title: Méthode CSystemClock. GetClassID (Sysclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2afb141c3a79255504eb13dadb39cc0fb5094c19e0979db04c251f1e2fe75133
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317189"
---
# <a name="csystemclockgetclassid-method"></a>Méthode CSystemClock. GetClassID

La `GetClassID` méthode récupère l’identificateur de classe (CLSID) de l’objet. Cette méthode implémente la méthode **IPersist :: GetClassID** .

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

Pointeur vers une variable qui reçoit la valeur CLSID \_ SystemClock.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le \_ pointeur S ou OK \_ .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | CSystemClock, classe<br/>                                                                                                                                                              |
| En-tête<br/>  | <dl> <dt>Sysclock. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




