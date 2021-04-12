---
description: Définit le type de base d’une surface corrective de poids fort.
ms.assetid: 18c31c77-7ba3-449c-af4a-717b8c1dced1
title: Énumération D3DBASISTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBASISTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 7e166f56aa2625c868d3e2e2223efbb577e05bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116190"
---
# <a name="d3dbasistype-enumeration"></a>Énumération D3DBASISTYPE

Définit le type de base d’une surface corrective de poids fort.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DBASISTYPE { 
  D3DBASIS_BEZIER       = 0,
  D3DBASIS_BSPLINE      = 1,
  D3DBASIS_CATMULL_ROM  = 2,
  D3DBASIS_FORCE_DWORD  = 0x7fffffff
} D3DBASISTYPE, *LPD3DBASISTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DBASIS_BEZIER"></span><span id="d3dbasis_bezier"></span>**D3DBASIS \_ Bézier**
</dt> <dd>

Les vertex d’entrée sont traités comme une série de correctifs de Bézier. Le nombre de vertex spécifié doit être divisible par 4. Les portions de la maille au-delà de ce critère ne seront pas rendues. Une continuité totale est utilisée entre les sous-correctifs à l’intérieur de la surface rendue par chaque appel. Seuls les vertex situés aux angles de chaque sous-correctif sont assurés de se trouver sur la surface résultante.

</dd> <dt>

<span id="D3DBASIS_BSPLINE"></span><span id="d3dbasis_bspline"></span>**D3DBASIS \_ BSPLINE**
</dt> <dd>

Les vertex d’entrée sont traités comme des points de contrôle d’une surface B-spline. Le nombre d’ouvertures rendues est inférieur à deux fois le nombre d’ouvertures dans cette direction. En général, la surface générée ne contient pas les vertex de contrôle spécifiés.

</dd> <dt>

<span id="D3DBASIS_CATMULL_ROM"></span><span id="d3dbasis_catmull_rom"></span>**D3DBASIS \_ CATMULL \_ ROM**
</dt> <dd>

Une base d’interpolation définit la surface afin que la surface passe par tous les vertex d’entrée spécifiés. Dans DirectX 8, il s’agissait de D3DBASIS \_ interpoliser.

</dd> <dt>

<span id="D3DBASIS_FORCE_DWORD"></span><span id="d3dbasis_force_dword"></span>**D3DBASIS \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Notes

Les membres de **D3DBASISTYPE** spécifient la formulation à utiliser lors de l’évaluation de la primitive de surface de patch de poids fort pendant le pavage.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**\_Informations D3DRECTPATCH**](d3drectpatch-info.md)
</dt> <dt>

[**\_Informations D3DTRIPATCH**](d3dtripatch-info.md)
</dt> </dl>

 

 




