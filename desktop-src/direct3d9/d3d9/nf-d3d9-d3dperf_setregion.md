---
title: D3DPERF_SetRegion fonction)
description: Marquez une série de frames avec la couleur et le nom spécifiés dans le fichier PIXRun. Cette fonction n’est pas actuellement prise en charge par PIX.
ms.localizationpriority: low
ms.topic: reference
ms.date: 04/06/2020
req.lib: d3d9.lib
req.dll: d3d9.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- d3d9.dll
api_name:
- D3DPERF_SetRegion
targetos: Windows
ms.openlocfilehash: 650cc6063865da5ce30b97ed1468c1718ace5da6
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2020
ms.locfileid: "106511475"
---
# <a name="d3dperf_setregion-function"></a>D3DPERF_SetRegion fonction)

Marquez une série de frames avec la couleur et le nom spécifiés dans le fichier PIXRun. Cette fonction n’est pas actuellement prise en charge par PIX.

## <a name="syntax"></a>Syntaxe

```cpp
void WINAPI D3DPERF_SetRegion(
  D3DCOLOR col,
  LPCWSTR wszName
);
```

## <a name="parameters"></a>Paramètres

`col`

Couleur de l’événement. Il s’agit de la couleur permettant d’afficher l’événement dans l’affichage des événements.

`wszName`

Nom de l’événement.

## <a name="return-value"></a>Valeur retournée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Pour faciliter l’analyse, le programme cible peut utiliser la couleur pour marquer chaque niveau d’un programme cible.

## <a name="requirements"></a>Configuration requise
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plateforme cible** | Windows |
| **En-tête** | d3d9. h |
| **Bibliothèque** | d3d9. lib |
| **DLL** | d3d9.dll |