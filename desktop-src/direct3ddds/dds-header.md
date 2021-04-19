---
title: Structure de DDS_HEADER (DDS. h)
description: Décrit un en-tête de fichier DDS.
ms.assetid: 7f8bde30-0ff9-4bb9-b444-5c875e6a0865
keywords:
- DDS_HEADER de la structure DDS
topic_type:
- apiref
api_name:
- DDS_HEADER
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d70fa0c4b05b6655ce0329cc73651ea21d4d808
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532426"
---
# <a name="dds_header-structure"></a><span data-ttu-id="d4d46-104">\_Structure d’en-tête DDS</span><span class="sxs-lookup"><span data-stu-id="d4d46-104">DDS\_HEADER structure</span></span>

<span data-ttu-id="d4d46-105">Décrit un en-tête de fichier DDS.</span><span class="sxs-lookup"><span data-stu-id="d4d46-105">Describes a DDS file header.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4d46-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4d46-106">Syntax</span></span>


```C++
typedef struct {
  DWORD           dwSize;
  DWORD           dwFlags;
  DWORD           dwHeight;
  DWORD           dwWidth;
  DWORD           dwPitchOrLinearSize;
  DWORD           dwDepth;
  DWORD           dwMipMapCount;
  DWORD           dwReserved1[11];
  DDS_PIXELFORMAT ddspf;
  DWORD           dwCaps;
  DWORD           dwCaps2;
  DWORD           dwCaps3;
  DWORD           dwCaps4;
  DWORD           dwReserved2;
} DDS_HEADER;
```



## <a name="members"></a><span data-ttu-id="d4d46-107">Membres</span><span class="sxs-lookup"><span data-stu-id="d4d46-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d4d46-108">**dwSize nul**</span><span class="sxs-lookup"><span data-stu-id="d4d46-108">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="d4d46-109">Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d4d46-109">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d4d46-110">Taille de la structure.</span><span class="sxs-lookup"><span data-stu-id="d4d46-110">Size of structure.</span></span> <span data-ttu-id="d4d46-111">Ce membre doit avoir la valeur 124.</span><span class="sxs-lookup"><span data-stu-id="d4d46-111">This member must be set to 124.</span></span>

</dd> <dt>

<span data-ttu-id="d4d46-112">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="d4d46-112">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="d4d46-113">Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d4d46-113">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d4d46-114">Indicateurs indiquant les membres qui contiennent des données valides.</span><span class="sxs-lookup"><span data-stu-id="d4d46-114">Flags to indicate which members contain valid data.</span></span>



| <span data-ttu-id="d4d46-115">Indicateur</span><span class="sxs-lookup"><span data-stu-id="d4d46-115">Flag</span></span>              | <span data-ttu-id="d4d46-116">Description</span><span class="sxs-lookup"><span data-stu-id="d4d46-116">Description</span></span>                                                  | <span data-ttu-id="d4d46-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4d46-117">Value</span></span>    |
|-------------------|--------------------------------------------------------------|----------|
| <span data-ttu-id="d4d46-118">DDSD \_ Cap</span><span class="sxs-lookup"><span data-stu-id="d4d46-118">DDSD\_CAPS</span></span>        | <span data-ttu-id="d4d46-119">Obligatoire dans chaque fichier. DDS.</span><span class="sxs-lookup"><span data-stu-id="d4d46-119">Required in every .dds file.</span></span>                                 | <span data-ttu-id="d4d46-120">0x1</span><span class="sxs-lookup"><span data-stu-id="d4d46-120">0x1</span></span>      |
| <span data-ttu-id="d4d46-121">hauteur de DDSD \_</span><span class="sxs-lookup"><span data-stu-id="d4d46-121">DDSD\_HEIGHT</span></span>      | <span data-ttu-id="d4d46-122">Obligatoire dans chaque fichier. DDS.</span><span class="sxs-lookup"><span data-stu-id="d4d46-122">Required in every .dds file.</span></span>                                 | <span data-ttu-id="d4d46-123">0x2</span><span class="sxs-lookup"><span data-stu-id="d4d46-123">0x2</span></span>      |
| <span data-ttu-id="d4d46-124">largeur de DDSD \_</span><span class="sxs-lookup"><span data-stu-id="d4d46-124">DDSD\_WIDTH</span></span>       | <span data-ttu-id="d4d46-125">Obligatoire dans chaque fichier. DDS.</span><span class="sxs-lookup"><span data-stu-id="d4d46-125">Required in every .dds file.</span></span>                                 | <span data-ttu-id="d4d46-126">0x4</span><span class="sxs-lookup"><span data-stu-id="d4d46-126">0x4</span></span>      |
| <span data-ttu-id="d4d46-127">DDSD \_</span><span class="sxs-lookup"><span data-stu-id="d4d46-127">DDSD\_PITCH</span></span>       | <span data-ttu-id="d4d46-128">Obligatoire lorsque le pas à pas est fourni pour une texture non compressée.</span><span class="sxs-lookup"><span data-stu-id="d4d46-128">Required when pitch is provided for an uncompressed texture.</span></span> | <span data-ttu-id="d4d46-129">0x8</span><span class="sxs-lookup"><span data-stu-id="d4d46-129">0x8</span></span>      |
| <span data-ttu-id="d4d46-130">DDSD \_ PIXELFORMAT</span><span class="sxs-lookup"><span data-stu-id="d4d46-130">DDSD\_PIXELFORMAT</span></span> | <span data-ttu-id="d4d46-131">Obligatoire dans chaque fichier. DDS.</span><span class="sxs-lookup"><span data-stu-id="d4d46-131">Required in every .dds file.</span></span>                                 | <span data-ttu-id="d4d46-132">0x1000</span><span class="sxs-lookup"><span data-stu-id="d4d46-132">0x1000</span></span>   |
| <span data-ttu-id="d4d46-133">DDSD \_ MIPMAPCOUNT</span><span class="sxs-lookup"><span data-stu-id="d4d46-133">DDSD\_MIPMAPCOUNT</span></span> | <span data-ttu-id="d4d46-134">Obligatoire dans une texture mipmapped.</span><span class="sxs-lookup"><span data-stu-id="d4d46-134">Required in a mipmapped texture.</span></span>                             | <span data-ttu-id="d4d46-135">0x20000</span><span class="sxs-lookup"><span data-stu-id="d4d46-135">0x20000</span></span>  |
| <span data-ttu-id="d4d46-136">DDSD \_ LINEARSIZE</span><span class="sxs-lookup"><span data-stu-id="d4d46-136">DDSD\_LINEARSIZE</span></span>  | <span data-ttu-id="d4d46-137">Obligatoire lorsque le pas à pas est fourni pour une texture compressée.</span><span class="sxs-lookup"><span data-stu-id="d4d46-137">Required when pitch is provided for a compressed texture.</span></span>    | <span data-ttu-id="d4d46-138">0x80000</span><span class="sxs-lookup"><span data-stu-id="d4d46-138">0x80000</span></span>  |
| <span data-ttu-id="d4d46-139">DDSD \_ profondeur)</span><span class="sxs-lookup"><span data-stu-id="d4d46-139">DDSD\_DEPTH</span></span>       | <span data-ttu-id="d4d46-140">Obligatoire dans une texture de profondeur.</span><span class="sxs-lookup"><span data-stu-id="d4d46-140">Required in a depth texture.</span></span>                                 | <span data-ttu-id="d4d46-141">0x800000</span><span class="sxs-lookup"><span data-stu-id="d4d46-141">0x800000</span></span> |



 

> [!Note]  
> <span data-ttu-id="d4d46-142">Lorsque vous écrivez des fichiers. DDS, vous devez définir les \_ indicateurs DDSD Cap et DDSD \_ PIXELFORMAT, et pour les textures mipmapped, vous devez également définir l' \_ indicateur DDSD MIPMAPCOUNT.</span><span class="sxs-lookup"><span data-stu-id="d4d46-142">When you write .dds files, you should set the DDSD\_CAPS and DDSD\_PIXELFORMAT flags, and for mipmapped textures you should also set the DDSD\_MIPMAPCOUNT flag.</span></span> <span data-ttu-id="d4d46-143">Toutefois, lorsque vous lisez un fichier. DDS, vous ne devez pas vous appuyer sur les \_ indicateurs DDSD Cap, DDSD \_ PIXELFORMAT et DDSD \_ MIPMAPCOUNT définis, car certains enregistreurs d’un tel fichier peuvent ne pas définir ces indicateurs.</span><span class="sxs-lookup"><span data-stu-id="d4d46-143">However, when you read a .dds file, you should not rely on the DDSD\_CAPS, DDSD\_PIXELFORMAT, and DDSD\_MIPMAPCOUNT flags being set because some writers of such a file might not set these flags.</span></span>

 

<span data-ttu-id="d4d46-144">L' \_ indicateur de \_ texture d’indicateurs d’en-tête DDS \_ , qui est défini dans DDS. h, est une combinaison au niveau du bit or de la DDSD \_ Cap, de DDSD \_ Height, de DDSD \_ Width et DDSD \_ PIXELFORMAT Flags.</span><span class="sxs-lookup"><span data-stu-id="d4d46-144">The DDS\_HEADER\_FLAGS\_TEXTURE flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSD\_CAPS, DDSD\_HEIGHT, DDSD\_WIDTH, and DDSD\_PIXELFORMAT flags.</span></span>

<span data-ttu-id="d4d46-145">L' \_ indicateur MIPMAP des indicateurs d’en-tête DDS \_ \_ , qui est défini dans DDS. h, est égal à l' \_ indicateur DDSD MIPMAPCOUNT.</span><span class="sxs-lookup"><span data-stu-id="d4d46-145">The DDS\_HEADER\_FLAGS\_MIPMAP flag, which is defined in Dds.h, is equal to the DDSD\_MIPMAPCOUNT flag.</span></span>

<span data-ttu-id="d4d46-146">L' \_ \_ indicateur de volume Flags de l’en-tête DDS \_ , qui est défini dans DDS. h, est égal à l' \_ indicateur de profondeur DDSD.</span><span class="sxs-lookup"><span data-stu-id="d4d46-146">The DDS\_HEADER\_FLAGS\_VOLUME flag, which is defined in Dds.h, is equal to the DDSD\_DEPTH flag.</span></span>

<span data-ttu-id="d4d46-147">L' \_ \_ indicateur de tangage des indicateurs d’en-tête DDS \_ , qui est défini dans DDS. h, est égal à l’indicateur de pas DDSD \_ .</span><span class="sxs-lookup"><span data-stu-id="d4d46-147">The DDS\_HEADER\_FLAGS\_PITCH flag, which is defined in Dds.h, is equal to the DDSD\_PITCH flag.</span></span>

<span data-ttu-id="d4d46-148">L' \_ indicateur LINEARSIZE de l’en-tête DDS \_ \_ , défini dans DDS. h, est égal à l' \_ indicateur DDSD LINEARSIZE.</span><span class="sxs-lookup"><span data-stu-id="d4d46-148">The DDS\_HEADER\_FLAGS\_LINEARSIZE flag, which is defined in Dds.h, is equal to the DDSD\_LINEARSIZE flag.</span></span>

</dd> <dt>

<span data-ttu-id="d4d46-149">**dwHeight**</span><span class="sxs-lookup"><span data-stu-id="d4d46-149">**dwHeight**</span></span>
</dt> <dd>

<span data-ttu-id="d4d46-150">Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d4d46-150">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d4d46-151">Hauteur de la surface (en pixels).</span><span class="sxs-lookup"><span data-stu-id="d4d46-151">Surface height (in pixels).</span></span>

</dd> <dt>

<span data-ttu-id="d4d46-152">**dwWidth**</span><span class="sxs-lookup"><span data-stu-id="d4d46-152">**dwWidth**</span></span>
</dt> <dd>

<span data-ttu-id="d4d46-153">Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d4d46-153">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d4d46-154">Largeur de la surface (en pixels).</span><span class="sxs-lookup"><span data-stu-id="d4d46-154">Surface width (in pixels).</span></span>

</dd> <dt>

<span data-ttu-id="d4d46-155">**dwPitchOrLinearSize**</span><span class="sxs-lookup"><span data-stu-id="d4d46-155">**dwPitchOrLinearSize**</span></span>
</dt> <dd>

<span data-ttu-id="d4d46-156">Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d4d46-156">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d4d46-157">La hauteur ou le nombre d’octets par ligne d’analyse dans une texture non compressée ; nombre total d’octets dans la texture de niveau supérieur pour une texture compressée.</span><span class="sxs-lookup"><span data-stu-id="d4d46-157">The pitch or number of bytes per scan line in an uncompressed texture; the total number of bytes in the top level texture for a compressed texture.</span></span> <span data-ttu-id="d4d46-158">Pour plus d’informations sur la façon de calculer le pas, consultez la section relative au format de fichier DDS [dans le Guide de programmation pour DDS](dx-graphics-dds-pguide.md).</span><span class="sxs-lookup"><span data-stu-id="d4d46-158">For information about how to compute the pitch, see the DDS File Layout section of the [Programming Guide for DDS](dx-graphics-dds-pguide.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4d46-159">**dwDepth**</span><span class="sxs-lookup"><span data-stu-id="d4d46-159">**dwDepth**</span></span>
</dt> <dd>

<span data-ttu-id="d4d46-160">Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d4d46-160">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d4d46-161">Profondeur d’une texture de volume (en pixels), sinon inutilisée.</span><span class="sxs-lookup"><span data-stu-id="d4d46-161">Depth of a volume texture (in pixels), otherwise unused.</span></span>

</dd> <dt>

<span data-ttu-id="d4d46-162">**dwMipMapCount**</span><span class="sxs-lookup"><span data-stu-id="d4d46-162">**dwMipMapCount**</span></span>
</dt> <dd>

<span data-ttu-id="d4d46-163">Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d4d46-163">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d4d46-164">Nombre de niveaux de mipmap, sinon non utilisé.</span><span class="sxs-lookup"><span data-stu-id="d4d46-164">Number of mipmap levels, otherwise unused.</span></span>

</dd> <dt>

<span data-ttu-id="d4d46-165">**dwReserved1 \[ 11\]**</span><span class="sxs-lookup"><span data-stu-id="d4d46-165">**dwReserved1\[11\]**</span></span>
</dt> <dd>

<span data-ttu-id="d4d46-166">Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d4d46-166">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d4d46-167">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="d4d46-167">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="d4d46-168">**ddspf**</span><span class="sxs-lookup"><span data-stu-id="d4d46-168">**ddspf**</span></span>
</dt> <dd>

<span data-ttu-id="d4d46-169">Type : **[ **DDS \_ PIXELFORMAT**](dds-pixelformat.md)**</span><span class="sxs-lookup"><span data-stu-id="d4d46-169">Type: **[**DDS\_PIXELFORMAT**](dds-pixelformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d4d46-170">Le format de pixel (voir [**DDS \_ PIXELFORMAT**](dds-pixelformat.md)).</span><span class="sxs-lookup"><span data-stu-id="d4d46-170">The pixel format (see [**DDS\_PIXELFORMAT**](dds-pixelformat.md)).</span></span>

</dd> <dt>

<span data-ttu-id="d4d46-171">**dwCaps**</span><span class="sxs-lookup"><span data-stu-id="d4d46-171">**dwCaps**</span></span>
</dt> <dd>

<span data-ttu-id="d4d46-172">Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d4d46-172">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d4d46-173">Spécifie la complexité des surfaces stockées.</span><span class="sxs-lookup"><span data-stu-id="d4d46-173">Specifies the complexity of the surfaces stored.</span></span>



| <span data-ttu-id="d4d46-174">Indicateur</span><span class="sxs-lookup"><span data-stu-id="d4d46-174">Flag</span></span>             | <span data-ttu-id="d4d46-175">Description</span><span class="sxs-lookup"><span data-stu-id="d4d46-175">Description</span></span>                                                                                                                              | <span data-ttu-id="d4d46-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4d46-176">Value</span></span>    |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------|----------|
| <span data-ttu-id="d4d46-177">DDSCAPS \_ complexe</span><span class="sxs-lookup"><span data-stu-id="d4d46-177">DDSCAPS\_COMPLEX</span></span> | <span data-ttu-id="d4d46-178">Facultatif doit être utilisé sur tout fichier qui contient plusieurs surfaces (un mipmap, une carte d’environnement cubique ou une texture de volume mipmapped).</span><span class="sxs-lookup"><span data-stu-id="d4d46-178">Optional; must be used on any file that contains more than one surface (a mipmap, a cubic environment map, or mipmapped volume texture).</span></span> | <span data-ttu-id="d4d46-179">0x8</span><span class="sxs-lookup"><span data-stu-id="d4d46-179">0x8</span></span>      |
| <span data-ttu-id="d4d46-180">\_MIPMAP DDSCAPS</span><span class="sxs-lookup"><span data-stu-id="d4d46-180">DDSCAPS\_MIPMAP</span></span>  | <span data-ttu-id="d4d46-181">Facultatif doit être utilisé pour un mipmap.</span><span class="sxs-lookup"><span data-stu-id="d4d46-181">Optional; should be used for a mipmap.</span></span>                                                                                                   | <span data-ttu-id="d4d46-182">0x400000</span><span class="sxs-lookup"><span data-stu-id="d4d46-182">0x400000</span></span> |
| <span data-ttu-id="d4d46-183">\_texture DDSCAPS</span><span class="sxs-lookup"><span data-stu-id="d4d46-183">DDSCAPS\_TEXTURE</span></span> | <span data-ttu-id="d4d46-184">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d4d46-184">Required</span></span>                                                                                                                                 | <span data-ttu-id="d4d46-185">0x1000</span><span class="sxs-lookup"><span data-stu-id="d4d46-185">0x1000</span></span>   |



 

> [!Note]  
> <span data-ttu-id="d4d46-186">Lorsque vous écrivez des fichiers. DDS, vous devez définir l' \_ indicateur de texture DDSCAPS et, pour plusieurs surfaces, vous devez également définir l' \_ indicateur complexe DDSCAPS.</span><span class="sxs-lookup"><span data-stu-id="d4d46-186">When you write .dds files, you should set the DDSCAPS\_TEXTURE flag, and for multiple surfaces you should also set the DDSCAPS\_COMPLEX flag.</span></span> <span data-ttu-id="d4d46-187">Toutefois, lorsque vous lisez un fichier. DDS, vous ne devez pas vous appuyer sur la \_ texture DDSCAPS et les \_ indicateurs complexes DDSCAPS sont définis, car certains enregistreurs d’un tel fichier peuvent ne pas définir ces indicateurs.</span><span class="sxs-lookup"><span data-stu-id="d4d46-187">However, when you read a .dds file, you should not rely on the DDSCAPS\_TEXTURE and DDSCAPS\_COMPLEX flags being set because some writers of such a file might not set these flags.</span></span>

 

<span data-ttu-id="d4d46-188">L' \_ \_ \_ indicateur mipmap des indicateurs de surface DDS, qui est défini dans DDS. h, est une combinaison de bits or des \_ indicateurs mipmap DDSCAPS et DDSCAPS \_ .</span><span class="sxs-lookup"><span data-stu-id="d4d46-188">The DDS\_SURFACE\_FLAGS\_MIPMAP flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS\_COMPLEX and DDSCAPS\_MIPMAP flags.</span></span>

<span data-ttu-id="d4d46-189">L' \_ \_ \_ indicateur de texture indicateurs de surface DDS, qui est défini dans DDS. h, est égal à l' \_ indicateur de texture DDSCAPS.</span><span class="sxs-lookup"><span data-stu-id="d4d46-189">The DDS\_SURFACE\_FLAGS\_TEXTURE flag, which is defined in Dds.h, is equal to the DDSCAPS\_TEXTURE flag.</span></span>

<span data-ttu-id="d4d46-190">L' \_ indicateur carte cubique des indicateurs de surface DDS \_ \_ , défini dans DDS. h, est égal à l' \_ indicateur complexe DDSCAPS.</span><span class="sxs-lookup"><span data-stu-id="d4d46-190">The DDS\_SURFACE\_FLAGS\_CUBEMAP flag, which is defined in Dds.h, is equal to the DDSCAPS\_COMPLEX flag.</span></span>

</dd> <dt>

<span data-ttu-id="d4d46-191">**dwCaps2**</span><span class="sxs-lookup"><span data-stu-id="d4d46-191">**dwCaps2**</span></span>
</dt> <dd>

<span data-ttu-id="d4d46-192">Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d4d46-192">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d4d46-193">Détails supplémentaires sur les surfaces stockées.</span><span class="sxs-lookup"><span data-stu-id="d4d46-193">Additional detail about the surfaces stored.</span></span>



| <span data-ttu-id="d4d46-194">Indicateur</span><span class="sxs-lookup"><span data-stu-id="d4d46-194">Flag</span></span>                         | <span data-ttu-id="d4d46-195">Description</span><span class="sxs-lookup"><span data-stu-id="d4d46-195">Description</span></span>                                            | <span data-ttu-id="d4d46-196">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4d46-196">Value</span></span>    |
|------------------------------|--------------------------------------------------------|----------|
| <span data-ttu-id="d4d46-197">DDSCAPS2 \_ carte cubique</span><span class="sxs-lookup"><span data-stu-id="d4d46-197">DDSCAPS2\_CUBEMAP</span></span>            | <span data-ttu-id="d4d46-198">Requis pour un mappage de cube.</span><span class="sxs-lookup"><span data-stu-id="d4d46-198">Required for a cube map.</span></span>                               | <span data-ttu-id="d4d46-199">0x200</span><span class="sxs-lookup"><span data-stu-id="d4d46-199">0x200</span></span>    |
| <span data-ttu-id="d4d46-200">DDSCAPS2 \_ carte cubique \_ POSITIVEX</span><span class="sxs-lookup"><span data-stu-id="d4d46-200">DDSCAPS2\_CUBEMAP\_POSITIVEX</span></span> | <span data-ttu-id="d4d46-201">Obligatoire lorsque ces surfaces sont stockées dans un mappage de cube.</span><span class="sxs-lookup"><span data-stu-id="d4d46-201">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="d4d46-202">0x400</span><span class="sxs-lookup"><span data-stu-id="d4d46-202">0x400</span></span>    |
| <span data-ttu-id="d4d46-203">DDSCAPS2 \_ carte cubique \_ NEGATIVEX</span><span class="sxs-lookup"><span data-stu-id="d4d46-203">DDSCAPS2\_CUBEMAP\_NEGATIVEX</span></span> | <span data-ttu-id="d4d46-204">Obligatoire lorsque ces surfaces sont stockées dans un mappage de cube.</span><span class="sxs-lookup"><span data-stu-id="d4d46-204">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="d4d46-205">0x800</span><span class="sxs-lookup"><span data-stu-id="d4d46-205">0x800</span></span>    |
| <span data-ttu-id="d4d46-206">DDSCAPS2 \_ carte cubique \_ positif</span><span class="sxs-lookup"><span data-stu-id="d4d46-206">DDSCAPS2\_CUBEMAP\_POSITIVEY</span></span> | <span data-ttu-id="d4d46-207">Obligatoire lorsque ces surfaces sont stockées dans un mappage de cube.</span><span class="sxs-lookup"><span data-stu-id="d4d46-207">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="d4d46-208">0x1000</span><span class="sxs-lookup"><span data-stu-id="d4d46-208">0x1000</span></span>   |
| <span data-ttu-id="d4d46-209">DDSCAPS2 \_ carte cubique \_ négatif</span><span class="sxs-lookup"><span data-stu-id="d4d46-209">DDSCAPS2\_CUBEMAP\_NEGATIVEY</span></span> | <span data-ttu-id="d4d46-210">Obligatoire lorsque ces surfaces sont stockées dans un mappage de cube.</span><span class="sxs-lookup"><span data-stu-id="d4d46-210">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="d4d46-211">0x2000</span><span class="sxs-lookup"><span data-stu-id="d4d46-211">0x2000</span></span>   |
| <span data-ttu-id="d4d46-212">DDSCAPS2 \_ carte cubique \_ POSITIVEZ</span><span class="sxs-lookup"><span data-stu-id="d4d46-212">DDSCAPS2\_CUBEMAP\_POSITIVEZ</span></span> | <span data-ttu-id="d4d46-213">Obligatoire lorsque ces surfaces sont stockées dans un mappage de cube.</span><span class="sxs-lookup"><span data-stu-id="d4d46-213">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="d4d46-214">0x4000</span><span class="sxs-lookup"><span data-stu-id="d4d46-214">0x4000</span></span>   |
| <span data-ttu-id="d4d46-215">DDSCAPS2 \_ carte cubique \_ NEGATIVEZ</span><span class="sxs-lookup"><span data-stu-id="d4d46-215">DDSCAPS2\_CUBEMAP\_NEGATIVEZ</span></span> | <span data-ttu-id="d4d46-216">Obligatoire lorsque ces surfaces sont stockées dans un mappage de cube.</span><span class="sxs-lookup"><span data-stu-id="d4d46-216">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="d4d46-217">0x8000</span><span class="sxs-lookup"><span data-stu-id="d4d46-217">0x8000</span></span>   |
| <span data-ttu-id="d4d46-218">\_Volume DDSCAPS2</span><span class="sxs-lookup"><span data-stu-id="d4d46-218">DDSCAPS2\_VOLUME</span></span>             | <span data-ttu-id="d4d46-219">Requis pour une texture de volume.</span><span class="sxs-lookup"><span data-stu-id="d4d46-219">Required for a volume texture.</span></span>                         | <span data-ttu-id="d4d46-220">0x200000</span><span class="sxs-lookup"><span data-stu-id="d4d46-220">0x200000</span></span> |



 

<span data-ttu-id="d4d46-221">L' \_ indicateur DDS carte cubique \_ POSITIVEX, qui est défini dans DDS. h, est une combinaison or au niveau du bit des \_ indicateurs DDSCAPS2 carte cubique \_ et \_ DDSCAPS2 carte cubique POSITIVEX.</span><span class="sxs-lookup"><span data-stu-id="d4d46-221">The DDS\_CUBEMAP\_POSITIVEX flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_POSITIVEX flags.</span></span>

<span data-ttu-id="d4d46-222">L' \_ indicateur DDS carte cubique \_ NEGATIVEX, qui est défini dans DDS. h, est une combinaison or au niveau du bit des \_ indicateurs DDSCAPS2 carte cubique \_ et \_ DDSCAPS2 carte cubique NEGATIVEX.</span><span class="sxs-lookup"><span data-stu-id="d4d46-222">The DDS\_CUBEMAP\_NEGATIVEX flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_NEGATIVEX flags.</span></span>

<span data-ttu-id="d4d46-223">L' \_ \_ indicateur de positif DDS carte cubique, qui est défini dans DDS. h, est une combinaison au niveau du bit or des \_ indicateurs positifs DDSCAPS2 carte cubique et DDSCAPS2 \_ carte cubique \_ .</span><span class="sxs-lookup"><span data-stu-id="d4d46-223">The DDS\_CUBEMAP\_POSITIVEY flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_POSITIVEY flags.</span></span>

<span data-ttu-id="d4d46-224">L' \_ \_ indicateur de négatif DDS carte cubique, qui est défini dans DDS. h, est une combinaison au niveau du bit ou de la DDSCAPS2 \_ carte cubique et DDSCAPS2 \_ carte cubique les \_ indicateurs négatifs.</span><span class="sxs-lookup"><span data-stu-id="d4d46-224">The DDS\_CUBEMAP\_NEGATIVEY flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_NEGATIVEY flags.</span></span>

<span data-ttu-id="d4d46-225">L' \_ indicateur DDS carte cubique \_ POSITIVEZ, qui est défini dans DDS. h, est une combinaison or au niveau du bit des \_ indicateurs DDSCAPS2 carte cubique \_ et \_ DDSCAPS2 carte cubique POSITIVEZ.</span><span class="sxs-lookup"><span data-stu-id="d4d46-225">The DDS\_CUBEMAP\_POSITIVEZ flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_POSITIVEZ flags.</span></span>

<span data-ttu-id="d4d46-226">L' \_ indicateur DDS carte cubique \_ NEGATIVEZ, qui est défini dans DDS. h, est une combinaison or au niveau du bit des \_ indicateurs DDSCAPS2 carte cubique \_ et \_ DDSCAPS2 carte cubique NEGATIVEZ.</span><span class="sxs-lookup"><span data-stu-id="d4d46-226">The DDS\_CUBEMAP\_NEGATIVEZ flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_NEGATIVEZ flags.</span></span>

<span data-ttu-id="d4d46-227">L' \_ indicateur DDS carte cubique \_ ALLFACES, qui est défini dans DDS. h, est une combinaison or au niveau du bit des \_ carte cubique DDS \_ POSITIVEX, DDS \_ carte cubique \_ NEGATIVEX, DDS \_ carte cubique \_ positive, DDS \_ carte cubique \_ Negative, DDS \_ carte cubique \_ POSITIVEZ et DDSCAPS2 \_ \_ carte cubique NEGATIVEZ.</span><span class="sxs-lookup"><span data-stu-id="d4d46-227">The DDS\_CUBEMAP\_ALLFACES flag, which is defined in Dds.h, is a bitwise-OR combination of the DDS\_CUBEMAP\_POSITIVEX, DDS\_CUBEMAP\_NEGATIVEX, DDS\_CUBEMAP\_POSITIVEY, DDS\_CUBEMAP\_NEGATIVEY, DDS\_CUBEMAP\_POSITIVEZ, and DDSCAPS2\_CUBEMAP\_NEGATIVEZ flags.</span></span>

<span data-ttu-id="d4d46-228">L' \_ \_ indicateur de volume des indicateurs DDS, défini dans DDS. h, est égal à l' \_ indicateur de volume DDSCAPS2.</span><span class="sxs-lookup"><span data-stu-id="d4d46-228">The DDS\_FLAGS\_VOLUME flag, which is defined in Dds.h, is equal to the DDSCAPS2\_VOLUME flag.</span></span>

> [!Note]  
> <span data-ttu-id="d4d46-229">Bien que Direct3D 9 prenne en charge les mappages de cubes partiels, Direct3D 10, 10,1 et 11 nécessitent que vous définissiez les six visages de mappage de cube (autrement dit, vous devez définir DDS \_ carte cubique \_ ALLFACES).</span><span class="sxs-lookup"><span data-stu-id="d4d46-229">Although Direct3D 9 supports partial cube-maps, Direct3D 10, 10.1, and 11 require that you define all six cube-map faces (that is, you must set DDS\_CUBEMAP\_ALLFACES).</span></span>

 

</dd> <dt>

<span data-ttu-id="d4d46-230">**dwCaps3**</span><span class="sxs-lookup"><span data-stu-id="d4d46-230">**dwCaps3**</span></span>
</dt> <dd>

<span data-ttu-id="d4d46-231">Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d4d46-231">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d4d46-232">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="d4d46-232">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="d4d46-233">**dwCaps4**</span><span class="sxs-lookup"><span data-stu-id="d4d46-233">**dwCaps4**</span></span>
</dt> <dd>

<span data-ttu-id="d4d46-234">Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d4d46-234">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d4d46-235">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="d4d46-235">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="d4d46-236">**dwReserved2**</span><span class="sxs-lookup"><span data-stu-id="d4d46-236">**dwReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="d4d46-237">Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d4d46-237">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d4d46-238">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="d4d46-238">Unused.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4d46-239">Notes</span><span class="sxs-lookup"><span data-stu-id="d4d46-239">Remarks</span></span>

<span data-ttu-id="d4d46-240">Incluez les indicateurs dans **dwFlags** pour les membres de la structure qui contiennent des données valides.</span><span class="sxs-lookup"><span data-stu-id="d4d46-240">Include flags in **dwFlags** for the members of the structure that contain valid data.</span></span>

<span data-ttu-id="d4d46-241">Utilisez cette structure en association avec un [**\_ en-tête DDS \_ DXT10**](dds-header-dxt10.md) pour stocker un tableau de ressources dans un fichier DDS.</span><span class="sxs-lookup"><span data-stu-id="d4d46-241">Use this structure in combination with a [**DDS\_HEADER\_DXT10**](dds-header-dxt10.md) to store a resource array in a DDS file.</span></span> <span data-ttu-id="d4d46-242">Pour plus d’informations, consultez [tableaux de texture](dx-graphics-dds-pguide.md).</span><span class="sxs-lookup"><span data-stu-id="d4d46-242">For more information, see [texture arrays](dx-graphics-dds-pguide.md).</span></span>

<span data-ttu-id="d4d46-243">**DDS \_ L’en-tête** est identique à la structure DDSURFACEDESC2 de DirectDraw sans les dépendances DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="d4d46-243">**DDS\_HEADER** is identical to the DirectDraw DDSURFACEDESC2 structure without DirectDraw dependencies.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4d46-244">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4d46-244">Requirements</span></span>



| <span data-ttu-id="d4d46-245">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4d46-245">Requirement</span></span> | <span data-ttu-id="d4d46-246">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4d46-246">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d4d46-247">En-tête</span><span class="sxs-lookup"><span data-stu-id="d4d46-247">Header</span></span><br/> | <dl> <span data-ttu-id="d4d46-248"><dt>DDS. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4d46-248"><dt>Dds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4d46-249">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4d46-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4d46-250">Référence pour DDS</span><span class="sxs-lookup"><span data-stu-id="d4d46-250">Reference for DDS</span></span>](dx-graphics-dds-reference.md)
</dt> </dl>

 

