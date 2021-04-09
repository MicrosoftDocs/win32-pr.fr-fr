---
description: Calcule les normales des unités pour chaque vertex d’une maille. Fourni pour prendre en charge les applications héritées. Utilisez D3DXComputeTangentFrameEx pour obtenir de meilleurs résultats.
ms.assetid: 7c879149-2c4c-4824-9604-e88696cc6ddc
title: D3DXComputeNormals, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeNormals
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f95e5e353c318429f5340d1a831f9ca3050ba3c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953902"
---
# <a name="d3dxcomputenormals-function"></a>D3DXComputeNormals fonction)

Calcule les normales des unités pour chaque vertex d’une maille. Fourni pour prendre en charge les applications héritées. Utilisez [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) pour obtenir de meilleurs résultats.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXComputeNormals(
  _Inout_       LPD3DXBASEMESH pMesh,
  _In_    const DWORD          *pAdjacency
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMesh* \[ in, out\]
</dt> <dd>

Type : **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Pointeur vers une interface [**ID3DXBaseMesh**](id3dxbasemesh.md) représentant l’objet de maillage normalisé.

</dd> <dt>

*pAdjacency* \[ dans\]
</dt> <dd>

Type : **const [**DWORD**](../winprog/windows-data-types.md) \***

Pointeur vers un tableau de trois DWORD par visage qui spécifient les trois voisins pour chaque visage dans la maille progressive créée. Ce paramètre est facultatif et doit avoir la valeur **null** s’il n’est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est S \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Le maillage d’entrée doit avoir l’indicateur [ \_ normal D3DFVF](d3dfvf.md) spécifié dans son format de vertex flexible.

Un normal pour un vertex est généré en calculant la moyenne des normales de tous les visages qui partagent ce vertex.

Si une contiguïté est fournie, les vertex répliqués sont ignorés et « lissés » sur. Si l’adjacence n’est pas fournie, les vertex répliqués auront des normales dont la moyenne est calculée à partir de uniquement les visages qui les référencent explicitement.

Cette fonction appelle simplement [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) avec les paramètres d’entrée suivants :


```
D3DXComputeTangentFrameEx( pMesh,
                           D3DX_DEFAULT,
                           0,
                           D3DX_DEFAULT,
                           0,
                           D3DX_DEFAULT,
                           0,
                           D3DDECLUSAGE_NORMAL,
                           0,
                           D3DXTANGENT_GENERATE_IN_PLACE | D3DXTANGENT_CALCULATE_NORMALS,
                           pAdjacency,
                           -1.01f,
                           -0.01f,
                           -1.01f,
                           NULL,
                           NULL);
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
