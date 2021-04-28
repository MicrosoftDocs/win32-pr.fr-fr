---
description: 'Fonction D3DXSHEvalDirection (D3dx9math. h) : évalue les fonctions de base de l’harmonique sphérique (SH) à partir d’un vecteur de direction d’entrée.'
ms.assetid: f30ba32c-d6b0-4e4e-b5cd-839ed7821855
title: D3DXSHEvalDirection, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalDirection
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e02f0f3d8770b4b703f275de3225eacb301a7843
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093959"
---
# <a name="d3dxshevaldirection-function-d3dx9mathh"></a>D3DXSHEvalDirection, fonction (D3dx9math. h)

Évalue les fonctions de base de l’harmonique sphérique (SH) à partir d’un vecteur de direction d’entrée.

## <a name="syntax"></a>Syntaxe


```C++
FLOAT* D3DXSHEvalDirection(
  _Out_       FLOAT       *pOut,
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pDir
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ à\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Pointeur vers les coefficients de sortie de l’harmonique sphérique (SH). L’évaluation génère des coefficients de commande ². Consultez la section Notes.

</dd> <dt>

*Commande* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Ordre de l’évaluation SH. La valeur doit être comprise entre [D3DXSH \_ MINORDER](other-d3dx-constants.md) et D3DXSH \_ MAXORDER, inclus. L’évaluation génère des coefficients de commande ². Le degré de l’évaluation est Order-1.

</dd> <dt>

*pDir* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

(x, y, z) vecteur de direction dans lequel évaluer les fonctions de base SH. Doit être normalisé. Consultez la section Notes.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **float**](../winprog/windows-data-types.md)\***

Pointeur vers les coefficients de sortie SH. Consultez la section Notes.

## <a name="remarks"></a>Notes 

Chaque coefficient de la fonction de base YLM est stocké à l’emplacement de mémoire l ² + m + l, où :

-   l est le degré de la fonction de base.
-   m est l’index de fonction de base pour la valeur l donnée et est compris entre-l et l, inclus.

Sur la sphère avec rayon d’unité, comme indiqué dans l’illustration suivante, la direction peut être spécifiée simplement avec thêta, l’angle autour de l’axe z dans la [direction de droite](coordinate-systems.md), et Phi, l’angle de z.

![illustration d’une sphère avec rayon unitaire](images/spherical-coordinates.png)

Les équations suivantes montrent la relation entre les coordonnées cartésiennes (x, y, z) et sphériques (thêta, Phi) sur la sphère d’unité. Le thêta angulaire varie d’une plage de 0 à 2 pi, tandis que la valeur de Phi varie de 0 à pi.

![équations de la relation entre les coordonnées cartésiennes et sphériques](images/spherical-coordinates-equations.png)

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

 

 
