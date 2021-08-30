---
description: Tessellates un carreau rectangulaire de surface d’ordre supérieur dans un maillage de triangle.
ms.assetid: d941d994-8a13-49ff-a0b1-b21a3f84ed78
title: D3DXTessellateRectPatch, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateRectPatch
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b7fb3ab1c47ded6fe6ca6548ca6c90b3027e30280acf819d5d024fd0bd554d58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119049"
---
# <a name="d3dxtessellaterectpatch-function"></a>D3DXTessellateRectPatch fonction)

Tessellates un carreau rectangulaire de surface d’ordre supérieur dans un maillage de triangle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXTessellateRectPatch(
  _In_          LPDIRECT3DVERTEXBUFFER9 pVB,
  _In_    const FLOAT                   *pNumSegs,
  _In_    const D3DVERTEXELEMENT9       *pInDecl,
  _In_    const D3DRECTPATCH_INFO       *pRectPatchInfo,
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

Pointeur vers un tableau de quatre valeurs à virgule flottante qui identifient le nombre de segments dans lequel chaque bord du correctif de rectangle doit être divisé lorsqu’il est fractionné. Consultez [**D3DRECTPATCH \_ info**](d3drectpatch-info.md).

</dd> <dt>

*pInDecl* \[ dans\]
</dt> <dd>

Type : **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Structure de déclaration de vertex qui définit les données de vertex. Consultez [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

</dd> <dt>

*pRectPatchInfo* \[ dans\]
</dt> <dd>

Type : **const [**D3DRECTPATCH \_ info**](d3drectpatch-info.md) \***

Décrit un correctif rectangulaire. Consultez [**D3DRECTPATCH \_ info**](d3drectpatch-info.md).

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

Utilisez [**D3DXRectPatchSize**](d3dxrectpatchsize.md) pour connaître le nombre de vertex et d’index de sortie dont la fonction de pavage a besoin.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXTessellateTriPatch**](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
