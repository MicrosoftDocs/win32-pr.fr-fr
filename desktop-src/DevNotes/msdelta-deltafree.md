---
description: Libère le bloc de mémoire spécifié.
title: DeltaFree function
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: DeltaFree
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- DeltaFree
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: 606b8d91d20c74f7dd56ff4e09986abec3eef547989990a38bd8b4e3a27382c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079729"
---
# <a name="deltafree-function"></a>DeltaFree function

Libère le bloc de mémoire spécifié. Vous devez appeler cette fonction après avoir correctement appelé [CreateDeltaB](msdelta-createdeltab.md) et [ApplyDeltaB](msdelta-applydeltab.md) pour libérer la mémoire tampon allouée par MSDelta.

## <a name="syntax"></a>Syntaxe

```cpp
BOOL  WINAPI  DeltaFree(
    LPVOID  lpMemory
    );
```

## <a name="parameters"></a>Paramètres

*lpMemory*

dans Bloc de mémoire à libérer.

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

[CreateDeltaB](msdelta-createdeltab.md)

[ApplyDeltaB](msdelta-applydeltab.md)
