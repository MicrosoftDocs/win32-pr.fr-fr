---
description: Décrit un correctif de poids fort triangulaire.
ms.assetid: 3f97120b-3b32-4f95-8614-7b263ff330db
title: Structure D3DTRIPATCH_INFO (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTRIPATCH_INFO
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b910d38025c44d6157a76aa3e3425ba46d628787
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532468"
---
# <a name="d3dtripatch_info-structure"></a><span data-ttu-id="cc541-103">\_Structure d’informations D3DTRIPATCH</span><span class="sxs-lookup"><span data-stu-id="cc541-103">D3DTRIPATCH\_INFO structure</span></span>

<span data-ttu-id="cc541-104">Décrit un correctif de poids fort triangulaire.</span><span class="sxs-lookup"><span data-stu-id="cc541-104">Describes a triangular high-order patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc541-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc541-105">Syntax</span></span>


```C++
typedef struct D3DTRIPATCH_INFO {
  UINT          StartVertexOffset;
  UINT          NumVertices;
  D3DBASISTYPE  Basis;
  D3DDEGREETYPE Degree;
} D3DTRIPATCH_INFO, *LPD3DTRIPATCH_INFO;
```



## <a name="members"></a><span data-ttu-id="cc541-106">Membres</span><span class="sxs-lookup"><span data-stu-id="cc541-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="cc541-107">**StartVertexOffset**</span><span class="sxs-lookup"><span data-stu-id="cc541-107">**StartVertexOffset**</span></span>
</dt> <dd>

<span data-ttu-id="cc541-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc541-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="cc541-109">Décalage de début du vertex, en nombre de vertex.</span><span class="sxs-lookup"><span data-stu-id="cc541-109">Starting vertex offset, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="cc541-110">**NumVertices**</span><span class="sxs-lookup"><span data-stu-id="cc541-110">**NumVertices**</span></span>
</dt> <dd>

<span data-ttu-id="cc541-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc541-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="cc541-112">Nombre de vertex.</span><span class="sxs-lookup"><span data-stu-id="cc541-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="cc541-113">**basis**</span><span class="sxs-lookup"><span data-stu-id="cc541-113">**Basis**</span></span>
</dt> <dd>

<span data-ttu-id="cc541-114">Type : **[ **D3DBASISTYPE**](./d3dbasistype.md)**</span><span class="sxs-lookup"><span data-stu-id="cc541-114">Type: **[**D3DBASISTYPE**](./d3dbasistype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="cc541-115">Membre du type énuméré [**D3DBASISTYPE**](./d3dbasistype.md) , qui définit le type de base pour le correctif de poids fort triangulaire.</span><span class="sxs-lookup"><span data-stu-id="cc541-115">Member of the [**D3DBASISTYPE**](./d3dbasistype.md) enumerated type, which defines the basis type for the triangular high-order patch.</span></span> <span data-ttu-id="cc541-116">La seule valeur valide pour ce membre est D3DBASIS \_ Bezier.</span><span class="sxs-lookup"><span data-stu-id="cc541-116">The only valid value for this member is D3DBASIS\_BEZIER.</span></span>

</dd> <dt>

<span data-ttu-id="cc541-117">**Degré**</span><span class="sxs-lookup"><span data-stu-id="cc541-117">**Degree**</span></span>
</dt> <dd>

<span data-ttu-id="cc541-118">Type : **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**</span><span class="sxs-lookup"><span data-stu-id="cc541-118">Type: **[**D3DDEGREETYPE**](./d3ddegreetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="cc541-119">Membre du type énuméré [**D3DDEGREETYPE**](./d3ddegreetype.md) , définissant le type de degré pour le correctif de poids fort triangulaire.</span><span class="sxs-lookup"><span data-stu-id="cc541-119">Member of the [**D3DDEGREETYPE**](./d3ddegreetype.md) enumerated type, defining the degree type for the triangular high-order patch.</span></span>



| <span data-ttu-id="cc541-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc541-120">Value</span></span>                | <span data-ttu-id="cc541-121">Nombre de vertex</span><span class="sxs-lookup"><span data-stu-id="cc541-121">Number of vertices</span></span> |
|----------------------|--------------------|
| <span data-ttu-id="cc541-122">D3DDEGREE \_ cubique</span><span class="sxs-lookup"><span data-stu-id="cc541-122">D3DDEGREE\_CUBIC</span></span>     | <span data-ttu-id="cc541-123">10</span><span class="sxs-lookup"><span data-stu-id="cc541-123">10</span></span>                 |
| <span data-ttu-id="cc541-124">D3DDEGREE \_ linéaire</span><span class="sxs-lookup"><span data-stu-id="cc541-124">D3DDEGREE\_LINEAR</span></span>    | <span data-ttu-id="cc541-125">3</span><span class="sxs-lookup"><span data-stu-id="cc541-125">3</span></span>                  |
| <span data-ttu-id="cc541-126">D3DDEGREE \_ quadratique</span><span class="sxs-lookup"><span data-stu-id="cc541-126">D3DDEGREE\_QUADRATIC</span></span> | <span data-ttu-id="cc541-127">N/A</span><span class="sxs-lookup"><span data-stu-id="cc541-127">N/A</span></span>                |
| <span data-ttu-id="cc541-128">D3DDEGREE \_ quintaux</span><span class="sxs-lookup"><span data-stu-id="cc541-128">D3DDEGREE\_QUINTIC</span></span>   | <span data-ttu-id="cc541-129">21</span><span class="sxs-lookup"><span data-stu-id="cc541-129">21</span></span>                 |



 

<span data-ttu-id="cc541-130">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="cc541-130">N/A - Not available.</span></span> <span data-ttu-id="cc541-131">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="cc541-131">Not supported.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cc541-132">Notes</span><span class="sxs-lookup"><span data-stu-id="cc541-132">Remarks</span></span>

<span data-ttu-id="cc541-133">Par exemple, le diagramme suivant identifie l’ordre des vertex et les numéros de segment pour un correctif de triangle de Bézier cubique.</span><span class="sxs-lookup"><span data-stu-id="cc541-133">For example, the following diagram identifies the vertex order and segment numbers for a cubic Bézier triangle patch.</span></span> <span data-ttu-id="cc541-134">L’ordre des vertex détermine les numéros de segment utilisés par [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch).</span><span class="sxs-lookup"><span data-stu-id="cc541-134">The vertex order determines the segment numbers used by [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch).</span></span> <span data-ttu-id="cc541-135">Le décalage est le nombre d’octets du premier vertex de patch de triangle dans la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="cc541-135">The offset is the number of bytes to the first triangle patch vertex in the vertex buffer.</span></span>

![diagramme d’un correctif de poids fort triangulaire avec neuf vertex](images/hop-tripatch-info.png)

## <a name="requirements"></a><span data-ttu-id="cc541-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc541-137">Requirements</span></span>



| <span data-ttu-id="cc541-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc541-138">Requirement</span></span> | <span data-ttu-id="cc541-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc541-139">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc541-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="cc541-140">Header</span></span><br/> | <dl> <span data-ttu-id="cc541-141"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc541-141"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc541-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc541-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc541-143">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="cc541-143">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="cc541-144">**DrawTriPatch**</span><span class="sxs-lookup"><span data-stu-id="cc541-144">**DrawTriPatch**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch)
</dt> <dt>

[<span data-ttu-id="cc541-145">**D3DXTessellateTriPatch**</span><span class="sxs-lookup"><span data-stu-id="cc541-145">**D3DXTessellateTriPatch**</span></span>](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
