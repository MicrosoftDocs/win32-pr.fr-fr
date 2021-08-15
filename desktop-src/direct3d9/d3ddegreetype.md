---
description: Définit le degré des variables dans l’équation qui décrit une courbe.
ms.assetid: 52a9c57e-a48d-4d8a-a208-97a3d09e7abf
title: Énumération D3DDEGREETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEGREETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 6daacc007438903d3f003a19038b4ea6909814e3a5d024d3df6daa95a0c60602
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989049"
---
# <a name="d3ddegreetype-enumeration"></a>Énumération D3DDEGREETYPE

Définit le degré des variables dans l’équation qui décrit une courbe.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DDEGREETYPE { 
  D3DDEGREE_LINEAR     = 1,
  D3DDEGREE_QUADRATIC  = 2,
  D3DDEGREE_CUBIC      = 3,
  D3DDEGREE_QUINTIC    = 5,
  D3DCULL_FORCE_DWORD  = 0x7fffffff
} D3DDEGREETYPE, *LPD3DDEGREETYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DDEGREE_LINEAR"></span><span id="d3ddegree_linear"></span>**D3DDEGREE \_ linéaire**
</dt> <dd>

La courbe est décrite par les variables du premier ordre.

</dd> <dt>

<span id="D3DDEGREE_QUADRATIC"></span><span id="d3ddegree_quadratic"></span>**D3DDEGREE \_ quadratique**
</dt> <dd>

La courbe est décrite par les variables de la deuxième commande.

</dd> <dt>

<span id="D3DDEGREE_CUBIC"></span><span id="d3ddegree_cubic"></span>**D3DDEGREE \_ cubique**
</dt> <dd>

La courbe est décrite par les variables de troisième ordre.

</dd> <dt>

<span id="D3DDEGREE_QUINTIC"></span><span id="d3ddegree_quintic"></span>**D3DDEGREE \_ quintaux**
</dt> <dd>

La courbe est décrite par les variables du quatrième ordre.

</dd> <dt>

<span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les valeurs de cette énumération sont utilisées pour décrire les courbes utilisées par les correctifs de rectangle et de triangle. Pour plus d’informations, consultez D3DRS \_ CULLMODE.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
