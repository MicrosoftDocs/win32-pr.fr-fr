---
description: Type d'objet.
ms.assetid: ab405984-2ebc-4514-9400-bdb13676eda5
title: Énumération D3DXPARAMETER_CLASS (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_CLASS
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: c42bfc9335c38de04ab484193a1e178a122f2210
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870082"
---
# <a name="d3dxparameter_class-enumeration"></a><span data-ttu-id="215bf-103">\_Énumération de la classe D3DXPARAMETER</span><span class="sxs-lookup"><span data-stu-id="215bf-103">D3DXPARAMETER\_CLASS enumeration</span></span>

<span data-ttu-id="215bf-104">Type d'objet.</span><span class="sxs-lookup"><span data-stu-id="215bf-104">The type of object.</span></span>

## <a name="syntax"></a><span data-ttu-id="215bf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="215bf-105">Syntax</span></span>


```C++
typedef enum D3DXPARAMETER_CLASS { 
  D3DXPC_SCALAR,
  D3DXPC_VECTOR,
  D3DXPC_MATRIX_ROWS,
  D3DXPC_MATRIX_COLUMNS,
  D3DXPC_OBJECT,
  D3DXPC_STRUCT,
  D3DXPC_FORCE_DWORD     = 0x7fffffff
} D3DXPARAMETER_CLASS, *LPD3DXPARAMETER_CLASS;
```



## <a name="constants"></a><span data-ttu-id="215bf-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="215bf-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="215bf-107"><span id="D3DXPC_SCALAR"></span><span id="d3dxpc_scalar"></span>**\_Scalaire D3DXPC**</span><span class="sxs-lookup"><span data-stu-id="215bf-107"><span id="D3DXPC_SCALAR"></span><span id="d3dxpc_scalar"></span>**D3DXPC\_SCALAR**</span></span>
</dt> <dd>

<span data-ttu-id="215bf-108">La constante est un scalaire.</span><span class="sxs-lookup"><span data-stu-id="215bf-108">Constant is a scalar.</span></span>

</dd> <dt>

<span data-ttu-id="215bf-109"><span id="D3DXPC_VECTOR"></span><span id="d3dxpc_vector"></span>**\_Vecteur D3DXPC**</span><span class="sxs-lookup"><span data-stu-id="215bf-109"><span id="D3DXPC_VECTOR"></span><span id="d3dxpc_vector"></span>**D3DXPC\_VECTOR**</span></span>
</dt> <dd>

<span data-ttu-id="215bf-110">La constante est un vecteur.</span><span class="sxs-lookup"><span data-stu-id="215bf-110">Constant is a vector.</span></span>

</dd> <dt>

<span data-ttu-id="215bf-111"><span id="D3DXPC_MATRIX_ROWS"></span><span id="d3dxpc_matrix_rows"></span>**Lignes de la \_ matrice D3DXPC \_**</span><span class="sxs-lookup"><span data-stu-id="215bf-111"><span id="D3DXPC_MATRIX_ROWS"></span><span id="d3dxpc_matrix_rows"></span>**D3DXPC\_MATRIX\_ROWS**</span></span>
</dt> <dd>

<span data-ttu-id="215bf-112">La constante est une matrice principale de ligne.</span><span class="sxs-lookup"><span data-stu-id="215bf-112">Constant is a row major matrix.</span></span>

</dd> <dt>

<span data-ttu-id="215bf-113"><span id="D3DXPC_MATRIX_COLUMNS"></span><span id="d3dxpc_matrix_columns"></span>**\_Colonnes de matrice D3DXPC \_**</span><span class="sxs-lookup"><span data-stu-id="215bf-113"><span id="D3DXPC_MATRIX_COLUMNS"></span><span id="d3dxpc_matrix_columns"></span>**D3DXPC\_MATRIX\_COLUMNS**</span></span>
</dt> <dd>

<span data-ttu-id="215bf-114">La constante est une matrice principale de colonne.</span><span class="sxs-lookup"><span data-stu-id="215bf-114">Constant is a column major matrix.</span></span>

</dd> <dt>

<span data-ttu-id="215bf-115"><span id="D3DXPC_OBJECT"></span><span id="d3dxpc_object"></span>**\_Objet D3DXPC**</span><span class="sxs-lookup"><span data-stu-id="215bf-115"><span id="D3DXPC_OBJECT"></span><span id="d3dxpc_object"></span>**D3DXPC\_OBJECT**</span></span>
</dt> <dd>

<span data-ttu-id="215bf-116">La constante est une texture, un nuanceur ou une chaîne.</span><span class="sxs-lookup"><span data-stu-id="215bf-116">Constant is either a texture, shader, or a string.</span></span>

</dd> <dt>

<span data-ttu-id="215bf-117"><span id="D3DXPC_STRUCT"></span><span id="d3dxpc_struct"></span>**\_Struct D3DXPC**</span><span class="sxs-lookup"><span data-stu-id="215bf-117"><span id="D3DXPC_STRUCT"></span><span id="d3dxpc_struct"></span>**D3DXPC\_STRUCT**</span></span>
</dt> <dd>

<span data-ttu-id="215bf-118">La constante est une structure.</span><span class="sxs-lookup"><span data-stu-id="215bf-118">Constant is a structure.</span></span>

</dd> <dt>

<span data-ttu-id="215bf-119"><span id="D3DXPC_FORCE_DWORD"></span><span id="d3dxpc_force_dword"></span>**D3DXPC \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="215bf-119"><span id="D3DXPC_FORCE_DWORD"></span><span id="d3dxpc_force_dword"></span>**D3DXPC\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="215bf-120">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="215bf-120">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="215bf-121">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="215bf-121">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="215bf-122">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="215bf-122">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="215bf-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="215bf-123">Requirements</span></span>



| <span data-ttu-id="215bf-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="215bf-124">Requirement</span></span> | <span data-ttu-id="215bf-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="215bf-125">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="215bf-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="215bf-126">Header</span></span><br/> | <dl> <span data-ttu-id="215bf-127"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="215bf-127"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="215bf-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="215bf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="215bf-129">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="215bf-129">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="215bf-130">**D3DXSHADER \_ TypeInfo**</span><span class="sxs-lookup"><span data-stu-id="215bf-130">**D3DXSHADER\_TYPEINFO**</span></span>](d3dxshader-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="215bf-131">**D3DXCONSTANT \_ desc**</span><span class="sxs-lookup"><span data-stu-id="215bf-131">**D3DXCONSTANT\_DESC**</span></span>](d3dxconstant-desc.md)
</dt> </dl>

 

 




