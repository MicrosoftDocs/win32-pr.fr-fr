---
description: 'D3DXMATRIX structure (D3dx9math. h) : matrice 4x4 qui contient des méthodes et des surcharges d’opérateur.'
ms.assetid: 0911088b-50cf-4c4a-996e-351386fc359b
title: D3DXMATRIX, structure (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATRIX
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 7390b31aa2cc2c81d3d56656efb3c9ff3b6c1de81bf3e5d4de471fd1f7058553
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118525330"
---
# <a name="d3dxmatrix-structure-d3dx9mathh"></a>D3DXMATRIX, structure (D3dx9math. h)

Matrice 4x4 qui contient des méthodes et des surcharges d’opérateur.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXMATRIX {
  FLOAT _ij;
} D3DXMATRIX, *LPD3DXMATRIX;
```



## <a name="members"></a>Membres

<dl> <dt>

**\_soudé**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Composant (i, j) de la matrice, où i est le numéro de ligne et j le numéro de colonne. Par exemple, \_ 34 correspond à \[ un ₄ ₃ \] , le composant dans la troisième ligne et la quatrième colonne.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les programmeurs C ne peuvent pas utiliser la structure D3DXMATRIX, ils doivent utiliser la structure [**D3DMATRIX**](d3dmatrix.md) . Les programmeurs C++ peuvent tirer parti des opérateurs surchargés et des opérateurs d’assignation, unaires et binaires (y compris l’égalité).

Dans D3DX, l' \_ élément 34 d’une matrice de projection ne peut pas être un nombre négatif. Si votre application doit utiliser une valeur négative à cet emplacement, elle doit mettre à l’échelle la totalité de la matrice de projection par-1 à la place.

### <a name="d3dxmatrix-extensions"></a>Extensions D3DXMATRIX

**D3DXMATRIX** a les extensions C++ suivantes.


```
#ifdef __cplusplus
typedef struct D3DXMATRIX : public D3DMATRIX
{
public:
    D3DXMATRIX() {};
    D3DXMATRIX( CONST FLOAT * );
    D3DXMATRIX( CONST D3DMATRIX& );
    D3DXMATRIX( CONST D3DXFLOAT16 * );
    D3DXMATRIX( FLOAT _11, FLOAT _12, FLOAT _13, FLOAT _14,
                FLOAT _21, FLOAT _22, FLOAT _23, FLOAT _24,
                FLOAT _31, FLOAT _32, FLOAT _33, FLOAT _34,
                FLOAT _41, FLOAT _42, FLOAT _43, FLOAT _44 );


    // access grants
    FLOAT& operator () ( UINT Row, UINT Col );
    FLOAT  operator () ( UINT Row, UINT Col ) const;

    // casting operators
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXMATRIX& operator *= ( CONST D3DXMATRIX& );
    D3DXMATRIX& operator += ( CONST D3DXMATRIX& );
    D3DXMATRIX& operator -= ( CONST D3DXMATRIX& );
    D3DXMATRIX& operator *= ( FLOAT );
    D3DXMATRIX& operator /= ( FLOAT );

    // unary operators
    D3DXMATRIX operator + () const;
    D3DXMATRIX operator - () const;

    // binary operators
    D3DXMATRIX operator * ( CONST D3DXMATRIX& ) const;
    D3DXMATRIX operator + ( CONST D3DXMATRIX& ) const;
    D3DXMATRIX operator - ( CONST D3DXMATRIX& ) const;
    D3DXMATRIX operator * ( FLOAT ) const;
    D3DXMATRIX operator / ( FLOAT ) const;

    friend D3DXMATRIX operator * ( FLOAT, CONST D3DXMATRIX& );

    BOOL operator == ( CONST D3DXMATRIX& ) const;
    BOOL operator != ( CONST D3DXMATRIX& ) const;

} D3DXMATRIX, *LPD3DXMATRIX;

#else //!__cplusplus
typedef struct _D3DMATRIX D3DXMATRIX, *LPD3DXMATRIX;
#endif //!__cplusplus
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DMATRIX**](d3dmatrix.md)
</dt> </dl>

 

 
