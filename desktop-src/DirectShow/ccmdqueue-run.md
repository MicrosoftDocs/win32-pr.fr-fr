---
description: La méthode Run bascule en mode Running afin que les commandes qui sont différées par l’heure du flux de temps puissent être exécutées.
ms.assetid: c529ae84-c9b7-46f1-a1e4-716fc9e9df13
title: CCmdQueue. Run, méthode (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 424914e53a12ff0f43e8b7e2a3345c28d84437d2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012292"
---
# <a name="ccmdqueuerun-method"></a>CCmdQueue. Run, méthode

La `Run` méthode bascule en mode d’exécution afin que les commandes qui sont différées par l’heure du flux de temps puissent être exécutées.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT Run(
   REFERENCE_TIME tStreamTimeOffset
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*tStreamTimeOffset* 
</dt> <dd>

Heure du décalage.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK.

## <a name="remarks"></a>Notes

En mode exécution, le mappage flux-temps-durée-présentation est connu.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CCmdQueue, classe**](ccmdqueue.md)
</dt> </dl>

 

 




