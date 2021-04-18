---
description: Traite les demandes. Il s’agit d’une fonction membre virtuelle pure.
ms.assetid: ffdbc287-ca17-44e4-b00a-d72a2367f510
title: Méthode CMsgThread. ThreadMessageProc (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.ThreadMessageProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf47eb63a6f9d8fe4921985bb64567de6678b44c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526566"
---
# <a name="cmsgthreadthreadmessageproc-method"></a>Méthode CMsgThread. ThreadMessageProc

Traite les demandes. Il s’agit d’une fonction membre virtuelle pure.

## <a name="syntax"></a>Syntaxe


```C++
virtual LRESULT ThreadMessageProc(
   UINT     uMsg,
   DWORD    dwFlags,
   LPVOID   lpParam,
   CAMEvent *pEvent
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*uMsg* 
</dt> <dd>

Code de la requête.

</dd> <dt>

*dwFlags* 
</dt> <dd>

Paramètre d’indicateur facultatif à demander.

</dd> <dt>

*lpParam* 
</dt> <dd>

Pointeur facultatif vers des données supplémentaires ou un bloc de données de retour.

</dd> <dt>

*pEvent* 
</dt> <dd>

Pointeur facultatif vers un objet d’événement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Tout retour différent de zéro provoque la fermeture du thread. Retourne zéro sauf si une demande de sortie a été traitée récemment.

## <a name="remarks"></a>Notes

Cette fonction virtuelle pure doit être substituée dans votre classe dérivée. Elle est appelée une fois pour chaque demande en file d’attente par un appel à la fonction membre [**CMsgThread ::P utthreadmsg**](cmsgthread-putthreadmsg.md) .

La fonction membre définit les quatre paramètres. En général, utilisez le paramètre *uMsg* pour indiquer la demande, et les trois autres paramètres seront des paramètres supplémentaires facultatifs. L’application appelante peut fournir un pointeur vers un objet [**CAMEvent**](camevent.md) dans le paramètre *pEvent* si votre application l’exige. Vous devez définir cet événement après avoir traité l’événement à l’aide d’une expression telle que :


```C++
pEvent->SetEvent
```



Un code de demande doit être mis de côté pour indiquer au thread de travail de se fermer. Une fois cette demande reçue, retournez 1 à partir de cette fonction membre. Retourne 0 si vous ne souhaitez pas que le thread de travail se termine.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Msgthrd. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMsgThread, classe**](cmsgthread.md)
</dt> </dl>

 

 




