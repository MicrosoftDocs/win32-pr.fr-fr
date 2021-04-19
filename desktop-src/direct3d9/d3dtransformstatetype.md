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
ms.openlocfilehash: c618e0e19bf7dd01dec73d35436f23189f9e78a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522348"
---
# <a name="d3dtransformstatetype-enumeration"></a><span data-ttu-id="ec3d7-103">Énumération D3DTRANSFORMSTATETYPE</span><span class="sxs-lookup"><span data-stu-id="ec3d7-103">D3DTRANSFORMSTATETYPE enumeration</span></span>

<span data-ttu-id="ec3d7-104">Définit des constantes qui décrivent les valeurs d’état de transformation.</span><span class="sxs-lookup"><span data-stu-id="ec3d7-104">Defines constants that describe transformation state values.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec3d7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec3d7-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="ec3d7-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="ec3d7-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ec3d7-107"><span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**\_Vue D3DTS**</span><span class="sxs-lookup"><span data-stu-id="ec3d7-107"><span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**D3DTS\_VIEW**</span></span>
</dt> <dd>

<span data-ttu-id="ec3d7-108">Identifie la matrice de transformation qui est définie comme matrice de transformation de la vue.</span><span class="sxs-lookup"><span data-stu-id="ec3d7-108">Identifies the transformation matrix being set as the view transformation matrix.</span></span> <span data-ttu-id="ec3d7-109">La valeur par défaut est **null** (la matrice d’identité).</span><span class="sxs-lookup"><span data-stu-id="ec3d7-109">The default value is **NULL** (the identity matrix).</span></span>

</dd> <dt>

<span data-ttu-id="ec3d7-110"><span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**\_Projection D3DTS**</span><span class="sxs-lookup"><span data-stu-id="ec3d7-110"><span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**D3DTS\_PROJECTION**</span></span>
</dt> <dd>

<span data-ttu-id="ec3d7-111">Identifie la matrice de transformation qui est définie comme matrice de transformation de projection.</span><span class="sxs-lookup"><span data-stu-id="ec3d7-111">Identifies the transformation matrix being set as the projection transformation matrix.</span></span> <span data-ttu-id="ec3d7-112">La valeur par défaut est **null** (la matrice d’identité).</span><span class="sxs-lookup"><span data-stu-id="ec3d7-112">The default value is **NULL** (the identity matrix).</span></span>

</dd> <dt>

<span data-ttu-id="ec3d7-113"><span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**D3DTS \_ TEXTURE0**</span><span class="sxs-lookup"><span data-stu-id="ec3d7-113"><span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**D3DTS\_TEXTURE0**</span></span>
</dt> <dd>

<span data-ttu-id="ec3d7-114">Identifie la matrice de transformation qui est définie pour l’étape de texture spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ec3d7-114">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="ec3d7-115"><span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**D3DTS \_ TEXTURE1**</span><span class="sxs-lookup"><span data-stu-id="ec3d7-115"><span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**D3DTS\_TEXTURE1**</span></span>
</dt> <dd>

<span data-ttu-id="ec3d7-116">Identifie la matrice de transformation qui est définie pour l’étape de texture spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ec3d7-116">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="ec3d7-117"><span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**D3DTS \_ TEXTURE2**</span><span class="sxs-lookup"><span data-stu-id="ec3d7-117"><span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**D3DTS\_TEXTURE2**</span></span>
</dt> <dd>

<span data-ttu-id="ec3d7-118">Identifie la matrice de transformation qui est définie pour l’étape de texture spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ec3d7-118">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="ec3d7-119"><span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**D3DTS \_ TEXTURE3**</span><span class="sxs-lookup"><span data-stu-id="ec3d7-119"><span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**D3DTS\_TEXTURE3**</span></span>
</dt> <dd>

<span data-ttu-id="ec3d7-120">Identifie la matrice de transformation qui est définie pour l’étape de texture spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ec3d7-120">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="ec3d7-121"><span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**D3DTS \_ TEXTURE4**</span><span class="sxs-lookup"><span data-stu-id="ec3d7-121"><span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**D3DTS\_TEXTURE4**</span></span>
</dt> <dd>

<span data-ttu-id="ec3d7-122">Identifie la matrice de transformation qui est définie pour l’étape de texture spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ec3d7-122">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="ec3d7-123"><span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**D3DTS \_ TEXTURE5**</span><span class="sxs-lookup"><span data-stu-id="ec3d7-123"><span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**D3DTS\_TEXTURE5**</span></span>
</dt> <dd>

<span data-ttu-id="ec3d7-124">Identifie la matrice de transformation qui est définie pour l’étape de texture spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ec3d7-124">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="ec3d7-125"><span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**D3DTS \_ TEXTURE6**</span><span class="sxs-lookup"><span data-stu-id="ec3d7-125"><span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**D3DTS\_TEXTURE6**</span></span>
</dt> <dd>

<span data-ttu-id="ec3d7-126">Identifie la matrice de transformation qui est définie pour l’étape de texture spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ec3d7-126">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="ec3d7-127"><span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**D3DTS \_ TEXTURE7**</span><span class="sxs-lookup"><span data-stu-id="ec3d7-127"><span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**D3DTS\_TEXTURE7**</span></span>
</dt> <dd>

<span data-ttu-id="ec3d7-128">Identifie la matrice de transformation qui est définie pour l’étape de texture spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ec3d7-128">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="ec3d7-129"><span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="ec3d7-129"><span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="ec3d7-130">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="ec3d7-130">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="ec3d7-131">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="ec3d7-131">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="ec3d7-132">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="ec3d7-132">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec3d7-133">Notes</span><span class="sxs-lookup"><span data-stu-id="ec3d7-133">Remarks</span></span>

<span data-ttu-id="ec3d7-134">Les États de transformation de la plage 256 à 511 sont réservés pour stocker jusqu’à 256 matrices universelles qui peuvent être indexées à l’aide des \_ macros D3DTS WORLDMATRIX et D3DTS \_ World.</span><span class="sxs-lookup"><span data-stu-id="ec3d7-134">The transform states in the range 256 through 511 are reserved to store up to 256 world matrices that can be indexed using the D3DTS\_WORLDMATRIX and D3DTS\_WORLD macros.</span></span>



| <span data-ttu-id="ec3d7-135">Macros</span><span class="sxs-lookup"><span data-stu-id="ec3d7-135">Macros</span></span>                                                  |                                                                                                                                                                       |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ec3d7-136">**D3DTS \_ World**</span><span class="sxs-lookup"><span data-stu-id="ec3d7-136">**D3DTS\_WORLD**</span></span>](d3dts-world.md)                     | <span data-ttu-id="ec3d7-137">Équivalent à D3DTS \_ WORLDMATRIX (0).</span><span class="sxs-lookup"><span data-stu-id="ec3d7-137">Equivalent to D3DTS\_WORLDMATRIX(0).</span></span>                                                                                                                                  |
| <span data-ttu-id="ec3d7-138">[**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) (index)</span><span class="sxs-lookup"><span data-stu-id="ec3d7-138">[**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) (index)</span></span> | <span data-ttu-id="ec3d7-139">Identifie la matrice de transformation à définir pour la matrice universelle à l’index.</span><span class="sxs-lookup"><span data-stu-id="ec3d7-139">Identifies the transform matrix to set for the world matrix at index.</span></span> <span data-ttu-id="ec3d7-140">Plusieurs matrices universelles sont utilisées uniquement pour la fusion de vertex.</span><span class="sxs-lookup"><span data-stu-id="ec3d7-140">Multiple world matrices are used only for vertex blending.</span></span> <span data-ttu-id="ec3d7-141">Dans le cas contraire, seul D3DTS \_ World est utilisé.</span><span class="sxs-lookup"><span data-stu-id="ec3d7-141">Otherwise only D3DTS\_WORLD is used.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="ec3d7-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec3d7-142">Requirements</span></span>



| <span data-ttu-id="ec3d7-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec3d7-143">Requirement</span></span> | <span data-ttu-id="ec3d7-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec3d7-144">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec3d7-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="ec3d7-145">Header</span></span><br/> | <dl> <span data-ttu-id="ec3d7-146"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec3d7-146"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec3d7-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec3d7-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec3d7-148">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="ec3d7-148">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="ec3d7-149">**IDirect3DDevice9::GetTransform**</span><span class="sxs-lookup"><span data-stu-id="ec3d7-149">**IDirect3DDevice9::GetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[<span data-ttu-id="ec3d7-150">**IDirect3DDevice9::MultiplyTransform**</span><span class="sxs-lookup"><span data-stu-id="ec3d7-150">**IDirect3DDevice9::MultiplyTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[<span data-ttu-id="ec3d7-151">**IDirect3DDevice9::SetTransform**</span><span class="sxs-lookup"><span data-stu-id="ec3d7-151">**IDirect3DDevice9::SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[<span data-ttu-id="ec3d7-152">**D3DTS \_ World**</span><span class="sxs-lookup"><span data-stu-id="ec3d7-152">**D3DTS\_WORLD**</span></span>](d3dts-world.md)
</dt> <dt>

[<span data-ttu-id="ec3d7-153">**D3DTS \_ worldn**</span><span class="sxs-lookup"><span data-stu-id="ec3d7-153">**D3DTS\_WORLDn**</span></span>](d3dts-worldn.md)
</dt> <dt>

[<span data-ttu-id="ec3d7-154">**D3DTS \_ WORLDMATRIX**</span><span class="sxs-lookup"><span data-stu-id="ec3d7-154">**D3DTS\_WORLDMATRIX**</span></span>](d3dts-worldmatrix.md)
</dt> </dl>

 

 
