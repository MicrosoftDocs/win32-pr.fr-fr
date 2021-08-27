---
title: D3DPERF_GetStatus fonction)
description: Déterminez l’état actuel du profileur à partir du programme cible.
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
- D3DPERF_GetStatus
targetos: Windows
ms.openlocfilehash: 78ff9eda9ab224faf4b2a117f6230e3361664bbfea35d8b2a8484ba7f5ab764a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805744"
---
# <a name="d3dperf_getstatus-function"></a>D3DPERF_GetStatus fonction)

Déterminez l’état actuel du profileur à partir du programme cible.

## <a name="syntax"></a>Syntaxe

```cpp
DWORD WINAPI D3DPERF_GetStatus( void );
```

## <a name="return-value"></a>Valeur de retour

Valeur différente de zéro quand PIX Profile le programme cible ; Sinon, zéro.

## <a name="requirements"></a>Configuration requise
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plateforme cible** | Windows |
| **En-tête** | d3d9. h |
| **Bibliothèque** | d3d9. lib |
| **DLL** | d3d9.dll |