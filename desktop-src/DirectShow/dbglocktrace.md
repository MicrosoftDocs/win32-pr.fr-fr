---
description: Active ou désactive la journalisation du débogage d’une section critique donnée.
ms.assetid: 6e6e3de4-8bea-4e28-b04e-54a52226b59a
title: DbgLockTrace, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgLockTrace
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8daf3c33b43bda95bb1d54145e9e5aebc6f89c2f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007578"
---
# <a name="dbglocktrace-function"></a>DbgLockTrace fonction)

Active ou désactive la journalisation du débogage d’une section critique donnée.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI DbgLockTrace(
   CCritSec *pcCrit,
   BOOL     fTrace
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pcCrit* 
</dt> <dd>

Pointeur vers une section critique [**CCritSec**](ccritsec.md) .

</dd> <dt>

*fTrace* 
</dt> <dd>

Valeur spécifiant si la journalisation est activée. Utilisez **true** pour activer la journalisation ou **false** pour la désactiver.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Utilisez cette fonction pour tracer une section critique spécifique. Par défaut, la journalisation du débogage des sections critiques est désactivée, en raison du grand nombre de sections critiques.

Pour suivre une section critique, procédez comme suit :

1.  définissez debug ou \_ debug avant d’inclure les en-têtes de DirectShow.
2.  Activez la journalisation du débogage pour les sections critiques en appelant [**DbgSetModuleLevel**](dbgsetmodulelevel.md) avec l’indicateur de verrouillage du journal \_ .
3.  Appelez **DbgLockTrace** sur la section critique que vous souhaitez tracer.

Dans les versions commerciales, la fonction **DbgLockTrace** n’a aucun effet.

## <a name="examples"></a>Exemples

L’exemple de code suivant montre comment suivre une section critique.


```
DbgInitialise(g_hInst);
DbgSetModuleLevel(LOG_LOCKING, 3);

{
    CCritSec MyLock;
    DbgLockTrace(&MyLock, TRUE);
    
    CAutoLock cObjectLock(&MyLock);

    // Protected section of code.    
    DbgOutString("This code is inside a critical section.\n");

} // Lock goes out of scope here.

DbgTerminate();
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de débogage des sections critiques](critical-section-debugging-functions.md)
</dt> </dl>

 

 




