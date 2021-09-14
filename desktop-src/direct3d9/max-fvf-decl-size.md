---
description: Cette constante est le nombre maximal de déclarateurs de vertex pour une maille.
ms.assetid: 234e99a2-1907-4065-b03b-fb9e8d6812ab
title: Énumération MAX_FVF_DECL_SIZE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MAX_FVF_DECL_SIZE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 7204308e6b9355b416218f31af301b5ea6d8fff5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918255"
---
# <a name="max_fvf_decl_size-enumeration"></a>\_Énumération Max Commission de la \_ \_ taille decl

Cette constante est le nombre maximal de déclarateurs de vertex pour une maille.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum  { 
  MAX_FVF_DECL_SIZE  = MAXD3DDECLLENGTH + 1
} MAX_FVF_DECL_SIZE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MAX_FVF_DECL_SIZE"></span><span id="max_fvf_decl_size"></span>**\_taille de \_ décl max. \_**
</dt> <dd>

Nombre maximal d’éléments dans la déclaration de vertex. Le supplémentaire (+ 1) est pour [**la \_ terminaison D3DDECL**](d3ddecl-end.md).

</dd> </dl>

## <a name="remarks"></a>Notes

MAXD3DDECLLENGTH est défini comme un maximum de 64 (voir d3d9types. h). Cela n’inclut pas l’élément de vertex du marqueur « end ».

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**ID3DXBaseMesh**](id3dxbasemesh.md)
</dt> <dt>

[**GetDeclaration**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexdeclaration9-getdeclaration)
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> <dt>

[**ID3DXSkinInfo**](id3dxskininfo.md)
</dt> </dl>

 

 
