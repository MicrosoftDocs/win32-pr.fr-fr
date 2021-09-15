---
description: Crée un objet ID3DXPRTEngine capable de générer efficacement des simulations de transfert de luminance précalculées (PRT) d’une scène 3D.
ms.assetid: fdfe02b5-03fb-4bee-a53b-012ae3572644
title: D3DXCreatePRTEngine, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTEngine
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b76b58953de81041922659c3315bba9cdf7788b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296555"
---
# <a name="d3dxcreateprtengine-function"></a>D3DXCreatePRTEngine fonction)

Crée un objet [**ID3DXPRTEngine**](id3dxprtengine.md) capable de générer efficacement des simulations de transfert de luminance précalculées (PRT) d’une scène 3D.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXCreatePRTEngine(
  _In_    LPD3DXMESH      pMesh,
  _In_    DWORD           *pAdjacency,
  _In_    BOOL            ExtractUVs,
  _In_    LPD3DXMESH      pBlockerMesh,
  _Inout_ LPD3DXPRTENGINE ppEngine
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMesh* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)**

Pointeur vers un objet de maillage [**ID3DXMesh**](id3dxmesh.md) d’entrée qui modélise la scène 3D. Ce maillage doit avoir une table d’attributs dans laquelle les vertex sont dans un attribut unique.

</dd> <dt>

*pAdjacency* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Pointeur facultatif vers un tableau de trois DWORDs par visage à remplir avec des indices de face adjacente. Le nombre d’octets dans ce tableau doit être au moins égal à ((3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof (DWORD)). Peut avoir la **valeur null**.

</dd> <dt>

*ExtractUVs* \[ dans\]
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)**

Si la **valeur est true**, les textures sont utilisées pour stocker les vecteurs ALBEDOS ou PRT.

</dd> <dt>

*pBlockerMesh* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)**

Pointeur vers un objet de maillage [**ID3DXMesh**](id3dxmesh.md) facultatif qui bloque la scène 3D. Peut avoir la **valeur null**.

</dd> <dt>

*ppEngine* \[ in, out\]
</dt> <dd>

Type : **[ **LPD3DXPRTENGINE**](id3dxprtengine.md)**

Pointeur vers un objet [**ID3DXPRTEngine**](id3dxprtengine.md) de sortie.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Utilisez [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) pour combiner plusieurs mailles en une seule interface de maillage.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de transfert luminance précalculées](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
