---
description: Prend une maille et retourne un nouveau maillage avec des poids de fusion par vertex, des index et une table de combinaisons de segments. Le tableau décrit les palettes osseuses qui affectent les sous-ensembles de la maille.
ms.assetid: e4758a3b-8a45-4ed3-aa62-9713d12afc56
title: 'ID3DXSkinInfo :: ConvertToIndexedBlendedMesh, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.ConvertToIndexedBlendedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 87c8a4b943a647e52d7260f1ff53b32b40756761
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918275"
---
# <a name="id3dxskininfoconverttoindexedblendedmesh-method"></a>ID3DXSkinInfo :: ConvertToIndexedBlendedMesh, méthode

Prend une maille et retourne un nouveau maillage avec des poids de fusion par vertex, des index et une table de combinaisons de segments. Le tableau décrit les palettes osseuses qui affectent les sous-ensembles de la maille.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ConvertToIndexedBlendedMesh(
  [in]        LPD3DXMESH   pMesh,
  [in]        DWORD        Options,
  [in]        DWORD        paletteSize,
  [in]  const DWORD        *pAdjacencyIn,
  [in]        LPDWORD      pAdjacencyOut,
  [out]       DWORD        *pFaceRemap,
  [out]       LPD3DXBUFFER *ppVertexRemap,
  [out]       DWORD        *pMaxVertexInfl,
  [out]       DWORD        *pNumBoneCombinations,
  [out]       LPD3DXBUFFER *ppBoneCombinationTable,
  [out]       LPD3DXMESH   *ppMesh
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMesh* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)**

Maillage d’entrée. Consultez [**ID3DXMesh**](id3dxmesh.md).

</dd> <dt>

*Options* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Actuellement inutilisé.

</dd> <dt>

*paletteSize* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Nombre de matrices osseuses disponibles pour le dépouillement de palette de matrice.

</dd> <dt>

*pAdjacencyIn* \[ dans\]
</dt> <dd>

Type : **const [**DWORD**](../winprog/windows-data-types.md) \***

Informations d’adjacence de maillage d’entrée.

</dd> <dt>

*pAdjacencyOut* \[ dans\]
</dt> <dd>

Type : **[ **LPDWORD**](../winprog/windows-data-types.md)**

Informations d’adjacence de maillage de sortie.

</dd> <dt>

*pFaceRemap* \[ à\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Tableau de DWORDs, un par visage, qui identifie la facette d’origine qui correspond à chaque visage dans le maillage fusionné. Si la valeur fournie pour cet argument est **null**, les données de remappage de visage ne sont pas retournées.

</dd> <dt>

*ppVertexRemap* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) , qui contient une valeur DWORD pour chaque vertex qui spécifie la façon dont les nouveaux vertex sont mappés aux anciens vertex. Ce remappage est utile si vous devez modifier des données externes en fonction du nouveau mappage de vertex. Ce paramètre est facultatif. La **valeur null** peut être utilisée.

</dd> <dt>

*pMaxVertexInfl* \[ à\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Pointeur vers une valeur DWORD qui contient le nombre maximal d’influences osseuses requises par vertex pour cette méthode d’habillage.

</dd> <dt>

*pNumBoneCombinations* \[ à\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Pointeur vers le nombre d’os dans le tableau de combinaisons de segments.

</dd> <dt>

*ppBoneCombinationTable* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Pointeur vers la table de combinaisons de segments. Les données sont organisées dans une structure [**D3DXBONECOMBINATION**](d3dxbonecombination.md) .

</dd> <dt>

*ppMesh* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***

Pointeur vers le nouveau maillage.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Notes

Chaque élément dans les tableaux de remappage spécifie l’index précédent pour cette position. Par exemple, si un vertex était à la position 3 mais a été remappé à la position 5, le cinquième élément de pVertexRemap contiendra 3.

Cette méthode ne s’exécute pas sur un matériel qui ne prend pas en charge la fusion de vertex à fonction fixe.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
