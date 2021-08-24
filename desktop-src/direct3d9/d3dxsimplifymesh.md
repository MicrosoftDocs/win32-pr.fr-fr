---
description: Génère un maillage simplifié à l’aide des poids fournis qui sont disponibles le plus près possible de l’MinValue donné.
ms.assetid: 589356a9-f272-4851-92ae-54dbecc0b234
title: D3DXSimplifyMesh, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSimplifyMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3cc0bfe18afef7b91dbdf887500b485a446b154cb5775cbf950a7e712a332a9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749779"
---
# <a name="d3dxsimplifymesh-function"></a>D3DXSimplifyMesh fonction)

Génère un maillage simplifié à l’aide des poids fournis qui sont disponibles le plus près possible de l’MinValue donné.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXSimplifyMesh(
  _In_        LPD3DXMESH           pMesh,
  _In_  const DWORD                *pAdjacency,
  _In_  const D3DXATTRIBUTEWEIGHTS *pVertexAttributeWeights,
  _In_  const FLOAT                *pVertexWeights,
  _In_        DWORD                MinValue,
  _In_        DWORD                Options,
  _Out_       LPD3DXMESH           *ppMesh
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMesh* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)**

Pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) représentant la maille source.

</dd> <dt>

*pAdjacency* \[ dans\]
</dt> <dd>

Type : **const [**DWORD**](../winprog/windows-data-types.md) \***

Pointeur vers un tableau de trois DWORD par visage qui spécifient les trois voisins pour chaque visage de la maille à simplifier.

</dd> <dt>

*pVertexAttributeWeights* \[ dans\]
</dt> <dd>

Type : **const [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) \***

Pointeur vers une structure [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) , contenant le poids de chaque composant de vertex. Si ce paramètre a la valeur **null**, une structure par défaut est utilisée. Consultez la section Notes.

</dd> <dt>

*pVertexWeights* \[ dans\]
</dt> <dd>

Type : **const [**float**](../winprog/windows-data-types.md) \***

Pointeur vers un tableau de poids de vertex. Si ce paramètre a la valeur **null**, tous les poids des vertex ont la valeur 1,0.

</dd> <dt>

*MinValue* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Nombre de vertex ou de faces, selon l’indicateur défini dans le paramètre *options* , par lequel simplifier le maillage source.

</dd> <dt>

*Options* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Spécifie les options de simplification de la maille. L’un des indicateurs dans [**D3DXMESHSIMP**](./d3dxmeshsimp.md) peut être défini.

</dd> <dt>

*ppMesh* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***

Adresse d’un pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) représentant le maillage de simplification retourné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

Cette fonction génère un maillage qui a des vertex ou des visages *MinValue* .

Si le processus de simplification ne peut pas réduire le maillage à *MinValue*, l’appel s’effectue toujours car *MinValue* est un minimum souhaité, et non un minimum absolu.

Si *pVertexAttributeWeights* a la valeur **null**, les valeurs suivantes sont affectées à la structure [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) par défaut.


```
D3DXATTRIBUTEWEIGHTS AttributeWeights;
    
AttributeWeights.Position  = 1.0;
AttributeWeights.Boundary =  1.0;
AttributeWeights.Normal   =  1.0;
AttributeWeights.Diffuse  =  0.0;
AttributeWeights.Specular =  0.0;
AttributeWeights.Tex[8]   =  {0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0};
```



Il s’agit de la structure par défaut que la plupart des applications doivent utiliser, car elle ne prend en compte que le réglage géométrique et normal. Dans certains cas particuliers, les autres champs de membre doivent être modifiés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
