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
ms.openlocfilehash: a2f83d3e3c2efcbcb5d4604bc5c50a37dc020f0a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010014"
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

## <a name="return-value"></a>Valeur de retour

Retourne le \_ pointeur S ou OK \_ .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | CSystemClock, classe<br/>                                                                                                                                                              |
| En-tête<br/>  | <dl> <dt>Sysclock. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




