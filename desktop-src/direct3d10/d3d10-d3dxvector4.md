---
description: Décrit un vecteur à quatre composants incluant des surcharges d’opérateur et des casts de type.
ms.assetid: c6348346-f317-48ed-a369-e39fdb4dc1d6
title: D3DXVECTOR4, structure (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR4
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: ce65fe5cc6de9d842fb7c93b1089e53b9b27920c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394231"
---
# <a name="d3dxvector4-structure-d3dx10mathh"></a><span data-ttu-id="37c40-103">D3DXVECTOR4, structure (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="37c40-103">D3DXVECTOR4 structure (D3DX10Math.h)</span></span>

<span data-ttu-id="37c40-104">Décrit un vecteur à quatre composants incluant des surcharges d’opérateur et des casts de type.</span><span class="sxs-lookup"><span data-stu-id="37c40-104">Describes a four-component vector including operator overloads and type casts.</span></span>

## <a name="syntax"></a><span data-ttu-id="37c40-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37c40-105">Syntax</span></span>


```C++
typedef struct D3DXVECTOR4 {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXVECTOR4, *LPD3DXVECTOR4;
```



## <a name="members"></a><span data-ttu-id="37c40-106">Membres</span><span class="sxs-lookup"><span data-stu-id="37c40-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="37c40-107">**x**</span><span class="sxs-lookup"><span data-stu-id="37c40-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="37c40-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="37c40-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="37c40-109">Composant x.</span><span class="sxs-lookup"><span data-stu-id="37c40-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="37c40-110">**y**</span><span class="sxs-lookup"><span data-stu-id="37c40-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="37c40-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="37c40-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="37c40-112">Composant y.</span><span class="sxs-lookup"><span data-stu-id="37c40-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="37c40-113">**z**</span><span class="sxs-lookup"><span data-stu-id="37c40-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="37c40-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="37c40-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="37c40-115">Composant z.</span><span class="sxs-lookup"><span data-stu-id="37c40-115">The z-component.</span></span>

</dd> <dt>

<span data-ttu-id="37c40-116">**w**</span><span class="sxs-lookup"><span data-stu-id="37c40-116">**w**</span></span>
</dt> <dd>

<span data-ttu-id="37c40-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="37c40-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="37c40-118">Composant w.</span><span class="sxs-lookup"><span data-stu-id="37c40-118">The w-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37c40-119">Notes</span><span class="sxs-lookup"><span data-stu-id="37c40-119">Remarks</span></span>

<span data-ttu-id="37c40-120">**D3DXVECTOR4** a les extensions C++ suivantes.</span><span class="sxs-lookup"><span data-stu-id="37c40-120">**D3DXVECTOR4** has the following C++ extensions.</span></span>

### <a name="d3dxvector4-extensions"></a><span data-ttu-id="37c40-121">Extensions D3DXVECTOR4</span><span class="sxs-lookup"><span data-stu-id="37c40-121">D3DXVECTOR4 Extensions</span></span>


```
typedef struct D3DXVECTOR4
{
#ifdef __cplusplus
public:
    D3DXVECTOR4() {};
    D3DXVECTOR4( CONST FLOAT* );
    D3DXVECTOR4( CONST D3DXFLOAT16 * );
    D3DXVECTOR4( CONST D3DVECTOR& xyz, FLOAT w );
    D3DXVECTOR4( FLOAT x, FLOAT y, FLOAT z, FLOAT w );

    // casting
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXVECTOR4& operator += ( CONST D3DXVECTOR4& );
    D3DXVECTOR4& operator -= ( CONST D3DXVECTOR4& );
    D3DXVECTOR4& operator *= ( FLOAT );
    D3DXVECTOR4& operator /= ( FLOAT );

    // unary operators
    D3DXVECTOR4 operator + () const;
    D3DXVECTOR4 operator - () const;

    // binary operators
    D3DXVECTOR4 operator + ( CONST D3DXVECTOR4& ) const;
    D3DXVECTOR4 operator - ( CONST D3DXVECTOR4& ) const;
    D3DXVECTOR4 operator * ( FLOAT ) const;
    D3DXVECTOR4 operator / ( FLOAT ) const;

    friend D3DXVECTOR4 operator * ( FLOAT, CONST D3DXVECTOR4& );

    BOOL operator == ( CONST D3DXVECTOR4& ) const;
    BOOL operator != ( CONST D3DXVECTOR4& ) const;

public:
#endif //__cplusplus
    FLOAT x, y, z, w;
} D3DXVECTOR4, *LPD3DXVECTOR4;
        
```



## <a name="requirements"></a><span data-ttu-id="37c40-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37c40-122">Requirements</span></span>



| <span data-ttu-id="37c40-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37c40-123">Requirement</span></span> | <span data-ttu-id="37c40-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="37c40-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37c40-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="37c40-125">Header</span></span><br/> | <dl> <span data-ttu-id="37c40-126"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="37c40-126"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37c40-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37c40-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37c40-128">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="37c40-128">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
