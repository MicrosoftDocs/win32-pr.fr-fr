---
title: Structure CD3DX12_RESOURCE_DESC (D3dx12. h)
description: Une structure d’assistance pour faciliter l’initialisation d’une structure d’application de \_ Description de ressource D3D12 \_ .
ms.assetid: F18D41BE-8AEF-444E-AC8B-EC57C63BF083
keywords:
- Structure CD3DX12_RESOURCE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b341646b2dee7f469235c0b0bc9bb4550e56ff5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539922"
---
# <a name="cd3dx12_resource_desc-structure"></a><span data-ttu-id="41da2-104">CD3DX12, structure de description de la \_ ressource \_</span><span class="sxs-lookup"><span data-stu-id="41da2-104">CD3DX12\_RESOURCE\_DESC structure</span></span>

<span data-ttu-id="41da2-105">Une structure d’assistance pour faciliter l’initialisation d’une structure d’application de [**\_ \_ Description de ressource D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) .</span><span class="sxs-lookup"><span data-stu-id="41da2-105">A helper structure to enable easy initialization of a [**D3D12\_RESOURCE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="41da2-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41da2-106">Syntax</span></span>


```C++
struct CD3DX12_RESOURCE_DESC  : public D3D12_RESOURCE_DESC{
                        CD3DX12_RESOURCE_DESC();
                        explicit CD3DX12_RESOURCE_DESC(const D3D12_RESOURCE_DESC& o);
                        CD3DX12_RESOURCE_DESC(D3D12_RESOURCE_DIMENSION dimension, UINT64 alignment, UINT64 width, UINT height, UINT16 depthOrArraySize, UINT16 mipLevels, DXGI_FORMAT format, UINT sampleCount, UINT sampleQuality, D3D12_TEXTURE_LAYOUT layout, D3D12_RESOURCE_FLAGS flags);
  CD3DX12_RESOURCE_DESC static inline Buffer(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE);
  CD3DX12_RESOURCE_DESC static inline Buffer(UINT64 width, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex1D(DXGI_FORMAT format, UINT64 width, UINT16 arraySize = 1, UINT16 mipLevels = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex2D(DXGI_FORMAT format, UINT64 width, UINT height, UINT16 arraySize = 1, UINT16 mipLevels = 0, UINT sampleCount = 1, UINT sampleQuality = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex3D(DXGI_FORMAT format, UINT64 width, UINT height, UINT16 depth, UINT16 mipLevels = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  UINT16                inline Depth() const;
  UINT16                inline ArraySize() const;
  UINT8                 inline PlaneCount(ID3D12Device* pDevice) const;
  UINT                  inline Subresources(ID3D12Device* pDevice) const;
  UINT                  inline CalcSubresource(UINT MipSlice, UINT ArraySlice, UINT PlaneSlice);
                        operator const D3D12_RESOURCE_DESC&() const;
                        operator == (const D3D12_RESOURCE_DESC& l, const D3D12_RESOURCE_DESC& r);
                        operator !=  (const D3D12_RESOURCE_DESC& l, const D3D12_RESOURCE_DESC& r);
};
```



## <a name="members"></a><span data-ttu-id="41da2-107">Membres</span><span class="sxs-lookup"><span data-stu-id="41da2-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="41da2-108">**\_Description de la ressource CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="41da2-108">**CD3DX12\_RESOURCE\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="41da2-109">Crée une nouvelle instance non initialisée d’une description de la \_ ressource CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="41da2-109">Creates a new, uninitialized, instance of a CD3DX12\_RESOURCE\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="41da2-110">**Description de la ressource CD3DX12 explicite \_ \_ (CONSt D3D12 \_ resource \_ desc& o)**</span><span class="sxs-lookup"><span data-stu-id="41da2-110">**explicit CD3DX12\_RESOURCE\_DESC(const D3D12\_RESOURCE\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="41da2-111">Crée une nouvelle instance d’une description de la \_ ressource CD3DX12 \_ , initialisée avec le contenu d’une autre structure [**\_ \_ desc des ressources D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) .</span><span class="sxs-lookup"><span data-stu-id="41da2-111">Creates a new instance of a CD3DX12\_RESOURCE\_DESC, initialized with the contents of another [**D3D12\_RESOURCE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="41da2-112">**CD3DX12 \_ Resource \_ desc ( \_ dimension de dimension de ressource D3D12 \_ , alignement de UInt64, mise en forme de UInt64, hauteur uint, UINT16 depthOrArraySize, UInt16 miplevels a, \_ format de format dxgi, uint sampleCount, uint sampleQuality, \_ \_ disposition de texture de texture D3D12, \_ indicateurs d’indicateurs de ressources D3D12 \_ )**</span><span class="sxs-lookup"><span data-stu-id="41da2-112">**CD3DX12\_RESOURCE\_DESC(D3D12\_RESOURCE\_DIMENSION dimension, UINT64 alignment, UINT64 width, UINT height, UINT16 depthOrArraySize, UINT16 mipLevels, DXGI\_FORMAT format, UINT sampleCount, UINT sampleQuality, D3D12\_TEXTURE\_LAYOUT layout, D3D12\_RESOURCE\_FLAGS flags)**</span></span>
</dt> <dd>

<span data-ttu-id="41da2-113">Crée une nouvelle instance d’une \_ Description de \_ la ressource CD3DX12, en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="41da2-113">Creates a new instance of a CD3DX12\_RESOURCE\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="41da2-114">[**D3D12 \_ Dimension de \_ dimension de ressource**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)</span><span class="sxs-lookup"><span data-stu-id="41da2-114">[**D3D12\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) dimension</span></span>

<span data-ttu-id="41da2-115">Alignement de UINT64</span><span class="sxs-lookup"><span data-stu-id="41da2-115">UINT64 alignment</span></span>

<span data-ttu-id="41da2-116">La largeur UINT64</span><span class="sxs-lookup"><span data-stu-id="41da2-116">UINT64 width</span></span>

<span data-ttu-id="41da2-117">Hauteur UINT</span><span class="sxs-lookup"><span data-stu-id="41da2-117">UINT height</span></span>

<span data-ttu-id="41da2-118">UINT16 depthOrArraySize</span><span class="sxs-lookup"><span data-stu-id="41da2-118">UINT16 depthOrArraySize</span></span>

<span data-ttu-id="41da2-119">UINT16 Miplevels a</span><span class="sxs-lookup"><span data-stu-id="41da2-119">UINT16 mipLevels</span></span>

<span data-ttu-id="41da2-120">[**Dxgi \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Format de format</span><span class="sxs-lookup"><span data-stu-id="41da2-120">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="41da2-121">UINT sampleCount</span><span class="sxs-lookup"><span data-stu-id="41da2-121">UINT sampleCount</span></span>

<span data-ttu-id="41da2-122">UINT sampleQuality</span><span class="sxs-lookup"><span data-stu-id="41da2-122">UINT sampleQuality</span></span>

<span data-ttu-id="41da2-123">[**D3D12 \_ Disposition \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) de la texture</span><span class="sxs-lookup"><span data-stu-id="41da2-123">[**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) layout</span></span>

<span data-ttu-id="41da2-124">[**D3D12 \_ Indicateurs \_ de ressource**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) indicateurs</span><span class="sxs-lookup"><span data-stu-id="41da2-124">[**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags</span></span>

</dd> <dt>

<span data-ttu-id="41da2-125">**Mémoire tampon Inline statique (const D3D12 \_ Resource \_ ALLOCATION \_ info& resAllocInfo, D3D12 \_ indicateurs de ressource \_ indicateurs = D3D12 \_ indicateur de ressource \_ \_ aucun)**</span><span class="sxs-lookup"><span data-stu-id="41da2-125">**static inline Buffer(const D3D12\_RESOURCE\_ALLOCATION\_INFO& resAllocInfo, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="41da2-126">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="41da2-126">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="41da2-127">[**D3D12 \_ \_ \_ Informations d’allocation de ressources**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span><span class="sxs-lookup"><span data-stu-id="41da2-127">[**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span></span>

<span data-ttu-id="41da2-128">possibilité [**D3D12 \_ Indicateurs \_ de ressource**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) indicateurs = \_ indicateur de ressource D3D12 \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="41da2-128">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="41da2-129">**Mémoire tampon Inline statique (UINT64 Width, D3D12 \_ Resource \_ Flags Flags = D3D12 \_ Resource \_ Flag \_ None, UINT64 Alignment = 0)**</span><span class="sxs-lookup"><span data-stu-id="41da2-129">**static inline Buffer(UINT64 width, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE, UINT64 alignment = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="41da2-130">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="41da2-130">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="41da2-131">La largeur UINT64</span><span class="sxs-lookup"><span data-stu-id="41da2-131">UINT64 width</span></span>

<span data-ttu-id="41da2-132">possibilité [**D3D12 \_ Indicateurs \_ de ressource**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) indicateurs = \_ indicateur de ressource D3D12 \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="41da2-132">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

<span data-ttu-id="41da2-133">possibilité -Alignement de UINT64 = 0</span><span class="sxs-lookup"><span data-stu-id="41da2-133">(opt) UINT64 alignment = 0</span></span>

</dd> <dt>

<span data-ttu-id="41da2-134">**static Inline Tex1D ( \_ format de format dxgi, UINT64 Width, UINT16 arraySize = 1, UINT16 miplevels a = 0, D3D12 \_ Resource \_ Flags Flags = D3D12 \_ \_ indicateur de ressource \_ None, D3D12 \_ texture \_ disposition layout = D3D12 \_ \_ disposition de texture \_ inconnue, alignement UINT64 = 0)**</span><span class="sxs-lookup"><span data-stu-id="41da2-134">**static inline Tex1D(DXGI\_FORMAT format, UINT64 width, UINT16 arraySize = 1, UINT16 mipLevels = 0, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE, D3D12\_TEXTURE\_LAYOUT layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN, UINT64 alignment = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="41da2-135">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="41da2-135">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="41da2-136">[**Dxgi \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Format de format</span><span class="sxs-lookup"><span data-stu-id="41da2-136">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="41da2-137">La largeur UINT64</span><span class="sxs-lookup"><span data-stu-id="41da2-137">UINT64 width</span></span>

<span data-ttu-id="41da2-138">possibilité UINT16 arraySize = 1</span><span class="sxs-lookup"><span data-stu-id="41da2-138">(opt) UINT16 arraySize = 1</span></span>

<span data-ttu-id="41da2-139">possibilité UINT16 Miplevels a = 0</span><span class="sxs-lookup"><span data-stu-id="41da2-139">(opt) UINT16 mipLevels = 0</span></span>

<span data-ttu-id="41da2-140">possibilité [**D3D12 \_ Indicateurs \_ de ressource**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) indicateurs = \_ indicateur de ressource D3D12 \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="41da2-140">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

<span data-ttu-id="41da2-141">possibilité [**D3D12 \_ Disposition \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) de la disposition de texture = \_ disposition de texture D3D12 \_ \_ inconnue</span><span class="sxs-lookup"><span data-stu-id="41da2-141">(opt) [**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN</span></span>

<span data-ttu-id="41da2-142">possibilité -Alignement de UINT64 = 0</span><span class="sxs-lookup"><span data-stu-id="41da2-142">(opt) UINT64 alignment = 0</span></span>

</dd> <dt>

<span data-ttu-id="41da2-143">**static Inline Tex2D ( \_ format de format dxgi, UINT64 Width, valeur uint Height, UINT16 arraySize = 1, UINT16 miplevels a = 0, uint sampleCount = 1, uint sampleQuality = 0, D3D12 \_ Resource \_ Flags Flags = D3D12 \_ ressource \_ indicateur \_ None, D3D12 \_ texture \_ Layout disposition = D3D12 \_ \_ disposition de texture \_ inconnue, alignement de UINT64 = 0)**</span><span class="sxs-lookup"><span data-stu-id="41da2-143">**static inline Tex2D(DXGI\_FORMAT format, UINT64 width, UINT height, UINT16 arraySize = 1, UINT16 mipLevels = 0, UINT sampleCount = 1, UINT sampleQuality = 0, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE, D3D12\_TEXTURE\_LAYOUT layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN, UINT64 alignment = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="41da2-144">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="41da2-144">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="41da2-145">[**Dxgi \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Format de format</span><span class="sxs-lookup"><span data-stu-id="41da2-145">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="41da2-146">La largeur UINT64</span><span class="sxs-lookup"><span data-stu-id="41da2-146">UINT64 width</span></span>

<span data-ttu-id="41da2-147">Hauteur UINT</span><span class="sxs-lookup"><span data-stu-id="41da2-147">UINT height</span></span>

<span data-ttu-id="41da2-148">possibilité UINT16 arraySize = 1</span><span class="sxs-lookup"><span data-stu-id="41da2-148">(opt) UINT16 arraySize = 1</span></span>

<span data-ttu-id="41da2-149">possibilité UINT16 Miplevels a = 0</span><span class="sxs-lookup"><span data-stu-id="41da2-149">(opt) UINT16 mipLevels = 0</span></span>

<span data-ttu-id="41da2-150">possibilité UINT sampleCount = 1</span><span class="sxs-lookup"><span data-stu-id="41da2-150">(opt) UINT sampleCount = 1</span></span>

<span data-ttu-id="41da2-151">possibilité UINT sampleQuality = 0</span><span class="sxs-lookup"><span data-stu-id="41da2-151">(opt) UINT sampleQuality = 0</span></span>

<span data-ttu-id="41da2-152">possibilité [**D3D12 \_ Indicateurs \_ de ressource**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) indicateurs = \_ indicateur de ressource D3D12 \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="41da2-152">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

<span data-ttu-id="41da2-153">possibilité [**D3D12 \_ Disposition \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) de la disposition de texture = \_ disposition de texture D3D12 \_ \_ inconnue</span><span class="sxs-lookup"><span data-stu-id="41da2-153">(opt) [**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN</span></span>

<span data-ttu-id="41da2-154">possibilité -Alignement de UINT64 = 0</span><span class="sxs-lookup"><span data-stu-id="41da2-154">(opt) UINT64 alignment = 0</span></span>

</dd> <dt>

<span data-ttu-id="41da2-155">**static Inline Tex3D ( \_ format de format dxgi, UINT64 Width, valeur uint Height, fonction UInt16 Depth, Uint16 miplevels a = 0, D3D12 \_ Resource \_ Flags Flags = D3D12 \_ \_ indicateur \_ de ressource None, D3D12 \_ texture \_ disposition layout = D3D12 \_ \_ disposition de texture \_ inconnue, alignement UINT64 = 0)**</span><span class="sxs-lookup"><span data-stu-id="41da2-155">**static inline Tex3D(DXGI\_FORMAT format, UINT64 width, UINT height, UINT16 depth, UINT16 mipLevels = 0, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE, D3D12\_TEXTURE\_LAYOUT layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN, UINT64 alignment = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="41da2-156">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="41da2-156">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="41da2-157">[**Dxgi \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Format de format</span><span class="sxs-lookup"><span data-stu-id="41da2-157">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="41da2-158">La largeur UINT64</span><span class="sxs-lookup"><span data-stu-id="41da2-158">UINT64 width</span></span>

<span data-ttu-id="41da2-159">Hauteur UINT</span><span class="sxs-lookup"><span data-stu-id="41da2-159">UINT height</span></span>

<span data-ttu-id="41da2-160">Profondeur UINT16</span><span class="sxs-lookup"><span data-stu-id="41da2-160">UINT16 depth</span></span>

<span data-ttu-id="41da2-161">possibilité UINT16 Miplevels a = 0</span><span class="sxs-lookup"><span data-stu-id="41da2-161">(opt) UINT16 mipLevels = 0</span></span>

<span data-ttu-id="41da2-162">possibilité [**D3D12 \_ Indicateurs \_ de ressource**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) indicateurs = \_ indicateur de ressource D3D12 \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="41da2-162">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

<span data-ttu-id="41da2-163">possibilité [**D3D12 \_ Disposition \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) de la disposition de texture = \_ disposition de texture D3D12 \_ \_ inconnue</span><span class="sxs-lookup"><span data-stu-id="41da2-163">(opt) [**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN</span></span>

<span data-ttu-id="41da2-164">possibilité -Alignement de UINT64 = 0</span><span class="sxs-lookup"><span data-stu-id="41da2-164">(opt) UINT64 alignment = 0</span></span>

</dd> <dt>

<span data-ttu-id="41da2-165">**const de profondeur inline ()**</span><span class="sxs-lookup"><span data-stu-id="41da2-165">**inline Depth() const**</span></span>
</dt> <dd>

<span data-ttu-id="41da2-166">Si dimension = = [**D3D12 \_ ressource \_ dimension**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) \_ TEXTURE3D, retourne DepthOrArraySize.</span><span class="sxs-lookup"><span data-stu-id="41da2-166">If Dimension == [**D3D12\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)\_TEXTURE3D, returns DepthOrArraySize.</span></span> <span data-ttu-id="41da2-167">Si dimension ! = D3D12 \_ ressource \_ dimension \_ TEXTURE3D, retourne 1.</span><span class="sxs-lookup"><span data-stu-id="41da2-167">If Dimension != D3D12\_RESOURCE\_DIMENSION\_TEXTURE3D, returns 1.</span></span>

</dd> <dt>

<span data-ttu-id="41da2-168">**const Inline ArraySize ()**</span><span class="sxs-lookup"><span data-stu-id="41da2-168">**inline ArraySize() const**</span></span>
</dt> <dd>

<span data-ttu-id="41da2-169">Si dimension ! = D3D12 \_ ressource \_ dimension \_ TEXTURE3D, retourne DepthOrArraySize.</span><span class="sxs-lookup"><span data-stu-id="41da2-169">If Dimension != D3D12\_RESOURCE\_DIMENSION\_TEXTURE3D, returns DepthOrArraySize.</span></span> <span data-ttu-id="41da2-170">Si dimension = = D3D12 \_ ressource \_ dimension \_ TEXTURE3D, retourne 1.</span><span class="sxs-lookup"><span data-stu-id="41da2-170">If Dimension == D3D12\_RESOURCE\_DIMENSION\_TEXTURE3D, returns 1.</span></span> <span data-ttu-id="41da2-171">Voir [**la \_ \_ dimension de ressource D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) \_ TEXTURE3D.</span><span class="sxs-lookup"><span data-stu-id="41da2-171">See [**D3D12\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)\_TEXTURE3D.</span></span>

</dd> <dt>

<span data-ttu-id="41da2-172">**Inline PlaneCount (ID3D12Device \* pDevice) const**</span><span class="sxs-lookup"><span data-stu-id="41da2-172">**inline PlaneCount(ID3D12Device\* pDevice) const**</span></span>
</dt> <dd>

<span data-ttu-id="41da2-173">Retourne D3D12GetFormatPlaneCount (pDevice, format).</span><span class="sxs-lookup"><span data-stu-id="41da2-173">Returns D3D12GetFormatPlaneCount(pDevice, Format).</span></span> <span data-ttu-id="41da2-174">Consultez [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md) et [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device).</span><span class="sxs-lookup"><span data-stu-id="41da2-174">See [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md) and [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device).</span></span>

</dd> <dt>

<span data-ttu-id="41da2-175">**sous-ressources en ligne (ID3D12Device \* pDevice) const**</span><span class="sxs-lookup"><span data-stu-id="41da2-175">**inline Subresources(ID3D12Device\* pDevice) const**</span></span>
</dt> <dd>

<span data-ttu-id="41da2-176">Retourne le nombre de sous-ressources, calculé en tant que Miplevels a \* ArraySize () \* PlaneCount (pDevice).</span><span class="sxs-lookup"><span data-stu-id="41da2-176">Returns the number of subresources, calculated as MipLevels \* ArraySize() \* PlaneCount(pDevice).</span></span>

</dd> <dt>

<span data-ttu-id="41da2-177">**Inline CalcSubresource (UINT MipSlice, UINT ArraySlice, UINT PlaneSlice)**</span><span class="sxs-lookup"><span data-stu-id="41da2-177">**inline CalcSubresource(UINT MipSlice, UINT ArraySlice, UINT PlaneSlice)**</span></span>
</dt> <dd>

<span data-ttu-id="41da2-178">Calcule un index de sous-ressource, à l’aide de [**D3D12CalcSubresource**](d3d12calcsubresource.md).</span><span class="sxs-lookup"><span data-stu-id="41da2-178">Calculates a subresource index, by using [**D3D12CalcSubresource**](d3d12calcsubresource.md).</span></span>

</dd> <dt>

<span data-ttu-id="41da2-179">**const D3D12 \_ Resource \_ desc& () const**</span><span class="sxs-lookup"><span data-stu-id="41da2-179">**operator const D3D12\_RESOURCE\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="41da2-180">Définit le & opérateur de passage par référence pour le type de structure parent.</span><span class="sxs-lookup"><span data-stu-id="41da2-180">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> <dt>

<span data-ttu-id="41da2-181">**opérateur = = (const D3D12 \_ Resource \_ desc& l, CONSt D3D12 \_ resource \_ desc& r)**</span><span class="sxs-lookup"><span data-stu-id="41da2-181">**operator == (const D3D12\_RESOURCE\_DESC& l, const D3D12\_RESOURCE\_DESC& r)**</span></span>
</dt> <dd>

<span data-ttu-id="41da2-182">Retourne la valeur true si tous les membres de chaque structure sont identiques.</span><span class="sxs-lookup"><span data-stu-id="41da2-182">Returns true if all members of each structure are identical.</span></span>

</dd> <dt>

<span data-ttu-id="41da2-183">**opérateur ! = (const D3D12 \_ Resource \_ desc& l, CONSt D3D12 \_ resource \_ desc& r)**</span><span class="sxs-lookup"><span data-stu-id="41da2-183">**operator != (const D3D12\_RESOURCE\_DESC& l, const D3D12\_RESOURCE\_DESC& r)**</span></span>
</dt> <dd>

<span data-ttu-id="41da2-184">Retourne la valeur false si tous les membres de chaque structure sont identiques.</span><span class="sxs-lookup"><span data-stu-id="41da2-184">Returns false if all members of each structure are identical.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="41da2-185">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41da2-185">Requirements</span></span>



| <span data-ttu-id="41da2-186">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41da2-186">Requirement</span></span> | <span data-ttu-id="41da2-187">Valeur</span><span class="sxs-lookup"><span data-stu-id="41da2-187">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="41da2-188">En-tête</span><span class="sxs-lookup"><span data-stu-id="41da2-188">Header</span></span><br/> | <dl> <span data-ttu-id="41da2-189"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="41da2-189"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41da2-190">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41da2-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41da2-191">**Description de la \_ ressource D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="41da2-191">**D3D12\_RESOURCE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)
</dt> <dt>

[<span data-ttu-id="41da2-192">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="41da2-192">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

