---
description: Évalue une lumière sphérique et retourne des données de l’harmonique sphérique spectral (SH).
ms.assetid: aa46c162-9c2d-49c0-925c-d0c06456f918
title: D3DXSHEvalSphericalLight, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalSphericalLight
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8581b4284e270b6df587be1a71fcf11f29c843d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322825"
---
# <a name="d3dxshevalsphericallight-function-d3dx9mathh"></a>D3DXSHEvalSphericalLight, fonction (D3dx9math. h)

Évalue une lumière sphérique et retourne des données de l’harmonique sphérique spectral (SH).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXSHEvalSphericalLight(
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pPos,
  _In_        FLOAT       Radius,
  _In_        FLOAT       RIntensity,
  _In_        FLOAT       GIntensity,
  _In_        FLOAT       BIntensity,
  _Out_       FLOAT       *pROut,
  _Out_       FLOAT       *pGOut,
  _Out_       FLOAT       *pBOut
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Commande* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Ordre de l’évaluation SH. La valeur doit être comprise entre [D3DXSH \_ MINORDER](other-d3dx-constants.md) et D3DXSH \_ MAXORDER, inclus. L’évaluation génère des coefficients de commande ². Le degré de l’évaluation est Order-1.

</dd> <dt>

*pPos* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers la position de la lumière.

</dd> <dt>

*Rayon* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Rayon de la source de lumière sphérique.

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

*pROut* \[ à\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Pointeur vers le vecteur de sortie SH pour le composant rouge.

</dd> <dt>

*pGOut* \[ à\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Pointeur vers le vecteur de sortie SH pour le composant vert.

</dd> <dt>

*pBOut* \[ à\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Pointeur vers le vecteur de sortie SH pour le composant bleu.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être : D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Notes

Évalue une lumière sphérique et retourne des données SH spectrales. Il n’y a aucune normalisation de l’intensité de la lumière comme c’est le cas pour les [lumières directionnelles](light-types.md). vous devez donc veiller à spécifier les inintensités. Cela permet de calculer trois échantillons spectraux. *pROut* est retourné, tandis que *pGOut* et *pBOut* peuvent être retournés.

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

 

 
