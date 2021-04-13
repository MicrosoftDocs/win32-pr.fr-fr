---
description: Spécifie les attributs de poids de maille.
ms.assetid: 554bb8f2-9e92-4e9e-b500-c3cc47d57830
title: Structure D3DX10_ATTRIBUTE_WEIGHTS (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ATTRIBUTE_WEIGHTS
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 4f137c1ecc29c184c4dec3995fb0202741ce9f09
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323021"
---
# <a name="d3dx10_attribute_weights-structure"></a><span data-ttu-id="22132-103">\_Structure des \_ pondérations d’attribut d3dx10</span><span class="sxs-lookup"><span data-stu-id="22132-103">D3DX10\_ATTRIBUTE\_WEIGHTS structure</span></span>

<span data-ttu-id="22132-104">Spécifie les attributs de poids de maille.</span><span class="sxs-lookup"><span data-stu-id="22132-104">Specifies mesh weight attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="22132-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22132-105">Syntax</span></span>


```C++
typedef struct D3DX10_ATTRIBUTE_WEIGHTS {
  FLOAT Position;
  FLOAT Boundary;
  FLOAT Normal;
  FLOAT Diffuse;
  FLOAT Specular;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
} D3DX10_ATTRIBUTE_WEIGHTS, *LPD3DX10_ATTRIBUTE_WEIGHTS;
```



## <a name="members"></a><span data-ttu-id="22132-106">Membres</span><span class="sxs-lookup"><span data-stu-id="22132-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="22132-107">**Position**</span><span class="sxs-lookup"><span data-stu-id="22132-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="22132-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="22132-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="22132-109">Endroit.</span><span class="sxs-lookup"><span data-stu-id="22132-109">Position.</span></span>

</dd> <dt>

<span data-ttu-id="22132-110">**Limite**</span><span class="sxs-lookup"><span data-stu-id="22132-110">**Boundary**</span></span>
</dt> <dd>

<span data-ttu-id="22132-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="22132-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="22132-112">Poids de fusion.</span><span class="sxs-lookup"><span data-stu-id="22132-112">Blend weight.</span></span>

</dd> <dt>

<span data-ttu-id="22132-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="22132-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="22132-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="22132-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="22132-115">Normal.</span><span class="sxs-lookup"><span data-stu-id="22132-115">Normal.</span></span>

</dd> <dt>

<span data-ttu-id="22132-116">**Diffus**</span><span class="sxs-lookup"><span data-stu-id="22132-116">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="22132-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="22132-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="22132-118">Valeur d’éclairage diffus.</span><span class="sxs-lookup"><span data-stu-id="22132-118">Diffuse lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="22132-119">**Spéculaire**</span><span class="sxs-lookup"><span data-stu-id="22132-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="22132-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="22132-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="22132-121">Valeur d’éclairage spéculaire.</span><span class="sxs-lookup"><span data-stu-id="22132-121">Specular lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="22132-122">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="22132-122">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="22132-123">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="22132-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="22132-124">Huit coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="22132-124">Eight texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="22132-125">**Tangence**</span><span class="sxs-lookup"><span data-stu-id="22132-125">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="22132-126">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="22132-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="22132-127">Tangence.</span><span class="sxs-lookup"><span data-stu-id="22132-127">Tangent.</span></span>

</dd> <dt>

<span data-ttu-id="22132-128">**Binormal**</span><span class="sxs-lookup"><span data-stu-id="22132-128">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="22132-129">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="22132-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="22132-130">Binormal.</span><span class="sxs-lookup"><span data-stu-id="22132-130">Binormal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="22132-131">Notes</span><span class="sxs-lookup"><span data-stu-id="22132-131">Remarks</span></span>

<span data-ttu-id="22132-132">Cette structure décrit comment une opération de simplification prend en compte les données de vertex lors du calcul des coûts relatifs entre les bords réduits.</span><span class="sxs-lookup"><span data-stu-id="22132-132">This structure describes how a simplification operation will consider vertex data when calculating relative costs between collapsing edges.</span></span> <span data-ttu-id="22132-133">Par exemple, si le champ normal est 0,0, l’opération de simplification ignore le composant de vertex normal lors du calcul de l’erreur pour la réduction.</span><span class="sxs-lookup"><span data-stu-id="22132-133">For example, if the Normal field is 0.0, the simplification operation will ignore the vertex normal component when calculating the error for the collapse.</span></span> <span data-ttu-id="22132-134">Toutefois, si le champ normal est 1,0, l’opération de simplification utilise le composant de vertex normal.</span><span class="sxs-lookup"><span data-stu-id="22132-134">However, if the Normal field is 1.0, the simplification operation will use the vertex normal component.</span></span> <span data-ttu-id="22132-135">Si le champ normal est 2,0, doublez le nombre d’erreurs ; Si le champ normal est 4,0, Quadruplez le nombre d’erreurs, etc.</span><span class="sxs-lookup"><span data-stu-id="22132-135">If the Normal field is 2.0, double the amount of errors; if the Normal field is 4.0, then quadruple the number of errors, and so on.</span></span>

<span data-ttu-id="22132-136">Le \_ type de \_ poids de l’attribut LPD3DX est défini en tant que pointeur vers la \_ structure des pondérations de l’attribut D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="22132-136">The LPD3DX\_ATTRIBUTE\_WEIGHTS type is defined as a pointer to the D3DX\_ATTRIBUTE\_WEIGHTS structure.</span></span>


```
    typedef D3DX_ATTRIBUTE_WEIGHTS* LPD3DX_ATTRIBUTE_WEIGHTS;
```



## <a name="requirements"></a><span data-ttu-id="22132-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22132-137">Requirements</span></span>



| <span data-ttu-id="22132-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22132-138">Requirement</span></span> | <span data-ttu-id="22132-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="22132-139">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="22132-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="22132-140">Header</span></span><br/> | <dl> <span data-ttu-id="22132-141"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="22132-141"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22132-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22132-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22132-143">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="22132-143">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
