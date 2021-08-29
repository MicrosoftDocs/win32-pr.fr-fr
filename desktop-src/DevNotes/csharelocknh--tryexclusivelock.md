---
description: Obtient un verrou exclusivement si aucun autre ne le contient actuellement.
ms.assetid: d655b89c-f2c8-4965-a21b-f539b1598296
title: 'CShareLockNH :: TryExclusiveLock, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.TryExclusiveLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 28bd569c287b00cf6b0a146022ade6ce7f7bf29d5ced9eb5ef62341c873059c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654659"
---
# <a name="csharelocknhtryexclusivelock-method"></a>CShareLockNH :: TryExclusiveLock, méthode

Obtient un verrou exclusivement si aucun autre ne le contient actuellement.

## <a name="syntax"></a>Syntaxe


```C++
BOOL TryExclusiveLock();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si la fonction est réussie ; Sinon, elle retourne **false**.

## <a name="remarks"></a>Remarques

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



 

 
