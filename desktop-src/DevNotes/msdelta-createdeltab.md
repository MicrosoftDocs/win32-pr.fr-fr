---
description: Crée un delta entre la source et la cible (fourni sous forme de mémoires tampons) et retourne le delta de sortie comme une mémoire tampon allouée par MSDelta.
title: CreateDeltaB function
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: CreateDeltaB
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateDeltaB
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: a2142f26499514c24967e5334d782c2dee559cd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523480"
---
# <a name="createdeltab-function"></a>CreateDeltaB function

Crée un delta entre la source et la cible (fourni sous forme de mémoires tampons) et retourne le delta de sortie comme une mémoire tampon allouée par MSDelta.

> [!NOTE]
> Vous devez appeler [DeltaFree](msdelta-deltafree.md) pour libérer la mémoire tampon de sortie une fois cette fonction terminée.

## <a name="syntax"></a>Syntaxe

```cpp
BOOL  WINAPI  CreateDeltaB(
           DELTA_FILE_TYPE  FileTypeSet,
           DELTA_FLAG_TYPE  SetFlags,
           DELTA_FLAG_TYPE  ResetFlags,
           DELTA_INPUT      Source,
           DELTA_INPUT      Target,
           DELTA_INPUT      SourceOptions,
           DELTA_INPUT      TargetOptions,
           DELTA_INPUT      GlobalOptions,
    const  FILETIME        *lpTargetFileTime,
           ALG_ID           HashAlgId,
           LPDELTA_OUTPUT   lpDelta
    );
```

## <a name="parameters"></a>Paramètres

*FileTypeSet*

dans Valeur [DELTA_FILE_TYPE](/previous-versions/bb417345(v=msdn.10)#file-type-sets) qui indique le type de fichier à utiliser pour le processus de création.

*SetFlags*

dans Une ou plusieurs valeurs [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) qui spécifient les indicateurs à utiliser pendant le processus de création, en plus des indicateurs par défaut.

*ResetFlags*

dans Une ou plusieurs valeurs [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) qui spécifient les indicateurs par défaut à réinitialiser au cours du processus de création.

*Source*

dans Structure [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) contenant un pointeur vers la mémoire tampon contenant les données sources.

*Cible*

dans Structure [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) contenant un pointeur vers la mémoire tampon contenant les données cibles.

*SourceOptions*

[in] Réservée. Passer une structure [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) avec la valeur *modifiable* définie à **false**, *lpStart* défini sur **null** et *uSize* défini sur 0.

*TargetOptions*

[in] Réservée. Passer une structure [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) avec la valeur *modifiable* définie à **false**, *lpStart* défini sur **null** et *uSize* défini sur 0.

*GlobalOptions*

[in] Réservée. Transmettez une structure [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) avec *LpStart* défini sur **null** et *uSize* défini sur 0.

*lpTargetFileTime*

dans L’horodatage défini sur le fichier cible après Delta s’applique. Si la **valeur est null**, l’horodatage cible sera l’heure actuelle pendant le processus de création.

*HashAlgId*

dans ALG_ID de l’algorithme à utiliser pour générer la signature cible. Certaines valeurs spéciales sont les suivantes :

- 0 = aucune signature
- 32 = CRC de 32 bits défini dans msdelta.dll

*lpDelta*

à Pointeur vers la structure [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) dans laquelle le delta doit être écrit.

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
