---
description: 'D3DXSHScale, fonction (D3dx9math. h) : met à l’échelle un vecteur d’harmonique sphérique (SH). en d’autres termes, moue \[ i \] = PA \[ i \] \* Scale.'
ms.assetid: e7b08b55-e2e7-4f13-bbee-10b844d3ef91
title: D3DXSHScale, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHScale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6a91c3ea1cb49c4c501ab847cb63fe8a39d66665
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093857"
---
# <a name="d3dxshscale-function-d3dx9mathh"></a>D3DXSHScale, fonction (D3dx9math. h)

Met à l’échelle un vecteur d’harmonique sphérique (SH); en d’autres termes, moue \[ i \] = PA \[ i \] \* Scale.

## <a name="syntax"></a>Syntaxe


```C++
FLOAT* D3DXSHScale(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_  const FLOAT *pIn,
  _In_  const FLOAT *Scale
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

*code confidentiel* \[ dans\]
</dt> <dd>

Type : **const [**float**](../winprog/windows-data-types.md) \***

Pointeur vers le vecteur SH à mettre à l’échelle.

</dd> <dt>

Mise à l' *échelle* \[ dans\]
</dt> <dd>

Type : **const [**float**](../winprog/windows-data-types.md) \***

Pointeur désignant la valeur de l’échelle.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

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

 

 
