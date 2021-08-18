---
description: Met à jour les informations d’influence osseuse pour qu’elles correspondent aux sommets après leur réorganisation. Cette méthode doit être appelée si la mémoire tampon de vertex cible a été réorganisée en externe.
ms.assetid: bff5229f-e547-4ab3-84c6-58b15a7825e9
title: 'ID3DXSkinInfo :: remapper, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.Remap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 941a71539184b7d49e35627c932da77b4494486c35506b1b4e5f69ad52c40829
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727779"
---
# <a name="id3dxskininforemap-method"></a>ID3DXSkinInfo :: remapper, méthode

Met à jour les informations d’influence osseuse pour qu’elles correspondent aux sommets après leur réorganisation. Cette méthode doit être appelée si la mémoire tampon de vertex cible a été réorganisée en externe.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Remap(
  [in] DWORD NumVertices,
  [in] DWORD *pVertexRemap
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*NumVertices* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Nombre de vertex à remapper.

</dd> <dt>

*pVertexRemap* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Tableau de DWORDs dont la longueur est spécifiée par NumVertices.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Remarques

Chaque élément dans pVertexRemap spécifie l’index de vertex précédent pour cette position. Par exemple, si un vertex était à la position 3 mais a été remappé à la position 5, le cinquième élément de pVertexRemap doit contenir 3. Le tableau de remappage de vertex retourné par [**ID3DXMesh :: Optimize**](id3dxmesh--optimize.md) peut être utilisé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
