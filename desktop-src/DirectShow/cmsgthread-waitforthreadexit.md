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
ms.openlocfilehash: c8b48573c4297a2d5d5d008eba88fd8ea437333c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528896"
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

## <a name="remarks"></a>Notes

Assurez-vous que le thread de travail s’est terminé complètement avant de terminer la destruction de votre classe dérivée. dans le cas contraire, le thread peut encore s’exécuter après que votre bibliothèque de liens dynamiques (DLL) a été déchargée de l’espace d’adressage du processus. Même si la seule instruction restante à Exit est une instruction à retour unique, cela provoquerait une exception. La seule méthode fiable pour s’assurer que le thread s’est arrêté est de signaler au thread de quitter (à l’aide d’un objet [**CMsg**](cmsg.md) négocié en privé envoyé à la fonction membre [**CMsgThread ::P utthreadmsg**](cmsgthread-putthreadmsg.md) ), puis d’appeler cette fonction membre. Vous devez le faire dans le destructeur de votre classe dérivée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Msgthrd. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMsgThread, classe**](cmsgthread.md)
</dt> </dl>

 

 




