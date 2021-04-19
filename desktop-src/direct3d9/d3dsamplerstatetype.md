---
description: Les États de l’échantillonneur définissent des opérations d’échantillonnage de texture, telles que l’adressage et le filtrage de texture.
ms.assetid: 03a6a5f1-5e4f-4ba8-be4a-74d78fbc85d0
title: Énumération D3DSAMPLERSTATETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSAMPLERSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3e12764db306e61422f8c06ef514f6fad59b3ed8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538500"
---
# <a name="d3dsamplerstatetype-enumeration"></a><span data-ttu-id="82a30-103">Énumération D3DSAMPLERSTATETYPE</span><span class="sxs-lookup"><span data-stu-id="82a30-103">D3DSAMPLERSTATETYPE enumeration</span></span>

<span data-ttu-id="82a30-104">Les États de l’échantillonneur définissent des opérations d’échantillonnage de texture, telles que l’adressage et le filtrage de texture.</span><span class="sxs-lookup"><span data-stu-id="82a30-104">Sampler states define texture sampling operations such as texture addressing and texture filtering.</span></span> <span data-ttu-id="82a30-105">Certains États de l’échantillonneur configurent le traitement des vertex et un traitement des pixels configurés.</span><span class="sxs-lookup"><span data-stu-id="82a30-105">Some sampler states set-up vertex processing, and some set-up pixel processing.</span></span> <span data-ttu-id="82a30-106">Les États de l’échantillonneur peuvent être enregistrés et restaurés à l’aide de stateblocks (consultez États d' [enregistrement et de restauration des blocs d’État (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="82a30-106">Sampler states can be saved and restored using stateblocks (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="82a30-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82a30-107">Syntax</span></span>


```C++
typedef enum D3DSAMPLERSTATETYPE { 
  D3DSAMP_ADDRESSU       = 1,
  D3DSAMP_ADDRESSV       = 2,
  D3DSAMP_ADDRESSW       = 3,
  D3DSAMP_BORDERCOLOR    = 4,
  D3DSAMP_MAGFILTER      = 5,
  D3DSAMP_MINFILTER      = 6,
  D3DSAMP_MIPFILTER      = 7,
  D3DSAMP_MIPMAPLODBIAS  = 8,
  D3DSAMP_MAXMIPLEVEL    = 9,
  D3DSAMP_MAXANISOTROPY  = 10,
  D3DSAMP_SRGBTEXTURE    = 11,
  D3DSAMP_ELEMENTINDEX   = 12,
  D3DSAMP_DMAPOFFSET     = 13,
  D3DSAMP_FORCE_DWORD    = 0x7fffffff
} D3DSAMPLERSTATETYPE, *LPD3DSAMPLERSTATETYPE;
```



## <a name="constants"></a><span data-ttu-id="82a30-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="82a30-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="82a30-109"><span id="D3DSAMP_ADDRESSU"></span><span id="d3dsamp_addressu"></span>**\_Adresse D3DSAMP**</span><span class="sxs-lookup"><span data-stu-id="82a30-109"><span id="D3DSAMP_ADDRESSU"></span><span id="d3dsamp_addressu"></span>**D3DSAMP\_ADDRESSU**</span></span>
</dt> <dd>

<span data-ttu-id="82a30-110">Texture-mode d’adresse pour la coordonnée u.</span><span class="sxs-lookup"><span data-stu-id="82a30-110">Texture-address mode for the u coordinate.</span></span> <span data-ttu-id="82a30-111">La valeur par défaut est D3DTADDRESS \_ Wrap.</span><span class="sxs-lookup"><span data-stu-id="82a30-111">The default is D3DTADDRESS\_WRAP.</span></span> <span data-ttu-id="82a30-112">Pour plus d’informations, consultez [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span><span class="sxs-lookup"><span data-stu-id="82a30-112">For more information, see [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span></span>

</dd> <dt>

<span data-ttu-id="82a30-113"><span id="D3DSAMP_ADDRESSV"></span><span id="d3dsamp_addressv"></span>**D3DSAMP \_ ADDRESSV**</span><span class="sxs-lookup"><span data-stu-id="82a30-113"><span id="D3DSAMP_ADDRESSV"></span><span id="d3dsamp_addressv"></span>**D3DSAMP\_ADDRESSV**</span></span>
</dt> <dd>

<span data-ttu-id="82a30-114">Texture-mode d’adresse pour la coordonnée v.</span><span class="sxs-lookup"><span data-stu-id="82a30-114">Texture-address mode for the v coordinate.</span></span> <span data-ttu-id="82a30-115">La valeur par défaut est D3DTADDRESS \_ Wrap.</span><span class="sxs-lookup"><span data-stu-id="82a30-115">The default is D3DTADDRESS\_WRAP.</span></span> <span data-ttu-id="82a30-116">Pour plus d’informations, consultez [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span><span class="sxs-lookup"><span data-stu-id="82a30-116">For more information, see [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span></span>

</dd> <dt>

<span data-ttu-id="82a30-117"><span id="D3DSAMP_ADDRESSW"></span><span id="d3dsamp_addressw"></span>**D3DSAMP \_ ADDRESSW**</span><span class="sxs-lookup"><span data-stu-id="82a30-117"><span id="D3DSAMP_ADDRESSW"></span><span id="d3dsamp_addressw"></span>**D3DSAMP\_ADDRESSW**</span></span>
</dt> <dd>

<span data-ttu-id="82a30-118">Texture-mode d’adresse pour la coordonnée w.</span><span class="sxs-lookup"><span data-stu-id="82a30-118">Texture-address mode for the w coordinate.</span></span> <span data-ttu-id="82a30-119">La valeur par défaut est D3DTADDRESS \_ Wrap.</span><span class="sxs-lookup"><span data-stu-id="82a30-119">The default is D3DTADDRESS\_WRAP.</span></span> <span data-ttu-id="82a30-120">Pour plus d’informations, consultez [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span><span class="sxs-lookup"><span data-stu-id="82a30-120">For more information, see [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span></span>

</dd> <dt>

<span data-ttu-id="82a30-121"><span id="D3DSAMP_BORDERCOLOR"></span><span id="d3dsamp_bordercolor"></span>**D3DSAMP \_ BORDERCOLOR**</span><span class="sxs-lookup"><span data-stu-id="82a30-121"><span id="D3DSAMP_BORDERCOLOR"></span><span id="d3dsamp_bordercolor"></span>**D3DSAMP\_BORDERCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="82a30-122">Couleur de la bordure ou [**D3DCOLOR**](d3dcolor.md)de type.</span><span class="sxs-lookup"><span data-stu-id="82a30-122">Border color or type [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="82a30-123">La couleur par défaut est 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="82a30-123">The default color is 0x00000000.</span></span>

</dd> <dt>

<span data-ttu-id="82a30-124"><span id="D3DSAMP_MAGFILTER"></span><span id="d3dsamp_magfilter"></span>**D3DSAMP \_ MAGFILTER**</span><span class="sxs-lookup"><span data-stu-id="82a30-124"><span id="D3DSAMP_MAGFILTER"></span><span id="d3dsamp_magfilter"></span>**D3DSAMP\_MAGFILTER**</span></span>
</dt> <dd>

<span data-ttu-id="82a30-125">Filtre d’agrandissement de type [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="82a30-125">Magnification filter of type [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span> <span data-ttu-id="82a30-126">La valeur par défaut est D3DTEXF \_ point.</span><span class="sxs-lookup"><span data-stu-id="82a30-126">The default value is D3DTEXF\_POINT.</span></span>

</dd> <dt>

<span data-ttu-id="82a30-127"><span id="D3DSAMP_MINFILTER"></span><span id="d3dsamp_minfilter"></span>**D3DSAMP \_ MINFILTER**</span><span class="sxs-lookup"><span data-stu-id="82a30-127"><span id="D3DSAMP_MINFILTER"></span><span id="d3dsamp_minfilter"></span>**D3DSAMP\_MINFILTER**</span></span>
</dt> <dd>

<span data-ttu-id="82a30-128">Filtre de minimisation de type [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="82a30-128">Minification filter of type [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span> <span data-ttu-id="82a30-129">La valeur par défaut est D3DTEXF \_ point.</span><span class="sxs-lookup"><span data-stu-id="82a30-129">The default value is D3DTEXF\_POINT.</span></span>

</dd> <dt>

<span data-ttu-id="82a30-130"><span id="D3DSAMP_MIPFILTER"></span><span id="d3dsamp_mipfilter"></span>**D3DSAMP \_ MIPFILTER**</span><span class="sxs-lookup"><span data-stu-id="82a30-130"><span id="D3DSAMP_MIPFILTER"></span><span id="d3dsamp_mipfilter"></span>**D3DSAMP\_MIPFILTER**</span></span>
</dt> <dd>

<span data-ttu-id="82a30-131">Filtre mipmap à utiliser pendant la minimisation.</span><span class="sxs-lookup"><span data-stu-id="82a30-131">Mipmap filter to use during minification.</span></span> <span data-ttu-id="82a30-132">Consultez [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="82a30-132">See [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span> <span data-ttu-id="82a30-133">La valeur par défaut est D3DTEXF \_ None.</span><span class="sxs-lookup"><span data-stu-id="82a30-133">The default value is D3DTEXF\_NONE.</span></span>

</dd> <dt>

<span data-ttu-id="82a30-134"><span id="D3DSAMP_MIPMAPLODBIAS"></span><span id="d3dsamp_mipmaplodbias"></span>**D3DSAMP \_ MIPMAPLODBIAS**</span><span class="sxs-lookup"><span data-stu-id="82a30-134"><span id="D3DSAMP_MIPMAPLODBIAS"></span><span id="d3dsamp_mipmaplodbias"></span>**D3DSAMP\_MIPMAPLODBIAS**</span></span>
</dt> <dd>

<span data-ttu-id="82a30-135">Biais du niveau de détail mipmap.</span><span class="sxs-lookup"><span data-stu-id="82a30-135">Mipmap level-of-detail bias.</span></span> <span data-ttu-id="82a30-136">La valeur par défaut est zéro.</span><span class="sxs-lookup"><span data-stu-id="82a30-136">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="82a30-137"><span id="D3DSAMP_MAXMIPLEVEL"></span><span id="d3dsamp_maxmiplevel"></span>**D3DSAMP \_ MAXMIPLEVEL**</span><span class="sxs-lookup"><span data-stu-id="82a30-137"><span id="D3DSAMP_MAXMIPLEVEL"></span><span id="d3dsamp_maxmiplevel"></span>**D3DSAMP\_MAXMIPLEVEL**</span></span>
</dt> <dd>

<span data-ttu-id="82a30-138">index de niveau de détail du mappage le plus grand à utiliser.</span><span class="sxs-lookup"><span data-stu-id="82a30-138">level-of-detail index of largest map to use.</span></span> <span data-ttu-id="82a30-139">Les valeurs sont comprises entre 0 et (n-1), 0 étant le plus grand.</span><span class="sxs-lookup"><span data-stu-id="82a30-139">Values range from 0 to (n - 1) where 0 is the largest.</span></span> <span data-ttu-id="82a30-140">La valeur par défaut est zéro.</span><span class="sxs-lookup"><span data-stu-id="82a30-140">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="82a30-141"><span id="D3DSAMP_MAXANISOTROPY"></span><span id="d3dsamp_maxanisotropy"></span>**D3DSAMP \_ MAXANISOTROPY**</span><span class="sxs-lookup"><span data-stu-id="82a30-141"><span id="D3DSAMP_MAXANISOTROPY"></span><span id="d3dsamp_maxanisotropy"></span>**D3DSAMP\_MAXANISOTROPY**</span></span>
</dt> <dd>

<span data-ttu-id="82a30-142">Anisotropie maximale DWORD.</span><span class="sxs-lookup"><span data-stu-id="82a30-142">DWORD maximum anisotropy.</span></span> <span data-ttu-id="82a30-143">Les valeurs sont comprises entre 1 et la valeur spécifiée dans le membre **MaxAnisotropy** de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .</span><span class="sxs-lookup"><span data-stu-id="82a30-143">Values range from 1 to the value that is specified in the **MaxAnisotropy** member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure.</span></span> <span data-ttu-id="82a30-144">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="82a30-144">The default value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="82a30-145"><span id="D3DSAMP_SRGBTEXTURE"></span><span id="d3dsamp_srgbtexture"></span>**D3DSAMP \_ SRGBTEXTURE**</span><span class="sxs-lookup"><span data-stu-id="82a30-145"><span id="D3DSAMP_SRGBTEXTURE"></span><span id="d3dsamp_srgbtexture"></span>**D3DSAMP\_SRGBTEXTURE**</span></span>
</dt> <dd>

<span data-ttu-id="82a30-146">Valeur de correction gamma.</span><span class="sxs-lookup"><span data-stu-id="82a30-146">Gamma correction value.</span></span> <span data-ttu-id="82a30-147">La valeur par défaut est 0, ce qui signifie que gamma est 1,0 et qu’aucune correction n’est requise.</span><span class="sxs-lookup"><span data-stu-id="82a30-147">The default value is 0, which means gamma is 1.0 and no correction is required.</span></span> <span data-ttu-id="82a30-148">Dans le cas contraire, cette valeur signifie que l’échantillonneur doit supposer la valeur gamma de 2,2 sur le contenu et le convertir en linéaire (gamma 1,0) avant de le présenter au nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="82a30-148">Otherwise, this value means that the sampler should assume gamma of 2.2 on the content and convert it to linear (gamma 1.0) before presenting it to the pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="82a30-149"><span id="D3DSAMP_ELEMENTINDEX"></span><span id="d3dsamp_elementindex"></span>**D3DSAMP \_ ELEMENTINDEX**</span><span class="sxs-lookup"><span data-stu-id="82a30-149"><span id="D3DSAMP_ELEMENTINDEX"></span><span id="d3dsamp_elementindex"></span>**D3DSAMP\_ELEMENTINDEX**</span></span>
</dt> <dd>

<span data-ttu-id="82a30-150">Quand une texture multiélément est assignée à l’échantillonneur, cela indique l’index d’élément à utiliser.</span><span class="sxs-lookup"><span data-stu-id="82a30-150">When a multielement texture is assigned to the sampler, this indicates which element index to use.</span></span> <span data-ttu-id="82a30-151">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="82a30-151">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="82a30-152"><span id="D3DSAMP_DMAPOFFSET"></span><span id="d3dsamp_dmapoffset"></span>**D3DSAMP \_ DMAPOFFSET**</span><span class="sxs-lookup"><span data-stu-id="82a30-152"><span id="D3DSAMP_DMAPOFFSET"></span><span id="d3dsamp_dmapoffset"></span>**D3DSAMP\_DMAPOFFSET**</span></span>
</dt> <dd>

<span data-ttu-id="82a30-153">Décalage du vertex dans le mappage de déplacement prééchantillonné.</span><span class="sxs-lookup"><span data-stu-id="82a30-153">Vertex offset in the presampled displacement map.</span></span> <span data-ttu-id="82a30-154">Il s’agit d’une constante utilisée par du paveur, sa valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="82a30-154">This is a constant used by the tessellator, its default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="82a30-155"><span id="D3DSAMP_FORCE_DWORD"></span><span id="d3dsamp_force_dword"></span>**D3DSAMP \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="82a30-155"><span id="D3DSAMP_FORCE_DWORD"></span><span id="d3dsamp_force_dword"></span>**D3DSAMP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="82a30-156">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="82a30-156">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="82a30-157">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="82a30-157">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="82a30-158">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="82a30-158">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="82a30-159">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82a30-159">Requirements</span></span>



| <span data-ttu-id="82a30-160">Condition requise</span><span class="sxs-lookup"><span data-stu-id="82a30-160">Requirement</span></span> | <span data-ttu-id="82a30-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="82a30-161">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="82a30-162">En-tête</span><span class="sxs-lookup"><span data-stu-id="82a30-162">Header</span></span><br/> | <dl> <span data-ttu-id="82a30-163"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="82a30-163"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82a30-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82a30-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82a30-165">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="82a30-165">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 
