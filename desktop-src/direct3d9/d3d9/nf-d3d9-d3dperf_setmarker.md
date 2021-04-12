---
title: D3DPERF_SetMarker fonction)
description: Marquez un événement instantané. PIX peut utiliser cet événement pour déclencher une action.
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
- D3DPERF_SetMarker
targetos: Windows
ms.openlocfilehash: 8eef59b9914ce30b95751641c16becf1963b19e0
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2020
ms.locfileid: "104381640"
---
# <a name="d3dperf_setmarker-function"></a>D3DPERF_SetMarker fonction)

Marquez un événement instantané. PIX peut utiliser cet événement pour déclencher une action.

## <a name="syntax"></a>Syntaxe

```cpp
void WINAPI D3DPERF_SetMarker(
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

Les événements utilisateur instantanés ne dépassent pas ou ne regroupent pas d’autres événements. Par exemple, lorsque l’utilisateur lance une arme dans un jeu, un événement déclenché par une *capture* peut être créé par un appel de **D3DPERF_SetMarker** . Pour regrouper plusieurs événements sous un seul nom défini par l’utilisateur, utilisez **D3DPERF_BeginEvent** et **D3DPERF_EndEvent** plutôt que **D3DPERF_SetMarker**.

## <a name="requirements"></a>Configuration requise
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plateforme cible** | Windows |
| **En-tête** | d3d9. h |
| **Bibliothèque** | d3d9. lib |
| **DLL** | d3d9.dll |