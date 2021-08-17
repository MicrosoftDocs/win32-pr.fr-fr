---
description: Tessellates un carreau de surface d’ordre supérieur triangulaire dans un maillage de triangles.
ms.assetid: bcc9143f-fec0-491a-8d32-1df961b8dade
title: D3DXTessellateTriPatch, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateTriPatch
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1cae3ff9709cb74e15c176abc0e738e4f12d1417eec1d040b90269b7e3cbc6c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122711"
---
# <a name="d3dxtessellatetripatch-function"></a>D3DXTessellateTriPatch fonction)

Tessellates un carreau de surface d’ordre supérieur triangulaire dans un maillage de triangles.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXTessellateTriPatch(
  _In_          LPDIRECT3DVERTEXBUFFER9 pVB,
  _In_    const FLOAT                   *pNumSegs,
  _In_    const D3DVERTEXELEMENT9       *pInDecl,
  _In_    const D3TRIPATCH_INFO         *pTriPatchInfo,
  _Inout_       LPD3DXMESH              pMesh
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pVB* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**

Mémoire tampon de vertex contenant les données de correctif.

</dd> <dt>

*pNumSegs* \[ dans\]
</dt> <dd>

Type : **const [**float**](../winprog/windows-data-types.md) \***

Pointeur vers un tableau de trois valeurs à virgule flottante qui identifient le nombre de segments dans lequel chaque bord du correctif triangulaire doit être divisé lorsqu’il est fractionné. Consultez [**D3DTRIPATCH \_ info**](d3dtripatch-info.md).

</dd> <dt>

*pInDecl* \[ dans\]
</dt> <dd>

Type : **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Structure de déclaration de vertex qui définit les données de vertex. Consultez [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

</dd> <dt>

*pTriPatchInfo* \[ dans\]
</dt> <dd>

Type : **const [**D3TRIPATCH \_ info**](d3dtripatch-info.md) \***

Décrit un correctif triangulaire. Consultez [**D3DTRIPATCH \_ info**](d3dtripatch-info.md).

</dd> <dt>

*pMesh* \[ in, out\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)**

Pointeur vers le maillage créé. Consultez [**ID3DXMesh**](id3dxmesh.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

Utilisez [**D3DXTriPatchSize**](d3dxtripatchsize.md) pour connaître le nombre de vertex et d’index de sortie dont la fonction de pavage a besoin.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXTessellateRectPatch**](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
