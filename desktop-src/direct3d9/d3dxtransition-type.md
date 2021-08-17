---
description: Définit le style de transition entre les valeurs d’une animation de maillage.
ms.assetid: 4416ef28-ba6b-47ca-be7d-831daad619e5
title: Énumération D3DXTRANSITION_TYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTRANSITION_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: f451b94fe204a82cd15c65e424cc214025aa670f82af5224897100cbc6f8f6e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730936"
---
# <a name="d3dxtransition_type-enumeration"></a>\_Énumération de type D3DXTRANSITION

Définit le style de transition entre les valeurs d’une animation de maillage.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DXTRANSITION_TYPE { 
  D3DXTRANSITION_LINEAR         = 0x000,
  D3DXTRANSITION_EASEINEASEOUT  = 0x001,
  D3DXTRANSITION_FORCE_DWORD    = 0x7fffffff
} D3DXTRANSITION_TYPE, *LPD3DXTRANSITION_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXTRANSITION_LINEAR"></span><span id="d3dxtransition_linear"></span>**D3DXTRANSITION \_ linéaire**
</dt> <dd>

Transition linéaire entre les valeurs.

</dd> <dt>

<span id="D3DXTRANSITION_EASEINEASEOUT"></span><span id="d3dxtransition_easeineaseout"></span>**D3DXTRANSITION \_ EASEINEASEOUT**
</dt> <dd>

Transition de spline facile et simplifiée entre les valeurs.

</dd> <dt>

<span id="D3DXTRANSITION_FORCE_DWORD"></span><span id="d3dxtransition_force_dword"></span>**D3DXTRANSITION \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Remarques

Le calcul de la rampe de l’accélération de la facilité d’atténuation est calculé comme suit :

<dl> Q (t) = 2 (x-y) t ³ + 3 (y-x) t ² + x  
</dl>

où la rampe est une fonction Q (t) avec les propriétés suivantes :

-   Q (t) est une spline cubique.
-   Q (t) interpole entre x et y en tant que t compris entre 0 et 1.
-   Q (t) est horizontal quand t = 0 et t = 1.

Mathématiquement, cela se traduit par :

<dl> Q (t) = à ³ + BT ² + CT + D (et par conséquent, Q' (t) = 3At ² + 2Bt + C)  
2a) Q (0) = x  
2b) Q (1) = y  
3A) Q' (0) = 0  
3b) Q' (1) = 0  
</dl>

Résolution pour A, B, C, D :

<dl> D = x (à partir de 2a)  
C = 0 (à partir de 3A)  
3A + 2B = 0 (à partir de 3b)  
A + B = y-x (à partir de 2b et D = x)  
</dl>

Par conséquent :

<dl> A = 2 (x-y), B = 3 (y-x), C = 0, D = x  
</dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




