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
ms.openlocfilehash: 4ab032864e59d8e7379fe347d241874d9336e431
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526062"
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

*alimentation* 
</dt> <dd>

Pointeur vers une structure de [**session**](session.md) qui contient des informations sur la session active.

Cette fonction libère la mémoire dans le membre **pFileList** de cette structure et affecte à **PFileList** la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Extraction**](extract.md)
</dt> <dt>

[**SESSION**](session.md)
</dt> </dl>

 

 
