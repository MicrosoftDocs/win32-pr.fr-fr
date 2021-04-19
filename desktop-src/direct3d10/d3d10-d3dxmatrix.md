---
description: Matrice 4x4 qui contient des méthodes et des surcharges d’opérateur.
ms.assetid: c354d28b-bb08-41c5-bb59-90a912181f0f
title: D3DXMATRIX, structure (D3DX10Math. h)
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
- D3DX10Math.h
ms.openlocfilehash: cae887e2e9a8782cdc7ba159db203c929006c58a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522387"
---
# <a name="d3dxmatrix-structure-d3dx10mathh"></a><span data-ttu-id="39527-103">D3DXMATRIX, structure (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="39527-103">D3DXMATRIX structure (D3DX10Math.h)</span></span>

<span data-ttu-id="39527-104">Matrice 4x4 qui contient des méthodes et des surcharges d’opérateur.</span><span class="sxs-lookup"><span data-stu-id="39527-104">A 4x4 matrix that contains methods and operator overloads.</span></span>

## <a name="syntax"></a><span data-ttu-id="39527-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39527-105">Syntax</span></span>


```C++
typedef struct D3DXMATRIX {
  FLOAT _ij;
} D3DXMATRIX, *LPD3DXMATRIX;
```



## <a name="members"></a><span data-ttu-id="39527-106">Membres</span><span class="sxs-lookup"><span data-stu-id="39527-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="39527-107">**\_soudé**</span><span class="sxs-lookup"><span data-stu-id="39527-107">**\_ij**</span></span>
</dt> <dd>

<span data-ttu-id="39527-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="39527-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="39527-109">Composant (i, j) de la matrice, où i est le numéro de ligne et j le numéro de colonne.</span><span class="sxs-lookup"><span data-stu-id="39527-109">The (i, j) component of the matrix, where i is the row number and j is the column number.</span></span> <span data-ttu-id="39527-110">Par exemple, \_ 34 correspond à \[ un ₄ ₃ \] , le composant dans la troisième ligne et la quatrième colonne.</span><span class="sxs-lookup"><span data-stu-id="39527-110">For example, \_34 means the same as \[a₃₄\], the component in the third row and fourth column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39527-111">Notes</span><span class="sxs-lookup"><span data-stu-id="39527-111">Remarks</span></span>

<span data-ttu-id="39527-112">Les programmeurs C ne peuvent pas utiliser la structure D3DXMATRIX, ils doivent utiliser la structure D3DMATRIX.</span><span class="sxs-lookup"><span data-stu-id="39527-112">C programmers cannot use the D3DXMATRIX structure, they must use the D3DMATRIX structure.</span></span> <span data-ttu-id="39527-113">Les programmeurs C++ peuvent tirer parti des opérateurs surchargés et des opérateurs d’assignation, unaires et binaires (y compris l’égalité).</span><span class="sxs-lookup"><span data-stu-id="39527-113">C++ programmers can take advantage of overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

<span data-ttu-id="39527-114">Dans D3DX, l' \_ élément 34 d’une matrice de projection ne peut pas être un nombre négatif.</span><span class="sxs-lookup"><span data-stu-id="39527-114">In D3DX, the \_34 element of a projection matrix cannot be a negative number.</span></span> <span data-ttu-id="39527-115">Si votre application doit utiliser une valeur négative à cet emplacement, elle doit mettre à l’échelle la totalité de la matrice de projection par-1 à la place.</span><span class="sxs-lookup"><span data-stu-id="39527-115">If your application needs to use a negative value in this location, it should scale the entire projection matrix by -1 instead.</span></span>

### <a name="d3dxmatrix-extensions"></a><span data-ttu-id="39527-116">Extensions D3DXMATRIX</span><span class="sxs-lookup"><span data-stu-id="39527-116">D3DXMATRIX Extensions</span></span>

<span data-ttu-id="39527-117">**D3DXMATRIX** a les extensions C++ suivantes.</span><span class="sxs-lookup"><span data-stu-id="39527-117">**D3DXMATRIX** has the following C++ extensions.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="39527-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39527-118">Requirements</span></span>



| <span data-ttu-id="39527-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39527-119">Requirement</span></span> | <span data-ttu-id="39527-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="39527-120">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39527-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="39527-121">Header</span></span><br/> | <dl> <span data-ttu-id="39527-122"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="39527-122"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39527-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39527-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39527-124">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="39527-124">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
