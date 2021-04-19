---
title: RoFailFastWithErrorContextInternal2 fonction)
description: Déclenche une exception non continuable dans le processus en cours et vous permet également d’inclure un contexte d’erreur supplémentaire qui n’a pas déjà été capturé par le système d’exploitation.
ms.localizationpriority: low
ms.topic: reference
ms.date: 03/13/2020
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- ComBase.dll
api_name:
- RoFailFastWithErrorContextInternal2
targetos: Windows
ms.openlocfilehash: 84584c339851ecbf8df5d6dbda2aaa575ca6487b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "106511717"
---
# <a name="rofailfastwitherrorcontextinternal2-function"></a>RoFailFastWithErrorContextInternal2 fonction)

Déclenche une exception non continuable dans le processus en cours et vous permet également d’inclure un contexte d’erreur supplémentaire qui n’a pas déjà été capturé par le système d’exploitation.

## <a name="syntax"></a>Syntaxe

```cpp
void WINAPI RoFailFastWithErrorContextInternal2(
  HRESULT hrError,
  ULONG cStowedExceptions,
  _In_reads_opt_(cStowedExceptions) PSTOWED_EXCEPTION_INFORMATION_V2 aStowedExceptionPointers[]
);
```

## <a name="parameters"></a>Paramètres

`hrError`

Type : **[HRESULT](../../com/structure-of-com-error-codes.md)**

**HRESULT** associé à l’erreur actuelle. L’exception est levée pour toute valeur de *hrError*.

`cStowedExceptions`

Type : **[ULong](../../winprog/windows-data-types.md)**

Nombre d’éléments dans le tableau *aStowedExceptionPointers* .

`aStowedExceptionPointers`

Type : **[PSTOWED_EXCEPTION_INFORMATION_V2](../../wer/stowed-exception-information-v2.md)\[\]**

Tableau de pointeurs vers des structures de [**STOWED_EXCEPTION_INFORMATION_V2**](../../wer/stowed-exception-information-v2.md) . Chaque structure contient des informations qui décrivent une exception arrimée. Les informations de ces structures sont ensuite envoyées à Rapport d’erreurs Windows (WER), ainsi que les informations sur les exceptions qui ont été capturées par la plateforme.

## <a name="return-value"></a>Valeur retournée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

**RoFailFastWithErrorContextInternal2** n’est pas associé à une bibliothèque d’importation ni à un fichier d’en-tête. Vous pouvez l’appeler en utilisant d’abord la fonction [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryw) (pour charger `ComBase.dll` ), puis en appelant la fonction [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour récupérer l’adresse de **RoFailFastWithErrorContextInternal2**.

Pour plus d’informations, consultez [fonction RoFailFastWithErrorContext](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext).

## <a name="requirements"></a>Configuration requise
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plateforme cible** | Windows |
| **En-tête** | N/A |
| **Bibliothèque** | N/A |
| **DLL** | ComBase.dll |

## <a name="see-also"></a>Voir aussi

* [RoFailFastWithErrorContext fonction)](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext)