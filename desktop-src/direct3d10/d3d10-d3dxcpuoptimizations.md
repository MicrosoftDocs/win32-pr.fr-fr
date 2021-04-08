---
description: Active ou désactive les optimisations de l’UC.
ms.assetid: 6f73df12-f2fc-4651-b0f7-f7a55e534d3d
title: D3DXCpuOptimizations, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCpuOptimizations
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a0ef276e6d3303acd77c9580b55a9aa49dbe2087
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762200"
---
# <a name="d3dxcpuoptimizations-function"></a>D3DXCpuOptimizations fonction)

Active ou désactive les optimisations de l’UC.

## <a name="syntax"></a>Syntaxe


```C++
D3DX_CPU_OPTIMIZATION D3DXCpuOptimizations(
  _In_ BOOL Enable
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Activer* \[ dans\]
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)**

**True** pour activer les optimisations de l’UC ; Sinon, **false**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : optimisation de l' **[ **\_ UC \_ D3DX**](d3dx-cpu-optimization.md)**

Retourne le type d’UC détecté et pour lequel des optimisations existent (consultez [**D3DX \_ CPU \_ Optimization**](d3dx-cpu-optimization.md)).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
