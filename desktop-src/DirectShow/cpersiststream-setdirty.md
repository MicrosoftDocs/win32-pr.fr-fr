---
description: Modifie l’indicateur de modification pour le flux actuel.
ms.assetid: 65fa7fbe-4fa7-45a3-91a4-4a3547b035b9
title: CPersistStream. SetDirty, méthode (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.SetDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31a00de873f33cedd1451ebebd0ec21f1dfaa83690923712d867ec4a8d34d502
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909299"
---
# <a name="cpersiststreamsetdirty-method"></a>CPersistStream. SetDirty, méthode

Modifie l’indicateur de modification pour le flux actuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetDirty(
   BOOL fDirty
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fDirty* 
</dt> <dd>

Nouvel indicateur de changement pour ce flux. **True** signifie que les données n’ont pas été enregistrées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Pstream. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPersistStream, classe**](cpersiststream.md)
</dt> </dl>

 

 




