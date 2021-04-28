---
description: 'Structure D3DXATTRIBUTEWEIGHTS : spécifie les attributs de poids de maille.'
ms.assetid: 8901a0fe-e38a-4045-8e8d-584be2620cc3
title: D3DXATTRIBUTEWEIGHTS, structure (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXATTRIBUTEWEIGHTS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 7a833d2a58db0f434f836126926e461cd2ee3ea0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115967"
---
# <a name="d3dxattributeweights-structure"></a><span data-ttu-id="7412b-103">D3DXATTRIBUTEWEIGHTS, structure</span><span class="sxs-lookup"><span data-stu-id="7412b-103">D3DXATTRIBUTEWEIGHTS structure</span></span>

<span data-ttu-id="7412b-104">Spécifie les attributs de poids de maille.</span><span class="sxs-lookup"><span data-stu-id="7412b-104">Specifies mesh weight attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="7412b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7412b-105">Syntax</span></span>


```C++
typedef struct D3DXATTRIBUTEWEIGHTS {
  FLOAT Position;
  FLOAT Boundary;
  FLOAT Normal;
  FLOAT Diffuse;
  FLOAT Specular;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
} D3DXATTRIBUTEWEIGHTS, *LPD3DXATTRIBUTEWEIGHTS;
```



## <a name="members"></a><span data-ttu-id="7412b-106">Membres</span><span class="sxs-lookup"><span data-stu-id="7412b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7412b-107">**Position**</span><span class="sxs-lookup"><span data-stu-id="7412b-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="7412b-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7412b-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7412b-109">Endroit.</span><span class="sxs-lookup"><span data-stu-id="7412b-109">Position.</span></span>

</dd> <dt>

<span data-ttu-id="7412b-110">**Limite**</span><span class="sxs-lookup"><span data-stu-id="7412b-110">**Boundary**</span></span>
</dt> <dd>

<span data-ttu-id="7412b-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7412b-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7412b-112">Poids de fusion.</span><span class="sxs-lookup"><span data-stu-id="7412b-112">Blend weight.</span></span>

</dd> <dt>

<span data-ttu-id="7412b-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="7412b-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="7412b-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7412b-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7412b-115">Normal.</span><span class="sxs-lookup"><span data-stu-id="7412b-115">Normal.</span></span>

</dd> <dt>

<span data-ttu-id="7412b-116">**Diffus**</span><span class="sxs-lookup"><span data-stu-id="7412b-116">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="7412b-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7412b-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7412b-118">Valeur d’éclairage diffus.</span><span class="sxs-lookup"><span data-stu-id="7412b-118">Diffuse lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="7412b-119">**Spéculaire**</span><span class="sxs-lookup"><span data-stu-id="7412b-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="7412b-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7412b-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7412b-121">Valeur d’éclairage spéculaire.</span><span class="sxs-lookup"><span data-stu-id="7412b-121">Specular lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="7412b-122">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="7412b-122">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="7412b-123">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7412b-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7412b-124">Huit coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="7412b-124">Eight texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="7412b-125">**Tangente**</span><span class="sxs-lookup"><span data-stu-id="7412b-125">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="7412b-126">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7412b-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7412b-127">Tangence.</span><span class="sxs-lookup"><span data-stu-id="7412b-127">Tangent.</span></span>

</dd> <dt>

<span data-ttu-id="7412b-128">**Binormal**</span><span class="sxs-lookup"><span data-stu-id="7412b-128">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="7412b-129">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7412b-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7412b-130">Binormal.</span><span class="sxs-lookup"><span data-stu-id="7412b-130">Binormal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7412b-131">Notes </span><span class="sxs-lookup"><span data-stu-id="7412b-131">Remarks</span></span>

<span data-ttu-id="7412b-132">Cette structure décrit comment une opération de simplification prend en compte les données de vertex lors du calcul des coûts relatifs entre les bords réduits.</span><span class="sxs-lookup"><span data-stu-id="7412b-132">This structure describes how a simplification operation will consider vertex data when calculating relative costs between collapsing edges.</span></span> <span data-ttu-id="7412b-133">Par exemple, si le champ normal est 0,0, l’opération de simplification ignore le composant de vertex normal lors du calcul de l’erreur pour la réduction.</span><span class="sxs-lookup"><span data-stu-id="7412b-133">For example, if the Normal field is 0.0, the simplification operation will ignore the vertex normal component when calculating the error for the collapse.</span></span> <span data-ttu-id="7412b-134">Toutefois, si le champ normal est 1,0, l’opération de simplification utilise le composant de vertex normal.</span><span class="sxs-lookup"><span data-stu-id="7412b-134">However, if the Normal field is 1.0, the simplification operation will use the vertex normal component.</span></span> <span data-ttu-id="7412b-135">Si le champ normal est 2,0, doublez le nombre d’erreurs ; Si le champ normal est 4,0, Quadruplez le nombre d’erreurs, etc.</span><span class="sxs-lookup"><span data-stu-id="7412b-135">If the Normal field is 2.0, double the amount of errors; if the Normal field is 4.0, then quadruple the number of errors, and so on.</span></span>

<span data-ttu-id="7412b-136">Le type LPD3DXATTRIBUTEWEIGHTS est défini en tant que pointeur vers la structure **D3DXATTRIBUTEWEIGHTS** .</span><span class="sxs-lookup"><span data-stu-id="7412b-136">The LPD3DXATTRIBUTEWEIGHTS type is defined as a pointer to the **D3DXATTRIBUTEWEIGHTS** structure.</span></span>


```
    
    typedef D3DXATTRIBUTEWEIGHTS* LPD3DXATTRIBUTEWEIGHTS;
```



## <a name="requirements"></a><span data-ttu-id="7412b-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7412b-137">Requirements</span></span>



| <span data-ttu-id="7412b-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7412b-138">Requirement</span></span> | <span data-ttu-id="7412b-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="7412b-139">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7412b-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="7412b-140">Header</span></span><br/> | <dl> <span data-ttu-id="7412b-141"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="7412b-141"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7412b-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7412b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7412b-143">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="7412b-143">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="7412b-144">**D3DXSimplifyMesh**</span><span class="sxs-lookup"><span data-stu-id="7412b-144">**D3DXSimplifyMesh**</span></span>](d3dxsimplifymesh.md)
</dt> </dl>

 

 
