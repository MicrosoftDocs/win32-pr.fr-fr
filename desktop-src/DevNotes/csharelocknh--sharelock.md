---
description: Obtient un verrou partagé.
ms.assetid: dff9a842-573a-4530-820d-6fd9001e502a
title: 'CShareLockNH :: ShareLock, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ShareLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 7fd398228c6d0feb7e63133e8faeefd7a2fd3359bf62e80a8f398a3467424b90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654829"
---
# <a name="csharelocknhsharelock-method"></a>CShareLockNH :: ShareLock, méthode

Obtient un verrou partagé.

## <a name="syntax"></a>Syntaxe


```C++
void ShareLock();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Chaque appel à **ShareLock** doit être associé à un seul appel à [**ShareUnlock**](csharelocknh--shareunlock.md). Seul un thread qui appelle avec succès **ShareLock** peut appeler **ShareUnlock**; dans le cas contraire, un interblocage peut se produire.

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ShareUnlock**](csharelocknh--shareunlock.md)
</dt> </dl>

 

 
