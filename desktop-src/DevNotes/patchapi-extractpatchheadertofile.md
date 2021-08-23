---
description: Extrait les informations d’en-tête d’un Delta.
title: ExtractPatchHeaderToFileA/W, fonction
ms.topic: reference
ms.date: 04/17/2020
ms.keywords: ExtractPatchHeaderToFileA, ExtractPatchHeaderToFileW
req.header: patchapi.h
req.dll: mspatchc.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtractPatchHeaderToFileW
api_type:
- DllExport
api_location:
- mspatchc.dll
ms.openlocfilehash: 626bd53e3361f4d29cc76e17ae2788ddea3bc8b99b580196bcbf77c27a6983d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571799"
---
# <a name="extractpatchheadertofileaw-function"></a>ExtractPatchHeaderToFileA/W, fonction

Les fonctions **ExtractPatchHeaderToFileA** et **ExtractPatchHeaderToFileW** extraient les informations d’en-tête d’un Delta. Le Delta est fourni sous la forme d’un chemin d’accès de fichier. L’en-tête de sortie est également écrit dans un chemin d’accès fourni.

## <a name="syntax"></a>Syntaxe

```cpp
BOOL  PATCHAPI  ExtractPatchHeaderToFileA(
    LPCTSTR  PatchFileName,
    LPCTSTR  PatchHeaderFileName
    );

BOOL  PATCHAPI  ExtractPatchHeaderToFileW(
    LPCWSTR  PatchFileName,
    LPCWSTR  PatchHeaderFileName
    );
```

## <a name="parameters"></a>Paramètres

*PatchFileName*

Nom du Delta contenant l’en-tête.

*PatchHeaderFileName*

Nom du fichier d’en-tête à créer.

## <a name="return-value"></a>Valeur retournée

Cette fonction retourne **true** si elle est réussie ; Sinon, elle retourne **false**.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|----------------|---------------------------------------------------------------------------------------|
| En-tête | patchapi. h |
| DLL | mspatchc.dll |
| Unicode | Implémenté en tant que ExtractPatchHeaderToFileW (Unicode) et ExtractPatchHeaderToFileA (ANSI) |

## <a name="see-also"></a>Voir aussi

[PatchAPI](patchapi.md)
