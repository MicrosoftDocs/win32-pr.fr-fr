---
description: Permet à un débogueur d’examiner les informations de table de fonctions dynamiques.
ms.assetid: 32fd0dfd-ca7c-45e4-9d59-2b3318d7e13d
title: RtlGetFunctionTableListHead fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetFunctionTableListHead
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: ff41aca0d268083132fd1a45371b0bb1ca026e5e6d693619ba1e2c2f9f2dd8f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666729"
---
# <a name="rtlgetfunctiontablelisthead-function"></a>RtlGetFunctionTableListHead fonction)

\[cette fonction peut être modifiée ou supprimée de Windows sans préavis.\]

Permet à un débogueur d’examiner les informations de table de fonctions dynamiques.

## <a name="syntax"></a>Syntaxe


```C++
PLIST_ENTRY RtlGetFunctionTableListHead(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Retourne un pointeur vers le début de la liste de tables de fonctions.

## <a name="remarks"></a>Remarques

notez que le fichier d’en-tête WDK (Windows Driver Kit) Ntdef. h est requis pour certaines définitions. La bibliothèque d’importation associée, ntdll. lib, est disponible dans le kit WDK. Vous pouvez également utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Ntdll.dll.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
