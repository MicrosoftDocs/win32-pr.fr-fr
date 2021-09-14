---
description: Identique à un D3DXVECTOR4, mais il utilise des valeurs à virgule flottante 16 bits pour x, y et z.
ms.assetid: 2db5fb3e-ffe0-4bcf-8894-a8bc7eefaf82
title: Structure D3DXVECTOR4_16F (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR4_16F
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: d3d46e6bc5423260e550fd026ca52420b1c392ca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008102"
---
# <a name="d3dxvector4_16f-structure"></a>D3DXVECTOR4 \_ 16F, structure

Identique à un [**D3DXVECTOR4**](d3d10-d3dxvector4.md), mais il utilise des valeurs à virgule flottante 16 bits pour x, y et z.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXVECTOR4_16F {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXVECTOR4_16F, *LPD3DXVECTOR4_16F;
```



## <a name="members"></a>Membres

<dl> <dt>

**x**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Composant x.

</dd> <dt>

**y**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Composant y.

</dd> <dt>

**Lettre**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Composant z.

</dd> <dt>

**w**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Composant w.

</dd> </dl>

## <a name="remarks"></a>Notes

**D3DXVECTOR4 \_ 16F** contient les extensions C++ suivantes.

### <a name="d3dxvector4_16f-extensions"></a>\_Extensions 16F D3DXVECTOR4


```
typedef struct D3DXVECTOR4_16F
{
#ifdef __cplusplus
public:
    D3DXVECTOR4_16F() {};
    D3DXVECTOR4_16F( CONST FLOAT * );
    D3DXVECTOR4_16F( CONST D3DXFLOAT16 * );
    D3DXVECTOR4_16F( CONST D3DXVECTOR3_16F& xyz, CONST D3DXFLOAT16& w );
    D3DXVECTOR4_16F( CONST D3DXFLOAT16& x, CONST D3DXFLOAT16& y, CONST D3DXFLOAT16& z, CONST D3DXFLOAT16& w );

    // casting
    operator D3DXFLOAT16* ();
    operator CONST D3DXFLOAT16* () const;

    // binary operators
    BOOL operator == ( CONST D3DXVECTOR4_16F& ) const;
    BOOL operator != ( CONST D3DXVECTOR4_16F& ) const;

public:
#endif //__cplusplus
    D3DXFLOAT16 x, y, z, w;

} D3DXVECTOR4_16F, *LPD3DXVECTOR4_16F;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
