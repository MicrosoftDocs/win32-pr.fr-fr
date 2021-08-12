---
description: Acquiert un verrou en lecture/écriture.
ms.assetid: fd212dd9-034b-4e0c-9111-e3460ea6f133
title: 'CShareLockNH :: ExclusiveLock, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ExclusiveLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 16a5d2ba49d5ff1c25079a99a979d7a0fb4a51ee64d54fa4042152d7b010dc1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667962"
---
# <a name="csharelocknhexclusivelock-method"></a>CShareLockNH :: ExclusiveLock, méthode

Acquiert un verrou en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
void ExclusiveLock();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Chaque appel à **ExclusiveLock** doit être associé à un seul appel à [**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md) pour éviter le risque d’un blocage.

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md)
</dt> </dl>

 

 
