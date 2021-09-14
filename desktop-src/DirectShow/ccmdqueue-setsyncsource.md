---
description: La méthode SetSyncSource définit l’horloge utilisée pour le minutage.
ms.assetid: 646d4d24-f9b7-438a-b842-58e90eb6a945
title: Méthode CCmdQueue. SetSyncSource (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 995df3afa5185d8f50278899ac6a5d67dc6d230e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012293"
---
# <a name="ccmdqueuesetsyncsource-method"></a>Méthode CCmdQueue. SetSyncSource

La `SetSyncSource` méthode définit l’horloge utilisée pour le minutage.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT SetSyncSource(
   IReferenceClock *pIrc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pIrc* 
</dt> <dd>

Pointeur vers l’interface [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CCmdQueue, classe**](ccmdqueue.md)
</dt> </dl>

 

 




