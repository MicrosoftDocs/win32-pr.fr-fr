---
description: Définit des constantes qui décrivent les modes d’ombrage pris en charge.
ms.assetid: ba4e0c62-b496-427b-a324-2fb560d153ba
title: Énumération D3DSHADEMODE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSHADEMODE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 9950e0074bef7a7b0c211177b3902cd69e2e112c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322793"
---
# <a name="d3dshademode-enumeration"></a>Énumération D3DSHADEMODE

Définit des constantes qui décrivent les modes d’ombrage pris en charge.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DSHADEMODE { 
  D3DSHADE_FLAT         = 1,
  D3DSHADE_GOURAUD      = 2,
  D3DSHADE_PHONG        = 3,
  D3DSHADE_FORCE_DWORD  = 0x7fffffff
} D3DSHADEMODE, *LPD3DSHADEMODE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DSHADE_FLAT"></span><span id="d3dshade_flat"></span>**D3DSHADE \_ plat**
</dt> <dd>

Mode d’ombrage plat. Le composant couleur et spéculaire du premier vertex du triangle est utilisé pour déterminer la couleur et le composant spéculaire du visage. Ces couleurs restent constantes dans le triangle. autrement dit, ils ne sont pas interpolés. L’alpha spéculaire est interpolé. Consultez la section Notes.

</dd> <dt>

<span id="D3DSHADE_GOURAUD"></span><span id="d3dshade_gouraud"></span>**D3DSHADE \_ Gouraud**
</dt> <dd>

Mode d’ombrage Gouraud. Les composants de couleur et spéculaire de la face sont déterminés par une interpolation linéaire entre les trois sommets du triangle.

</dd> <dt>

<span id="D3DSHADE_PHONG"></span><span id="d3dshade_phong"></span>**D3DSHADE \_ Phong**
</dt> <dd>

Non pris en charge.

</dd> <dt>

<span id="D3DSHADE_FORCE_DWORD"></span><span id="d3dshade_force_dword"></span>**D3DSHADE \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Notes

Le premier vertex d’un triangle pour le mode d’ombrage plat est défini de la manière suivante.

-   Pour une liste de triangles, le premier vertex du triangle i est i \* 3.
-   Pour une bande triangulaire, le premier vertex du triangle i est le sommet i.
-   Pour un ventilateur triangulaire, le premier vertex du triangle i est le sommet i + 1.

Les membres de ce type énuméré définissent le valeurs pour l' \_ État de rendu D3DRS SHADEMODE.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
