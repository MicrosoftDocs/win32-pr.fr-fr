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
ms.openlocfilehash: 1b1142bd2ece965a3f2fc58b6bb2f90586a8b391
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540398"
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

## <a name="remarks"></a>Notes

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DllGetVersion**](dllgetversion.md)
</dt> </dl>

 

 
