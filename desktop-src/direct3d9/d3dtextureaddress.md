---
description: Définit des constantes qui décrivent les modes d’adressage de texture pris en charge.
ms.assetid: 5c03c55f-4a74-4b0e-ba05-e4a6582ff47c
title: Énumération D3DTEXTUREADDRESS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREADDRESS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2cb1893541f80efb9bf85ea444b27bebba5dea29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043090"
---
# <a name="d3dtextureaddress-enumeration"></a>Énumération D3DTEXTUREADDRESS

Définit des constantes qui décrivent les modes d’adressage de texture pris en charge.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DTEXTUREADDRESS { 
  D3DTADDRESS_WRAP         = 1,
  D3DTADDRESS_MIRROR       = 2,
  D3DTADDRESS_CLAMP        = 3,
  D3DTADDRESS_BORDER       = 4,
  D3DTADDRESS_MIRRORONCE   = 5,
  D3DTADDRESS_FORCE_DWORD  = 0x7fffffff
} D3DTEXTUREADDRESS, *LPD3DTEXTUREADDRESS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DTADDRESS_WRAP"></span><span id="d3dtaddress_wrap"></span>**\_Retour à la ligne D3DTADDRESS**
</dt> <dd>

Juxtaposer la texture à chaque jonction d’entier. Par exemple, pour vos valeurs comprises entre 0 et 3, la texture est répétée trois fois. aucune mise en miroir n’est effectuée.

</dd> <dt>

<span id="D3DTADDRESS_MIRROR"></span><span id="d3dtaddress_mirror"></span>**\_Miroir D3DTADDRESS**
</dt> <dd>

Semblable à D3DTADDRESS \_ Wrap, sauf que la texture est retournée à chaque jonction d’entier. pour vos valeurs comprises entre 0 et 1, par exemple, la texture est traitée normalement ; entre 1 et 2, la texture est retournée (en miroir); entre 2 et 3, la texture est à nouveau normale ; et ainsi de suite.

</dd> <dt>

<span id="D3DTADDRESS_CLAMP"></span><span id="d3dtaddress_clamp"></span>**D3DTADDRESS \_ clamp**
</dt> <dd>

Les coordonnées de texture en dehors de la plage \[ 0,0, 1,0 \] sont définies sur la couleur de texture à 0,0 ou 1,0, respectivement.

</dd> <dt>

<span id="D3DTADDRESS_BORDER"></span><span id="d3dtaddress_border"></span>**\_Bordure D3DTADDRESS**
</dt> <dd>

Les coordonnées de texture en dehors de la plage \[ 0,0, 1,0 \] sont définies sur la couleur de la bordure.

</dd> <dt>

<span id="D3DTADDRESS_MIRRORONCE"></span><span id="d3dtaddress_mirroronce"></span>**D3DTADDRESS \_ MIRRORONCE**
</dt> <dd>

Semblable à D3DTADDRESS \_ Mirror et D3DTADDRESS \_ clamp. Prend la valeur absolue de la coordonnée de texture (par conséquent, la mise en miroir autour de 0), puis attache à la valeur maximale. L’utilisation la plus courante concerne les textures de volume, où la prise en charge du \_ mode d’adressage de texture MIRRORONCE D3DTADDRESS complet n’est pas nécessaire, mais les données sont symétriques autour de l’axe.

</dd> <dt>

<span id="D3DTADDRESS_FORCE_DWORD"></span><span id="d3dtaddress_force_dword"></span>**D3DTADDRESS \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)
</dt> </dl>

 

 
