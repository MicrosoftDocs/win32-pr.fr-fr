---
description: La méthode WaitMsg attend que l’événement soit signalé, tout en distribuant les messages envoyés.
ms.assetid: 5cab98ca-f9f3-4c7c-9ce2-8e16109d8fbb
title: Méthode CAMMsgEvent. WaitMsg (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent.WaitMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9622e962f130a082a5c1206367f4850cebb6ce02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542313"
---
# <a name="cammsgeventwaitmsg-method"></a>Méthode CAMMsgEvent. WaitMsg

La `WaitMsg` méthode attend que l’événement soit signalé, tout en distribuant les messages envoyés.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WaitMsg(
   DWORD dwTimeOut = INFINITE
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwTimeOut* 
</dt> <dd>

Valeur de délai d’attente facultative, en millisecondes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si l’événement est signalé, ou **false** si le délai d’attente a expiré.

## <a name="remarks"></a>Notes

Cette méthode appelle la fonction PeekMessage pour traiter les messages. Appelez cette méthode à la place de [**CAMEvent :: wait**](camevent-wait.md) si votre thread doit traiter des messages en attendant un événement. Si le thread ne traite pas les messages et qu’un autre thread envoie un message, un interblocage peut se produire.

Par exemple, supposons que vous créez un thread, puis que vous bloquiez jusqu’à ce que le thread initialise. Si le thread envoie un message à votre fenêtre en appelant la fonction SendMessage, cela provoque un interblocage. Cela est dû au fait que SendMessage ne retourne pas tant que le message n’a pas été traité. L’appel de WaitMsg permet à l’appel SendMessage de retourner, ce qui empêche le blocage.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMMsgEvent, classe**](cammsgevent.md)
</dt> </dl>

 

 




