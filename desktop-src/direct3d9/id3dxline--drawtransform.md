---
description: Dessine une bande de courbes dans l’espace à l’écran avec une matrice de transformation d’entrée spécifiée.
ms.assetid: 869dc705-8162-4cd9-ac6a-c0ce32f430c3
title: ID3DXLine ::D méthode rawTransform (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.DrawTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8a8f5f910f3513676132b00d4f8338744c14238872eaba305cbf4ca6b0b02ebd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095900"
---
# <a name="id3dxlinedrawtransform-method"></a>ID3DXLine ::D méthode rawTransform

Dessine une bande de courbes dans l’espace à l’écran avec une matrice de transformation d’entrée spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DrawTransform(
  [in] const D3DXVECTOR3 *pVertexList,
  [in]       DWORD       dwVertexListCount,
  [in] const D3DXMATRIX  *pTransform,
  [in]       D3DCOLOR    Color
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pVertexList* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Tableau des vertex qui composent la ligne. Consultez [**D3DXVECTOR3**](d3dxvector3.md).

</dd> <dt>

*dwVertexListCount* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Nombre de vertex dans la liste de vertex.

</dd> <dt>

*pTransform* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Matrice de mise à l’échelle, de rotation et de translation (SRT) pour la transformation des points. Consultez [**D3DXMATRIX**](d3dxmatrix.md). Si cette matrice est une matrice de projection, toutes les lignes stippled sont dessinées avec un modèle de stippling de perspective. Ou bien, vous pouvez transformer les vertex et utiliser [**ID3DXLine ::D RAW**](id3dxline--draw.md) pour dessiner la ligne avec un modèle de stipple de type non-perspective-correct.

</dd> <dt>

*Couleur* \[ dans\]
</dt> <dd>

Type : **[ **D3DCOLOR**](d3dcolor.md)**

Couleur de la ligne. Consultez [**D3DCOLOR**](d3dcolor.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
