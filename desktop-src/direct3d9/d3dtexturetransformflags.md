---
description: Définit les valeurs de transformation de la coordonnée de texture.
ms.assetid: a91f33ce-2db5-437a-ac29-402b26b0d4e1
title: Énumération D3DTEXTURETRANSFORMFLAGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTURETRANSFORMFLAGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 63426c0d57dee02823ee2f37327ba7c66d421b24
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211703"
---
# <a name="d3dtexturetransformflags-enumeration"></a>Énumération D3DTEXTURETRANSFORMFLAGS

Définit les valeurs de transformation de la coordonnée de texture.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DTEXTURETRANSFORMFLAGS { 
  D3DTTFF_DISABLE      = 0,
  D3DTTFF_COUNT1       = 1,
  D3DTTFF_COUNT2       = 2,
  D3DTTFF_COUNT3       = 3,
  D3DTTFF_COUNT4       = 4,
  D3DTTFF_PROJECTED    = 256,
  D3DTTFF_FORCE_DWORD  = 0x7fffffff
} D3DTEXTURETRANSFORMFLAGS, *LPD3DTEXTURETRANSFORMFLAGS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DTTFF_DISABLE"></span><span id="d3dttff_disable"></span>**Désactivation de D3DTTFF \_**
</dt> <dd>

Les coordonnées de texture sont passées directement au rastériseur.

</dd> <dt>

<span id="D3DTTFF_COUNT1"></span><span id="d3dttff_count1"></span>**D3DTTFF \_ COUNT1**
</dt> <dd>

Le rastériseur doit s’attendre à des coordonnées de texture 1D. Cette valeur est utilisée par le traitement du vertex de fonction fixe. elle doit être définie sur 0 lors de l’utilisation d’un nuanceur de sommet programmable.

</dd> <dt>

<span id="D3DTTFF_COUNT2"></span><span id="d3dttff_count2"></span>**D3DTTFF \_ COUNT2**
</dt> <dd>

Le rastériseur doit s’attendre à des coordonnées de texture 2D. Cette valeur est utilisée par le traitement du vertex de fonction fixe. elle doit être définie sur 0 lors de l’utilisation d’un nuanceur de sommet programmable.

</dd> <dt>

<span id="D3DTTFF_COUNT3"></span><span id="d3dttff_count3"></span>**D3DTTFF \_ COUNT3**
</dt> <dd>

Le rastériseur doit s’attendre à des coordonnées de texture 3D. Cette valeur est utilisée par le traitement du vertex de fonction fixe. elle doit être définie sur 0 lors de l’utilisation d’un nuanceur de sommet programmable.

</dd> <dt>

<span id="D3DTTFF_COUNT4"></span><span id="d3dttff_count4"></span>**D3DTTFF \_ COUNT4**
</dt> <dd>

Le rastériseur doit s’attendre à des coordonnées de texture 4D. Cette valeur est utilisée par le traitement du vertex de fonction fixe. elle doit être définie sur 0 lors de l’utilisation d’un nuanceur de sommet programmable.

</dd> <dt>

<span id="D3DTTFF_PROJECTED"></span><span id="d3dttff_projected"></span>**D3DTTFF \_ projetée**
</dt> <dd>

Cet indicateur est respecté par le pipeline de pixels de fonction fixe, ainsi que le pipeline de pixel programmable dans les versions PS \_ 1 \_ 1 à PS \_ 1 \_ 3. Lorsque la projection de texture est activée pour une étape de texture, les quatre valeurs à virgule flottante doivent être écrites dans le registre de texture correspondant. Chaque coordonnée de texture est divisée par le dernier élément avant d’être passée au rastériseur. Par exemple, si cet indicateur est spécifié avec l' \_ indicateur D3DTTFF COUNT3, les première et deuxième coordonnées de texture sont divisées par la troisième coordonnée avant d’être passées au rastériseur.

</dd> <dt>

<span id="D3DTTFF_FORCE_DWORD"></span><span id="d3dttff_force_dword"></span>**D3DTTFF \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Notes

Les coordonnées de texture peuvent être transformées à l’aide d’une matrice 4 x 4 avant que les résultats ne soient passés au rastériseur. Les transformations de coordonnées de texture sont définies en appelant [**IDirect3DDevice9 :: SetTextureStageState**](/windows/desktop/api)et en passant l’état de l' \_ étape de texture D3DTSS TEXTURETRANSFORMFLAGS et l’une des valeurs de **D3DTEXTURETRANSFORMFLAGS**. Pour plus d’informations sur les transformations de texture, consultez [transformations de coordonnées de texture (Direct3D 9)](texture-coordinate-transformations.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)
</dt> </dl>

 

 
