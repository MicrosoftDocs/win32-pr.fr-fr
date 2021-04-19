---
description: Libère un verrou acquis à l’aide de ExclusiveLock en mode partagé.
ms.assetid: d38354f0-2eb3-4924-99b5-1331e587ce32
title: 'CShareLockNH :: ExclusiveUnlock, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ExclusiveUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: f5fae5d6131bfcb386d52880b530f3def9464442
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540021"
---
# <a name="csharelocknhexclusiveunlock-method"></a>CShareLockNH :: ExclusiveUnlock, méthode

Libère un verrou acquis à l’aide de [**ExclusiveLock**](csharelocknh--exclusivelock.md) en mode partagé.

## <a name="syntax"></a>Syntaxe


```C++
void ExclusiveUnlock();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Chaque appel à [**ExclusiveLock**](csharelocknh--exclusivelock.md) doit être associé à un seul appel à **ExclusiveUnlock** pour éviter le risque d’un blocage.

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ExclusiveLock**](csharelocknh--exclusivelock.md)
</dt> </dl>

 

 
