---
description: La méthode Wait est bloquée jusqu’à ce que l’événement soit signalé, ou jusqu’à ce qu’un délai d’attente se produise.
ms.assetid: bcc13723-a59b-4e8a-bfc8-eadb6facf116
title: CAMEvent. Wait, méthode (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Wait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ab5bc2aabf77fb73739528e99cda7961ae87e9d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111353"
---
# <a name="cameventwait-method"></a>CAMEvent. Wait, méthode

La `Wait` méthode se bloque jusqu’à ce que l’événement soit signalé, ou jusqu’à ce qu’un délai d’attente se produise.

## <a name="syntax"></a>Syntaxe


```C++
BOOL Wait(
   DWORD dwTimeout = INFINITE
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwTimeout* 
</dt> <dd>

Valeur de délai d’attente facultative, exprimée en millisecondes.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** si l’événement est signalé. Sinon, retourne **false**.

## <a name="remarks"></a>Notes

Pour les événements de réinitialisation automatique, l’événement est réinitialisé à un État non signalé lorsque cette méthode est retournée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMEvent, classe**](camevent.md)
</dt> </dl>

 

 




