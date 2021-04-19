---
description: Méthode de constructeur.
ms.assetid: 0057adfe-e397-476b-90f9-7edbf7377b65
title: Constructeur CAMThread. CAMThread (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abaac0c3b0330cd41db7ecd21f894733de10a1b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534848"
---
# <a name="camthreadcamthread-constructor"></a>Constructeur CAMThread. CAMThread

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CAMThread(
   HRESULT *phr = NULL
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*phr* 
</dt> <dd>

Pointeur vers une valeur **HRESULT** . Si le constructeur échoue, ce paramètre reçoit un code d’erreur. Si cela se produit, l’état de l’objet n’est pas valide.

Pour la compatibilité descendante avec les versions antérieures de strmbase. lib, la valeur par défaut de ce paramètre est **null**. Toutefois, le passage d’une valeur non **null** est préférable, afin que l’appelant puisse vérifier l’état de l’objet.

</dd> </dl>

## <a name="remarks"></a>Notes

La méthode de constructeur ne crée pas le thread. Pour créer le thread, appelez la méthode [**CAMThread :: Create**](camthread-create.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMThread, classe**](camthread.md)
</dt> </dl>

 

 




