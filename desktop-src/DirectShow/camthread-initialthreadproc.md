---
description: La méthode InitialThreadProc appelle la procédure de thread principale.
ms.assetid: 1546c214-7ea9-4484-974b-dbd4b2b3e296
title: CAMThread.Iniméthode tialThreadProc (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.InitialThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d12e8d41ac0c6e1fd2af06c21accbb5c62e4eb25f2fc3f6c36988101a9b64d89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540299"
---
# <a name="camthreadinitialthreadproc-method"></a>CAMThread.Iniméthode tialThreadProc

La `InitialThreadProc` méthode appelle la procédure de thread principale.

## <a name="syntax"></a>Syntaxe


```C++
DWORD InitialThreadProc(
   LPVOID pv
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*va* 
</dt> <dd>

`this` dirigé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur DWORD** retournée par [**CAMThread :: ThreadProc**](camthread-threadproc.md). La classe dérivée définit cette valeur.

## <a name="remarks"></a>Remarques

La méthode [**CAMThread :: Create**](camthread-create.md) utilise cette méthode pour la procédure de thread lors de la création du thread. Elle utilise le `this` pointeur comme argument de thread.

Cette méthode appelle la méthode [**CAMThread :: CoInitializeHelper**](camthread-coinitializehelper.md) , puis ThreadProc.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMThread, classe**](camthread.md)
</dt> </dl>

 

 




