---
title: D3DPERF_SetOptions fonction)
description: Définissez les options du profileur spécifiées par le programme cible.
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
- D3DPERF_SetOptions
targetos: Windows
ms.openlocfilehash: 579c07d8f93696e4e3c83b1e61c1ff5fca65e12b5a7cf0a5937a254ecc6dc306
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805734"
---
# <a name="d3dperf_setoptions-function"></a>D3DPERF_SetOptions fonction)

Définissez les options du profileur spécifiées par le programme cible.

## <a name="syntax"></a>Syntaxe

```cpp
int WINAPI D3DPERF_SetOptions(
  DWORD dwOptions
);
```

## <a name="parameters"></a>Paramètres

`dwOptions`

Options utilisateur reconnaissables par PIX. Affectez-lui la valeur 1 pour indiquer à PIX que le programme cible n’accorde pas l’autorisation d’être profilée.

## <a name="return-value"></a>Valeur retournée

Cette fonction ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plateforme cible** | Windows |
| **En-tête** | d3d9. h |
| **Bibliothèque** | d3d9. lib |
| **DLL** | d3d9.dll |