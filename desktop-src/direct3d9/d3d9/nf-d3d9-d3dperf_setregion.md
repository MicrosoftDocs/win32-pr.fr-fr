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
ms.openlocfilehash: 05884fe8a3b104588a941dcaf3089a1c0f6f8eab4f4a01e143470f73454ad4ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989259"
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

## <a name="remarks"></a>Remarques

Pour faciliter l’analyse, le programme cible peut utiliser la couleur pour marquer chaque niveau d’un programme cible.

## <a name="requirements"></a>Configuration requise
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plateforme cible** | Windows |
| **En-tête** | d3d9. h |
| **Bibliothèque** | d3d9. lib |
| **DLL** | d3d9.dll |