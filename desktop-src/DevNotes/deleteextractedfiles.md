---
description: La fonction DeleteExtractedFiles supprime les fichiers qui ont été extraits par la fonction Extract.
ms.assetid: 253e6267-d4be-46d6-bad2-2eb20bbc7e33
title: DeleteExtractedFiles fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteExtractedFiles
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 500de4df41c82f1956f50abcc25dc84f11484b693dc8d1a5f8bc53ab556ade0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162090"
---
# <a name="deleteextractedfiles-function"></a>DeleteExtractedFiles fonction)

\[Cette fonction n’étant plus prise en charge, son comportement ne peut pas être garanti.\]

La fonction **DeleteExtractedFiles** supprime les fichiers qui ont été extraits par la fonction [**extract**](extract.md) .

## <a name="syntax"></a>Syntaxe


```C++
VOID WINAPI DeleteExtractedFiles(
   PSESSION ps
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ps* 
</dt> <dd>

Pointeur vers une structure de [**session**](session.md) qui contient des informations sur la session active.

Cette fonction libère la mémoire dans le membre **pFileList** de cette structure et affecte à **PFileList** la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Extract**](extract.md)
</dt> <dt>

[**SESSION**](session.md)
</dt> </dl>

 

 
