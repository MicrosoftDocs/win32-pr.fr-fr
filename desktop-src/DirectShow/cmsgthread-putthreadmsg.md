---
description: Met en file d’attente une demande d’exécution par le thread de travail.
ms.assetid: a854f962-143d-4776-bf98-119d003867df
title: Méthode CMsgThread. PutThreadMsg (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.PutThreadMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3445d9af4ec9c7abe6a4401e219fc305e254d555
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923615"
---
# <a name="cmsgthreadputthreadmsg-method"></a>Méthode CMsgThread. PutThreadMsg

Met en file d’attente une demande d’exécution par le thread de travail.

## <a name="syntax"></a>Syntaxe


```C++
void PutThreadMsg(
   UINT     uMsg,
   DWORD    dwMsgFlags,
   LPVOID   lpMsgParam,
   CAMEvent *pEvent = NULL
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*uMsg* 
</dt> <dd>

Code de la requête.

</dd> <dt>

*dwMsgFlags* 
</dt> <dd>

Paramètre flags facultatif.

</dd> <dt>

*lpMsgParam* 
</dt> <dd>

Pointeur facultatif vers un bloc de données contenant des paramètres ou des valeurs de retour supplémentaires. Doit être statique ou alloué par segment de mémoire et non automatique.

</dd> <dt>

*pEvent* 
</dt> <dd>

Pointeur facultatif vers un objet d’événement à signaler à l’achèvement.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette fonction membre met en file d’attente une requête d’exécution par le thread de travail. Les paramètres de cette fonction membre seront mis en file d’attente (dans un objet [**CMsg**](cmsg.md) ) et passés à la fonction membre [**CMsgThread :: ThreadMessageProc**](cmsgthread-threadmessageproc.md) du thread de travail. Cette fonction membre retourne immédiatement après la mise en file d’attente de la demande et n’attend pas que le thread exécute la demande. La fonction membre **CMsgThread :: ThreadMessageProc** de la classe dérivée définit les quatre paramètres.

Cette fonction membre utilise une liste sécurisée multithread. par conséquent, plusieurs appels à cette fonction membre à partir de différents threads peuvent être effectués en toute sécurité.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Msgthrd. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMsgThread, classe**](cmsgthread.md)
</dt> </dl>

 

 




