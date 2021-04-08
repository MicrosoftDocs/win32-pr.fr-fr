---
description: Définit le mode de fusion pris en charge.
ms.assetid: 60ff384c-15a0-4c6f-9e2c-59fdea76b7a1
title: Énumération D3DBLEND (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBLEND
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: d8d779ad714e396f9c9a82bbbc42ddd09b76e2ac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953816"
---
# <a name="d3dblend-enumeration"></a><span data-ttu-id="4fa2d-103">Énumération D3DBLEND</span><span class="sxs-lookup"><span data-stu-id="4fa2d-103">D3DBLEND enumeration</span></span>

<span data-ttu-id="4fa2d-104">Définit le mode de fusion pris en charge.</span><span class="sxs-lookup"><span data-stu-id="4fa2d-104">Defines the supported blend mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fa2d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4fa2d-105">Syntax</span></span>


```C++
typedef enum D3DBLEND { 
  D3DBLEND_ZERO             = 1,
  D3DBLEND_ONE              = 2,
  D3DBLEND_SRCCOLOR         = 3,
  D3DBLEND_INVSRCCOLOR      = 4,
  D3DBLEND_SRCALPHA         = 5,
  D3DBLEND_INVSRCALPHA      = 6,
  D3DBLEND_DESTALPHA        = 7,
  D3DBLEND_INVDESTALPHA     = 8,
  D3DBLEND_DESTCOLOR        = 9,
  D3DBLEND_INVDESTCOLOR     = 10,
  D3DBLEND_SRCALPHASAT      = 11,
  D3DBLEND_BOTHSRCALPHA     = 12,
  D3DBLEND_BOTHINVSRCALPHA  = 13,
  D3DBLEND_BLENDFACTOR      = 14,
  D3DBLEND_INVBLENDFACTOR   = 15,
  D3DBLEND_SRCCOLOR2        = 16,
  D3DBLEND_INVSRCCOLOR2     = 17,
  D3DBLEND_FORCE_DWORD      = 0x7fffffff
} D3DBLEND, *LPD3DBLEND;
```



## <a name="constants"></a><span data-ttu-id="4fa2d-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="4fa2d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4fa2d-107"><span id="D3DBLEND_ZERO"></span><span id="d3dblend_zero"></span>**D3DBLEND \_ zéro**</span><span class="sxs-lookup"><span data-stu-id="4fa2d-107"><span id="D3DBLEND_ZERO"></span><span id="d3dblend_zero"></span>**D3DBLEND\_ZERO**</span></span>
</dt> <dd>

<span data-ttu-id="4fa2d-108">Le facteur de fusion est (0, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="4fa2d-108">Blend factor is (0, 0, 0, 0).</span></span>

</dd> <dt>

<span data-ttu-id="4fa2d-109"><span id="D3DBLEND_ONE"></span><span id="d3dblend_one"></span>**D3DBLEND \_ un**</span><span class="sxs-lookup"><span data-stu-id="4fa2d-109"><span id="D3DBLEND_ONE"></span><span id="d3dblend_one"></span>**D3DBLEND\_ONE**</span></span>
</dt> <dd>

<span data-ttu-id="4fa2d-110">Le facteur de fusion est (1, 1, 1, 1).</span><span class="sxs-lookup"><span data-stu-id="4fa2d-110">Blend factor is (1, 1, 1, 1).</span></span>

</dd> <dt>

<span data-ttu-id="4fa2d-111"><span id="D3DBLEND_SRCCOLOR"></span><span id="d3dblend_srccolor"></span>**D3DBLEND \_ SRCCOLOR**</span><span class="sxs-lookup"><span data-stu-id="4fa2d-111"><span id="D3DBLEND_SRCCOLOR"></span><span id="d3dblend_srccolor"></span>**D3DBLEND\_SRCCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="4fa2d-112">Le facteur de fusion est (RS, GS, BS, As).</span><span class="sxs-lookup"><span data-stu-id="4fa2d-112">Blend factor is (Rₛ, Gₛ, Bₛ, Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="4fa2d-113"><span id="D3DBLEND_INVSRCCOLOR"></span><span id="d3dblend_invsrccolor"></span>**D3DBLEND \_ INVSRCCOLOR**</span><span class="sxs-lookup"><span data-stu-id="4fa2d-113"><span id="D3DBLEND_INVSRCCOLOR"></span><span id="d3dblend_invsrccolor"></span>**D3DBLEND\_INVSRCCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="4fa2d-114">Le facteur de fusion est (1-RS, 1-GS, 1-BS, 1-As).</span><span class="sxs-lookup"><span data-stu-id="4fa2d-114">Blend factor is (1 - Rₛ, 1 - Gₛ, 1 - Bₛ, 1 - Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="4fa2d-115"><span id="D3DBLEND_SRCALPHA"></span><span id="d3dblend_srcalpha"></span>**D3DBLEND \_ SRCALPHA**</span><span class="sxs-lookup"><span data-stu-id="4fa2d-115"><span id="D3DBLEND_SRCALPHA"></span><span id="d3dblend_srcalpha"></span>**D3DBLEND\_SRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="4fa2d-116">Le facteur de fusion est (As, As, As, As).</span><span class="sxs-lookup"><span data-stu-id="4fa2d-116">Blend factor is (Aₛ, Aₛ, Aₛ, Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="4fa2d-117"><span id="D3DBLEND_INVSRCALPHA"></span><span id="d3dblend_invsrcalpha"></span>**D3DBLEND \_ INVSRCALPHA**</span><span class="sxs-lookup"><span data-stu-id="4fa2d-117"><span id="D3DBLEND_INVSRCALPHA"></span><span id="d3dblend_invsrcalpha"></span>**D3DBLEND\_INVSRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="4fa2d-118">Le facteur de fusion est (1-As, 1-As, 1-As, 1-As).</span><span class="sxs-lookup"><span data-stu-id="4fa2d-118">Blend factor is ( 1 - Aₛ, 1 - Aₛ, 1 - Aₛ, 1 - Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="4fa2d-119"><span id="D3DBLEND_DESTALPHA"></span><span id="d3dblend_destalpha"></span>**D3DBLEND \_ DESTALPHA**</span><span class="sxs-lookup"><span data-stu-id="4fa2d-119"><span id="D3DBLEND_DESTALPHA"></span><span id="d3dblend_destalpha"></span>**D3DBLEND\_DESTALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="4fa2d-120">Le<sub>facteur de fusion</sub> est<sub>(a d a d</sub> <sub>a d</sub> <sub>).</sub></span><span class="sxs-lookup"><span data-stu-id="4fa2d-120">Blend factor is (A<sub>d</sub> A<sub>d</sub> A<sub>d</sub> A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="4fa2d-121"><span id="D3DBLEND_INVDESTALPHA"></span><span id="d3dblend_invdestalpha"></span>**D3DBLEND \_ INVDESTALPHA**</span><span class="sxs-lookup"><span data-stu-id="4fa2d-121"><span id="D3DBLEND_INVDESTALPHA"></span><span id="d3dblend_invdestalpha"></span>**D3DBLEND\_INVDESTALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="4fa2d-122">Le facteur de fusion est (1-A<sub>d</sub> 1-a<sub>d</sub> 1-A<sub>d</sub> 1-a<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="4fa2d-122">Blend factor is (1 - A<sub>d</sub> 1 - A<sub>d</sub> 1 - A<sub>d</sub> 1 - A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="4fa2d-123"><span id="D3DBLEND_DESTCOLOR"></span><span id="d3dblend_destcolor"></span>**D3DBLEND \_ DESTCOLOR**</span><span class="sxs-lookup"><span data-stu-id="4fa2d-123"><span id="D3DBLEND_DESTCOLOR"></span><span id="d3dblend_destcolor"></span>**D3DBLEND\_DESTCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="4fa2d-124">Le facteur de fusion est (R<sub>d</sub>, G<sub>d</sub>, B<sub>d</sub>, A<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="4fa2d-124">Blend factor is (R<sub>d</sub>, G<sub>d</sub>, B<sub>d</sub>, A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="4fa2d-125"><span id="D3DBLEND_INVDESTCOLOR"></span><span id="d3dblend_invdestcolor"></span>**D3DBLEND \_ INVDESTCOLOR**</span><span class="sxs-lookup"><span data-stu-id="4fa2d-125"><span id="D3DBLEND_INVDESTCOLOR"></span><span id="d3dblend_invdestcolor"></span>**D3DBLEND\_INVDESTCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="4fa2d-126">Le facteur de fusion est (1-R<sub>d</sub>, 1-G<sub>d</sub>, 1-B<sub>d</sub>, 1-A<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="4fa2d-126">Blend factor is (1 - R<sub>d</sub>, 1 - G<sub>d</sub>, 1 - B<sub>d</sub>, 1 - A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="4fa2d-127"><span id="D3DBLEND_SRCALPHASAT"></span><span id="d3dblend_srcalphasat"></span>**D3DBLEND \_ SRCALPHASAT**</span><span class="sxs-lookup"><span data-stu-id="4fa2d-127"><span id="D3DBLEND_SRCALPHASAT"></span><span id="d3dblend_srcalphasat"></span>**D3DBLEND\_SRCALPHASAT**</span></span>
</dt> <dd>

<span data-ttu-id="4fa2d-128">Le facteur de fusion est (f, f, f, 1); où f = min (As, 1-A<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="4fa2d-128">Blend factor is (f, f, f, 1); where f = min(Aₛ, 1 - A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="4fa2d-129"><span id="D3DBLEND_BOTHSRCALPHA"></span><span id="d3dblend_bothsrcalpha"></span>**D3DBLEND \_ BOTHSRCALPHA**</span><span class="sxs-lookup"><span data-stu-id="4fa2d-129"><span id="D3DBLEND_BOTHSRCALPHA"></span><span id="d3dblend_bothsrcalpha"></span>**D3DBLEND\_BOTHSRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="4fa2d-130">**Obsolète**.</span><span class="sxs-lookup"><span data-stu-id="4fa2d-130">**Obsolete**.</span></span> <span data-ttu-id="4fa2d-131">À partir de DirectX 6, vous pouvez obtenir le même effet en définissant les facteurs de fusion source et destination sur D3DBLEND \_ SRCALPHA et D3DBLEND \_ INVSRCALPHA dans des appels distincts.</span><span class="sxs-lookup"><span data-stu-id="4fa2d-131">Starting with DirectX 6, you can achieve the same effect by setting the source and destination blend factors to D3DBLEND\_SRCALPHA and D3DBLEND\_INVSRCALPHA in separate calls.</span></span>

</dd> <dt>

<span data-ttu-id="4fa2d-132"><span id="D3DBLEND_BOTHINVSRCALPHA"></span><span id="d3dblend_bothinvsrcalpha"></span>**D3DBLEND \_ BOTHINVSRCALPHA**</span><span class="sxs-lookup"><span data-stu-id="4fa2d-132"><span id="D3DBLEND_BOTHINVSRCALPHA"></span><span id="d3dblend_bothinvsrcalpha"></span>**D3DBLEND\_BOTHINVSRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="4fa2d-133">**Obsolète**.</span><span class="sxs-lookup"><span data-stu-id="4fa2d-133">**Obsolete**.</span></span> <span data-ttu-id="4fa2d-134">Le facteur de fusion source est (1-As, 1-As, 1-As, 1-As) et le facteur de fusion de destination est (As, As, As); la sélection Blend de destination est remplacée.</span><span class="sxs-lookup"><span data-stu-id="4fa2d-134">Source blend factor is (1 - Aₛ, 1 - Aₛ, 1 - Aₛ, 1 - Aₛ), and destination blend factor is (Aₛ, Aₛ, Aₛ, Aₛ); the destination blend selection is overridden.</span></span> <span data-ttu-id="4fa2d-135">Ce mode de fusion est pris en charge uniquement pour l' \_ État de rendu D3DRS SRCBLEND.</span><span class="sxs-lookup"><span data-stu-id="4fa2d-135">This blend mode is supported only for the D3DRS\_SRCBLEND render state.</span></span>

</dd> <dt>

<span data-ttu-id="4fa2d-136"><span id="D3DBLEND_BLENDFACTOR"></span><span id="d3dblend_blendfactor"></span>**D3DBLEND \_ BLENDFACTOR**</span><span class="sxs-lookup"><span data-stu-id="4fa2d-136"><span id="D3DBLEND_BLENDFACTOR"></span><span id="d3dblend_blendfactor"></span>**D3DBLEND\_BLENDFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="4fa2d-137">Facteur de fusion de couleur constant utilisé par le mélangeur de mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="4fa2d-137">Constant color blending factor used by the frame-buffer blender.</span></span> <span data-ttu-id="4fa2d-138">Ce mode de fusion est pris en charge uniquement si D3DPBLENDCAPS \_ BLENDFACTOR est défini dans les membres **SrcBlendCaps** ou **DestBlendCaps** de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="4fa2d-138">This blend mode is supported only if D3DPBLENDCAPS\_BLENDFACTOR is set in the **SrcBlendCaps** or **DestBlendCaps** members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="4fa2d-139"><span id="D3DBLEND_INVBLENDFACTOR"></span><span id="d3dblend_invblendfactor"></span>**D3DBLEND \_ INVBLENDFACTOR**</span><span class="sxs-lookup"><span data-stu-id="4fa2d-139"><span id="D3DBLEND_INVBLENDFACTOR"></span><span id="d3dblend_invblendfactor"></span>**D3DBLEND\_INVBLENDFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="4fa2d-140">Facteur de fusion de couleur inversé inversé utilisé par le mélangeur de mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="4fa2d-140">Inverted constant color-blending factor used by the frame-buffer blender.</span></span> <span data-ttu-id="4fa2d-141">Ce mode de fusion est pris en charge uniquement si le \_ bit D3DPBLENDCAPS BLENDFACTOR est défini dans les membres **SrcBlendCaps** ou **DestBlendCaps** de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="4fa2d-141">This blend mode is supported only if the D3DPBLENDCAPS\_BLENDFACTOR bit is set in the **SrcBlendCaps** or **DestBlendCaps** members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="4fa2d-142"><span id="D3DBLEND_SRCCOLOR2"></span><span id="d3dblend_srccolor2"></span>**D3DBLEND \_ SRCCOLOR2**</span><span class="sxs-lookup"><span data-stu-id="4fa2d-142"><span id="D3DBLEND_SRCCOLOR2"></span><span id="d3dblend_srccolor2"></span>**D3DBLEND\_SRCCOLOR2**</span></span>
</dt> <dd>

<span data-ttu-id="4fa2d-143">Le facteur de fusion est (PSOutColor \[ 1 \] <sub>r</sub>, PSOutColor \[ 1 \] <sub>g</sub>, PSOutColor \[ 1 \] <sub>b</sub>, non utilisé).</span><span class="sxs-lookup"><span data-stu-id="4fa2d-143">Blend factor is (PSOutColor\[1\]<sub>r</sub>, PSOutColor\[1\]<sub>g</sub>, PSOutColor\[1\]<sub>b</sub>, not used).</span></span> <span data-ttu-id="4fa2d-144">Consultez [fusion de cibles de rendu](#render-target-blending).</span><span class="sxs-lookup"><span data-stu-id="4fa2d-144">See [Render Target Blending](#render-target-blending).</span></span>



|                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fa2d-145">Différences entre Direct3D 9 et Direct3D 9Ex :</span><span class="sxs-lookup"><span data-stu-id="4fa2d-145">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="4fa2d-146">Cet indicateur est disponible uniquement dans Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="4fa2d-146">This flag is available in Direct3D 9Ex only.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4fa2d-147"><span id="D3DBLEND_INVSRCCOLOR2"></span><span id="d3dblend_invsrccolor2"></span>**D3DBLEND \_ INVSRCCOLOR2**</span><span class="sxs-lookup"><span data-stu-id="4fa2d-147"><span id="D3DBLEND_INVSRCCOLOR2"></span><span id="d3dblend_invsrccolor2"></span>**D3DBLEND\_INVSRCCOLOR2**</span></span>
</dt> <dd>

<span data-ttu-id="4fa2d-148">Le facteur de fusion est (1-PSOutColor \[ 1 \] <sub>r</sub>, 1-PSOutColor \[ 1 \] <sub>g</sub>, 1-PSOutColor \[ 1 \] <sub>b</sub>, non utilisé)).</span><span class="sxs-lookup"><span data-stu-id="4fa2d-148">Blend factor is (1 - PSOutColor\[1\]<sub>r</sub>, 1 - PSOutColor\[1\]<sub>g</sub>, 1 - PSOutColor\[1\]<sub>b</sub>, not used)).</span></span> <span data-ttu-id="4fa2d-149">Consultez [fusion de cibles de rendu](#render-target-blending).</span><span class="sxs-lookup"><span data-stu-id="4fa2d-149">See [Render Target Blending](#render-target-blending).</span></span>



|                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fa2d-150">Différences entre Direct3D 9 et Direct3D 9Ex :</span><span class="sxs-lookup"><span data-stu-id="4fa2d-150">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="4fa2d-151">Cet indicateur est disponible uniquement dans Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="4fa2d-151">This flag is available in Direct3D 9Ex only.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4fa2d-152"><span id="D3DBLEND_FORCE_DWORD"></span><span id="d3dblend_force_dword"></span>**D3DBLEND \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="4fa2d-152"><span id="D3DBLEND_FORCE_DWORD"></span><span id="d3dblend_force_dword"></span>**D3DBLEND\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="4fa2d-153">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="4fa2d-153">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="4fa2d-154">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4fa2d-154">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="4fa2d-155">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4fa2d-155">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4fa2d-156">Notes</span><span class="sxs-lookup"><span data-stu-id="4fa2d-156">Remarks</span></span>

<span data-ttu-id="4fa2d-157">Dans les descriptions de membre précédentes, les valeurs RVBA de la source et de la destination sont indiquées par les indices s et d.</span><span class="sxs-lookup"><span data-stu-id="4fa2d-157">In the preceding member descriptions, the RGBA values of the source and destination are indicated by the s and d subscripts.</span></span>

<span data-ttu-id="4fa2d-158">Les valeurs de ce type énuméré sont utilisées par les États de rendu suivants :</span><span class="sxs-lookup"><span data-stu-id="4fa2d-158">The values in this enumerated type are used by the following render states:</span></span>

-   <span data-ttu-id="4fa2d-159">D3DRS \_ DESTBLEND</span><span class="sxs-lookup"><span data-stu-id="4fa2d-159">D3DRS\_DESTBLEND</span></span>
-   <span data-ttu-id="4fa2d-160">D3DRS \_ SRCBLEND</span><span class="sxs-lookup"><span data-stu-id="4fa2d-160">D3DRS\_SRCBLEND</span></span>
-   <span data-ttu-id="4fa2d-161">D3DRS \_ DESTBLENDALPHA</span><span class="sxs-lookup"><span data-stu-id="4fa2d-161">D3DRS\_DESTBLENDALPHA</span></span>
-   <span data-ttu-id="4fa2d-162">D3DRS \_ SRCBLENDALPHA</span><span class="sxs-lookup"><span data-stu-id="4fa2d-162">D3DRS\_SRCBLENDALPHA</span></span>

<span data-ttu-id="4fa2d-163">Voir [ **D3DRENDERSTATETYPE**](./d3drenderstatetype.md)</span><span class="sxs-lookup"><span data-stu-id="4fa2d-163">See [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)</span></span>

### <a name="render-target-blending"></a><span data-ttu-id="4fa2d-164">Fusion de la cible de rendu</span><span class="sxs-lookup"><span data-stu-id="4fa2d-164">Render Target Blending</span></span>

<span data-ttu-id="4fa2d-165">Direct3D 9Ex a amélioré les fonctionnalités de rendu de texte.</span><span class="sxs-lookup"><span data-stu-id="4fa2d-165">Direct3D 9Ex has improved text rendering capabilities.</span></span> <span data-ttu-id="4fa2d-166">Le rendu des polices Clear-type nécessite normalement deux passes.</span><span class="sxs-lookup"><span data-stu-id="4fa2d-166">Rendering clear-type fonts would normally require two passes.</span></span> <span data-ttu-id="4fa2d-167">Pour éliminer la deuxième passe, un nuanceur de pixels peut être utilisé pour sortir deux couleurs, que nous pouvons appeler PSOutColor \[ 0 \] et PSOutColor \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="4fa2d-167">To eliminate the second pass, a pixel shader can be used to output two colors, which we can call PSOutColor\[0\] and PSOutColor\[1\].</span></span> <span data-ttu-id="4fa2d-168">La première couleur contient les composants RVB (standard 3 Color Components).</span><span class="sxs-lookup"><span data-stu-id="4fa2d-168">The first color would contain the standard 3 color components (RGB).</span></span> <span data-ttu-id="4fa2d-169">La deuxième couleur contient 3 composants alpha (un pour chaque composant de la première couleur).</span><span class="sxs-lookup"><span data-stu-id="4fa2d-169">The second color would contain 3 alpha components (one for each component of the first color).</span></span>

<span data-ttu-id="4fa2d-170">Ces nouveaux modes de fusion sont utilisés uniquement pour le rendu de texte sur la première cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="4fa2d-170">These new blending modes are only used for text rendering on the first render target.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fa2d-171">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4fa2d-171">Requirements</span></span>



| <span data-ttu-id="4fa2d-172">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4fa2d-172">Requirement</span></span> | <span data-ttu-id="4fa2d-173">Valeur</span><span class="sxs-lookup"><span data-stu-id="4fa2d-173">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4fa2d-174">En-tête</span><span class="sxs-lookup"><span data-stu-id="4fa2d-174">Header</span></span><br/> | <dl> <span data-ttu-id="4fa2d-175"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fa2d-175"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fa2d-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fa2d-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fa2d-177">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="4fa2d-177">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 
