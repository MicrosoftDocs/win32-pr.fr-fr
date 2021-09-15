---
description: Récupère l’élément suivant de la file d’attente.
ms.assetid: 406ae640-5903-427d-91f9-8b01beb1aaa7
title: Méthode CQueue. GetQueueObject (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue.GetQueueObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c3ae68c0564c7f76f38e91b7d27c8c3deb5ef2b4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413992"
---
# <a name="cqueuegetqueueobject-method"></a>Méthode CQueue. GetQueueObject

Récupère l’élément suivant de la file d’attente.

## <a name="syntax"></a>Syntaxe


```C++
T GetQueueObject();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne un objet de type **T** (type de modèle).

## <a name="remarks"></a>Notes

Cette méthode bloque jusqu’à ce qu’un élément soit disponible dans la file d’attente.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CQueue, classe**](cqueue.md)
</dt> </dl>

 

 




