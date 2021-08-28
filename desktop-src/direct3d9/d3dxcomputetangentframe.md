---
description: Vecteurs de calcul tangent, Binormal et normal pour une maille.
ms.assetid: 54edb9a5-440d-4191-a58f-296e5b804e0c
title: D3DXComputeTangentFrame, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangentFrame
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 532b265f387179d88581f6f0a05227162de6a8402e324e7be2e13a16ca4a3ed1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849829"
---
# <a name="d3dxcomputetangentframe-function"></a>D3DXComputeTangentFrame fonction)

Vecteurs de calcul tangent, Binormal et normal pour une maille.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXComputeTangentFrame(
  _In_ ID3DXMesh *pMesh,
  _In_ DWORD     dwOptions
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMesh* \[ dans\]
</dt> <dd>

Type : **[ **ID3DXMesh**](id3dxmesh.md)\***

Pointeur vers un objet de maillage [**ID3DXMesh**](id3dxmesh.md) d’entrée.

</dd> <dt>

*dwOptions* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Combinaison d’un ou plusieurs indicateurs [**D3DXTANGENT**](./d3dxtangent.md) .

Utilisez la **valeur null** pour spécifier les options suivantes :

-   Pondérez la longueur du vecteur normal par l’angle, en radians, sous-tendus par les deux bords quittant le sommet.
-   Calculez les coordonnées Cartésienles orthogonales à partir des coordonnées de texture UV.
-   Les textures ne sont pas encapsulées dans les directions U ou V
-   Les dérivés partiels en ce qui concerne les coordonnées de texture sont normalisés.
-   Les vertex sont triés dans le sens inverse des aiguilles d’une passe autour de chaque triangle.
-   Utilisez des vecteurs normaux par vertex déjà présents dans le maillage d’entrée.
-   Les résultats seront stockés dans le maillage d’entrée d’origine. La fonction échoue si de nouveaux vertex doivent être créés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est S \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

Cette fonction appelle simplement [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) avec les paramètres d’entrée suivants :


```
D3DXComputeTangentFrameEx(pMesh, D3DDECLUSAGE_TEXCOORD, 0,   
      D3DDECLUSAGE_BINORMAL, 0, D3DDECLUSAGE_TANGENT, 0, 
      D3DDECLUSAGE_NORMAL, 0, 
      dwOptions | D3DXTANGENT_GENERATE_IN_PLACE,
      NULL, 0.01f, 0.25f, 0.01f, NULL, NULL);
```



Les singularités sont gérées en fonction des besoins en regroupant les bords et en fractionnant les vertex. Si des vertex doivent être fractionnés, la fonction échoue. Le vecteur normal calculé à chaque vertex est toujours normalisé pour avoir une longueur d’unité.

La solution la plus robuste pour calculer les coordonnées Cartésienles orthogonales consiste à ne pas définir les indicateurs D3DXTANGENT \_ \_ de manière orthogonale à partir de \_ vous et D3DXTANGENT \_ à orthogonaliser \_ à partir de \_ V, afin que les coordonnées orthogonales soient calculées à partir des coordonnées de la texture UV. Toutefois, dans ce cas, si U ou V est égal à zéro, la fonction calcule les coordonnées orthogonales à l’aide \_ de D3DXTANGENT orthogonale \_ à partir de \_ V ou \_ de D3DXTANGENT orthogonale \_ à partir de \_ U, respectivement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md)
</dt> <dt>

[**D3DXTANGENT**](./d3dxtangent.md)
</dt> </dl>

 

 
