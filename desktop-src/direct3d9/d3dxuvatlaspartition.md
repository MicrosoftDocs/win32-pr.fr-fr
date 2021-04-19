---
description: Créez un Atlas UV pour une maille.
ms.assetid: c46f3e47-8e72-435c-875d-cccfa4b893a2
title: D3DXUVAtlasPartition, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasPartition
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 707a503832a4fd66ab2e8d9346587d11544a885c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531536"
---
# <a name="d3dxuvatlaspartition-function"></a>D3DXUVAtlasPartition fonction)

Créez un Atlas UV pour une maille.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXUVAtlasPartition(
  _In_        LPD3DXMESH      pMesh,
  _In_        UINT            dwMaxChartNumber,
  _In_        FLOAT           fMaxStretch,
  _In_        DWORD           dwTextureIndex,
  _In_  const DWORD           *pdwAdjacency,
        const DWORD           *pdwFalseEdges,
  _In_        FLOAT           *pfIMTArray,
  _In_        LPD3DXUVATLASCB pCallback,
  _In_        FLOAT           fCallbackFrequency,
  _In_        LPVOID          pUserContent,
  _In_        DWORD           dwOptions,
  _In_        LPD3DXMESH      *ppMeshOut,
  _Out_       LPD3DXBUFFER    pFacePartitioning,
  _Out_       LPD3DXBUFFER    *ppVertexRemapArray,
              LPD3DXBUFFER    *ppPartitionResultAdjacency,
  _Out_       FLOAT           *pfMaxStretchOut,
  _Out_       UINT            *pdwNumChartsOut
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMesh* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)**

Pointeur vers un maillage d’entrée (voir [**ID3DXMesh**](id3dxmesh.md)) qui contient la géométrie de l’objet pour le calcul de l’Atlas. Au minimum, la maille doit contenir des données de position et des coordonnées de texture 2D.

</dd> <dt>

*dwMaxChartNumber* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre maximal de graphiques dans lesquels partitionner le maillage. Consultez les remarques sur les modes de partitionnement. Utilisez 0 pour indiquer à D3DX que l’Atlas doit être paramétré en fonction de Stretch.

</dd> <dt>

*fMaxStretch* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Quantité d’étirement autorisée. 0 signifie qu’aucun étirement n’est autorisé, 1 signifie qu’une quantité d’étirement peut être utilisée.

</dd> <dt>

*dwTextureIndex* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Index de coordonnées de texture de base zéro qui identifie le jeu de coordonnées de texture à utiliser.

</dd> <dt>

*pdwAdjacency* \[ dans\]
</dt> <dd>

Type : **const [**DWORD**](../winprog/windows-data-types.md) \***

Pointeur vers un tableau de données d’contiguïté avec 3 DWORDs par face, indiquant quels triangles sont adjacents les uns aux autres (voir [**ID3DXBaseMesh :: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).

</dd> <dt>

*pdwFalseEdges* 
</dt> <dd>

Type : **const [**DWORD**](../winprog/windows-data-types.md) \***

Tableau avec 3 DWORDs par face. Chaque visage indique si une arête est false ou non. Un bord non-faux est indiqué par-1, un faux bord est indiqué par une autre valeur. Cela permet le paramétrage d’une maille de quatre cœurs où les bords du milieu de chaque quadruple ne sont pas coupés.

</dd> <dt>

*pfIMTArray* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Pointeur vers un tableau de dizaines de métriques intégrés qui décrit comment étirer un triangle (voir [IntegratedMetricTensor](using-uvatlas.md)).

</dd> <dt>

*pCallback* \[ dans\]
</dt> <dd>

Type : **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**

Pointeur vers une fonction de rappel (voir [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) qui est utile pour surveiller la progression.

</dd> <dt>

*fCallbackFrequency* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Spécifiez la fréquence à laquelle D3DX appellera le rappel. une valeur par défaut raisonnable est 0,0001 f.

</dd> <dt>

*pUserContent* \[ dans\]
</dt> <dd>

Type : **[ **LPVOID**](../winprog/windows-data-types.md)**

Pointeur vers une valeur définie par l’utilisateur qui est passée à la fonction de rappel ; généralement utilisé par une application pour passer un pointeur vers une structure de données qui fournit des informations de contexte pour la fonction de rappel.

</dd> <dt>

*dwOptions* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Spécifiez la qualité des graphiques générés en combinant un ou plusieurs indicateurs [**D3DXUVATLAS**](./d3dxuvatlas.md) .

</dd> <dt>

*ppMeshOut* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***

Pointeur vers la maille créée avec l’Atlas (voir [**ID3DXMesh**](id3dxmesh.md)).

</dd> <dt>

*pFacePartitioning* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)**

Pointeur vers un tableau des données de partitionnement de type final. Chaque élément contient un DWORD par face (voir [**ID3DXBuffer**](id3dxbuffer.md)).

</dd> <dt>

*ppVertexRemapArray* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Pointeur vers un tableau de vertex remappés. Chaque élément de tableau identifie le sommet d’origine à partir duquel provient chaque sommet final (si le Vertex a été fractionné pendant le remappage). Chaque élément de tableau contient une valeur DWORD par vertex.

</dd> <dt>

*ppPartitionResultAdjacency* 
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) . Cette mémoire tampon contient un tableau de trois DWORD par visage qui spécifient les trois voisins pour chaque visage dans le maillage de sortie. Ce paramètre ne doit pas avoir la **valeur null**, car l’appel suivant à D3DXUVAtlasPack () en a besoin.

</dd> <dt>

*pfMaxStretchOut* \[ à\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Pointeur vers la valeur d’étirement maximale générée par l’algorithme Atlas. La plage est comprise entre 0,0 et 1,0.

</dd> <dt>

*pdwNumChartsOut* \[ à\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Pointeur vers le nombre de graphiques créés par l’algorithme Atlas. Si dwMaxChartNumber est trop faible, ce paramètre retourne le nombre minimal de graphiques requis pour créer un Atlas.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK ; sinon, la valeur est D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Notes

D3DXUVAtlasPartition est similaire à [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md), à ceci près que D3DXUVAtlasPartition n’effectue pas l’étape de compression finale.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[UVAtlas, fonctions](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[Outil Command-Line d’Atlas UV (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)
</dt> </dl>

 

 
