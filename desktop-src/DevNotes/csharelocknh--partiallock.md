---
description: Empêche plusieurs threads de terminer l’acquisition d’un verrou.
ms.assetid: 9cdcc6d5-b2f1-4c88-b859-1c15a80e70a9
title: CShareLockNH ::P méthode artialLock
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.PartialLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 7eae3f0eb57d534ea352b7d1c1e0834ef54dfb42460dfe7b2edc4f6fc07fa013
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162343"
---
# <a name="csharelocknhpartiallock-method"></a>CShareLockNH ::P méthode artialLock

Empêche plusieurs threads de terminer l’acquisition d’un verrou.

## <a name="syntax"></a>Syntaxe


```C++
void PartialLock();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Alors que **PartialLock** est activé, les autres threads appelant [**ShareLock**](csharelocknh--sharelock.md) peuvent entrer le verrou.

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



 

 
