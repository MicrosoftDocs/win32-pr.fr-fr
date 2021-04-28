---
description: 'Fonction D3DXSHAdd (D3dx9math. h) : ajoute deux vecteurs d’harmoniques sphériques (SH). en d’autres termes, moue \[ i \] = PA \[ i \] + PB \[ i \] .'
ms.assetid: 12775c90-ed9d-4931-a449-2571816dd079
title: D3DXSHAdd, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHAdd
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7333d1803b9f7ea7b056ff78ffd053bd6086184b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117957"
---
# <a name="d3dxshadd-function-d3dx9mathh"></a>D3DXSHAdd, fonction (D3dx9math. h)

Ajoute deux vecteurs d’harmoniques sphériques (SH). en d’autres termes, moue \[ i \] = PA \[ i \] + PB \[ i \] .

## <a name="syntax"></a>Syntaxe


```C++
FLOAT* D3DXSHAdd(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_  const FLOAT *pA,
  _In_  const FLOAT *pB
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ à\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Pointeur vers les coefficients de sortie SH. L’évaluation génère des coefficients de commande ². Consultez la section Notes.

</dd> <dt>

*Commande* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Ordre de l’évaluation SH. La valeur doit être comprise entre [D3DXSH \_ MINORDER](other-d3dx-constants.md) et D3DXSH \_ MAXORDER, inclus. L’évaluation génère des coefficients de commande ². Le degré de l’évaluation est Order-1.

</dd> <dt>

*PA* \[ dans\]
</dt> <dd>

Type : **const [**float**](../winprog/windows-data-types.md) \***

Pointeur vers le premier vecteur SH.

</dd> <dt>

*PB* \[ dans\]
</dt> <dd>

Type : **const [**float**](../winprog/windows-data-types.md) \***

Pointeur vers le deuxième vecteur SH.

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

 

 
