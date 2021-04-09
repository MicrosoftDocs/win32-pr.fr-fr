---
description: Fait pivoter le vecteur d’harmonique sphérique (SH) dans l’axe z selon l’angle donné.
ms.assetid: 7c4bec55-4a4c-4f7e-8849-1cac373a2340
title: D3DXSHRotateZ, fonction (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHRotateZ
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0348dd8dfed9b100f64c53427ca2b77dd48ccded
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953926"
---
# <a name="d3dxshrotatez-function-d3dx10h"></a>D3DXSHRotateZ, fonction (D3DX10. h)

Fait pivoter le vecteur d’harmonique sphérique (SH) dans l’axe z selon l’angle donné.

## <a name="syntax"></a>Syntaxe


```C++
FLOAT* D3DXSHRotateZ(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_       FLOAT Angle,
  _In_ const FLOAT *pIn
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Pointeur vers les coefficients de sortie de l’harmonique sphérique (SH). L’évaluation génère des coefficients de commande ². Ce pointeur ne doit pas être un alias avec pIn. Consultez la section Notes.

</dd> <dt>

*Commande* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Ordre de l’évaluation SH. La valeur doit être comprise entre D3DXSH \_ MINORDER et D3DXSH \_ MAXORDER, inclus. L’évaluation génère des coefficients de commande ². Le degré de l’évaluation est Order-1.

</dd> <dt>

*Angle* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Angle de rotation en radians. La rotation est effectuée autour de l’axe z.

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
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
