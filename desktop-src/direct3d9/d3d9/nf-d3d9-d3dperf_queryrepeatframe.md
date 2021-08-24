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
ms.openlocfilehash: dbc46ff05b6fa1846bb0e1ffc1fca928ca1d68ee38a43708c77a109b61a405da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751239"
---
# <a name="d3dperf_queryrepeatframe-function"></a>D3DPERF_QueryRepeatFrame fonction)

Déterminez si un profileur de performances demande que le frame actuel soit renvoyé à Direct3D pour l’analyse des performances. Cette fonction n’est pas actuellement prise en charge par PIX.

## <a name="syntax"></a>Syntaxe

```cpp
BOOL WINAPI D3DPERF_QueryRepeatFrame( void );
```

## <a name="return-value"></a>Valeur de retour

Si la valeur de retour est TRUE, l’appelant doit répéter la même séquence d’appels. Si la valeur est FALSe, l’appelant doit continuer.

## <a name="remarks"></a>Remarques

La fonction doit être appelée immédiatement après **IDirect3DDevice9 ::P renvoyé** est appelé.

## <a name="requirements"></a>Configuration requise
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plateforme cible** | Windows |
| **En-tête** | d3d9. h |
| **Bibliothèque** | d3d9. lib |
| **DLL** | d3d9.dll |