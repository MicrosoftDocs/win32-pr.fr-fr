---
description: Fonction D3DXSHEvalHemisphereLight (D3DX10. h)-évalue une lumière qui est une interpolation linéaire entre deux couleurs sur la sphère.
ms.assetid: 7523ff42-c81d-4857-a50d-7efa213214b8
title: D3DXSHEvalHemisphereLight, fonction (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalHemisphereLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e32221167e2a736e46b847c88300221c3bd8b1675973604703600bb8e36549a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497909"
---
# <a name="d3dxshevalhemispherelight-function-d3dx10h"></a>D3DXSHEvalHemisphereLight, fonction (D3DX10. h)

Évalue une lumière qui est une interpolation linéaire entre deux couleurs sur la sphère.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXSHEvalHemisphereLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       D3DXCOLOR   Top,
  _In_       D3DXCOLOR   Bottom,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Commande* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Ordre de l’évaluation de l’harmonique sphérique (SH). La valeur doit être comprise entre D3DXSH \_ MINORDER et D3DXSH \_ MAXORDER, inclus. L’évaluation génère des coefficients de commande ². Le degré de l’évaluation est Order-1.

</dd> <dt>

*pDir* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Pointeur vers le vecteur de direction de l’axe (x, y, z) de l’hémisphère dans lequel évaluer les fonctions de base SH. Consultez la section Notes.

</dd> <dt>

En *haut* \[ dans\]
</dt> <dd>

Type : **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**

Couleur du ciel.

</dd> <dt>

En *bas* \[ dans\]
</dt> <dd>

Type : **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**

Couleur de fond.

</dd> <dt>

*pROut* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Pointeur vers le vecteur de sortie SH pour le composant rouge.

</dd> <dt>

*pGOut* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Pointeur vers le vecteur de sortie SH pour le composant vert.

</dd> <dt>

*pBOut* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Pointeur vers le vecteur de sortie SH pour le composant bleu.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être : D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Remarques

L’interpolation est effectuée de façon linéaire entre les deux points, et non pas sur la surface de la sphère (autrement dit, si l’axe était (0, 0, 1) elle est linéaire en Z, et non pas dans l’angle de l’azimut). La fonction d’éclairage sphérique qui en résulte est normalisée, de sorte qu’un point sur une surface parfaitement diffuse sans occultation et un point perpendiculaire dans la direction pDir entraînerait la sortie de luminance avec une valeur de 1 (si la couleur supérieure était blanche et la couleur inférieure était noire). Il s’agit d’un modèle très simple où Top représente l’intensité de « Sky » et Bottom représente l’intensité du « Ground ».

Sur la sphère avec rayon d’unité, comme indiqué dans l’illustration suivante, la direction peut être spécifiée simplement avec thêta, l’angle autour de l’axe z dans la direction de droite, et Phi, l’angle de z.

![illustration d’une sphère avec rayon unitaire](images/spherical-coordinates.png)

Les équations suivantes montrent la relation entre les coordonnées cartésiennes (x, y, z) et sphériques (thêta, Phi) sur la sphère d’unité. Le thêta angulaire varie d’une plage de 0 à 2 pi, tandis que la valeur de Phi varie de 0 à pi.

![équations de la relation entre les coordonnées cartésiennes et sphériques](images/spherical-coordinates-equations.png)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
