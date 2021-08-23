---
description: Utilise la fonction Microsoft Win32 SetThreadPriority pour définir la priorité du thread sur une nouvelle valeur.
ms.assetid: 5b8ad024-e651-47e5-b32a-c44d56c086cd
title: CMsgThread. SetThreadPriority, méthode (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.SetThreadPriority
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce293f32f765a89451ecf07b4532afc5fc4a7a132287d5b09b54962f93135215
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585669"
---
# <a name="cmsgthreadsetthreadpriority-method"></a>CMsgThread. SetThreadPriority, méthode

Utilise la fonction Microsoft Win32 **SetThreadPriority** pour définir la priorité du thread sur une nouvelle valeur.

## <a name="syntax"></a>Syntaxe


```C++
BOOL SetThreadPriority(
   int nPriority
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nPriority* 
</dt> <dd>

Priorité du thread.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs suivantes.



| Code de retour                                                                              | Description                               |
|------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>VRAI * * * * *</dt> </dl>  | La priorité a été correctement définie.<br/> |
| <dl> <dt>FALSe * * * * *</dt> </dl> | La priorité n’a pas été définie.<br/>          |



 

## <a name="remarks"></a>Remarques

Le client et le thread de travail peuvent appeler cette fonction membre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Msgthrd. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMsgThread, classe**](cmsgthread.md)
</dt> </dl>

 

 




