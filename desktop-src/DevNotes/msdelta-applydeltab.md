---
description: Utilise le Delta et la source (fournis sous forme de mémoires tampons) pour créer une nouvelle copie des données cibles. Les données de sortie sont retournées dans une mémoire tampon allouée par MSDelta.
title: ApplyDeltaB function
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: ApplyDeltaB
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplyDeltaB
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: 2a6034ca101a192be66db1b16a4ac7b27e7288d9453dfaaab5782e55e11d4c67
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079759"
---
# <a name="applydeltab-function"></a>ApplyDeltaB function

Utilise le Delta et la source (fournis sous forme de mémoires tampons) pour créer une nouvelle copie des données cibles. Les données de sortie sont retournées dans une mémoire tampon allouée par MSDelta.

> [!NOTE]
> Vous devez appeler [DeltaFree](msdelta-deltafree.md) pour libérer la mémoire tampon de sortie une fois cette fonction terminée.

> [!NOTE]
> Si le delta spécifié a été créé à l’aide de [PatchAPI](patchapi.md)et que l’indicateur [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) est défini, MSDelta appellera PatchAPI pour appliquer le delta.

## <a name="syntax"></a>Syntaxe

```cpp
BOOL  WINAPI  ApplyDeltaB(
    DELTA_FLAG_TYPE  ApplyFlags,
    DELTA_INPUT      Source,
    DELTA_INPUT      Delta,
    LPDELTA_OUTPUT   lpTarget
   );
```

## <a name="parameters"></a>Paramètres

*ApplyFlags*

dans [DELTA_FLAG_NONE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) ou [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags).

*Source*

dans Structure [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) contenant un pointeur vers la mémoire tampon contenant les données sources.

*Delta*

dans Structure [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) contenant un pointeur vers la mémoire tampon contenant les données Delta.

*lpTarget*

à Pointeur vers la structure [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) dans laquelle la cible doit être écrite.

## <a name="return-value"></a>Valeur retournée

Cette fonction retourne **true** si elle est réussie ; Sinon, elle retourne **false**. Quand la fonction retourne **false**, vous pouvez appeler [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour recevoir le code d’erreur système Win32 correspondant.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|----------------|---------------------------------------------------------------------------------------|
| En-tête | msdelta. h |
| DLL | msdelta.dll |
| Unicode | Non applicable |

## <a name="see-also"></a>Voir aussi

[MSDelta](msdelta.md)

[DeltaFree](msdelta-deltafree.md)
