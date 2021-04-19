---
description: La méthode Insert ajoute un objet CDeferredCommand à la file d’attente.
ms.assetid: 41f9c30c-6267-435a-9089-eb34ae606896
title: CCmdQueue. Insert, méthode (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Insert
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bad004641258e29ed42d7142a5b0ab2c0ceb78d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532909"
---
# <a name="ccmdqueueinsert-method"></a>CCmdQueue. Insert, méthode

La `Insert` méthode ajoute un objet [**CDeferredCommand**](cdeferredcommand.md) à la file d’attente.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT Insert(
   CDeferredCommand *pCmd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCmd* 
</dt> <dd>

Pointeur vers l’objet **CDeferredCommand** à ajouter à la file d’attente.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK dans l’implémentation par défaut.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CCmdQueue, classe**](ccmdqueue.md)
</dt> </dl>

 

 




