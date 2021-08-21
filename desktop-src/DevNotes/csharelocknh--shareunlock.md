---
description: Libère un verrou partagé.
ms.assetid: c2e9eb68-aacb-4196-b09e-d2748efb7fd6
title: 'CShareLockNH :: ShareUnlock, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ShareUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 2bf59b6e1aa0f6718cece105007a8ba502291c23868aca6ec55283dd7292f8b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162184"
---
# <a name="csharelocknhshareunlock-method"></a>CShareLockNH :: ShareUnlock, méthode

Libère un verrou partagé.

## <a name="syntax"></a>Syntaxe


```C++
void ShareUnlock();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Chaque appel à [**ShareLock**](csharelocknh--sharelock.md) doit être associé à un seul appel à **ShareUnlock**. Seul un thread qui appelle avec succès **ShareLock** peut appeler **ShareUnlock**; dans le cas contraire, un interblocage peut se produire.

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ShareLock**](csharelocknh--sharelock.md)
</dt> </dl>

 

 
