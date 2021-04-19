---
description: Décrit la résolution de la mémoire tampon z de l’ombre qui sera utilisée dans la simulation d’éclairage direct luminance Transfer (PRT) précalculé sur le GPU.
ms.assetid: 05354328-9b6f-45f5-a913-47ede170b03f
title: Énumération D3DXSHGPUSIMOPT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHGPUSIMOPT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: a94845faf4c34657f486cfa371c5d41a12dc4336
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520341"
---
# <a name="d3dxshgpusimopt-enumeration"></a>Énumération D3DXSHGPUSIMOPT

Décrit la résolution de la mémoire tampon z de l’ombre qui sera utilisée dans la simulation d’éclairage direct luminance Transfer (PRT) précalculé sur le GPU. Une mémoire tampon z de qualité supérieure peut également être spécifiée pour réduire le bruit dans les résultats de la simulation d’éclairage direct, même si la simulation est plus lente.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DXSHGPUSIMOPT { 
  D3DXSHGPUSIMOPT_SHADOWRES256   = 1,
  D3DXSHGPUSIMOPT_SHADOWRES512   = 0,
  D3DXSHGPUSIMOPT_SHADOWRES1024  = 2,
  D3DXSHGPUSIMOPT_SHADOWRES2048  = 3,
  D3DXSHGPUSIMOPT_HIGHQUALITY    = 4,
  D3DXSHGPUSIMOPT_FORCE_DWORD    = 0x7fffffff
} D3DXSHGPUSIMOPT, *LPD3DXSHGPUSIMOPT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXSHGPUSIMOPT_SHADOWRES256"></span><span id="d3dxshgpusimopt_shadowres256"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES256**
</dt> <dd>

Simulation de faible résolution. Une texture de 256 x 256 pixels est utilisée dans la simulation pour encoder la mémoire tampon z de l’ombre.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_SHADOWRES512"></span><span id="d3dxshgpusimopt_shadowres512"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES512**
</dt> <dd>

Simulation de résolution moyenne. Une texture de 512 x 512 pixels est utilisée dans la simulation pour encoder la mémoire tampon z de l’ombre. Il s’agit de la valeur par défaut.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_SHADOWRES1024"></span><span id="d3dxshgpusimopt_shadowres1024"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES1024**
</dt> <dd>

Simulation haute résolution. Une texture de 1024 x 1024 pixels est utilisée dans la simulation pour encoder la mémoire tampon z de l’ombre.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_SHADOWRES2048"></span><span id="d3dxshgpusimopt_shadowres2048"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES2048**
</dt> <dd>

Simulation de résolution la plus élevée. Une texture de 2048 x 2048 pixels est utilisée dans la simulation pour encoder la mémoire tampon z de l’ombre.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_HIGHQUALITY"></span><span id="d3dxshgpusimopt_highquality"></span>**D3DXSHGPUSIMOPT \_ highquality**
</dt> <dd>

La simulation est de haute précision, quelle que soit la résolution sélectionnée. La définition de cette valeur permet de réduire le bruit dans les résultats de la simulation d’éclairage direct, même si la simulation est plus lente. Peut être combiné avec l’une des valeurs de résolution.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_FORCE_DWORD"></span><span id="d3dxshgpusimopt_force_dword"></span>**D3DXSHGPUSIMOPT \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Notes

Une seule des valeurs de résolution peut être spécifiée et peut être combinée avec la valeur de haute qualité.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




