---
description: La fonction GetDllVersion récupère le numéro de version de Cabinet.dll.
ms.assetid: b324d5cd-1ede-473e-a10f-249c95eda057
title: GetDllVersion fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDllVersion
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 14f2da8c6f8c786042c2abd5f41e02bdfab6f33d9b8aa42a5b5f90a6c4357103
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390709"
---
# <a name="getdllversion-function"></a>GetDllVersion fonction)

\[Cette fonction n’étant plus prise en charge, son comportement ne peut pas être garanti. \]

La fonction **GetDllVersion** récupère le numéro de version de Cabinet.dll.

## <a name="syntax"></a>Syntaxe


```C++
LPCSTR WINAPI GetDllVersion(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Numéro de version du fichier (consultez la [ressource VERSIONINFO](../menurc/versioninfo-resource.md)).

## <a name="remarks"></a>Remarques

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DllGetVersion**](dllgetversion.md)
</dt> </dl>

 

 
