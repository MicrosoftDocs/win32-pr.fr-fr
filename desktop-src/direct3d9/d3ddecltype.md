---
description: Définit un type de données de déclaration de vertex.
ms.assetid: 993fc7e4-4752-4bce-82d0-0a034fdc69c0
title: Énumération D3DDECLTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3edb3f936772a7265c627f10eeb7aeb4f461701e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322729"
---
# <a name="d3ddecltype-enumeration"></a><span data-ttu-id="7c1b9-103">Énumération D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="7c1b9-103">D3DDECLTYPE enumeration</span></span>

<span data-ttu-id="7c1b9-104">Définit un type de données de déclaration de vertex.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-104">Defines a vertex declaration data type.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c1b9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c1b9-105">Syntax</span></span>


```C++
typedef enum D3DDECLTYPE { 
  D3DDECLTYPE_FLOAT1     = 0,
  D3DDECLTYPE_FLOAT2     = 1,
  D3DDECLTYPE_FLOAT3     = 2,
  D3DDECLTYPE_FLOAT4     = 3,
  D3DDECLTYPE_D3DCOLOR   = 4,
  D3DDECLTYPE_UBYTE4     = 5,
  D3DDECLTYPE_SHORT2     = 6,
  D3DDECLTYPE_SHORT4     = 7,
  D3DDECLTYPE_UBYTE4N    = 8,
  D3DDECLTYPE_SHORT2N    = 9,
  D3DDECLTYPE_SHORT4N    = 10,
  D3DDECLTYPE_USHORT2N   = 11,
  D3DDECLTYPE_USHORT4N   = 12,
  D3DDECLTYPE_UDEC3      = 13,
  D3DDECLTYPE_DEC3N      = 14,
  D3DDECLTYPE_FLOAT16_2  = 15,
  D3DDECLTYPE_FLOAT16_4  = 16,
  D3DDECLTYPE_UNUSED     = 17
} D3DDECLTYPE, *LPD3DDECLTYPE;
```



## <a name="constants"></a><span data-ttu-id="7c1b9-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="7c1b9-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7c1b9-107"><span id="D3DDECLTYPE_FLOAT1"></span><span id="d3ddecltype_float1"></span>**D3DDECLTYPE \_ FLOAT1**</span><span class="sxs-lookup"><span data-stu-id="7c1b9-107"><span id="D3DDECLTYPE_FLOAT1"></span><span id="d3ddecltype_float1"></span>**D3DDECLTYPE\_FLOAT1**</span></span>
</dt> <dd>

<span data-ttu-id="7c1b9-108">Float à un composant développé sur (float, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="7c1b9-108">One-component float expanded to (float, 0, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="7c1b9-109"><span id="D3DDECLTYPE_FLOAT2"></span><span id="d3ddecltype_float2"></span>**D3DDECLTYPE \_ FLOAT2**</span><span class="sxs-lookup"><span data-stu-id="7c1b9-109"><span id="D3DDECLTYPE_FLOAT2"></span><span id="d3ddecltype_float2"></span>**D3DDECLTYPE\_FLOAT2**</span></span>
</dt> <dd>

<span data-ttu-id="7c1b9-110">Float à deux composants développé sur (float, float, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="7c1b9-110">Two-component float expanded to (float, float, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="7c1b9-111"><span id="D3DDECLTYPE_FLOAT3"></span><span id="d3ddecltype_float3"></span>**D3DDECLTYPE \_ FLOAT3**</span><span class="sxs-lookup"><span data-stu-id="7c1b9-111"><span id="D3DDECLTYPE_FLOAT3"></span><span id="d3ddecltype_float3"></span>**D3DDECLTYPE\_FLOAT3**</span></span>
</dt> <dd>

<span data-ttu-id="7c1b9-112">Float à trois composants développé sur (float, float, float, 1).</span><span class="sxs-lookup"><span data-stu-id="7c1b9-112">Three-component float expanded to (float, float, float, 1).</span></span>

</dd> <dt>

<span data-ttu-id="7c1b9-113"><span id="D3DDECLTYPE_FLOAT4"></span><span id="d3ddecltype_float4"></span>**D3DDECLTYPE \_ float4**</span><span class="sxs-lookup"><span data-stu-id="7c1b9-113"><span id="D3DDECLTYPE_FLOAT4"></span><span id="d3ddecltype_float4"></span>**D3DDECLTYPE\_FLOAT4**</span></span>
</dt> <dd>

<span data-ttu-id="7c1b9-114">Float à quatre composants développé sur (float, float, float, float).</span><span class="sxs-lookup"><span data-stu-id="7c1b9-114">Four-component float expanded to (float, float, float, float).</span></span>

</dd> <dt>

<span data-ttu-id="7c1b9-115"><span id="D3DDECLTYPE_D3DCOLOR"></span><span id="d3ddecltype_d3dcolor"></span>**D3DDECLTYPE \_ D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="7c1b9-115"><span id="D3DDECLTYPE_D3DCOLOR"></span><span id="d3ddecltype_d3dcolor"></span>**D3DDECLTYPE\_D3DCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="7c1b9-116">Octets compressés à quatre composants, non signés, mappés à 0 à 1 plage.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-116">Four-component, packed, unsigned bytes mapped to 0 to 1 range.</span></span> <span data-ttu-id="7c1b9-117">L’entrée est un [**D3DCOLOR**](d3dcolor.md) et est développé en ordre RVBA.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-117">Input is a [**D3DCOLOR**](d3dcolor.md) and is expanded to RGBA order.</span></span>

</dd> <dt>

<span data-ttu-id="7c1b9-118"><span id="D3DDECLTYPE_UBYTE4"></span><span id="d3ddecltype_ubyte4"></span>**D3DDECLTYPE \_ UBYTE4**</span><span class="sxs-lookup"><span data-stu-id="7c1b9-118"><span id="D3DDECLTYPE_UBYTE4"></span><span id="d3ddecltype_ubyte4"></span>**D3DDECLTYPE\_UBYTE4**</span></span>
</dt> <dd>

<span data-ttu-id="7c1b9-119">Octet non signé de quatre composants.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-119">Four-component, unsigned byte.</span></span>

</dd> <dt>

<span data-ttu-id="7c1b9-120"><span id="D3DDECLTYPE_SHORT2"></span><span id="d3ddecltype_short2"></span>**D3DDECLTYPE \_ SHORT2**</span><span class="sxs-lookup"><span data-stu-id="7c1b9-120"><span id="D3DDECLTYPE_SHORT2"></span><span id="d3ddecltype_short2"></span>**D3DDECLTYPE\_SHORT2**</span></span>
</dt> <dd>

<span data-ttu-id="7c1b9-121">Deux composants, signés Short, étendus à (valeur, valeur, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="7c1b9-121">Two-component, signed short expanded to (value, value, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="7c1b9-122"><span id="D3DDECLTYPE_SHORT4"></span><span id="d3ddecltype_short4"></span>**D3DDECLTYPE \_ SHORT4**</span><span class="sxs-lookup"><span data-stu-id="7c1b9-122"><span id="D3DDECLTYPE_SHORT4"></span><span id="d3ddecltype_short4"></span>**D3DDECLTYPE\_SHORT4**</span></span>
</dt> <dd>

<span data-ttu-id="7c1b9-123">Quatre-Components, signés Short, étendus à (valeur, valeur, valeur, valeur).</span><span class="sxs-lookup"><span data-stu-id="7c1b9-123">Four-component, signed short expanded to (value, value, value, value).</span></span>

</dd> <dt>

<span data-ttu-id="7c1b9-124"><span id="D3DDECLTYPE_UBYTE4N"></span><span id="d3ddecltype_ubyte4n"></span>**D3DDECLTYPE \_ UBYTE4N**</span><span class="sxs-lookup"><span data-stu-id="7c1b9-124"><span id="D3DDECLTYPE_UBYTE4N"></span><span id="d3ddecltype_ubyte4n"></span>**D3DDECLTYPE\_UBYTE4N**</span></span>
</dt> <dd>

<span data-ttu-id="7c1b9-125">Octet à quatre composants avec chaque octet normalisé en divisant avec 255.0 f.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-125">Four-component byte with each byte normalized by dividing with 255.0f.</span></span>

</dd> <dt>

<span data-ttu-id="7c1b9-126"><span id="D3DDECLTYPE_SHORT2N"></span><span id="d3ddecltype_short2n"></span>**D3DDECLTYPE \_ SHORT2N**</span><span class="sxs-lookup"><span data-stu-id="7c1b9-126"><span id="D3DDECLTYPE_SHORT2N"></span><span id="d3ddecltype_short2n"></span>**D3DDECLTYPE\_SHORT2N**</span></span>
</dt> <dd>

<span data-ttu-id="7c1b9-127">Normald, à deux composants, signé à Short, étendu à (First Short/32767.0, second Short/32767.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="7c1b9-127">Normalized, two-component, signed short, expanded to (first short/32767.0, second short/32767.0, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="7c1b9-128"><span id="D3DDECLTYPE_SHORT4N"></span><span id="d3ddecltype_short4n"></span>**D3DDECLTYPE \_ SHORT4N**</span><span class="sxs-lookup"><span data-stu-id="7c1b9-128"><span id="D3DDECLTYPE_SHORT4N"></span><span id="d3ddecltype_short4n"></span>**D3DDECLTYPE\_SHORT4N**</span></span>
</dt> <dd>

<span data-ttu-id="7c1b9-129">Normalized, quatre-Components, signés Short, étendus à (First Short/32767.0, second Short/32767.0, Third Short/32767.0, quatrième Short/32767.0).</span><span class="sxs-lookup"><span data-stu-id="7c1b9-129">Normalized, four-component, signed short, expanded to (first short/32767.0, second short/32767.0, third short/32767.0, fourth short/32767.0).</span></span>

</dd> <dt>

<span data-ttu-id="7c1b9-130"><span id="D3DDECLTYPE_USHORT2N"></span><span id="d3ddecltype_ushort2n"></span>**D3DDECLTYPE \_ USHORT2N**</span><span class="sxs-lookup"><span data-stu-id="7c1b9-130"><span id="D3DDECLTYPE_USHORT2N"></span><span id="d3ddecltype_ushort2n"></span>**D3DDECLTYPE\_USHORT2N**</span></span>
</dt> <dd>

<span data-ttu-id="7c1b9-131">Normald, deux composants, unsigned short, Expanded to (First Short/65535.0, Short Short/65535.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="7c1b9-131">Normalized, two-component, unsigned short, expanded to (first short/65535.0, short short/65535.0, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="7c1b9-132"><span id="D3DDECLTYPE_USHORT4N"></span><span id="d3ddecltype_ushort4n"></span>**D3DDECLTYPE \_ USHORT4N**</span><span class="sxs-lookup"><span data-stu-id="7c1b9-132"><span id="D3DDECLTYPE_USHORT4N"></span><span id="d3ddecltype_ushort4n"></span>**D3DDECLTYPE\_USHORT4N**</span></span>
</dt> <dd>

<span data-ttu-id="7c1b9-133">Normald, quatre composants, unsigned short, Expanded à (First Short/65535.0, second Short/65535.0, Third Short/65535.0, quatrième Short/65535.0).</span><span class="sxs-lookup"><span data-stu-id="7c1b9-133">Normalized, four-component, unsigned short, expanded to (first short/65535.0, second short/65535.0, third short/65535.0, fourth short/65535.0).</span></span>

</dd> <dt>

<span data-ttu-id="7c1b9-134"><span id="D3DDECLTYPE_UDEC3"></span><span id="d3ddecltype_udec3"></span>**D3DDECLTYPE \_ UDEC3**</span><span class="sxs-lookup"><span data-stu-id="7c1b9-134"><span id="D3DDECLTYPE_UDEC3"></span><span id="d3ddecltype_udec3"></span>**D3DDECLTYPE\_UDEC3**</span></span>
</dt> <dd>

<span data-ttu-id="7c1b9-135">Le format 3 composants, non signé, 10 10 10 développé sur (valeur, valeur, valeur, 1).</span><span class="sxs-lookup"><span data-stu-id="7c1b9-135">Three-component, unsigned, 10 10 10 format expanded to (value, value, value, 1).</span></span>

</dd> <dt>

<span data-ttu-id="7c1b9-136"><span id="D3DDECLTYPE_DEC3N"></span><span id="d3ddecltype_dec3n"></span>**D3DDECLTYPE \_ DEC3N**</span><span class="sxs-lookup"><span data-stu-id="7c1b9-136"><span id="D3DDECLTYPE_DEC3N"></span><span id="d3ddecltype_dec3n"></span>**D3DDECLTYPE\_DEC3N**</span></span>
</dt> <dd>

<span data-ttu-id="7c1b9-137">Format à trois composants, signé, 10 10 10 normalisé et développé pour (v \[ 0 \] /511,0, v \[ 1 \] /511,0, v \[ 2 \] /511,0, 1).</span><span class="sxs-lookup"><span data-stu-id="7c1b9-137">Three-component, signed, 10 10 10 format normalized and expanded to (v\[0\]/511.0, v\[1\]/511.0, v\[2\]/511.0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="7c1b9-138"><span id="D3DDECLTYPE_FLOAT16_2"></span><span id="d3ddecltype_float16_2"></span>**D3DDECLTYPE \_ FLOAT16 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="7c1b9-138"><span id="D3DDECLTYPE_FLOAT16_2"></span><span id="d3ddecltype_float16_2"></span>**D3DDECLTYPE\_FLOAT16\_2**</span></span>
</dt> <dd>

<span data-ttu-id="7c1b9-139">Virgule flottante à deux composants, 16 bits, développée à (valeur, valeur, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="7c1b9-139">Two-component, 16-bit, floating point expanded to (value, value, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="7c1b9-140"><span id="D3DDECLTYPE_FLOAT16_4"></span><span id="d3ddecltype_float16_4"></span>**D3DDECLTYPE \_ FLOAT16 \_ 4**</span><span class="sxs-lookup"><span data-stu-id="7c1b9-140"><span id="D3DDECLTYPE_FLOAT16_4"></span><span id="d3ddecltype_float16_4"></span>**D3DDECLTYPE\_FLOAT16\_4**</span></span>
</dt> <dd>

<span data-ttu-id="7c1b9-141">Virgule flottante à quatre composants, 16 bits et développée en (valeur, valeur, valeur, valeur).</span><span class="sxs-lookup"><span data-stu-id="7c1b9-141">Four-component, 16-bit, floating point expanded to (value, value, value, value).</span></span>

</dd> <dt>

<span data-ttu-id="7c1b9-142"><span id="D3DDECLTYPE_UNUSED"></span><span id="d3ddecltype_unused"></span>**D3DDECLTYPE \_ INutilisé**</span><span class="sxs-lookup"><span data-stu-id="7c1b9-142"><span id="D3DDECLTYPE_UNUSED"></span><span id="d3ddecltype_unused"></span>**D3DDECLTYPE\_UNUSED**</span></span>
</dt> <dd>

<span data-ttu-id="7c1b9-143">Le champ de type dans la déclaration n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-143">Type field in the declaration is unused.</span></span> <span data-ttu-id="7c1b9-144">Il est conçu pour être utilisé avec D3DDECLMETHOD \_ UV et D3DDECLMETHOD \_ LOOKUPPRESAMPLED.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-144">This is designed for use with D3DDECLMETHOD\_UV and D3DDECLMETHOD\_LOOKUPPRESAMPLED.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c1b9-145">Notes</span><span class="sxs-lookup"><span data-stu-id="7c1b9-145">Remarks</span></span>

<span data-ttu-id="7c1b9-146">Les données de vertex sont déclarées avec un tableau de structures [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) .</span><span class="sxs-lookup"><span data-stu-id="7c1b9-146">Vertex data is declared with an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) structures.</span></span> <span data-ttu-id="7c1b9-147">Chaque élément du tableau contient un type de données de déclaration de vertex.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-147">Each element in the array contains a vertex declaration data type.</span></span>

<span data-ttu-id="7c1b9-148">Utilisez l’outil visionneuse de la prise en charge DirectX (DXCapsViewer.exe) pour déterminer les types pris en charge sur votre appareil.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-148">Use the DirectX Caps Viewer Tool (DXCapsViewer.exe) to see which types are supported on your device.</span></span> <span data-ttu-id="7c1b9-149">Vous pouvez obtenir cet outil et en savoir plus à ce sujet à partir du kit de développement logiciel (SDK) DirectX.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-149">You can get this tool and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="7c1b9-150">Pour plus d’informations sur DirectX SDK, consultez [où se trouve le kit de développement logiciel (SDK) DirectX ?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="7c1b9-150">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c1b9-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c1b9-151">Requirements</span></span>



| <span data-ttu-id="7c1b9-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c1b9-152">Requirement</span></span> | <span data-ttu-id="7c1b9-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c1b9-153">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c1b9-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="7c1b9-154">Header</span></span><br/> | <dl> <span data-ttu-id="7c1b9-155"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c1b9-155"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c1b9-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c1b9-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c1b9-157">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="7c1b9-157">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="7c1b9-158">**D3DDECLMETHOD**</span><span class="sxs-lookup"><span data-stu-id="7c1b9-158">**D3DDECLMETHOD**</span></span>](./d3ddeclmethod.md)
</dt> </dl>

 

 
