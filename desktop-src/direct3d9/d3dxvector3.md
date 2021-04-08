---
description: Décrit un vecteur à trois composants incluant des surcharges d’opérateur et des casts de type.
ms.assetid: 4d73de4b-82fe-452a-8a1e-17208f172a03
title: D3DXVECTOR3, structure (D3dx9math. h)
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
- d3dx9math.h
ms.openlocfilehash: 2c49902677999c78737e7dec094c839cd8941f08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043196"
---
# <a name="d3dxvector3-structure-d3dx9mathh"></a><span data-ttu-id="da38b-103">D3DXVECTOR3, structure (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="da38b-103">D3DXVECTOR3 structure (D3dx9math.h)</span></span>

<span data-ttu-id="da38b-104">Décrit un vecteur à trois composants incluant des surcharges d’opérateur et des casts de type.</span><span class="sxs-lookup"><span data-stu-id="da38b-104">Describes a three-component vector including operator overloads and type casts.</span></span>

## <a name="syntax"></a><span data-ttu-id="da38b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da38b-105">Syntax</span></span>


```C++
typedef struct D3DXVECTOR3 {
  FLOAT x;
  FLOAT y;
  FLOAT z;
} D3DXVECTOR3, *LPD3DXVECTOR3;
```



## <a name="members"></a><span data-ttu-id="da38b-106">Membres</span><span class="sxs-lookup"><span data-stu-id="da38b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="da38b-107">**x**</span><span class="sxs-lookup"><span data-stu-id="da38b-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="da38b-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="da38b-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="da38b-109">Composant x.</span><span class="sxs-lookup"><span data-stu-id="da38b-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="da38b-110">**y**</span><span class="sxs-lookup"><span data-stu-id="da38b-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="da38b-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="da38b-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="da38b-112">Composant y.</span><span class="sxs-lookup"><span data-stu-id="da38b-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="da38b-113">**z**</span><span class="sxs-lookup"><span data-stu-id="da38b-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="da38b-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="da38b-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="da38b-115">Composant z.</span><span class="sxs-lookup"><span data-stu-id="da38b-115">The z-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da38b-116">Notes</span><span class="sxs-lookup"><span data-stu-id="da38b-116">Remarks</span></span>

### <a name="d3dxvector3-extensions"></a><span data-ttu-id="da38b-117">Extensions D3DXVECTOR3</span><span class="sxs-lookup"><span data-stu-id="da38b-117">D3DXVECTOR3 Extensions</span></span>

<span data-ttu-id="da38b-118">D3DXVECTOR3 a les extensions C++ suivantes.</span><span class="sxs-lookup"><span data-stu-id="da38b-118">D3DXVECTOR3 has the following C++ extensions.</span></span>


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

typedef struct D3DXVECTOR3_16F
{
#ifdef __cplusplus
public:
    D3DXVECTOR3_16F() {};
    D3DXVECTOR3_16F( CONST FLOAT * );
    D3DXVECTOR3_16F( CONST D3DVECTOR& );
    D3DXVECTOR3_16F( CONST D3DXFLOAT16 * );
    D3DXVECTOR3_16F( CONST D3DXFLOAT16 &x, CONST D3DXFLOAT16 &y, CONST D3DXFLOAT16 &z );

    // casting
    operator D3DXFLOAT16* ();
    operator CONST D3DXFLOAT16* () const;

    // binary operators
    BOOL operator == ( CONST D3DXVECTOR3_16F& ) const;
    BOOL operator != ( CONST D3DXVECTOR3_16F& ) const;

public:
#endif //__cplusplus
    D3DXFLOAT16 x, y, z;

} D3DXVECTOR3_16F, *LPD3DXVECTOR3_16F;
        
```



## <a name="requirements"></a><span data-ttu-id="da38b-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da38b-119">Requirements</span></span>



| <span data-ttu-id="da38b-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da38b-120">Requirement</span></span> | <span data-ttu-id="da38b-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="da38b-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="da38b-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="da38b-122">Header</span></span><br/> | <dl> <span data-ttu-id="da38b-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="da38b-123"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da38b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da38b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da38b-125">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="da38b-125">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
