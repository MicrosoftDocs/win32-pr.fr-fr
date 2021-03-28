---
title: Structure D3DX11_STATE_BLOCK_MASK (D3dx11effect. h)
description: Indique l’état de l’appareil.
ms.assetid: 42044a6d-6a11-4f90-889a-82e7954da6c7
keywords:
- Structure D3DX11_STATE_BLOCK_MASK Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_STATE_BLOCK_MASK
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41236c541fc251902a7a0a5ad6030a28dd36e3a4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323121"
---
# <a name="d3dx11_state_block_mask-structure"></a><span data-ttu-id="ca027-104">\_Structure de \_ masque de bloc d’État D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="ca027-104">D3DX11\_STATE\_BLOCK\_MASK structure</span></span>

<span data-ttu-id="ca027-105">Indique l’état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ca027-105">Indicates the device state.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca027-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca027-106">Syntax</span></span>


```C++
typedef struct _D3DX11_STATE_BLOCK_MASK {
  BYTE VS;
  BYTE VSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE VSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE VSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE VSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE HS;
  BYTE HSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE HSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE HSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE HSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE DS;
  BYTE DSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE DSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE DSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE DSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE GS;
  BYTE GSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE GSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE GSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE GSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE PS;
  BYTE PSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE PSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE PSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE PSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE PSUnorderedAccessViews;
  BYTE CS;
  BYTE CSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE CSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE CSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE CSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE CSUnorderedAccessViews;
  BYTE IAVertexBuffers[D3DX11_BYTES_FROM_BITS(D3D11_IA_VERTEX_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE IAIndexBuffer;
  BYTE IAInputLayout;
  BYTE IAPrimitiveTopology;
  BYTE OMRenderTargets;
  BYTE OMDepthStencilState;
  BYTE OMBlendState;
  BYTE RSViewports;
  BYTE RSScissorRects;
  BYTE RSRasterizerState;
  BYTE SOBuffers;
  BYTE Predication;
} D3DX11_STATE_BLOCK_MASK;
```



## <a name="members"></a><span data-ttu-id="ca027-107">Membres</span><span class="sxs-lookup"><span data-stu-id="ca027-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ca027-108">**COMPARATIF**</span><span class="sxs-lookup"><span data-stu-id="ca027-108">**VS**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-109">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-109">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-110">Valeur booléenne indiquant s’il faut enregistrer l’état du nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="ca027-110">Boolean value indicating whether to save the vertex shader state.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-111">**VSSamplers**</span><span class="sxs-lookup"><span data-stu-id="ca027-111">**VSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-112">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-112">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-113">Tableau d’échantillonneurs vertex-shader.</span><span class="sxs-lookup"><span data-stu-id="ca027-113">Array of vertex-shader samplers.</span></span> <span data-ttu-id="ca027-114">Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="ca027-114">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-115">**VSShaderResources**</span><span class="sxs-lookup"><span data-stu-id="ca027-115">**VSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-116">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-116">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-117">Tableau de ressources de nuanceur de vertex.</span><span class="sxs-lookup"><span data-stu-id="ca027-117">Array of vertex-shader resources.</span></span> <span data-ttu-id="ca027-118">Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement de ressource.</span><span class="sxs-lookup"><span data-stu-id="ca027-118">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-119">**VSConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="ca027-119">**VSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-120">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-120">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-121">Tableau de mémoires tampons constantes de nuanceur de vertex.</span><span class="sxs-lookup"><span data-stu-id="ca027-121">Array of vertex-shader constant buffers.</span></span> <span data-ttu-id="ca027-122">Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement de mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="ca027-122">The array is a multi-byte bitmask where each bit represents one constant buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-123">**VSInterfaces**</span><span class="sxs-lookup"><span data-stu-id="ca027-123">**VSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-124">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-124">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-125">Tableau d’interfaces de nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="ca027-125">Array of vertex-shader interfaces.</span></span> <span data-ttu-id="ca027-126">Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement d’interface.</span><span class="sxs-lookup"><span data-stu-id="ca027-126">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-127">**SH**</span><span class="sxs-lookup"><span data-stu-id="ca027-127">**HS**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-128">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-128">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-129">Valeur booléenne indiquant s’il faut enregistrer l’état du nuanceur de coque.</span><span class="sxs-lookup"><span data-stu-id="ca027-129">Boolean value indicating whether to save the hull shader state.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-130">**HSSamplers**</span><span class="sxs-lookup"><span data-stu-id="ca027-130">**HSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-131">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-131">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-132">Tableau d’échantillonneurs de nuanceur de coque.</span><span class="sxs-lookup"><span data-stu-id="ca027-132">Array of hull-shader samplers.</span></span> <span data-ttu-id="ca027-133">Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="ca027-133">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-134">**HSShaderResources**</span><span class="sxs-lookup"><span data-stu-id="ca027-134">**HSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-135">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-135">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-136">Tableau de ressources de nuanceur de coque.</span><span class="sxs-lookup"><span data-stu-id="ca027-136">Array of hull-shader resources.</span></span> <span data-ttu-id="ca027-137">Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement de ressource.</span><span class="sxs-lookup"><span data-stu-id="ca027-137">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-138">**HSConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="ca027-138">**HSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-139">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-139">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-140">Tableau de mémoires tampons constantes de nuanceur de coque.</span><span class="sxs-lookup"><span data-stu-id="ca027-140">Array of hull-shader constant buffers.</span></span> <span data-ttu-id="ca027-141">Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement de mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="ca027-141">The array is a multi-byte bitmask where each bit represents one constant buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-142">**HSInterfaces**</span><span class="sxs-lookup"><span data-stu-id="ca027-142">**HSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-143">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-143">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-144">Tableau d’interfaces de nuanceur de coque.</span><span class="sxs-lookup"><span data-stu-id="ca027-144">Array of hull-shader interfaces.</span></span> <span data-ttu-id="ca027-145">Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement d’interface.</span><span class="sxs-lookup"><span data-stu-id="ca027-145">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-146">**SD**</span><span class="sxs-lookup"><span data-stu-id="ca027-146">**DS**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-147">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-147">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-148">Valeur booléenne indiquant s’il faut enregistrer l’état du nuanceur de domaine.</span><span class="sxs-lookup"><span data-stu-id="ca027-148">Boolean value indicating whether to save the domain shader state.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-149">**DSSamplers**</span><span class="sxs-lookup"><span data-stu-id="ca027-149">**DSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-150">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-150">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-151">Tableau d’échantillonneurs de nuanceur de domaine.</span><span class="sxs-lookup"><span data-stu-id="ca027-151">Array of domain-shader samplers.</span></span> <span data-ttu-id="ca027-152">Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="ca027-152">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-153">**DSShaderResources**</span><span class="sxs-lookup"><span data-stu-id="ca027-153">**DSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-154">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-154">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-155">Tableau de ressources de nuanceur de domaine.</span><span class="sxs-lookup"><span data-stu-id="ca027-155">Array of domain-shader resources.</span></span> <span data-ttu-id="ca027-156">Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement de ressource.</span><span class="sxs-lookup"><span data-stu-id="ca027-156">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-157">**DSConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="ca027-157">**DSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-158">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-158">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-159">Tableau de mémoires tampons constantes de nuanceur de domaine.</span><span class="sxs-lookup"><span data-stu-id="ca027-159">Array of domain-shader constant buffers.</span></span> <span data-ttu-id="ca027-160">Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="ca027-160">The array is a multi-byte bitmask where each bit represents one buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-161">**DSInterfaces**</span><span class="sxs-lookup"><span data-stu-id="ca027-161">**DSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-162">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-162">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-163">Tableau d’interfaces de nuanceur de domaine.</span><span class="sxs-lookup"><span data-stu-id="ca027-163">Array of domain-shader interfaces.</span></span> <span data-ttu-id="ca027-164">Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement d’interface.</span><span class="sxs-lookup"><span data-stu-id="ca027-164">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-165">**GS**</span><span class="sxs-lookup"><span data-stu-id="ca027-165">**GS**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-166">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-166">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-167">Valeur booléenne indiquant si l’état du nuanceur Geometry doit être enregistré.</span><span class="sxs-lookup"><span data-stu-id="ca027-167">Boolean value indicating whether to save the geometry shader state.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-168">**GSSamplers**</span><span class="sxs-lookup"><span data-stu-id="ca027-168">**GSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-169">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-169">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-170">Tableau d’échantillonneurs Geometry-Shader.</span><span class="sxs-lookup"><span data-stu-id="ca027-170">Array of geometry-shader samplers.</span></span> <span data-ttu-id="ca027-171">Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="ca027-171">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-172">**GSShaderResources**</span><span class="sxs-lookup"><span data-stu-id="ca027-172">**GSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-173">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-173">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-174">Tableau de ressources Geometry-Shader.</span><span class="sxs-lookup"><span data-stu-id="ca027-174">Array of geometry-shader resources.</span></span> <span data-ttu-id="ca027-175">Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement de ressource.</span><span class="sxs-lookup"><span data-stu-id="ca027-175">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-176">**GSConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="ca027-176">**GSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-177">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-177">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-178">Tableau de mémoires tampons constantes de nuanceur de géométrie.</span><span class="sxs-lookup"><span data-stu-id="ca027-178">Array of geometry-shader constant buffers.</span></span> <span data-ttu-id="ca027-179">Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="ca027-179">The array is a multi-byte bitmask where each bit represents one buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-180">**GSInterfaces**</span><span class="sxs-lookup"><span data-stu-id="ca027-180">**GSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-181">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-181">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-182">Tableau d’interfaces Geometry-Shader.</span><span class="sxs-lookup"><span data-stu-id="ca027-182">Array of geometry-shader interfaces.</span></span> <span data-ttu-id="ca027-183">Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement d’interface.</span><span class="sxs-lookup"><span data-stu-id="ca027-183">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-184">**PS**</span><span class="sxs-lookup"><span data-stu-id="ca027-184">**PS**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-185">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-185">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-186">Valeur booléenne indiquant s’il faut enregistrer l’état du nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="ca027-186">Boolean value indicating whether to save the pixel shader state.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-187">**PSSamplers**</span><span class="sxs-lookup"><span data-stu-id="ca027-187">**PSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-188">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-188">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-189">Tableau d’échantillonneurs de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="ca027-189">Array of pixel-shader samplers.</span></span> <span data-ttu-id="ca027-190">Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="ca027-190">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-191">**PSShaderResources**</span><span class="sxs-lookup"><span data-stu-id="ca027-191">**PSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-192">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-192">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-193">Tableau de ressources de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="ca027-193">Array of pixel-shader resources.</span></span> <span data-ttu-id="ca027-194">Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement de ressource.</span><span class="sxs-lookup"><span data-stu-id="ca027-194">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-195">**PSConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="ca027-195">**PSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-196">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-196">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-197">Tableau de mémoires tampons constantes de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="ca027-197">Array of pixel-shader constant buffers.</span></span> <span data-ttu-id="ca027-198">Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement de mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="ca027-198">The array is a multi-byte bitmask where each bit represents one constant buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-199">**PSInterfaces**</span><span class="sxs-lookup"><span data-stu-id="ca027-199">**PSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-200">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-200">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-201">Tableau d’interfaces de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="ca027-201">Array of pixel-shader interfaces.</span></span> <span data-ttu-id="ca027-202">Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement d’interface.</span><span class="sxs-lookup"><span data-stu-id="ca027-202">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-203">**PSUnorderedAccessViews**</span><span class="sxs-lookup"><span data-stu-id="ca027-203">**PSUnorderedAccessViews**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-204">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-204">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-205">Valeur booléenne indiquant s’il faut enregistrer les vues d’accès non trié de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="ca027-205">Boolean value indicating whether to save the pixel shader unordered access views.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-206">**CS**</span><span class="sxs-lookup"><span data-stu-id="ca027-206">**CS**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-207">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-207">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-208">Valeur booléenne indiquant s’il faut enregistrer l’état du nuanceur de calcul.</span><span class="sxs-lookup"><span data-stu-id="ca027-208">Boolean value indicating whether to save the compute shader state.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-209">**CSSamplers**</span><span class="sxs-lookup"><span data-stu-id="ca027-209">**CSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-210">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-210">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-211">Tableau d’échantillonneurs de nuanceur de calcul.</span><span class="sxs-lookup"><span data-stu-id="ca027-211">Array of compute-shader samplers.</span></span> <span data-ttu-id="ca027-212">Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="ca027-212">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-213">**CSShaderResources**</span><span class="sxs-lookup"><span data-stu-id="ca027-213">**CSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-214">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-214">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-215">Tableau de ressources de nuanceur de calcul.</span><span class="sxs-lookup"><span data-stu-id="ca027-215">Array of compute-shader resources.</span></span> <span data-ttu-id="ca027-216">Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement de ressource.</span><span class="sxs-lookup"><span data-stu-id="ca027-216">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-217">**CSConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="ca027-217">**CSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-218">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-218">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-219">Tableau de mémoires tampons constantes de nuanceur de calcul.</span><span class="sxs-lookup"><span data-stu-id="ca027-219">Array of compute-shader constant buffers.</span></span> <span data-ttu-id="ca027-220">Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement de mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="ca027-220">The array is a multi-byte bitmask where each bit represents one constant buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-221">**CSInterfaces**</span><span class="sxs-lookup"><span data-stu-id="ca027-221">**CSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-222">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-222">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-223">Tableau d’interfaces de nuanceur de calcul.</span><span class="sxs-lookup"><span data-stu-id="ca027-223">Array of compute-shader interfaces.</span></span> <span data-ttu-id="ca027-224">Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement d’interface.</span><span class="sxs-lookup"><span data-stu-id="ca027-224">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-225">**CSUnorderedAccessViews**</span><span class="sxs-lookup"><span data-stu-id="ca027-225">**CSUnorderedAccessViews**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-226">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-226">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-227">Valeur booléenne indiquant s’il faut enregistrer les vues d’accès non ordonnées du nuanceur de calcul.</span><span class="sxs-lookup"><span data-stu-id="ca027-227">Boolean value indicating whether to save the compute shader unordered access views.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-228">**IAVertexBuffers**</span><span class="sxs-lookup"><span data-stu-id="ca027-228">**IAVertexBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-229">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-229">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-230">Tableau de mémoires tampons de vertex.</span><span class="sxs-lookup"><span data-stu-id="ca027-230">Array of vertex buffers.</span></span> <span data-ttu-id="ca027-231">Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement de ressource.</span><span class="sxs-lookup"><span data-stu-id="ca027-231">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-232">**IAIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="ca027-232">**IAIndexBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-233">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-233">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-234">Valeur booléenne indiquant s’il faut enregistrer l’état de la mémoire tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="ca027-234">Boolean value indicating whether to save the index buffer state.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-235">**IAInputLayout**</span><span class="sxs-lookup"><span data-stu-id="ca027-235">**IAInputLayout**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-236">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-236">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-237">Valeur booléenne indiquant si l’état de la disposition d’entrée doit être enregistré.</span><span class="sxs-lookup"><span data-stu-id="ca027-237">Boolean value indicating whether to save the input layout state.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-238">**IAPrimitiveTopology**</span><span class="sxs-lookup"><span data-stu-id="ca027-238">**IAPrimitiveTopology**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-239">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-239">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-240">Valeur booléenne indiquant s’il faut enregistrer l’état de la topologie primitive.</span><span class="sxs-lookup"><span data-stu-id="ca027-240">Boolean value indicating whether to save the primitive topology state.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-241">**OMRenderTargets**</span><span class="sxs-lookup"><span data-stu-id="ca027-241">**OMRenderTargets**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-242">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-242">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-243">Valeur booléenne indiquant s’il faut enregistrer les États des cibles de rendu.</span><span class="sxs-lookup"><span data-stu-id="ca027-243">Boolean value indicating whether to save the render targets states.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-244">**OMDepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="ca027-244">**OMDepthStencilState**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-245">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-245">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-246">Valeur booléenne indiquant s’il faut enregistrer l’état de gabarit de profondeur.</span><span class="sxs-lookup"><span data-stu-id="ca027-246">Boolean value indicating whether to save the depth-stencil state.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-247">**OMBlendState**</span><span class="sxs-lookup"><span data-stu-id="ca027-247">**OMBlendState**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-248">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-248">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-249">Valeur booléenne indiquant s’il faut enregistrer l’état de fusion.</span><span class="sxs-lookup"><span data-stu-id="ca027-249">Boolean value indicating whether to save the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-250">**RSViewports**</span><span class="sxs-lookup"><span data-stu-id="ca027-250">**RSViewports**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-251">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-251">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-252">Valeur booléenne indiquant s’il faut enregistrer les États des Viewports.</span><span class="sxs-lookup"><span data-stu-id="ca027-252">Boolean value indicating whether to save the viewports states.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-253">**RSScissorRects**</span><span class="sxs-lookup"><span data-stu-id="ca027-253">**RSScissorRects**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-254">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-254">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-255">Valeur booléenne indiquant s’il faut enregistrer les États des rectangles de ciseaux.</span><span class="sxs-lookup"><span data-stu-id="ca027-255">Boolean value indicating whether to save the scissor rectangles states.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-256">**RSRasterizerState**</span><span class="sxs-lookup"><span data-stu-id="ca027-256">**RSRasterizerState**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-257">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-257">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-258">Valeur booléenne indiquant s’il faut enregistrer l’état du rastériseur.</span><span class="sxs-lookup"><span data-stu-id="ca027-258">Boolean value indicating whether to save the rasterizer state.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-259">**SOBuffers**</span><span class="sxs-lookup"><span data-stu-id="ca027-259">**SOBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-260">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-260">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-261">Valeur booléenne indiquant s’il faut enregistrer les États des mémoires tampons de sortie de flux.</span><span class="sxs-lookup"><span data-stu-id="ca027-261">Boolean value indicating whether to save the stream-out buffers states.</span></span>

</dd> <dt>

<span data-ttu-id="ca027-262">**Prédicat**</span><span class="sxs-lookup"><span data-stu-id="ca027-262">**Predication**</span></span>
</dt> <dd>

<span data-ttu-id="ca027-263">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ca027-263">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ca027-264">Valeur booléenne indiquant s’il faut enregistrer l’état du prédicat.</span><span class="sxs-lookup"><span data-stu-id="ca027-264">Boolean value indicating whether to save the predication state.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca027-265">Notes</span><span class="sxs-lookup"><span data-stu-id="ca027-265">Remarks</span></span>

<span data-ttu-id="ca027-266">Un masque de bloc d’État indique les États de l’appareil qu’une réussite ou une technique change.</span><span class="sxs-lookup"><span data-stu-id="ca027-266">A state-block mask indicates the device states that a pass or a technique changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca027-267">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ca027-267">Requirements</span></span>



| <span data-ttu-id="ca027-268">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca027-268">Requirement</span></span> | <span data-ttu-id="ca027-269">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca027-269">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca027-270">En-tête</span><span class="sxs-lookup"><span data-stu-id="ca027-270">Header</span></span><br/> | <dl> <span data-ttu-id="ca027-271"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca027-271"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca027-272">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca027-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca027-273">Effets 11 structures</span><span class="sxs-lookup"><span data-stu-id="ca027-273">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

