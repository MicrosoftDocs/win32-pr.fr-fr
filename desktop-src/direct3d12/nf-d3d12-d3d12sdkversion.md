---
title: Symbole D3D12SDKVersion
description: Numéro de version du kit de développement logiciel (SDK) Direct3D 12.
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/25/2021
req.lib: ''
req.dll: d3d12core.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- d3d12core.dll
api_name:
- D3D12SDKVersion
targetos: Windows
ms.openlocfilehash: f77786d0a057d8922923913984149c4b8ecd3bc8
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520035"
---
# <a name="d3d12sdkversion-symbol"></a>Symbole D3D12SDKVersion

Numéro de version du kit de développement logiciel (SDK) Direct3D 12.

## <a name="syntax"></a>Syntaxe

```cpp
extern "C" { _declspec(dllexport) extern const UINT D3D12SDKVersion = n;}
```

## <a name="return-value"></a>Valeur de retour

[Uint](../winprog/windows-data-types.md) qui contient le numéro de version du kit de développement logiciel (SDK) Direct3D 12.

## <a name="remarks"></a>Remarques

**D3D12SDKVersion** n’est pas associé à une bibliothèque d’importation ni à un fichier d’en-tête.

## <a name="requirements"></a>Configuration requise

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plateforme cible** | Windows |
| **En-tête** | N/A |
| **Bibliothèque** | N/A |
| **DLL** | d3d12core.dll |

## <a name="see-also"></a>Voir aussi
