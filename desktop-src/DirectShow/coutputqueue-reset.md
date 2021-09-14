---
description: La méthode reset réinitialise l’objet afin qu’il puisse recevoir plus de données.
ms.assetid: 7074ed71-1650-4b21-a9a2-ad74d0e3e882
title: COutputQueue. Reset, méthode (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.Reset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d380ef738af3b684606e86a7c36dc04217c54b7c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006724"
---
# <a name="coutputqueuereset-method"></a>COutputQueue. Reset, méthode

La `Reset` méthode réinitialise l’objet afin qu’il puisse recevoir plus de données.

## <a name="syntax"></a>Syntaxe


```C++
void Reset();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode réinitialise la variable de membre [**COutputQueue :: m \_ HR**](coutputqueue-m-hr.md) sur S \_ OK. L’objet peut recevoir à nouveau des exemples de supports. par exemple, après une opération de vidage.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Outputq. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COutputQueue, classe**](coutputqueue.md)
</dt> </dl>

 

 




