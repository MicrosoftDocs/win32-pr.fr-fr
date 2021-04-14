---
title: D3DPERF_BeginEvent fonction)
description: Marque le début d’un événement défini par l’utilisateur. PIX peut utiliser cet événement pour déclencher une action.
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
- D3DPERF_BeginEvent
targetos: Windows
ms.openlocfilehash: f6732d4ce969cbd26cdb32f4750654c7baacd324
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2020
ms.locfileid: "104381639"
---
# <a name="d3dperf_beginevent-function"></a>D3DPERF_BeginEvent fonction)

Marque le début d’un événement défini par l’utilisateur. PIX peut utiliser cet événement pour déclencher une action.

## <a name="syntax"></a>Syntaxe

```cpp
int WINAPI D3DPERF_BeginEvent(
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

Niveau de base zéro de la hiérarchie à partir duquel cet événement commence. Si une erreur se produit, la valeur de retour est négative.

## <a name="remarks"></a>Notes

Les événements définis par l’utilisateur regroupent d’autres événements d’une manière significative pour le programme cible afin qu’ils puissent être mieux représentés dans les outils de profilage des performances. Par exemple, un événement d' *espace de dessin* peut comporter un certain nombre d’appels Direct3D qui gèrent le dessin d’un espace dans un jeu. Les événements peuvent être imbriqués.

Chaque appel de **D3DPERF_BeginEvent** doit avoir un appel de **D3DPERF_EndEvent** correspondant. Les événements instantanés (qui ne comportent pas d’autres événements) doivent être étiquetés à l’aide de **D3DPERF_SetMarker** plutôt que par **D3DPERF_BeginEvent** et **D3DPERF_EndEvent**.

## <a name="requirements"></a>Configuration requise
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plateforme cible** | Windows |
| **En-tête** | d3d9. h |
| **Bibliothèque** | d3d9. lib |
| **DLL** | d3d9.dll |