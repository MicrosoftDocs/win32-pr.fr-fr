---
description: Ferme un handle de recherche.
ms.assetid: 2e6a547f-26a7-401a-b1e4-3f085ce82729
title: CSCFindClose fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindClose
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 862159ed74d6c7c9ddbe4d6f97bede37bab7dca949e6d3259715737de07b8df5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758719"
---
# <a name="cscfindclose-function"></a>CSCFindClose fonction)

\[Cette fonction n’est pas prise en charge et ne doit pas être utilisée.\]

Ferme un handle de recherche.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI CSCFindClose(
  _In_ HANDLE hFind
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hFind* \[ dans\]
</dt> <dd>

Un handle de recherche retourné par la fonction [**CSCFindFirstFileW**](cscfindfirstfilew.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction retourne **true** si elle est réussie ; Sinon, elle retourne **false**.

## <a name="remarks"></a>Remarques

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSCFindFirstFileW**](cscfindfirstfilew.md)
</dt> </dl>

 

 
