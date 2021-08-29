---
description: Définit le type de données de maillage présentes dans D3DXMESHDATA.
ms.assetid: e5324f85-17cc-46a7-886a-c8f3464baade
title: Énumération D3DXMESHDATATYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESHDATATYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: d204390bcc1ab5ef3bb4325b3ce1fa5b1adb05b548329dc75d3d16a5e93e5b66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564649"
---
# <a name="d3dxmeshdatatype-enumeration"></a>Énumération D3DXMESHDATATYPE

Définit le type de données de maillage présentes dans [**D3DXMESHDATA**](d3dxmeshdata.md).

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DXMESHDATATYPE { 
  D3DXMESHTYPE_MESH         = 0x001,
  D3DXMESHTYPE_PATCHMESH    = 0x003,
  D3DXMESHTYPE_FORCE_DWORD  = 0x7fffffff
} D3DXMESHDATATYPE, *LPD3DXMESHDATATYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXMESHTYPE_MESH"></span><span id="d3dxmeshtype_mesh"></span>**\_Maille D3DXMESHTYPE**
</dt> <dd>

Le type de données est une maille. Consultez [**ID3DXMesh**](id3dxmesh.md).

</dd> <dt>

<span id="D3DXMESHTYPE_PATCHMESH"></span><span id="d3dxmeshtype_patchmesh"></span>**D3DXMESHTYPE \_ PATCHMESH**
</dt> <dd>

Le type de données est un maillage de correctifs. Consultez [**ID3DXPatchMesh**](id3dxpatchmesh.md).

</dd> <dt>

<span id="D3DXMESHTYPE_FORCE_DWORD"></span><span id="d3dxmeshtype_force_dword"></span>**D3DXMESHTYPE \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXMESHDATA**](d3dxmeshdata.md)
</dt> </dl>

 

 




