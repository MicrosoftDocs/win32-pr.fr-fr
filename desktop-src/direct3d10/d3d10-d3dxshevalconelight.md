---
description: D3DXSHEvalConeLight fonction (D3DX10. h)-évalue une lumière qui est un cône d’intensité constante et retourne des données de l’harmonique sphérique spectral (SH).
ms.assetid: ad2b9c86-cf1a-426e-88e6-4c543519e002
title: D3DXSHEvalConeLight, fonction (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalConeLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fc11e7bab4cbbd6c8a685b289d4bde476cd465ca
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108607"
---
# <a name="d3dxshevalconelight-function-d3dx10h"></a>D3DXSHEvalConeLight, fonction (D3DX10. h)

Évalue une lumière qui est un cône d’intensité constante et retourne des données d’harmonique sphérique spectral (SH).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXSHEvalConeLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       FLOAT       Radius,
  _In_       FLOAT       RIntensity,
  _In_       FLOAT       GIntensity,
  _In_       FLOAT       BIntensity,
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

Ordre de l’évaluation SH. La valeur doit être comprise entre D3DXSH \_ MINORDER et D3DXSH \_ MAXORDER, inclus. L’évaluation génère des coefficients de commande ². Le degré de l’évaluation est Order-1.

</dd> <dt>

*pDir* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Pointeur vers le vecteur de direction de l’axe (x, y, z) de l’hémisphère dans lequel évaluer les fonctions de base SH. Consultez la section Notes.

</dd> <dt>

*Rayon* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Rayon du cône en radians.

</dd> <dt>

*RIntensity* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Intensité rouge de la lumière.

</dd> <dt>

*GIntensity* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Intensité verte de la lumière.

</dd> <dt>

*BIntensity* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Intensité bleue de la lumière.

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

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être : D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Notes 

Évalue une lumière qui est un cône d’intensité constante et retourne des données SH spectrales. Le vecteur de sortie est calculé de sorte que si le rapport d’intensité R/G/B est égal à 1, le luminance de sortie d’un point situé directement sous la lumière (orienté dans la direction du cône sur un objet diffus avec un albedo de 1) est 1,0. Cela permet de calculer trois échantillons spectraux. pROut est retourné, tandis que pGOut et pBOut peuvent être retournés.

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

 

 
