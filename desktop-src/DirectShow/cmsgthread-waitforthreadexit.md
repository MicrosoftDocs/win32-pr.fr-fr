---
description: Bloque jusqu’à ce que le thread se termine.
ms.assetid: 1ee547b5-cd73-4ce8-8e66-c2062714d0f0
title: Méthode CMsgThread. WaitForThreadExit (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.WaitForThreadExit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: de9861a1c7cae3055be288c4624b9e0b98c7b719e1534c1841ddb17770d91cf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915709"
---
# <a name="cmsgthreadwaitforthreadexit-method"></a>Méthode CMsgThread. WaitForThreadExit

Bloque jusqu’à ce que le thread se termine.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WaitForThreadExit(
   LPDWORD lpdwExitCode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpdwExitCode* 
</dt> <dd>

Pointeur désignant le code de sortie retourné par le thread.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** ou **false**, dont la signification est déterminée par la classe qui fournit la fonction membre [**CMsgThread :: ThreadMessageProc**](cmsgthread-threadmessageproc.md) substituée et la fonction membre d’appel.

## <a name="remarks"></a>Remarques

Assurez-vous que le thread de travail s’est terminé complètement avant de terminer la destruction de votre classe dérivée. dans le cas contraire, le thread peut encore s’exécuter après que votre bibliothèque de liens dynamiques (DLL) a été déchargée de l’espace d’adressage du processus. Même si la seule instruction restante à Exit est une instruction à retour unique, cela provoquerait une exception. La seule méthode fiable pour s’assurer que le thread s’est arrêté est de signaler au thread de quitter (à l’aide d’un objet [**CMsg**](cmsg.md) négocié en privé envoyé à la fonction membre [**CMsgThread ::P utthreadmsg**](cmsgthread-putthreadmsg.md) ), puis d’appeler cette fonction membre. Vous devez le faire dans le destructeur de votre classe dérivée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Msgthrd. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMsgThread, classe**](cmsgthread.md)
</dt> </dl>

 

 




