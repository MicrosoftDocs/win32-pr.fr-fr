---
title: D3DPERF_QueryRepeatFrame fonction)
description: Déterminez si un profileur de performances demande que le frame actuel soit renvoyé à Direct3D pour l’analyse des performances. Cette fonction n’est pas actuellement prise en charge par PIX.
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
- D3DPERF_QueryRepeatFrame
targetos: Windows
ms.openlocfilehash: c4054a0704fd0258483ee0d3d3d555cb5eabe7f9
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2020
ms.locfileid: "103723875"
---
# <a name="d3dperf_queryrepeatframe-function"></a>D3DPERF_QueryRepeatFrame fonction)

Déterminez si un profileur de performances demande que le frame actuel soit renvoyé à Direct3D pour l’analyse des performances. Cette fonction n’est pas actuellement prise en charge par PIX.

## <a name="syntax"></a>Syntaxe

```cpp
BOOL WINAPI D3DPERF_QueryRepeatFrame( void );
```

## <a name="return-value"></a>Valeur de retour

Si la valeur de retour est TRUE, l’appelant doit répéter la même séquence d’appels. Si la valeur est FALSe, l’appelant doit continuer.

## <a name="remarks"></a>Notes

La fonction doit être appelée immédiatement après **IDirect3DDevice9 ::P renvoyé** est appelé.

## <a name="requirements"></a>Configuration requise
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plateforme cible** | Windows |
| **En-tête** | d3d9. h |
| **Bibliothèque** | d3d9. lib |
| **DLL** | d3d9.dll |