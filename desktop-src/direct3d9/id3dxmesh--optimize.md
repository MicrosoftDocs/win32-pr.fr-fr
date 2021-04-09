---
description: Génère un nouveau maillage avec des faces et des sommets réorganisés pour optimiser les performances du dessin.
ms.assetid: 6a9bf7b9-2cb9-4b42-92d9-2a121ff79284
title: 'ID3DXMesh :: Optimize, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.Optimize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7752e08236094d7038a5e77ac1a679f787305022
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103954018"
---
# <a name="id3dxmeshoptimize-method"></a>ID3DXMesh :: Optimize, méthode

Génère un nouveau maillage avec des faces et des sommets réorganisés pour optimiser les performances du dessin.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Optimize(
  [in]            DWORD        Flags,
  [in]      const DWORD        *pAdjacencyIn,
  [in, out]       DWORD        *pAdjacencyOut,
  [in, out]       DWORD        *pFaceRemap,
  [out]           LPD3DXBUFFER *ppVertexRemap,
  [out]           LPD3DXMESH   *ppOptMesh
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Spécifie le type d’optimisation à effectuer. Ce paramètre peut être défini sur une combinaison d’un ou plusieurs indicateurs de [**D3DXMESHOPT**](./d3dxmeshopt.md) et [**D3DXMESH**](./d3dxmesh.md) (à l’exception de D3DXMESH \_ 32 bits, D3DXMESH \_ IB \_ WriteOnly et D3DXMESH \_ WRITEONLY).

</dd> <dt>

*pAdjacencyIn* \[ dans\]
</dt> <dd>

Type : **const [**DWORD**](../winprog/windows-data-types.md) \***

Pointeur vers un tableau de trois DWORD par visage qui spécifie les trois voisins pour chaque visage dans le maillage source. Si le bord n’a pas de faces adjacentes, la valeur est 0xFFFFFFFF. Consultez la section Notes.

</dd> <dt>

*pAdjacencyOut* \[ in, out\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Pointeur vers un tableau de trois DWORD par visage qui spécifie les trois voisins pour chaque visage dans le maillage optimisé. Si le bord n’a pas de faces adjacentes, la valeur est 0xFFFFFFFF.

</dd> <dt>

*pFaceRemap* \[ in, out\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Tableau de DWORDs, un par visage, qui identifie la face d’origine du maillage qui correspond à chaque visage dans le maillage optimisé. Si la valeur fournie pour cet argument est **null**, les données de remappage de visage ne sont pas retournées.

</dd> <dt>

*ppVertexRemap* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) , qui contient une valeur DWORD pour chaque vertex qui spécifie la façon dont les nouveaux vertex sont mappés aux anciens vertex. Ce remappage est utile si vous devez modifier des données externes en fonction du nouveau mappage de vertex.

</dd> <dt>

*ppOptMesh* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***

Adresse d’un pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) , représentant la maille optimisée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Cette méthode génère un nouveau maillage. Avant d’exécuter Optimize, une application doit générer une mémoire tampon de contiguïté en appelant [**ID3DXBaseMesh :: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md). La mémoire tampon d’adjacence contient des données d’contiguïté, telles qu’une liste de bords et les faces adjacentes les unes aux autres.

Cette méthode est très similaire à la méthode [**ID3DXBaseMesh :: CloneMesh**](id3dxbasemesh--clonemesh.md) , à ceci près qu’elle peut effectuer une optimisation lors de la génération du nouveau clone de la maille. Le maillage de sortie hérite de tous les paramètres de création du maillage d’entrée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh::OptimizeInplace**](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
