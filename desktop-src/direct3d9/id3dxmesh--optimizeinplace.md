---
description: Génère un maillage avec des faces et des sommets réorganisés pour optimiser les performances du dessin. Cette méthode réorganise la maille existante.
ms.assetid: 2cdaf627-d1d3-44f0-a5ae-9023d4b0de45
title: 'ID3DXMesh :: OptimizeInplace, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.OptimizeInplace
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0075e7a0b823f0d747859a4717a440e0c244fde76076e4b285c7d1b2a7e78d00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120803"
---
# <a name="id3dxmeshoptimizeinplace-method"></a>ID3DXMesh :: OptimizeInplace, méthode

Génère un maillage avec des faces et des sommets réorganisés pour optimiser les performances du dessin. Cette méthode réorganise la maille existante.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT OptimizeInplace(
  [in]        DWORD        Flags,
  [in]  const DWORD        *pAdjacencyIn,
  [out]       DWORD        *pAdjacencyOut,
  [out]       DWORD        *pFaceRemap,
  [out]       LPD3DXBUFFER *ppVertexRemap
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Indicateurs* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Combinaison d’un ou plusieurs indicateurs [**D3DXMESHOPT**](./d3dxmeshopt.md) , en spécifiant le type d’optimisation à effectuer.

</dd> <dt>

*pAdjacencyIn* \[ dans\]
</dt> <dd>

Type : **const [**DWORD**](../winprog/windows-data-types.md) \***

Pointeur vers un tableau de trois DWORD par visage qui spécifie les trois voisins pour chaque visage dans le maillage source. Si le bord n’a pas de faces adjacentes, la valeur est 0xFFFFFFFF.

</dd> <dt>

*pAdjacencyOut* \[ à\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Pointeur vers un tableau de trois DWORD par visage qui spécifie les trois voisins pour chaque visage dans le maillage optimisé. Si le bord n’a pas de faces adjacentes, la valeur est 0xFFFFFFFF. Si la valeur fournie pour cet argument est **null**, les données d’contiguïté ne sont pas retournées.

</dd> <dt>

*pFaceRemap* \[ à\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Tableau de DWORDs, un par visage, qui identifie la face d’origine du maillage qui correspond à chaque visage dans le maillage optimisé. Si la valeur fournie pour cet argument est **null**, les données de remappage de visage ne sont pas retournées.

</dd> <dt>

*ppVertexRemap* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) , qui contient une valeur DWORD pour chaque vertex qui spécifie la façon dont les nouveaux vertex sont mappés aux anciens vertex. Ce remappage est utile si vous devez modifier des données externes en fonction du nouveau mappage de vertex. Si la valeur fournie pour cet argument est **null**, les données de remappage de vertex ne sont pas retournées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ CANNOTATTRSORT, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

Avant d’exécuter **ID3DXMesh :: OptimizeInplace**, une application doit générer une mémoire tampon de contiguïté en appelant [**ID3DXBaseMesh :: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md). La mémoire tampon d’adjacence contient des données d’contiguïté, telles qu’une liste de bords et les faces adjacentes les unes aux autres.

> [!Note]  
> Cette méthode échoue si le maillage partage sa mémoire tampon de vertex avec un autre maillage, sauf si le \_ IGNOREVERTS D3DXMESHOPT est défini dans Flags.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh :: Optimize**](id3dxmesh--optimize.md)
</dt> </dl>

 

 
