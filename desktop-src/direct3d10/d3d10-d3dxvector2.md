---
description: Décrit un vecteur à deux composants, notamment des surcharges d’opérateur et des casts de type.
ms.assetid: 5b7b4847-b994-48c6-ae3c-e48ee1716ddd
title: D3DXVECTOR2, structure (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR2
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 860c7ddaba61adcd93a38469117b2a95779240a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211866"
---
# <a name="d3dxvector2-structure-d3dx10mathh"></a><span data-ttu-id="b96e8-103">D3DXVECTOR2, structure (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="b96e8-103">D3DXVECTOR2 structure (D3DX10Math.h)</span></span>

<span data-ttu-id="b96e8-104">Décrit un vecteur à deux composants, notamment des surcharges d’opérateur et des casts de type.</span><span class="sxs-lookup"><span data-stu-id="b96e8-104">Describes a two-component vector including operator overloads and type casts.</span></span>

## <a name="syntax"></a><span data-ttu-id="b96e8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b96e8-105">Syntax</span></span>


```C++
typedef struct D3DXVECTOR2 {
  FLOAT x;
  FLOAT y;
} D3DXVECTOR2, *LPD3DXVECTOR2;
```



## <a name="members"></a><span data-ttu-id="b96e8-106">Membres</span><span class="sxs-lookup"><span data-stu-id="b96e8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b96e8-107">**x**</span><span class="sxs-lookup"><span data-stu-id="b96e8-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="b96e8-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b96e8-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b96e8-109">Composant x.</span><span class="sxs-lookup"><span data-stu-id="b96e8-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="b96e8-110">**y**</span><span class="sxs-lookup"><span data-stu-id="b96e8-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="b96e8-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b96e8-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b96e8-112">Composant y.</span><span class="sxs-lookup"><span data-stu-id="b96e8-112">The y-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b96e8-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b96e8-113">Remarks</span></span>

<span data-ttu-id="b96e8-114">**D3DXVECTOR2** a les extensions C++ suivantes.</span><span class="sxs-lookup"><span data-stu-id="b96e8-114">**D3DXVECTOR2** has the following C++ extensions.</span></span>

### <a name="d3dxvector2-extensions"></a><span data-ttu-id="b96e8-115">Extensions D3DXVECTOR2</span><span class="sxs-lookup"><span data-stu-id="b96e8-115">D3DXVECTOR2 Extensions</span></span>


```
typedef struct D3DXVECTOR2
{
#ifdef __cplusplus
public:
    D3DXVECTOR2() {};
    D3DXVECTOR2( CONST FLOAT * );
    D3DXVECTOR2( CONST D3DXFLOAT16 * );
    D3DXVECTOR2( FLOAT x, FLOAT y );

    // casting
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXVECTOR2& operator += ( CONST D3DXVECTOR2& );
    D3DXVECTOR2& operator -= ( CONST D3DXVECTOR2& );
    D3DXVECTOR2& operator *= ( FLOAT );
    D3DXVECTOR2& operator /= ( FLOAT );

    // unary operators
    D3DXVECTOR2 operator + () const;
    D3DXVECTOR2 operator - () const;

    // binary operators
    D3DXVECTOR2 operator + ( CONST D3DXVECTOR2& ) const;
    D3DXVECTOR2 operator - ( CONST D3DXVECTOR2& ) const;
    D3DXVECTOR2 operator * ( FLOAT ) const;
    D3DXVECTOR2 operator / ( FLOAT ) const;

    friend D3DXVECTOR2 operator * ( FLOAT, CONST D3DXVECTOR2& );

    BOOL operator == ( CONST D3DXVECTOR2& ) const;
    BOOL operator != ( CONST D3DXVECTOR2& ) const;


public:
#endif //__cplusplus
    FLOAT x, y;
} D3DXVECTOR2, *LPD3DXVECTOR2;
        
```



## <a name="requirements"></a><span data-ttu-id="b96e8-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b96e8-116">Requirements</span></span>



| <span data-ttu-id="b96e8-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b96e8-117">Requirement</span></span> | <span data-ttu-id="b96e8-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b96e8-118">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b96e8-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="b96e8-119">Header</span></span><br/> | <dl> <span data-ttu-id="b96e8-120"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b96e8-120"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b96e8-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b96e8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b96e8-122">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="b96e8-122">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
