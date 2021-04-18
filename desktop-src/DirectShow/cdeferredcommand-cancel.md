---
description: 'La méthode Cancel annule une demande CDeferredCommand :: Invoke précédemment mise en file d’attente.'
ms.assetid: 77671f6b-db50-4d8a-b727-aeed365f0303
title: CDeferredCommand. Cancel, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Cancel
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 524300da374b10eaac884161bb0195d88f45476d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540687"
---
# <a name="cdeferredcommandcancel-method"></a>CDeferredCommand. Cancel, méthode

La `Cancel` méthode annule une demande [**CDeferredCommand :: Invoke**](cdeferredcommand-invoke.md) précédemment mise en file d’attente.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Cancel();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne VFW \_ E \_ déjà \_ annulé si **m \_ pQueue** a la **valeur null**. Retourne un **HRESULT** à partir de [**CCmdQueue :: Remove**](ccmdqueue-remove.md) si l’appel génère une erreur. Retourne S \_ OK en cas de réussite.

## <a name="remarks"></a>Notes

Cette fonction membre implémente la méthode [**IDeferredCommand :: Cancel**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDeferredCommand, classe**](cdeferredcommand.md)
</dt> </dl>

 

 




