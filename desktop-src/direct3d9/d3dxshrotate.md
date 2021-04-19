---
description: Fait pivoter le vecteur d’harmonique sphérique (SH) par la matrice donnée.
ms.assetid: 9e319725-6cbb-441e-b996-ec2c6f66e5df
title: D3DXSHRotate, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHRotate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 606ef1909237fd9c0277c5d7112284f6b7018e0e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106524851"
---
# <a name="d3dxshrotate-function-d3dx9mathh"></a>D3DXSHRotate, fonction (D3dx9math. h)

Fait pivoter le vecteur d’harmonique sphérique (SH) par la matrice donnée.

## <a name="syntax"></a>Syntaxe


```C++
FLOAT* D3DXSHRotate(
  _Out_       FLOAT      *pOut,
  _In_        UINT       Order,
  _In_  const D3DXMATRIX *pMatrix,
  _In_  const FLOAT      *pIn
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ à\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Pointeur vers les coefficients de sortie de l’harmonique sphérique (SH). L’évaluation génère des coefficients de commande ². Ce pointeur ne doit pas être un alias avec *pin*. Consultez la section Notes.

</dd> <dt>

*Commande* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Ordre de l’évaluation SH. La valeur doit être comprise entre [D3DXSH \_ MINORDER](other-d3dx-constants.md) et D3DXSH \_ MAXORDER, inclus. L’évaluation génère des coefficients de commande ². Le degré de l’évaluation est Order-1.

</dd> <dt>

*pMatrix* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Pointeur vers la matrice de rotation. La sous-matrice de rotation doit être orthogonale, avec un déterminant d’unité.

</dd> <dt>

*code confidentiel* \[ dans\]
</dt> <dd>

Type : **const [**float**](../winprog/windows-data-types.md) \***

Pointeur vers les coefficients SH pivotés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **float**](../winprog/windows-data-types.md)\***

Pointeur vers les coefficients de sortie SH.

## <a name="remarks"></a>Notes

Chaque coefficient de la fonction de base YLM est stocké à l’emplacement de mémoire l ² + m + l, où :

-   l est le degré de la fonction de base.
-   m est l’index de fonction de base pour la valeur l donnée et est compris entre-l et l, inclus.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[Transfert de luminance précalculé (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
