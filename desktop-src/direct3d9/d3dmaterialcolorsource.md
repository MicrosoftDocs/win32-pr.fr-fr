---
description: Définit l’emplacement auquel un composant couleur ou couleur doit être accédé pour les calculs d’éclairage.
ms.assetid: 76061d47-a31c-4008-aa8d-a0464dd3423f
title: Énumération D3DMATERIALCOLORSOURCE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATERIALCOLORSOURCE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3c8069fdde062fdc6dea311b40b8614d2165356ff397f0d056c43569f391e02a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988889"
---
# <a name="d3dmaterialcolorsource-enumeration"></a>Énumération D3DMATERIALCOLORSOURCE

Définit l’emplacement auquel un composant couleur ou couleur doit être accédé pour les calculs d’éclairage.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DMATERIALCOLORSOURCE { 
  D3DMCS_MATERIAL     = 0,
  D3DMCS_COLOR1       = 1,
  D3DMCS_COLOR2       = 2,
  D3DMCS_FORCE_DWORD  = 0x7fffffff
} D3DMATERIALCOLORSOURCE, *LPD3DMATERIALCOLORSOURCE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DMCS_MATERIAL"></span><span id="d3dmcs_material"></span>**\_Matériau D3DMCS**
</dt> <dd>

Utilisez la couleur de la matière actuelle.

</dd> <dt>

<span id="D3DMCS_COLOR1"></span><span id="d3dmcs_color1"></span>**D3DMCS \_ COLOR1**
</dt> <dd>

Utilisez la couleur de vertex diffuse.

</dd> <dt>

<span id="D3DMCS_COLOR2"></span><span id="d3dmcs_color2"></span>**D3DMCS \_ COLOR2**
</dt> <dd>

Utilisez la couleur de vertex spéculaire.

</dd> <dt>

<span id="D3DMCS_FORCE_DWORD"></span><span id="d3dmcs_force_dword"></span>**D3DMCS \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Remarques

Ces indicateurs sont utilisés pour définir la valeur des États de rendu suivants dans le type énuméré [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) .

-   D3DRS \_ AMBIENTMATERIALSOURCE
-   D3DRS \_ DIFFUSEMATERIALSOURCE
-   D3DRS \_ EMISSIVEMATERIALSOURCE
-   D3DRS \_ SPECULARMATERIALSOURCE

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
