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
ms.openlocfilehash: 40835a0b88558046ff9086ffcd7ec4609d1ed863
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530517"
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
