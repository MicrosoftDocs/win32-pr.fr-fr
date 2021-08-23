---
description: Crée un delta entre le fichier source spécifié et le fichier cible spécifié.
title: CreatePatchFileExA/W, fonction
ms.topic: reference
ms.date: 04/17/2020
ms.keywords: CreatePatchFileExA, CreatePatchFileExW
req.header: patchapi.h
req.dll: mspatchc.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePatchFileExW
api_type:
- DllExport
api_location:
- mspatchc.dll
ms.openlocfilehash: 7d73b6f4d10c52e9eca147227fdbfece31cba157af84fdf56dbef5cacda516b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690869"
---
# <a name="createpatchfileexaw-function"></a>CreatePatchFileExA/W, fonction

Les fonctions **CreatePatchFileExA** et **CreatePatchFileExW** créent un delta entre le fichier source spécifié et le fichier cible spécifié. Les fichiers source et cible sont fournis sous forme de chemins d’accès. Le delta de sortie est également écrit dans un chemin d’accès fourni. Ces fonctions fournissent des rapports de progression pendant le processus de création.

## <a name="syntax"></a>Syntaxe

```cpp
BOOL  PATCHAPI  CreatePatchFileExA(
    ULONG                     OldFileCount,
    PPATCH_OLD_FILE_INFO_A    OldFileInfoArray,
    LPCTSTR                   NewFileName,
    LPCTSTR                   PatchFileName,
    ULONG                     OptionFlags,
    PPATCH_OPTION_DATA        OptionData,
    PPATCH_PROGRESS_CALLBACK  ProgressCallback,
    PVOID                     CallbackContext
    );

BOOL  PATCHAPI  CreatePatchFileExW(
    ULONG                     OldFileCount,
    PPATCH_OLD_FILE_INFO_A    OldFileInfoArray,
    LPCWSTR                   NewFileName,
    LPCWSTR                   PatchFileName,
    ULONG                     OptionFlags,
    PPATCH_OPTION_DATA        OptionData,
    PPATCH_PROGRESS_CALLBACK  ProgressCallback,
    PVOID                     CallbackContext
    );
```

## <a name="parameters"></a>Paramètres

*OldFileCount*

Nombre total de fichiers sources. Utilisé pour créer des deltas sur plusieurs fichiers sources (255 maximum).

*OldFileInfoArray*

Pointeur vers le tableau d’informations du fichier source.

*NewFileName*

Nom du fichier cible.

*PatchFileName*

Nom du Delta créé.

*OptionFlags*

Indicateurs de création.

*ProgressCallback*

Pointeur vers le rappel de progression défini par l’application.

*CallbackContext*

Pointeur vers le contexte défini par l’application.

## <a name="return-value"></a>Valeur retournée

Cette fonction retourne **true** si elle est réussie ; Sinon, elle retourne **false**.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|----------------|---------------------------------------------------------------------------------------|
| En-tête | patchapi. h |
| DLL | mspatchc.dll |
| Unicode | Implémenté en tant que CreatePatchFileExW (Unicode) et CreatePatchFileExA (ANSI) |

## <a name="see-also"></a>Voir aussi

[PatchAPI](patchapi.md)
