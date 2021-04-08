---
description: Définit le mode de fusion pris en charge.
ms.assetid: 60ff384c-15a0-4c6f-9e2c-59fdea76b7a1
title: Énumération D3DBLEND (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBLEND
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: d8d779ad714e396f9c9a82bbbc42ddd09b76e2ac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953816"
---
# <a name="d3dblend-enumeration"></a>Énumération D3DBLEND

Définit le mode de fusion pris en charge.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DBLEND { 
  D3DBLEND_ZERO             = 1,
  D3DBLEND_ONE              = 2,
  D3DBLEND_SRCCOLOR         = 3,
  D3DBLEND_INVSRCCOLOR      = 4,
  D3DBLEND_SRCALPHA         = 5,
  D3DBLEND_INVSRCALPHA      = 6,
  D3DBLEND_DESTALPHA        = 7,
  D3DBLEND_INVDESTALPHA     = 8,
  D3DBLEND_DESTCOLOR        = 9,
  D3DBLEND_INVDESTCOLOR     = 10,
  D3DBLEND_SRCALPHASAT      = 11,
  D3DBLEND_BOTHSRCALPHA     = 12,
  D3DBLEND_BOTHINVSRCALPHA  = 13,
  D3DBLEND_BLENDFACTOR      = 14,
  D3DBLEND_INVBLENDFACTOR   = 15,
  D3DBLEND_SRCCOLOR2        = 16,
  D3DBLEND_INVSRCCOLOR2     = 17,
  D3DBLEND_FORCE_DWORD      = 0x7fffffff
} D3DBLEND, *LPD3DBLEND;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DBLEND_ZERO"></span><span id="d3dblend_zero"></span>**D3DBLEND \_ zéro**
</dt> <dd>

Le facteur de fusion est (0, 0, 0, 0).

</dd> <dt>

<span id="D3DBLEND_ONE"></span><span id="d3dblend_one"></span>**D3DBLEND \_ un**
</dt> <dd>

Le facteur de fusion est (1, 1, 1, 1).

</dd> <dt>

<span id="D3DBLEND_SRCCOLOR"></span><span id="d3dblend_srccolor"></span>**D3DBLEND \_ SRCCOLOR**
</dt> <dd>

Le facteur de fusion est (RS, GS, BS, As).

</dd> <dt>

<span id="D3DBLEND_INVSRCCOLOR"></span><span id="d3dblend_invsrccolor"></span>**D3DBLEND \_ INVSRCCOLOR**
</dt> <dd>

Le facteur de fusion est (1-RS, 1-GS, 1-BS, 1-As).

</dd> <dt>

<span id="D3DBLEND_SRCALPHA"></span><span id="d3dblend_srcalpha"></span>**D3DBLEND \_ SRCALPHA**
</dt> <dd>

Le facteur de fusion est (As, As, As, As).

</dd> <dt>

<span id="D3DBLEND_INVSRCALPHA"></span><span id="d3dblend_invsrcalpha"></span>**D3DBLEND \_ INVSRCALPHA**
</dt> <dd>

Le facteur de fusion est (1-As, 1-As, 1-As, 1-As).

</dd> <dt>

<span id="D3DBLEND_DESTALPHA"></span><span id="d3dblend_destalpha"></span>**D3DBLEND \_ DESTALPHA**
</dt> <dd>

Le<sub>facteur de fusion</sub> est<sub>(a d a d</sub> <sub>a d</sub> <sub>).</sub>

</dd> <dt>

<span id="D3DBLEND_INVDESTALPHA"></span><span id="d3dblend_invdestalpha"></span>**D3DBLEND \_ INVDESTALPHA**
</dt> <dd>

Le facteur de fusion est (1-A<sub>d</sub> 1-a<sub>d</sub> 1-A<sub>d</sub> 1-a<sub>d</sub>).

</dd> <dt>

<span id="D3DBLEND_DESTCOLOR"></span><span id="d3dblend_destcolor"></span>**D3DBLEND \_ DESTCOLOR**
</dt> <dd>

Le facteur de fusion est (R<sub>d</sub>, G<sub>d</sub>, B<sub>d</sub>, A<sub>d</sub>).

</dd> <dt>

<span id="D3DBLEND_INVDESTCOLOR"></span><span id="d3dblend_invdestcolor"></span>**D3DBLEND \_ INVDESTCOLOR**
</dt> <dd>

Le facteur de fusion est (1-R<sub>d</sub>, 1-G<sub>d</sub>, 1-B<sub>d</sub>, 1-A<sub>d</sub>).

</dd> <dt>

<span id="D3DBLEND_SRCALPHASAT"></span><span id="d3dblend_srcalphasat"></span>**D3DBLEND \_ SRCALPHASAT**
</dt> <dd>

Le facteur de fusion est (f, f, f, 1); où f = min (As, 1-A<sub>d</sub>).

</dd> <dt>

<span id="D3DBLEND_BOTHSRCALPHA"></span><span id="d3dblend_bothsrcalpha"></span>**D3DBLEND \_ BOTHSRCALPHA**
</dt> <dd>

**Obsolète**. À partir de DirectX 6, vous pouvez obtenir le même effet en définissant les facteurs de fusion source et destination sur D3DBLEND \_ SRCALPHA et D3DBLEND \_ INVSRCALPHA dans des appels distincts.

</dd> <dt>

<span id="D3DBLEND_BOTHINVSRCALPHA"></span><span id="d3dblend_bothinvsrcalpha"></span>**D3DBLEND \_ BOTHINVSRCALPHA**
</dt> <dd>

**Obsolète**. Le facteur de fusion source est (1-As, 1-As, 1-As, 1-As) et le facteur de fusion de destination est (As, As, As); la sélection Blend de destination est remplacée. Ce mode de fusion est pris en charge uniquement pour l' \_ État de rendu D3DRS SRCBLEND.

</dd> <dt>

<span id="D3DBLEND_BLENDFACTOR"></span><span id="d3dblend_blendfactor"></span>**D3DBLEND \_ BLENDFACTOR**
</dt> <dd>

Facteur de fusion de couleur constant utilisé par le mélangeur de mémoire tampon de trame. Ce mode de fusion est pris en charge uniquement si D3DPBLENDCAPS \_ BLENDFACTOR est défini dans les membres **SrcBlendCaps** ou **DestBlendCaps** de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

</dd> <dt>

<span id="D3DBLEND_INVBLENDFACTOR"></span><span id="d3dblend_invblendfactor"></span>**D3DBLEND \_ INVBLENDFACTOR**
</dt> <dd>

Facteur de fusion de couleur inversé inversé utilisé par le mélangeur de mémoire tampon de trame. Ce mode de fusion est pris en charge uniquement si le \_ bit D3DPBLENDCAPS BLENDFACTOR est défini dans les membres **SrcBlendCaps** ou **DestBlendCaps** de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

</dd> <dt>

<span id="D3DBLEND_SRCCOLOR2"></span><span id="d3dblend_srccolor2"></span>**D3DBLEND \_ SRCCOLOR2**
</dt> <dd>

Le facteur de fusion est (PSOutColor \[ 1 \] <sub>r</sub>, PSOutColor \[ 1 \] <sub>g</sub>, PSOutColor \[ 1 \] <sub>b</sub>, non utilisé). Consultez [fusion de cibles de rendu](#render-target-blending).



|                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------|
| Différences entre Direct3D 9 et Direct3D 9Ex :<br/> Cet indicateur est disponible uniquement dans Direct3D 9Ex.<br/> |



 

</dd> <dt>

<span id="D3DBLEND_INVSRCCOLOR2"></span><span id="d3dblend_invsrccolor2"></span>**D3DBLEND \_ INVSRCCOLOR2**
</dt> <dd>

Le facteur de fusion est (1-PSOutColor \[ 1 \] <sub>r</sub>, 1-PSOutColor \[ 1 \] <sub>g</sub>, 1-PSOutColor \[ 1 \] <sub>b</sub>, non utilisé)). Consultez [fusion de cibles de rendu](#render-target-blending).



|                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------|
| Différences entre Direct3D 9 et Direct3D 9Ex :<br/> Cet indicateur est disponible uniquement dans Direct3D 9Ex.<br/> |



 

</dd> <dt>

<span id="D3DBLEND_FORCE_DWORD"></span><span id="d3dblend_force_dword"></span>**D3DBLEND \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Notes

Dans les descriptions de membre précédentes, les valeurs RVBA de la source et de la destination sont indiquées par les indices s et d.

Les valeurs de ce type énuméré sont utilisées par les États de rendu suivants :

-   D3DRS \_ DESTBLEND
-   D3DRS \_ SRCBLEND
-   D3DRS \_ DESTBLENDALPHA
-   D3DRS \_ SRCBLENDALPHA

Voir [ **D3DRENDERSTATETYPE**](./d3drenderstatetype.md)

### <a name="render-target-blending"></a>Fusion de la cible de rendu

Direct3D 9Ex a amélioré les fonctionnalités de rendu de texte. Le rendu des polices Clear-type nécessite normalement deux passes. Pour éliminer la deuxième passe, un nuanceur de pixels peut être utilisé pour sortir deux couleurs, que nous pouvons appeler PSOutColor \[ 0 \] et PSOutColor \[ 1 \] . La première couleur contient les composants RVB (standard 3 Color Components). La deuxième couleur contient 3 composants alpha (un pour chaque composant de la première couleur).

Ces nouveaux modes de fusion sont utilisés uniquement pour le rendu de texte sur la première cible de rendu.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 
