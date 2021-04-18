---
description: Décrit un correctif rectangulaire de poids fort.
ms.assetid: 5f195009-d047-4dc0-a386-e1a434914e34
title: Structure D3DRECTPATCH_INFO (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRECTPATCH_INFO
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: a2b7fedbaac2cc9c204d4691828d31794cea1f47
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523198"
---
# <a name="d3drectpatch_info-structure"></a><span data-ttu-id="66cf6-103">\_Structure d’informations D3DRECTPATCH</span><span class="sxs-lookup"><span data-stu-id="66cf6-103">D3DRECTPATCH\_INFO structure</span></span>

<span data-ttu-id="66cf6-104">Décrit un correctif rectangulaire de poids fort.</span><span class="sxs-lookup"><span data-stu-id="66cf6-104">Describes a rectangular high-order patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="66cf6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66cf6-105">Syntax</span></span>


```C++
typedef struct D3DRECTPATCH_INFO {
  UINT          StartVertexOffsetWidth;
  UINT          StartVertexOffsetHeight;
  UINT          Width;
  UINT          Height;
  UINT          Stride;
  D3DBASISTYPE  Basis;
  D3DDEGREETYPE Degree;
} D3DRECTPATCH_INFO, *LPD3DRECTPATCH_INFO;
```



## <a name="members"></a><span data-ttu-id="66cf6-106">Membres</span><span class="sxs-lookup"><span data-stu-id="66cf6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="66cf6-107">**StartVertexOffsetWidth**</span><span class="sxs-lookup"><span data-stu-id="66cf6-107">**StartVertexOffsetWidth**</span></span>
</dt> <dd>

<span data-ttu-id="66cf6-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66cf6-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="66cf6-109">Largeur du décalage du vertex de départ, en nombre de vertex.</span><span class="sxs-lookup"><span data-stu-id="66cf6-109">Starting vertex offset width, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="66cf6-110">**StartVertexOffsetHeight**</span><span class="sxs-lookup"><span data-stu-id="66cf6-110">**StartVertexOffsetHeight**</span></span>
</dt> <dd>

<span data-ttu-id="66cf6-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66cf6-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="66cf6-112">Hauteur du décalage du vertex de départ, en nombre de vertex.</span><span class="sxs-lookup"><span data-stu-id="66cf6-112">Starting vertex offset height, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="66cf6-113">**Width**</span><span class="sxs-lookup"><span data-stu-id="66cf6-113">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="66cf6-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66cf6-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="66cf6-115">Largeur de chaque vertex, en nombre de vertex.</span><span class="sxs-lookup"><span data-stu-id="66cf6-115">Width of each vertex, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="66cf6-116">**Height**</span><span class="sxs-lookup"><span data-stu-id="66cf6-116">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="66cf6-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66cf6-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="66cf6-118">Hauteur de chaque vertex, en nombre de vertex.</span><span class="sxs-lookup"><span data-stu-id="66cf6-118">Height of each vertex, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="66cf6-119">**Progrès**</span><span class="sxs-lookup"><span data-stu-id="66cf6-119">**Stride**</span></span>
</dt> <dd>

<span data-ttu-id="66cf6-120">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66cf6-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="66cf6-121">Largeur du tableau de vertex imaginaire à deux dimensions, qui occupe le même espace que la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="66cf6-121">Width of the imaginary two-dimensional vertex array, which occupies the same space as the vertex buffer.</span></span> <span data-ttu-id="66cf6-122">Pour obtenir un exemple, consultez le diagramme ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="66cf6-122">For an example, see the diagram below.</span></span>

</dd> <dt>

<span data-ttu-id="66cf6-123">**basis**</span><span class="sxs-lookup"><span data-stu-id="66cf6-123">**Basis**</span></span>
</dt> <dd>

<span data-ttu-id="66cf6-124">Type : **[ **D3DBASISTYPE**](./d3dbasistype.md)**</span><span class="sxs-lookup"><span data-stu-id="66cf6-124">Type: **[**D3DBASISTYPE**](./d3dbasistype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="66cf6-125">Membre du type énuméré [**D3DBASISTYPE**](./d3dbasistype.md) , définissant le type de base pour le correctif rectangulaire de poids fort.</span><span class="sxs-lookup"><span data-stu-id="66cf6-125">Member of the [**D3DBASISTYPE**](./d3dbasistype.md) enumerated type, defining the basis type for the rectangular high-order patch.</span></span>



| <span data-ttu-id="66cf6-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="66cf6-126">Value</span></span>                 | <span data-ttu-id="66cf6-127">Commande prise en charge</span><span class="sxs-lookup"><span data-stu-id="66cf6-127">Order supported</span></span>            | <span data-ttu-id="66cf6-128">Largeur et hauteur</span><span class="sxs-lookup"><span data-stu-id="66cf6-128">Width and height</span></span>                  |
|-----------------------|----------------------------|-----------------------------------|
| <span data-ttu-id="66cf6-129">D3DBASIS \_ Bézier</span><span class="sxs-lookup"><span data-stu-id="66cf6-129">D3DBASIS\_BEZIER</span></span>      | <span data-ttu-id="66cf6-130">Linéaire, cubique et quintaux</span><span class="sxs-lookup"><span data-stu-id="66cf6-130">Linear, cubic, and quintic</span></span> | <span data-ttu-id="66cf6-131">Width = hauteur = (DWORD) ordre + 1</span><span class="sxs-lookup"><span data-stu-id="66cf6-131">Width = height = (DWORD)order + 1</span></span> |
| <span data-ttu-id="66cf6-132">D3DBASIS \_ BSPLINE</span><span class="sxs-lookup"><span data-stu-id="66cf6-132">D3DBASIS\_BSPLINE</span></span>     | <span data-ttu-id="66cf6-133">Linéaire, cubique et quintaux</span><span class="sxs-lookup"><span data-stu-id="66cf6-133">Linear, cubic, and quintic</span></span> | <span data-ttu-id="66cf6-134">Width = hauteur > (DWORD) Order</span><span class="sxs-lookup"><span data-stu-id="66cf6-134">Width = height > (DWORD)order</span></span>  |
| <span data-ttu-id="66cf6-135">\_Interpolation D3DBASIS</span><span class="sxs-lookup"><span data-stu-id="66cf6-135">D3DBASIS\_INTERPOLATE</span></span> | <span data-ttu-id="66cf6-136">Mètres</span><span class="sxs-lookup"><span data-stu-id="66cf6-136">Cubic</span></span>                      | <span data-ttu-id="66cf6-137">Width = hauteur > (DWORD) Order</span><span class="sxs-lookup"><span data-stu-id="66cf6-137">Width = height > (DWORD)order</span></span>  |



 

</dd> <dt>

<span data-ttu-id="66cf6-138">**Degré**</span><span class="sxs-lookup"><span data-stu-id="66cf6-138">**Degree**</span></span>
</dt> <dd>

<span data-ttu-id="66cf6-139">Type : **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**</span><span class="sxs-lookup"><span data-stu-id="66cf6-139">Type: **[**D3DDEGREETYPE**](./d3ddegreetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="66cf6-140">Membre du type énuméré [**D3DDEGREETYPE**](./d3ddegreetype.md) , définissant le degré pour le correctif rectangulaire.</span><span class="sxs-lookup"><span data-stu-id="66cf6-140">Member of the [**D3DDEGREETYPE**](./d3ddegreetype.md) enumerated type, defining the degree for the rectangular patch.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="66cf6-141">Notes</span><span class="sxs-lookup"><span data-stu-id="66cf6-141">Remarks</span></span>

<span data-ttu-id="66cf6-142">Le diagramme suivant identifie les paramètres qui spécifient un correctif de rectangle.</span><span class="sxs-lookup"><span data-stu-id="66cf6-142">The following diagram identifies the parameters that specify a rectangle patch.</span></span>

![diagramme d’un correctif de poids fort rectangulaire et des paramètres qui le spécifient](images/hop-rectpatch.png)

<span data-ttu-id="66cf6-144">Chacun des vertex de la mémoire tampon de vertex est affiché sous la forme d’un point noir.</span><span class="sxs-lookup"><span data-stu-id="66cf6-144">Each of the vertices in the vertex buffer is shown as a black dot.</span></span> <span data-ttu-id="66cf6-145">Dans ce cas, la mémoire tampon de vertex contient 20 sommets, dont 16 dans le carreau de rectangle.</span><span class="sxs-lookup"><span data-stu-id="66cf6-145">In this case, the vertex buffer has 20 vertices in it, 16 of which are in the rectangle patch.</span></span> <span data-ttu-id="66cf6-146">Le Stride est le nombre de vertex dans la largeur de la mémoire tampon de vertex, dans ce cas cinq.</span><span class="sxs-lookup"><span data-stu-id="66cf6-146">The stride is the number of vertices in the width of the vertex buffer, in this case five.</span></span> <span data-ttu-id="66cf6-147">Le décalage x du premier vertex est appelé StartIndexVertexWidth et est dans ce cas 1.</span><span class="sxs-lookup"><span data-stu-id="66cf6-147">The x offset to the first vertex is called the StartIndexVertexWidth and is in this case 1.</span></span> <span data-ttu-id="66cf6-148">Le décalage y du premier vertex patch est appelé StartIndexVertexHeight et est dans ce cas 0.</span><span class="sxs-lookup"><span data-stu-id="66cf6-148">The y offset to the first patch vertex is called the StartIndexVertexHeight and is in this case 0.</span></span>

<span data-ttu-id="66cf6-149">Pour afficher un flux de différents correctifs rectangulaires (non-mosaïques), vous devez interpréter votre géométrie comme un correctif rectangulaire long (1 x N).</span><span class="sxs-lookup"><span data-stu-id="66cf6-149">To render a stream of individual rectangular patches (non-mosaic), you should interpret your geometry as a long narrow (1 x N) rectangular patch.</span></span> <span data-ttu-id="66cf6-150">La structure d' **\_ informations D3DRECTPATCH** pour une telle bande (Bézier cubique) est configurée de la manière suivante.</span><span class="sxs-lookup"><span data-stu-id="66cf6-150">The **D3DRECTPATCH\_INFO** structure for such a strip (cubic Bézier) would be set up in the following manner.</span></span>


```
    
D3DRECTPATCH_INFO RectInfo;

RectInfo.Width = 4;
RectInfo.Height = 4;
RectInfo.Stride = 4;
RectInfo.Basis = D3DBASIS_BEZIER;
RectInfo.Order = D3DORDER_CUBIC;
RectInfo.StartVertexOffsetWidth = 0;
RectInfo.StartVertexOffsetHeight = 4*i;  // The variable i is the index of the 
//   patch you want to render.
```



## <a name="requirements"></a><span data-ttu-id="66cf6-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66cf6-151">Requirements</span></span>



| <span data-ttu-id="66cf6-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66cf6-152">Requirement</span></span> | <span data-ttu-id="66cf6-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="66cf6-153">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66cf6-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="66cf6-154">Header</span></span><br/> | <dl> <span data-ttu-id="66cf6-155"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="66cf6-155"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66cf6-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66cf6-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66cf6-157">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="66cf6-157">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="66cf6-158">**DrawRectPatch**</span><span class="sxs-lookup"><span data-stu-id="66cf6-158">**DrawRectPatch**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch)
</dt> <dt>

[<span data-ttu-id="66cf6-159">**D3DXTessellateRectPatch**</span><span class="sxs-lookup"><span data-stu-id="66cf6-159">**D3DXTessellateRectPatch**</span></span>](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
