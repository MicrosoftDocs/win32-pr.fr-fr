---
title: Structure de DDS_HEADER_DXT10 (DDS. h)
description: Extension d’en-tête DDS pour gérer des tableaux de ressources, des formats de pixel DXGI qui ne sont pas mappés aux structures de format de pixel Microsoft DirectDraw héritées et des métadonnées supplémentaires.
ms.assetid: 502d6943-8f25-446c-b990-8276f862c195
keywords:
- DDS_HEADER_DXT10 de la structure DDS
topic_type:
- apiref
api_name:
- DDS_HEADER_DXT10
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a2f5dd4a6948d38b86b49584db81937ce5148b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535167"
---
# <a name="dds_header_dxt10-structure"></a><span data-ttu-id="185d7-104">\_Structure DXT10 d’en-tête DDS \_</span><span class="sxs-lookup"><span data-stu-id="185d7-104">DDS\_HEADER\_DXT10 structure</span></span>

<span data-ttu-id="185d7-105">Extension d’en-tête DDS pour gérer des tableaux de ressources, des formats de pixel DXGI qui ne sont pas mappés aux structures de format de pixel Microsoft DirectDraw héritées et des métadonnées supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="185d7-105">DDS header extension to handle resource arrays, DXGI pixel formats that don't map to the legacy Microsoft DirectDraw pixel format structures, and additional metadata.</span></span>

## <a name="syntax"></a><span data-ttu-id="185d7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="185d7-106">Syntax</span></span>


```C++
typedef struct {
  DXGI_FORMAT              dxgiFormat;
  D3D10_RESOURCE_DIMENSION resourceDimension;
  UINT                     miscFlag;
  UINT                     arraySize;
  UINT                     miscFlags2;
} DDS_HEADER_DXT10;
```



## <a name="members"></a><span data-ttu-id="185d7-107">Membres</span><span class="sxs-lookup"><span data-stu-id="185d7-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="185d7-108">**dxgiFormat**</span><span class="sxs-lookup"><span data-stu-id="185d7-108">**dxgiFormat**</span></span>
</dt> <dd>

<span data-ttu-id="185d7-109">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="185d7-109">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="185d7-110">Format de pixel de la surface (voir [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span><span class="sxs-lookup"><span data-stu-id="185d7-110">The surface pixel format (see [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span></span>

</dd> <dt>

<span data-ttu-id="185d7-111">**resourceDimension**</span><span class="sxs-lookup"><span data-stu-id="185d7-111">**resourceDimension**</span></span>
</dt> <dd>

<span data-ttu-id="185d7-112">Type : **[ **\_ \_ dimension de ressource D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension)**</span><span class="sxs-lookup"><span data-stu-id="185d7-112">Type: **[**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension)**</span></span>

</dd> <dd>

<span data-ttu-id="185d7-113">Identifie le type de ressource.</span><span class="sxs-lookup"><span data-stu-id="185d7-113">Identifies the type of resource.</span></span> <span data-ttu-id="185d7-114">Les valeurs suivantes pour ce membre sont un sous-ensemble des valeurs de [**la \_ \_ dimension de ressource D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension) ou de l’énumération de [**\_ \_ dimension de ressource d3d11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_dimension) :</span><span class="sxs-lookup"><span data-stu-id="185d7-114">The following values for this member are a subset of the values in the [**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension) or [**D3D11\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_dimension) enumeration:</span></span>



| <span data-ttu-id="185d7-115">Type</span><span class="sxs-lookup"><span data-stu-id="185d7-115">Type</span></span>                                                              | <span data-ttu-id="185d7-116">Description</span><span class="sxs-lookup"><span data-stu-id="185d7-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="185d7-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="185d7-117">Value</span></span> |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="185d7-118">\_TEXTURE1D dimension DDS \_ (D3D10 de \_ dimension de ressource \_ \_ TEXTURE1D)</span><span class="sxs-lookup"><span data-stu-id="185d7-118">DDS\_DIMENSION\_TEXTURE1D (D3D10\_RESOURCE\_DIMENSION\_TEXTURE1D)</span></span> | <span data-ttu-id="185d7-119">La ressource est une [texture 1D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types).</span><span class="sxs-lookup"><span data-stu-id="185d7-119">Resource is a [1D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types).</span></span> <span data-ttu-id="185d7-120">Le membre **dwWidth** de [**l' \_ en-tête DDS**](dds-header.md) spécifie la taille de la texture.</span><span class="sxs-lookup"><span data-stu-id="185d7-120">The **dwWidth** member of [**DDS\_HEADER**](dds-header.md) specifies the size of the texture.</span></span> <span data-ttu-id="185d7-121">En règle générale, vous définissez le membre **dwHeight** de l' **\_ en-tête DDS** sur 1 ; vous devez également définir l' \_ indicateur DDSD Height dans le membre **dwFlags** de l' **\_ en-tête DDS**.</span><span class="sxs-lookup"><span data-stu-id="185d7-121">Typically, you set the **dwHeight** member of **DDS\_HEADER** to 1; you also must set the DDSD\_HEIGHT flag in the **dwFlags** member of **DDS\_HEADER**.</span></span>                      | <span data-ttu-id="185d7-122">2</span><span class="sxs-lookup"><span data-stu-id="185d7-122">2</span></span>     |
| <span data-ttu-id="185d7-123">\_TEXTURE2D dimension DDS \_ (D3D10 de \_ dimension de ressource \_ \_ TEXTURE2D)</span><span class="sxs-lookup"><span data-stu-id="185d7-123">DDS\_DIMENSION\_TEXTURE2D (D3D10\_RESOURCE\_DIMENSION\_TEXTURE2D)</span></span> | <span data-ttu-id="185d7-124">La ressource est une [texture 2D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) avec une zone spécifiée par les membres **dwWidth** et **dwHeight** de l' [**\_ en-tête DDS**](dds-header.md).</span><span class="sxs-lookup"><span data-stu-id="185d7-124">Resource is a [2D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) with an area specified by the **dwWidth** and **dwHeight** members of [**DDS\_HEADER**](dds-header.md).</span></span> <span data-ttu-id="185d7-125">Vous pouvez également utiliser ce type pour identifier une texture de mappage de cube.</span><span class="sxs-lookup"><span data-stu-id="185d7-125">You can also use this type to identify a cube-map texture.</span></span> <span data-ttu-id="185d7-126">Pour plus d’informations sur l’identification d’une texture de mappage de cube, consultez membres **miscFlag** et **arraySize** .</span><span class="sxs-lookup"><span data-stu-id="185d7-126">For more information about how to identify a cube-map texture, see **miscFlag** and **arraySize** members.</span></span> | <span data-ttu-id="185d7-127">3</span><span class="sxs-lookup"><span data-stu-id="185d7-127">3</span></span>     |
| <span data-ttu-id="185d7-128">\_TEXTURE3D dimension DDS \_ (D3D10 de \_ dimension de ressource \_ \_ TEXTURE3D)</span><span class="sxs-lookup"><span data-stu-id="185d7-128">DDS\_DIMENSION\_TEXTURE3D (D3D10\_RESOURCE\_DIMENSION\_TEXTURE3D)</span></span> | <span data-ttu-id="185d7-129">La ressource est une [texture 3D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) avec un volume spécifié par les membres **dwWidth**, **dwHeight** et **dwDepth** de [**l' \_ en-tête DDS**](dds-header.md).</span><span class="sxs-lookup"><span data-stu-id="185d7-129">Resource is a [3D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) with a volume specified by the **dwWidth**, **dwHeight**, and **dwDepth** members of [**DDS\_HEADER**](dds-header.md).</span></span> <span data-ttu-id="185d7-130">Vous devez également définir l' \_ indicateur de profondeur DDSD dans le membre **dwFlags** de l' **\_ en-tête DDS**.</span><span class="sxs-lookup"><span data-stu-id="185d7-130">You also must set the DDSD\_DEPTH flag in the **dwFlags** member of **DDS\_HEADER**.</span></span>                                                                   | <span data-ttu-id="185d7-131">4</span><span class="sxs-lookup"><span data-stu-id="185d7-131">4</span></span>     |



 

</dd> <dt>

<span data-ttu-id="185d7-132">**miscFlag**</span><span class="sxs-lookup"><span data-stu-id="185d7-132">**miscFlag**</span></span>
</dt> <dd>

<span data-ttu-id="185d7-133">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="185d7-133">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="185d7-134">Identifie d’autres options moins courantes pour les ressources.</span><span class="sxs-lookup"><span data-stu-id="185d7-134">Identifies other, less common options for resources.</span></span> <span data-ttu-id="185d7-135">La valeur suivante pour ce membre est un sous-ensemble des valeurs de [**l' \_ \_ \_ indicateur div de la ressource D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_misc_flag) ou de l’énumération des [**\_ \_ \_ indicateurs divers des ressources d3d11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) :</span><span class="sxs-lookup"><span data-stu-id="185d7-135">The following value for this member is a subset of the values in the [**D3D10\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_misc_flag) or [**D3D11\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) enumeration:</span></span>



| <span data-ttu-id="185d7-136">Type</span><span class="sxs-lookup"><span data-stu-id="185d7-136">Type</span></span>                             | <span data-ttu-id="185d7-137">Description</span><span class="sxs-lookup"><span data-stu-id="185d7-137">Description</span></span>                                                                                                  | <span data-ttu-id="185d7-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="185d7-138">Value</span></span> |
|----------------------------------|--------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="185d7-139">\_ \_ TEXTURECUBE divers des ressources DDS \_</span><span class="sxs-lookup"><span data-stu-id="185d7-139">DDS\_RESOURCE\_MISC\_TEXTURECUBE</span></span> | <span data-ttu-id="185d7-140">Indique qu’une [texture 2D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) est une texture de mappage de cube.</span><span class="sxs-lookup"><span data-stu-id="185d7-140">Indicates a [2D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) is a cube-map texture.</span></span> | <span data-ttu-id="185d7-141">0x4</span><span class="sxs-lookup"><span data-stu-id="185d7-141">0x4</span></span>   |



 

</dd> <dt>

<span data-ttu-id="185d7-142">**arraySize**</span><span class="sxs-lookup"><span data-stu-id="185d7-142">**arraySize**</span></span>
</dt> <dd>

<span data-ttu-id="185d7-143">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="185d7-143">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="185d7-144">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="185d7-144">The number of elements in the array.</span></span>

<span data-ttu-id="185d7-145">Pour une [texture 2D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) qui est également une texture de mappage de cube, ce nombre représente le nombre de cubes.</span><span class="sxs-lookup"><span data-stu-id="185d7-145">For a [2D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) that is also a cube-map texture, this number represents the number of cubes.</span></span> <span data-ttu-id="185d7-146">Ce nombre est le même que le nombre dans le membre **NumCubes** de [**D3D10 \_ TEXCUBE \_ array \_ SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1) ou [**d3d11 \_ TEXCUBE \_ array \_ SRV**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_texcube_array_srv)).</span><span class="sxs-lookup"><span data-stu-id="185d7-146">This number is the same as the number in the **NumCubes** member of [**D3D10\_TEXCUBE\_ARRAY\_SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1) or [**D3D11\_TEXCUBE\_ARRAY\_SRV**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_texcube_array_srv)).</span></span> <span data-ttu-id="185d7-147">Dans ce cas, le fichier DDS contient des \* textures 2D arraySize 6.</span><span class="sxs-lookup"><span data-stu-id="185d7-147">In this case, the DDS file contains **arraySize**\*6 2D textures.</span></span> <span data-ttu-id="185d7-148">Pour plus d’informations sur ce cas, consultez la description de **miscFlag** .</span><span class="sxs-lookup"><span data-stu-id="185d7-148">For more information about this case, see the **miscFlag** description.</span></span>

<span data-ttu-id="185d7-149">Pour une [texture 3D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types), vous devez définir ce nombre sur 1.</span><span class="sxs-lookup"><span data-stu-id="185d7-149">For a [3D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types), you must set this number to 1.</span></span>

</dd> <dt>

<span data-ttu-id="185d7-150">**miscFlags2**</span><span class="sxs-lookup"><span data-stu-id="185d7-150">**miscFlags2**</span></span>
</dt> <dd>

<span data-ttu-id="185d7-151">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="185d7-151">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="185d7-152">Contient des métadonnées supplémentaires (anciennement réservées).</span><span class="sxs-lookup"><span data-stu-id="185d7-152">Contains additional metadata (formerly was reserved).</span></span> <span data-ttu-id="185d7-153">Les 3 bits de poids faible indiquent le mode Alpha de la ressource associée.</span><span class="sxs-lookup"><span data-stu-id="185d7-153">The lower 3 bits indicate the alpha mode of the associated resource.</span></span> <span data-ttu-id="185d7-154">Les 29 premiers bits sont réservés et sont généralement 0.</span><span class="sxs-lookup"><span data-stu-id="185d7-154">The upper 29 bits are reserved and are typically 0.</span></span>



| <span data-ttu-id="185d7-155">Type</span><span class="sxs-lookup"><span data-stu-id="185d7-155">Type</span></span>                            | <span data-ttu-id="185d7-156">Description</span><span class="sxs-lookup"><span data-stu-id="185d7-156">Description</span></span>                                                                                                                              | <span data-ttu-id="185d7-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="185d7-157">Value</span></span> |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="185d7-158">\_mode Alpha \_ DDS \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="185d7-158">DDS\_ALPHA\_MODE\_UNKNOWN</span></span>       | <span data-ttu-id="185d7-159">Le contenu du canal alpha est inconnu.</span><span class="sxs-lookup"><span data-stu-id="185d7-159">Alpha channel content is unknown.</span></span> <span data-ttu-id="185d7-160">Il s’agit de la valeur des fichiers hérités, qui est généralement supposée être alpha « rectiligne ».</span><span class="sxs-lookup"><span data-stu-id="185d7-160">This is the value for legacy files, which typically is assumed to be 'straight' alpha.</span></span>                 | <span data-ttu-id="185d7-161">0x0</span><span class="sxs-lookup"><span data-stu-id="185d7-161">0x0</span></span>   |
| <span data-ttu-id="185d7-162">\_mode Alpha \_ DDS \_ simple</span><span class="sxs-lookup"><span data-stu-id="185d7-162">DDS\_ALPHA\_MODE\_STRAIGHT</span></span>      | <span data-ttu-id="185d7-163">Tout contenu de canal alpha est supposé utiliser une valeur alpha directe.</span><span class="sxs-lookup"><span data-stu-id="185d7-163">Any alpha channel content is presumed to use straight alpha.</span></span>                                                                             | <span data-ttu-id="185d7-164">0x1</span><span class="sxs-lookup"><span data-stu-id="185d7-164">0x1</span></span>   |
| <span data-ttu-id="185d7-165">\_mode Alpha \_ DDS \_ prémultiplié</span><span class="sxs-lookup"><span data-stu-id="185d7-165">DDS\_ALPHA\_MODE\_PREMULTIPLIED</span></span> | <span data-ttu-id="185d7-166">Tout contenu de canal alpha utilise l’alpha prémultiplié.</span><span class="sxs-lookup"><span data-stu-id="185d7-166">Any alpha channel content is using premultiplied alpha.</span></span> <span data-ttu-id="185d7-167">Les seuls formats de fichier hérités qui indiquent ces informations sont « DX2 » et « DX4 ».</span><span class="sxs-lookup"><span data-stu-id="185d7-167">The only legacy file formats that indicate this information are 'DX2' and 'DX4'.</span></span> | <span data-ttu-id="185d7-168">0x2</span><span class="sxs-lookup"><span data-stu-id="185d7-168">0x2</span></span>   |
| <span data-ttu-id="185d7-169">\_ \_ opaque en mode Alpha \_ opaque</span><span class="sxs-lookup"><span data-stu-id="185d7-169">DDS\_ALPHA\_MODE\_OPAQUE</span></span>        | <span data-ttu-id="185d7-170">Tout contenu de canal alpha est défini sur entièrement opaque.</span><span class="sxs-lookup"><span data-stu-id="185d7-170">Any alpha channel content is all set to fully opaque.</span></span>                                                                                    | <span data-ttu-id="185d7-171">0x3</span><span class="sxs-lookup"><span data-stu-id="185d7-171">0x3</span></span>   |
| <span data-ttu-id="185d7-172">\_ \_ personnalisé en mode Alpha DDS \_</span><span class="sxs-lookup"><span data-stu-id="185d7-172">DDS\_ALPHA\_MODE\_CUSTOM</span></span>        | <span data-ttu-id="185d7-173">Tout contenu de canal alpha est utilisé en tant que quatrième canal et n’est pas destiné à représenter la transparence (directe ou prémultipliée).</span><span class="sxs-lookup"><span data-stu-id="185d7-173">Any alpha channel content is being used as a 4th channel and is not intended to represent transparency (straight or premultiplied).</span></span>      | <span data-ttu-id="185d7-174">0x4</span><span class="sxs-lookup"><span data-stu-id="185d7-174">0x4</span></span>   |



 

> [!Note]  
> <span data-ttu-id="185d7-175">Les bibliothèques d’utilitaires D3DX 10 et [D3DX 11](/windows/desktop/direct3d11/d3d11-graphics-reference-d3dx11) héritées ne peuvent pas être chargées. Fichier DDS avec **miscFlags2** non égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="185d7-175">The legacy D3DX 10 and [D3DX 11](/windows/desktop/direct3d11/d3d11-graphics-reference-d3dx11) utility libraries will fail to load any .DDS file with **miscFlags2** not equal to zero.</span></span>

 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="185d7-176">Notes</span><span class="sxs-lookup"><span data-stu-id="185d7-176">Remarks</span></span>

<span data-ttu-id="185d7-177">Utilisez cette structure avec un [**\_ en-tête DDS**](dds-header.md) pour stocker un tableau de ressources dans un fichier DDS.</span><span class="sxs-lookup"><span data-stu-id="185d7-177">Use this structure together with a [**DDS\_HEADER**](dds-header.md) to store a resource array in a DDS file.</span></span> <span data-ttu-id="185d7-178">Pour plus d’informations, consultez [tableaux de texture](dx-graphics-dds-pguide.md).</span><span class="sxs-lookup"><span data-stu-id="185d7-178">For more info, see [texture arrays](dx-graphics-dds-pguide.md).</span></span>

<span data-ttu-id="185d7-179">Cet en-tête est présent si le membre **dwFourCC** de la structure [**DDS \_ PIXELFORMAT**](dds-pixelformat.md) a la valeur « facilement ».</span><span class="sxs-lookup"><span data-stu-id="185d7-179">This header is present if the **dwFourCC** member of the [**DDS\_PIXELFORMAT**](dds-pixelformat.md) structure is set to 'DX10'.</span></span>

## <a name="requirements"></a><span data-ttu-id="185d7-180">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="185d7-180">Requirements</span></span>



| <span data-ttu-id="185d7-181">Condition requise</span><span class="sxs-lookup"><span data-stu-id="185d7-181">Requirement</span></span> | <span data-ttu-id="185d7-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="185d7-182">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="185d7-183">En-tête</span><span class="sxs-lookup"><span data-stu-id="185d7-183">Header</span></span><br/> | <dl> <span data-ttu-id="185d7-184"><dt>DDS. h</dt></span><span class="sxs-lookup"><span data-stu-id="185d7-184"><dt>Dds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="185d7-185">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="185d7-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="185d7-186">Référence pour DDS</span><span class="sxs-lookup"><span data-stu-id="185d7-186">Reference for DDS</span></span>](dx-graphics-dds-reference.md)
</dt> </dl>

 

