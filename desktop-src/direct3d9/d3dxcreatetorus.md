---
description: Utilise un système de coordonnées droitier pour créer une maille contenant un tore.
ms.assetid: 68df7650-8a87-4762-8b57-5704c419b0d7
title: D3DXCreateTorus, fonction (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTorus
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 384950ca1f00d0115135cf9ae36a2883ec5470e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211768"
---
# <a name="d3dxcreatetorus-function"></a>D3DXCreateTorus fonction)

Utilise un système de coordonnées droitier pour créer une maille contenant un tore.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXCreateTorus(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             InnerRadius,
  _In_  FLOAT             OuterRadius,
  _In_  UINT              Sides,
  _In_  UINT              Rings,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil associé au maillage de tores créé.

</dd> <dt>

*InnerRadius* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Rayon interne du tore. La valeur doit être supérieure ou égale à 0.0 f.

</dd> <dt>

*OuterRadius* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Rayon externe du tore. La valeur doit être supérieure ou égale à 0.0 f.

</dd> <dt>

*Côtés* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de côtés dans une section croisée. La valeur doit être supérieure ou égale à 3.

</dd> <dt>

*Anneaux* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre d’anneaux composant le tore. La valeur doit être supérieure ou égale à 3.

</dd> <dt>

*ppMesh* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***

Adresse d’un pointeur vers la forme de sortie, une interface [**ID3DXMesh**](id3dxmesh.md) .

</dd> <dt>

*ppAdjacency* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) . Quand la méthode est retournée, ce paramètre est rempli avec un tableau de trois DWORDs par visage qui spécifient les trois voisins pour chaque visage de la maille. La **valeur null** peut être spécifiée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Le tore créé est centré au niveau de l’origine et son axe est aligné avec l’axe z. Le rayon interne du tore est le rayon de la coupe croisée (rayon mineur), et le rayon externe du tore est le rayon du trou central.

Cette fonction retourne un maillage qui peut être utilisé ultérieurement pour le dessin ou la manipulation par l’application.

Cette fonction crée une maille avec l' \_ option de création managée D3DXMESH et [D3DFVF \_ xyz \| D3DFVF \_ ](d3dfvf.md) le format de vertex flexible normal.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9shape. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de dessin de forme](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
