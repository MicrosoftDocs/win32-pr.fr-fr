---
description: Définit le type de lumière.
ms.assetid: 90ad82d3-ffa8-42bb-9d9c-cf28a416c32d
title: Énumération D3DLIGHTTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLIGHTTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 83c94db3126443f757f01a69d7d773417f70683a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106542168"
---
# <a name="d3dlighttype-enumeration"></a>Énumération D3DLIGHTTYPE

Définit le type de lumière.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DLIGHTTYPE { 
  D3DLIGHT_POINT        = 1,
  D3DLIGHT_SPOT         = 2,
  D3DLIGHT_DIRECTIONAL  = 3,
  D3DLIGHT_FORCE_DWORD  = 0x7fffffff
} D3DLIGHTTYPE, *LPD3DLIGHTTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DLIGHT_POINT"></span><span id="d3dlight_point"></span>**\_Point D3DLIGHT**
</dt> <dd>

Light est une source de point. La lumière a une position dans l’espace et rayonne la lumière dans toutes les directions.

</dd> <dt>

<span id="D3DLIGHT_SPOT"></span><span id="d3dlight_spot"></span>**D3DLIGHT \_**
</dt> <dd>

Light est une source Spotlight. Cette lumière est semblable à une lumière de point, sauf que l’éclairage est limité à un cône. Ce type de lumière a une direction et plusieurs autres paramètres qui déterminent la forme du cône qu’il produit. Pour plus d’informations sur ces paramètres, consultez la structure [**D3DLIGHT9**](d3dlight9.md) .

</dd> <dt>

<span id="D3DLIGHT_DIRECTIONAL"></span><span id="d3dlight_directional"></span>**D3DLIGHT \_ directionnelle**
</dt> <dd>

Light est une source de lumière directionnelle. Cela équivaut à utiliser une source de lumière de point à une distance infinie.

</dd> <dt>

<span id="D3DLIGHT_FORCE_DWORD"></span><span id="d3dlight_force_dword"></span>**D3DLIGHT \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Notes

Les lumières directionnelles sont légèrement plus rapides que les sources de point-lumière, mais les lumières de point sont un peu mieux adaptées. Les actualités offrent des effets visuels intéressants, mais prennent du temps sur le calcul.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DLIGHT9**](d3dlight9.md)
</dt> </dl>

 

 




