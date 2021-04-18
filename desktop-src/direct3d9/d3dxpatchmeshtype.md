---
description: Types de correctifs de maillage.
ms.assetid: 229d01b2-781c-48a8-93f2-9dd9dbd67f3e
title: Énumération D3DXPATCHMESHTYPE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPATCHMESHTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: d6a663e983b339d79ec89bf1b4ddfe7b4eaa9f1e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522562"
---
# <a name="d3dxpatchmeshtype-enumeration"></a>Énumération D3DXPATCHMESHTYPE

Types de correctifs de maillage.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DXPATCHMESHTYPE { 
  D3DXPATCHMESH_RECT         = 0x001,
  D3DXPATCHMESH_TRI          = 0x002,
  D3DXPATCHMESH_NPATCH       = 0x003,
  D3DXPATCHMESH_FORCE_DWORD  = 0x7fffffff
} D3DXPATCHMESHTYPE, *LPD3DXPATCHMESHTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXPATCHMESH_RECT"></span><span id="d3dxpatchmesh_rect"></span>**D3DXPATCHMESH \_ Rect**
</dt> <dd>

Type de maillage de correctif rectangle.

</dd> <dt>

<span id="D3DXPATCHMESH_TRI"></span><span id="d3dxpatchmesh_tri"></span>**D3DXPATCHMESH \_ Tri**
</dt> <dd>

Type de maillage de la partie triangulaire.

</dd> <dt>

<span id="D3DXPATCHMESH_NPATCH"></span><span id="d3dxpatchmesh_npatch"></span>**D3DXPATCHMESH \_ NPATCH**
</dt> <dd>

Type de maillage N-patch.

</dd> <dt>

<span id="D3DXPATCHMESH_FORCE_DWORD"></span><span id="d3dxpatchmesh_force_dword"></span>**D3DXPATCHMESH \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Notes

Les correctifs triangulaires ont trois côtés et sont décrits dans [**D3DTRIPATCH \_ info**](d3dtripatch-info.md). Les correctifs de rectangle sont à quatre côtés et sont décrits dans [**D3DRECTPATCH \_ info**](d3drectpatch-info.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[Utilisation de primitives Higher-Order (Direct3D 9)](using-higher-order-primitives.md)
</dt> </dl>

 

 




