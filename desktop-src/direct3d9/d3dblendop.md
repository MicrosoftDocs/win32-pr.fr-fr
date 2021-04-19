---
description: Définit les opérations de fusion prises en charge. Consultez la section Notes pour connaître les définitions des termes.
ms.assetid: ae750d84-ed7d-4a76-bf64-eae8828c66c7
title: Énumération D3DBLENDOP (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBLENDOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3ad23d3fb2a93734047f55a46c14335069c95ea9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106524845"
---
# <a name="d3dblendop-enumeration"></a><span data-ttu-id="5ad6e-104">Énumération D3DBLENDOP</span><span class="sxs-lookup"><span data-stu-id="5ad6e-104">D3DBLENDOP enumeration</span></span>

<span data-ttu-id="5ad6e-105">Définit les opérations de fusion prises en charge.</span><span class="sxs-lookup"><span data-stu-id="5ad6e-105">Defines the supported blend operations.</span></span> <span data-ttu-id="5ad6e-106">Consultez la section Notes pour connaître les définitions des termes.</span><span class="sxs-lookup"><span data-stu-id="5ad6e-106">See Remarks for definitions of terms.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ad6e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ad6e-107">Syntax</span></span>


```C++
typedef enum D3DBLENDOP { 
  D3DBLENDOP_ADD          = 1,
  D3DBLENDOP_SUBTRACT     = 2,
  D3DBLENDOP_REVSUBTRACT  = 3,
  D3DBLENDOP_MIN          = 4,
  D3DBLENDOP_MAX          = 5,
  D3DBLENDOP_FORCE_DWORD  = 0x7fffffff
} D3DBLENDOP, *LPD3DBLENDOP;
```



## <a name="constants"></a><span data-ttu-id="5ad6e-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="5ad6e-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5ad6e-109"><span id="D3DBLENDOP_ADD"></span><span id="d3dblendop_add"></span>**D3DBLENDOP \_ Ajouter**</span><span class="sxs-lookup"><span data-stu-id="5ad6e-109"><span id="D3DBLENDOP_ADD"></span><span id="d3dblendop_add"></span>**D3DBLENDOP\_ADD**</span></span>
</dt> <dd>

<span data-ttu-id="5ad6e-110">Le résultat est la destination ajoutée à la source.</span><span class="sxs-lookup"><span data-stu-id="5ad6e-110">The result is the destination added to the source.</span></span> <span data-ttu-id="5ad6e-111">Résultat = source + destination</span><span class="sxs-lookup"><span data-stu-id="5ad6e-111">Result = Source + Destination</span></span>

</dd> <dt>

<span data-ttu-id="5ad6e-112"><span id="D3DBLENDOP_SUBTRACT"></span><span id="d3dblendop_subtract"></span>**D3DBLENDOP \_ soustraire**</span><span class="sxs-lookup"><span data-stu-id="5ad6e-112"><span id="D3DBLENDOP_SUBTRACT"></span><span id="d3dblendop_subtract"></span>**D3DBLENDOP\_SUBTRACT**</span></span>
</dt> <dd>

<span data-ttu-id="5ad6e-113">Le résultat est soustrait de la destination à la source.</span><span class="sxs-lookup"><span data-stu-id="5ad6e-113">The result is the destination subtracted from to the source.</span></span> <span data-ttu-id="5ad6e-114">Résultat = source-destination</span><span class="sxs-lookup"><span data-stu-id="5ad6e-114">Result = Source - Destination</span></span>

</dd> <dt>

<span data-ttu-id="5ad6e-115"><span id="D3DBLENDOP_REVSUBTRACT"></span><span id="d3dblendop_revsubtract"></span>**D3DBLENDOP \_ REVSUBTRACT**</span><span class="sxs-lookup"><span data-stu-id="5ad6e-115"><span id="D3DBLENDOP_REVSUBTRACT"></span><span id="d3dblendop_revsubtract"></span>**D3DBLENDOP\_REVSUBTRACT**</span></span>
</dt> <dd>

<span data-ttu-id="5ad6e-116">Le résultat est la source soustraite de la destination.</span><span class="sxs-lookup"><span data-stu-id="5ad6e-116">The result is the source subtracted from the destination.</span></span> <span data-ttu-id="5ad6e-117">Résultat = source-destination</span><span class="sxs-lookup"><span data-stu-id="5ad6e-117">Result = Destination - Source</span></span>

</dd> <dt>

<span data-ttu-id="5ad6e-118"><span id="D3DBLENDOP_MIN"></span><span id="d3dblendop_min"></span>**D3DBLENDOP \_ min.**</span><span class="sxs-lookup"><span data-stu-id="5ad6e-118"><span id="D3DBLENDOP_MIN"></span><span id="d3dblendop_min"></span>**D3DBLENDOP\_MIN**</span></span>
</dt> <dd>

<span data-ttu-id="5ad6e-119">Le résultat est le minimum de la source et de la destination.</span><span class="sxs-lookup"><span data-stu-id="5ad6e-119">The result is the minimum of the source and destination.</span></span> <span data-ttu-id="5ad6e-120">Résultat = MIN (source, destination)</span><span class="sxs-lookup"><span data-stu-id="5ad6e-120">Result = MIN(Source, Destination)</span></span>

</dd> <dt>

<span data-ttu-id="5ad6e-121"><span id="D3DBLENDOP_MAX"></span><span id="d3dblendop_max"></span>**D3DBLENDOP \_ Max**</span><span class="sxs-lookup"><span data-stu-id="5ad6e-121"><span id="D3DBLENDOP_MAX"></span><span id="d3dblendop_max"></span>**D3DBLENDOP\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="5ad6e-122">Le résultat est le maximum de la source et de la destination.</span><span class="sxs-lookup"><span data-stu-id="5ad6e-122">The result is the maximum of the source and destination.</span></span> <span data-ttu-id="5ad6e-123">Résultat = MAX (source, destination)</span><span class="sxs-lookup"><span data-stu-id="5ad6e-123">Result = MAX(Source, Destination)</span></span>

</dd> <dt>

<span data-ttu-id="5ad6e-124"><span id="D3DBLENDOP_FORCE_DWORD"></span><span id="d3dblendop_force_dword"></span>**D3DBLENDOP \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="5ad6e-124"><span id="D3DBLENDOP_FORCE_DWORD"></span><span id="d3dblendop_force_dword"></span>**D3DBLENDOP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="5ad6e-125">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="5ad6e-125">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="5ad6e-126">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="5ad6e-126">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="5ad6e-127">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="5ad6e-127">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ad6e-128">Notes</span><span class="sxs-lookup"><span data-stu-id="5ad6e-128">Remarks</span></span>

<span data-ttu-id="5ad6e-129">La source, la destination et le résultat sont définis comme suit :</span><span class="sxs-lookup"><span data-stu-id="5ad6e-129">Source, Destination, and Result are defined as:</span></span>



| <span data-ttu-id="5ad6e-130">Terme</span><span class="sxs-lookup"><span data-stu-id="5ad6e-130">Term</span></span>        | <span data-ttu-id="5ad6e-131">Type</span><span class="sxs-lookup"><span data-stu-id="5ad6e-131">Type</span></span>   | <span data-ttu-id="5ad6e-132">Description</span><span class="sxs-lookup"><span data-stu-id="5ad6e-132">Description</span></span>                                                            |
|-------------|--------|------------------------------------------------------------------------|
| <span data-ttu-id="5ad6e-133">Source</span><span class="sxs-lookup"><span data-stu-id="5ad6e-133">Source</span></span>      | <span data-ttu-id="5ad6e-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="5ad6e-134">Input</span></span>  | <span data-ttu-id="5ad6e-135">Couleur du pixel source avant l’opération.</span><span class="sxs-lookup"><span data-stu-id="5ad6e-135">Color of the source pixel before the operation.</span></span>                        |
| <span data-ttu-id="5ad6e-136">Destination</span><span class="sxs-lookup"><span data-stu-id="5ad6e-136">Destination</span></span> | <span data-ttu-id="5ad6e-137">Entrée</span><span class="sxs-lookup"><span data-stu-id="5ad6e-137">Input</span></span>  | <span data-ttu-id="5ad6e-138">Couleur du pixel dans la mémoire tampon de destination avant l’opération.</span><span class="sxs-lookup"><span data-stu-id="5ad6e-138">Color of the pixel in the destination buffer before the operation.</span></span>     |
| <span data-ttu-id="5ad6e-139">Résultats</span><span class="sxs-lookup"><span data-stu-id="5ad6e-139">Result</span></span>      | <span data-ttu-id="5ad6e-140">Output</span><span class="sxs-lookup"><span data-stu-id="5ad6e-140">Output</span></span> | <span data-ttu-id="5ad6e-141">Valeur retournée qui correspond à la couleur fusionnée résultant de l’opération.</span><span class="sxs-lookup"><span data-stu-id="5ad6e-141">Returned value that is the blended color resulting from the operation.</span></span> |



 

<span data-ttu-id="5ad6e-142">Ce type énuméré définit les valeurs utilisées par les États de rendu suivants :</span><span class="sxs-lookup"><span data-stu-id="5ad6e-142">This enumerated type defines values used by the following render states:</span></span>

-   <span data-ttu-id="5ad6e-143">D3DRS \_ BLENDOP</span><span class="sxs-lookup"><span data-stu-id="5ad6e-143">D3DRS\_BLENDOP</span></span>
-   <span data-ttu-id="5ad6e-144">D3DRS \_ BLENDOPALPHA</span><span class="sxs-lookup"><span data-stu-id="5ad6e-144">D3DRS\_BLENDOPALPHA</span></span>

## <a name="requirements"></a><span data-ttu-id="5ad6e-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ad6e-145">Requirements</span></span>



| <span data-ttu-id="5ad6e-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ad6e-146">Requirement</span></span> | <span data-ttu-id="5ad6e-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ad6e-147">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ad6e-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="5ad6e-148">Header</span></span><br/> | <dl> <span data-ttu-id="5ad6e-149"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ad6e-149"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ad6e-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ad6e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ad6e-151">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="5ad6e-151">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="5ad6e-152">**D3DCAPS9**</span><span class="sxs-lookup"><span data-stu-id="5ad6e-152">**D3DCAPS9**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[<span data-ttu-id="5ad6e-153">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="5ad6e-153">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
