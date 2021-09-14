---
description: D3DXSHPRTSPLITMESHVERTDATA, structure
ms.assetid: 8799a680-bf5f-42cc-91aa-1a6aed164ca5
title: D3DXSHPRTSPLITMESHVERTDATA, structure (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTSPLITMESHVERTDATA
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 55424929a3d415fc1b89f7a1af53be849cf90185
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008029"
---
# <a name="d3dxshprtsplitmeshvertdata-structure"></a>D3DXSHPRTSPLITMESHVERTDATA, structure

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXSHPRTSPLITMESHVERTDATA {
  UINT uVertRemap;
  UINT uSubCluster;
  UINT ucVertStatus;
} D3DXSHPRTSPLITMESHVERTDATA, *LPD3DXSHPRTSPLITMESHVERTDATA;
```



## <a name="members"></a>Membres

<dl> <dt>

**uVertRemap**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Vertex dans le maillage d’origine qui correspond à.

</dd> <dt>

**uSubCluster**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Index de cluster, relatif au supercluster.

</dd> <dt>

**ucVertStatus**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

1 si le Vertex a des données valides, 0 s’il est « Full ».

</dd> </dl>

## <a name="remarks"></a>Notes

Alloué dans [**D3DXSHPRTCompSplitMeshSC**](d3dxshprtcompsplitmeshsc.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
