---
description: La fonction WaitDispatchingMessages attend qu’un objet soit signalé, tout en distribuant les messages de fenêtre.
ms.assetid: d15f6736-d141-47a3-b767-fbf774982fb4
title: WaitDispatchingMessages, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WaitDispatchingMessages
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e509a081243f28293dc2d8abf8311f69eaf9a44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540237"
---
# <a name="waitdispatchingmessages-function"></a>WaitDispatchingMessages fonction)

La `WaitDispatchingMessages` fonction attend qu’un objet soit signalé, tout en distribuant les messages de fenêtre.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI WaitDispatchingMessages(
   HANDLE hObject,
   DWORD  dwWait,
   HWND   hwnd = NULL,
   UINT   uMsg = 0,
   HANDLE hEvent = NULL
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hObject* 
</dt> <dd>

Handle de l’objet à attendre.

</dd> <dt>

*dwWait* 
</dt> <dd>

Intervalle de délai d’attente, en millisecondes.

</dd> <dt>

*HWND* 
</dt> <dd>

Handle facultatif vers une fenêtre.

</dd> <dt>

*uMsg* 
</dt> <dd>

Message de fenêtre facultatif, en spécifiant un message à distribuer.

</dd> <dt>

*hEvent* 
</dt> <dd>

Handle facultatif d’un événement à attendre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur de la fonction **WaitForMultipleObjects** .

## <a name="remarks"></a>Notes

Si un objet possède une fenêtre, il doit distribuer les messages de fenêtre en attente. Cette fonction permet à l’objet d’attendre un événement, un sémaphore ou un autre objet d’exclusion mutuelle lors de la distribution des messages.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions d’assistance diverses](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




