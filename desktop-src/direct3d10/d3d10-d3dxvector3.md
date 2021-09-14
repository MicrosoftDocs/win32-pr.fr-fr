---
description: D3DXVECTOR3 structure (D3DX10Math. h)-décrit un vecteur à trois composants incluant des surcharges d’opérateur et des casts de type.
ms.assetid: d170cd26-d705-4a31-82b3-f9ea070b6ca4
title: D3DXVECTOR3, structure (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR3
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 7b43348b6b5683e9fe75c5340fd0c2cab5efe719
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008103"
---
# <a name="d3dxvector3-structure-d3dx10mathh"></a>D3DXVECTOR3, structure (D3DX10Math. h)

Décrit un vecteur à trois composants incluant des surcharges d’opérateur et des casts de type.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXVECTOR3 {
  FLOAT x;
  FLOAT y;
  FLOAT z;
} D3DXVECTOR3, *LPD3DXVECTOR3;
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

**z**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Composant z.

</dd> </dl>

## <a name="remarks"></a>Notes

**D3DXVECTOR3** a les extensions C++ suivantes.

### <a name="d3dxvector3-extensions"></a>Extensions D3DXVECTOR3


```
#ifdef __cplusplus
typedef struct D3DXVECTOR3 : public D3DVECTOR
{
public:
    D3DXVECTOR3() {};
    D3DXVECTOR3( CONST FLOAT * );
    D3DXVECTOR3( CONST D3DVECTOR& );
    D3DXVECTOR3( CONST D3DXFLOAT16 * );
    D3DXVECTOR3( FLOAT x, FLOAT y, FLOAT z );

    // casting
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXVECTOR3& operator += ( CONST D3DXVECTOR3& );
    D3DXVECTOR3& operator -= ( CONST D3DXVECTOR3& );
    D3DXVECTOR3& operator *= ( FLOAT );
    D3DXVECTOR3& operator /= ( FLOAT );

    // unary operators
    D3DXVECTOR3 operator + () const;
    D3DXVECTOR3 operator - () const;

    // binary operators
    D3DXVECTOR3 operator + ( CONST D3DXVECTOR3& ) const;
    D3DXVECTOR3 operator - ( CONST D3DXVECTOR3& ) const;
    D3DXVECTOR3 operator * ( FLOAT ) const;
    D3DXVECTOR3 operator / ( FLOAT ) const;

    friend D3DXVECTOR3 operator * ( FLOAT, CONST struct D3DXVECTOR3& );

    BOOL operator == ( CONST D3DXVECTOR3& ) const;
    BOOL operator != ( CONST D3DXVECTOR3& ) const;

} D3DXVECTOR3, *LPD3DXVECTOR3;

#else //!__cplusplus
typedef struct _D3DVECTOR D3DXVECTOR3, *LPD3DXVECTOR3;
#endif //!__cplusplus
        
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
