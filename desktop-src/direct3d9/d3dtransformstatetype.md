---
description: Définit des constantes qui décrivent les valeurs d’état de transformation.
ms.assetid: 53535d9f-246a-42cf-82a2-fb3cf6d4ebac
title: Énumération D3DTRANSFORMSTATETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTRANSFORMSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 022aa20fab0739b32aa75eb5f4bc575c0a8ad853
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342994"
---
# <a name="d3dtransformstatetype-enumeration"></a><span data-ttu-id="6f36d-103">Énumération D3DTRANSFORMSTATETYPE</span><span class="sxs-lookup"><span data-stu-id="6f36d-103">D3DTRANSFORMSTATETYPE enumeration</span></span>

<span data-ttu-id="6f36d-104">Définit des constantes qui décrivent les valeurs d’état de transformation.</span><span class="sxs-lookup"><span data-stu-id="6f36d-104">Defines constants that describe transformation state values.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f36d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6f36d-105">Syntax</span></span>


```C++
typedef enum D3DTRANSFORMSTATETYPE { 
  D3DTS_VIEW         = 2,
  D3DTS_PROJECTION   = 3,
  D3DTS_TEXTURE0     = 16,
  D3DTS_TEXTURE1     = 17,
  D3DTS_TEXTURE2     = 18,
  D3DTS_TEXTURE3     = 19,
  D3DTS_TEXTURE4     = 20,
  D3DTS_TEXTURE5     = 21,
  D3DTS_TEXTURE6     = 22,
  D3DTS_TEXTURE7     = 23,
  D3DTS_FORCE_DWORD  = 0x7fffffff
} D3DTRANSFORMSTATETYPE, *LPD3DTRANSFORMSTATETYPE;
```



## <a name="constants"></a><span data-ttu-id="6f36d-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="6f36d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6f36d-107"><span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**\_Vue D3DTS**</span><span class="sxs-lookup"><span data-stu-id="6f36d-107"><span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**D3DTS\_VIEW**</span></span>
</dt> <dd>

<span data-ttu-id="6f36d-108">Identifie la matrice de transformation qui est définie comme matrice de transformation de la vue.</span><span class="sxs-lookup"><span data-stu-id="6f36d-108">Identifies the transformation matrix being set as the view transformation matrix.</span></span> <span data-ttu-id="6f36d-109">La valeur par défaut est **null** (la matrice d’identité).</span><span class="sxs-lookup"><span data-stu-id="6f36d-109">The default value is **NULL** (the identity matrix).</span></span>

</dd> <dt>

<span data-ttu-id="6f36d-110"><span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**\_Projection D3DTS**</span><span class="sxs-lookup"><span data-stu-id="6f36d-110"><span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**D3DTS\_PROJECTION**</span></span>
</dt> <dd>

<span data-ttu-id="6f36d-111">Identifie la matrice de transformation qui est définie comme matrice de transformation de projection.</span><span class="sxs-lookup"><span data-stu-id="6f36d-111">Identifies the transformation matrix being set as the projection transformation matrix.</span></span> <span data-ttu-id="6f36d-112">La valeur par défaut est **null** (la matrice d’identité).</span><span class="sxs-lookup"><span data-stu-id="6f36d-112">The default value is **NULL** (the identity matrix).</span></span>

</dd> <dt>

<span data-ttu-id="6f36d-113"><span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**D3DTS \_ TEXTURE0**</span><span class="sxs-lookup"><span data-stu-id="6f36d-113"><span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**D3DTS\_TEXTURE0**</span></span>
</dt> <dd>

<span data-ttu-id="6f36d-114">Identifie la matrice de transformation qui est définie pour l’étape de texture spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6f36d-114">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="6f36d-115"><span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**D3DTS \_ TEXTURE1**</span><span class="sxs-lookup"><span data-stu-id="6f36d-115"><span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**D3DTS\_TEXTURE1**</span></span>
</dt> <dd>

<span data-ttu-id="6f36d-116">Identifie la matrice de transformation qui est définie pour l’étape de texture spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6f36d-116">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="6f36d-117"><span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**D3DTS \_ TEXTURE2**</span><span class="sxs-lookup"><span data-stu-id="6f36d-117"><span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**D3DTS\_TEXTURE2**</span></span>
</dt> <dd>

<span data-ttu-id="6f36d-118">Identifie la matrice de transformation qui est définie pour l’étape de texture spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6f36d-118">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="6f36d-119"><span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**D3DTS \_ TEXTURE3**</span><span class="sxs-lookup"><span data-stu-id="6f36d-119"><span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**D3DTS\_TEXTURE3**</span></span>
</dt> <dd>

<span data-ttu-id="6f36d-120">Identifie la matrice de transformation qui est définie pour l’étape de texture spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6f36d-120">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="6f36d-121"><span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**D3DTS \_ TEXTURE4**</span><span class="sxs-lookup"><span data-stu-id="6f36d-121"><span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**D3DTS\_TEXTURE4**</span></span>
</dt> <dd>

<span data-ttu-id="6f36d-122">Identifie la matrice de transformation qui est définie pour l’étape de texture spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6f36d-122">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="6f36d-123"><span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**D3DTS \_ TEXTURE5**</span><span class="sxs-lookup"><span data-stu-id="6f36d-123"><span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**D3DTS\_TEXTURE5**</span></span>
</dt> <dd>

<span data-ttu-id="6f36d-124">Identifie la matrice de transformation qui est définie pour l’étape de texture spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6f36d-124">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="6f36d-125"><span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**D3DTS \_ TEXTURE6**</span><span class="sxs-lookup"><span data-stu-id="6f36d-125"><span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**D3DTS\_TEXTURE6**</span></span>
</dt> <dd>

<span data-ttu-id="6f36d-126">Identifie la matrice de transformation qui est définie pour l’étape de texture spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6f36d-126">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="6f36d-127"><span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**D3DTS \_ TEXTURE7**</span><span class="sxs-lookup"><span data-stu-id="6f36d-127"><span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**D3DTS\_TEXTURE7**</span></span>
</dt> <dd>

<span data-ttu-id="6f36d-128">Identifie la matrice de transformation qui est définie pour l’étape de texture spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6f36d-128">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="6f36d-129"><span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6f36d-129"><span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="6f36d-130">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="6f36d-130">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="6f36d-131">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6f36d-131">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="6f36d-132">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="6f36d-132">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6f36d-133">Remarques</span><span class="sxs-lookup"><span data-stu-id="6f36d-133">Remarks</span></span>

<span data-ttu-id="6f36d-134">Les États de transformation de la plage 256 à 511 sont réservés pour stocker jusqu’à 256 matrices universelles qui peuvent être indexées à l’aide des \_ macros D3DTS WORLDMATRIX et D3DTS \_ World.</span><span class="sxs-lookup"><span data-stu-id="6f36d-134">The transform states in the range 256 through 511 are reserved to store up to 256 world matrices that can be indexed using the D3DTS\_WORLDMATRIX and D3DTS\_WORLD macros.</span></span>



| <span data-ttu-id="6f36d-135">Macros</span><span class="sxs-lookup"><span data-stu-id="6f36d-135">Macros</span></span>                                                  | <span data-ttu-id="6f36d-136">Description</span><span class="sxs-lookup"><span data-stu-id="6f36d-136">Description</span></span>                                                                                                                                                                      |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f36d-137">**D3DTS \_ World**</span><span class="sxs-lookup"><span data-stu-id="6f36d-137">**D3DTS\_WORLD**</span></span>](d3dts-world.md)                     | <span data-ttu-id="6f36d-138">Équivalent à D3DTS \_ WORLDMATRIX (0).</span><span class="sxs-lookup"><span data-stu-id="6f36d-138">Equivalent to D3DTS\_WORLDMATRIX(0).</span></span>                                                                                                                                  |
| <span data-ttu-id="6f36d-139">[**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) (index)</span><span class="sxs-lookup"><span data-stu-id="6f36d-139">[**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) (index)</span></span> | <span data-ttu-id="6f36d-140">Identifie la matrice de transformation à définir pour la matrice universelle à l’index.</span><span class="sxs-lookup"><span data-stu-id="6f36d-140">Identifies the transform matrix to set for the world matrix at index.</span></span> <span data-ttu-id="6f36d-141">Plusieurs matrices universelles sont utilisées uniquement pour la fusion de vertex.</span><span class="sxs-lookup"><span data-stu-id="6f36d-141">Multiple world matrices are used only for vertex blending.</span></span> <span data-ttu-id="6f36d-142">Dans le cas contraire, seul D3DTS \_ World est utilisé.</span><span class="sxs-lookup"><span data-stu-id="6f36d-142">Otherwise only D3DTS\_WORLD is used.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="6f36d-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f36d-143">Requirements</span></span>



| <span data-ttu-id="6f36d-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f36d-144">Requirement</span></span> | <span data-ttu-id="6f36d-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f36d-145">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f36d-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="6f36d-146">Header</span></span><br/> | <dl> <span data-ttu-id="6f36d-147"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f36d-147"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f36d-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f36d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f36d-149">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="6f36d-149">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="6f36d-150">**IDirect3DDevice9::GetTransform**</span><span class="sxs-lookup"><span data-stu-id="6f36d-150">**IDirect3DDevice9::GetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[<span data-ttu-id="6f36d-151">**IDirect3DDevice9::MultiplyTransform**</span><span class="sxs-lookup"><span data-stu-id="6f36d-151">**IDirect3DDevice9::MultiplyTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[<span data-ttu-id="6f36d-152">**IDirect3DDevice9::SetTransform**</span><span class="sxs-lookup"><span data-stu-id="6f36d-152">**IDirect3DDevice9::SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[<span data-ttu-id="6f36d-153">**D3DTS \_ World**</span><span class="sxs-lookup"><span data-stu-id="6f36d-153">**D3DTS\_WORLD**</span></span>](d3dts-world.md)
</dt> <dt>

[<span data-ttu-id="6f36d-154">**D3DTS \_ worldn**</span><span class="sxs-lookup"><span data-stu-id="6f36d-154">**D3DTS\_WORLDn**</span></span>](d3dts-worldn.md)
</dt> <dt>

[<span data-ttu-id="6f36d-155">**D3DTS \_ WORLDMATRIX**</span><span class="sxs-lookup"><span data-stu-id="6f36d-155">**D3DTS\_WORLDMATRIX**</span></span>](d3dts-worldmatrix.md)
</dt> </dl>

 

 
