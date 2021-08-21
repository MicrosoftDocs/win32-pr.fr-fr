---
title: D3DPERF_EndEvent fonction)
description: Marque la fin d’un événement défini par l’utilisateur. PIX peut utiliser cet événement pour déclencher une action.
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
- D3DPERF_EndEvent
targetos: Windows
ms.openlocfilehash: bd12780dfdfcb86e83495ae877d8debf1e768517826329ccee8d40ffaa88fbbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989249"
---
# <a name="d3dperf_endevent-function"></a>D3DPERF_EndEvent fonction)

Marque la fin d’un événement défini par l’utilisateur. PIX peut utiliser cet événement pour déclencher une action.

## <a name="syntax"></a>Syntaxe

```cpp
int WINAPI D3DPERF_EndEvent(void);
```

## <a name="return-value"></a>Valeur de retour

Niveau de la hiérarchie dans laquelle l’événement se termine. Si une erreur se produit, cette valeur est négative.

## <a name="requirements"></a>Configuration requise
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plateforme cible** | Windows |
| **En-tête** | d3d9. h |
| **Bibliothèque** | d3d9. lib |
| **DLL** | d3d9.dll |