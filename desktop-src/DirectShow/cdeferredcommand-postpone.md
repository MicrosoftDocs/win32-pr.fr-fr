---
description: La méthode ajourner spécifie une nouvelle heure de présentation pour une commande précédemment mise en file d’attente.
ms.assetid: 6201eb18-8180-445c-8d29-980511748fe4
title: CDeferredCommand. ajourner, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Postpone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9ce19c5391541336f52dd872b44bb9f3a447c27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541373"
---
# <a name="cdeferredcommandpostpone-method"></a>CDeferredCommand. ajourne, méthode

La `Postpone` méthode spécifie une nouvelle heure de présentation pour une commande précédemment mise en file d’attente.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Postpone(
   REFTIME newtime
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*newtime* 
</dt> <dd>

Heure de la nouvelle présentation.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l' \_ heure de VFW E \_ \_ déjà \_ passée si *Newtime* est déjà passé. Sinon, retourne un **HRESULT** résultant d’un appel à [**CCmdQueue :: Remove**](ccmdqueue-remove.md) (lors de l’extraction de la liste) ou [**CCmdQueue :: Insert**](ccmdqueue-insert.md) (lors de la réinsertion avec l’heure modifiée).

## <a name="remarks"></a>Notes

Cette fonction membre implémente la méthode [**IDeferredCommand ::P ostpone**](/windows/desktop/api/Control/nf-control-ideferredcommand-postpone) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDeferredCommand, classe**](cdeferredcommand.md)
</dt> </dl>

 

 




