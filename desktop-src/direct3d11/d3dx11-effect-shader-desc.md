---
title: Structure D3DX11_EFFECT_SHADER_DESC (D3dx11effect. h)
description: Décrit un nuanceur d’effet.
ms.assetid: 4377eec6-f331-4cad-bf16-189d6296f886
keywords:
- Structure D3DX11_EFFECT_SHADER_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_SHADER_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c518d4f7930d0651e519d23218121b8ed4bed288
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870182"
---
# <a name="d3dx11_effect_shader_desc-structure"></a><span data-ttu-id="43570-104">\_ \_ Structure DESC du nuanceur d’effets D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="43570-104">D3DX11\_EFFECT\_SHADER\_DESC structure</span></span>

<span data-ttu-id="43570-105">Décrit un nuanceur d’effet.</span><span class="sxs-lookup"><span data-stu-id="43570-105">Describes an effect shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="43570-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43570-106">Syntax</span></span>


```C++
typedef struct _D3DX11_EFFECT_SHADER_DESC {
  const BYTE *pInputSignature;
  BOOL       IsInline;
  const BYTE *pBytecode;
  UINT       BytecodeLength;
  LPCSTR     SODecls[D3D11_SO_STREAM_COUNT];
  UINT       RasterizedStream;
  UINT       NumInputSignatureEntries;
  UINT       NumOutputSignatureEntries;
  UINT       NumPatchConstantSignatureEntries;
} D3DX11_EFFECT_SHADER_DESC;
```



## <a name="members"></a><span data-ttu-id="43570-107">Membres</span><span class="sxs-lookup"><span data-stu-id="43570-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="43570-108">**pInputSignature**</span><span class="sxs-lookup"><span data-stu-id="43570-108">**pInputSignature**</span></span>
</dt> <dd>

<span data-ttu-id="43570-109">Type : **const [**Byte**](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="43570-109">Type: **const [**BYTE**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

</dd> <dd>

<span data-ttu-id="43570-110">Passé dans CreateInputLayout.</span><span class="sxs-lookup"><span data-stu-id="43570-110">Passed into CreateInputLayout.</span></span> <span data-ttu-id="43570-111">Valide uniquement sur un nuanceur de sommets ou un nuanceur de géométrie.</span><span class="sxs-lookup"><span data-stu-id="43570-111">Only valid on a vertex shader or geometry shader.</span></span> <span data-ttu-id="43570-112">Consultez [**ID3D11Device :: CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout).</span><span class="sxs-lookup"><span data-stu-id="43570-112">See [**ID3D11Device::CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout).</span></span>

</dd> <dt>

<span data-ttu-id="43570-113">**IsInline**</span><span class="sxs-lookup"><span data-stu-id="43570-113">**IsInline**</span></span>
</dt> <dd>

<span data-ttu-id="43570-114">Type : **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="43570-114">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="43570-115">**True** si le nuanceur est défini en ligne ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="43570-115">**TRUE** is the shader is defined inline; otherwise **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="43570-116">**pBytecode**</span><span class="sxs-lookup"><span data-stu-id="43570-116">**pBytecode**</span></span>
</dt> <dd>

<span data-ttu-id="43570-117">Type : **const [**Byte**](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="43570-117">Type: **const [**BYTE**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

</dd> <dd>

<span data-ttu-id="43570-118">Bytecode du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="43570-118">Shader bytecode.</span></span>

</dd> <dt>

<span data-ttu-id="43570-119">**BytecodeLength**</span><span class="sxs-lookup"><span data-stu-id="43570-119">**BytecodeLength**</span></span>
</dt> <dd>

<span data-ttu-id="43570-120">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="43570-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="43570-121">Longueur de pBytecode.</span><span class="sxs-lookup"><span data-stu-id="43570-121">The length of pBytecode.</span></span>

</dd> <dt>

<span data-ttu-id="43570-122">**SODecls**</span><span class="sxs-lookup"><span data-stu-id="43570-122">**SODecls**</span></span>
</dt> <dd>

<span data-ttu-id="43570-123">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="43570-123">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="43570-124">Chaîne de déclaration de flux de sortie (pour le nuanceur Geometry avec SO).</span><span class="sxs-lookup"><span data-stu-id="43570-124">Stream out declaration string (for geometry shader with SO).</span></span>

</dd> <dt>

<span data-ttu-id="43570-125">**RasterizedStream**</span><span class="sxs-lookup"><span data-stu-id="43570-125">**RasterizedStream**</span></span>
</dt> <dd>

<span data-ttu-id="43570-126">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="43570-126">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="43570-127">Indique le flux pixellisé.</span><span class="sxs-lookup"><span data-stu-id="43570-127">Indicates which stream is rasterized.</span></span> <span data-ttu-id="43570-128">Les nuanceurs de géométrie D3D11 peuvent générer jusqu’à quatre flux de données, dont l’un peut être pixellisé.</span><span class="sxs-lookup"><span data-stu-id="43570-128">D3D11 geometry shaders can output up to four streams of data, one of which can be rasterized.</span></span>

</dd> <dt>

<span data-ttu-id="43570-129">**NumInputSignatureEntries**</span><span class="sxs-lookup"><span data-stu-id="43570-129">**NumInputSignatureEntries**</span></span>
</dt> <dd>

<span data-ttu-id="43570-130">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="43570-130">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="43570-131">Nombre d’entrées dans la signature d’entrée.</span><span class="sxs-lookup"><span data-stu-id="43570-131">Number of entries in the input signature.</span></span>

</dd> <dt>

<span data-ttu-id="43570-132">**NumOutputSignatureEntries**</span><span class="sxs-lookup"><span data-stu-id="43570-132">**NumOutputSignatureEntries**</span></span>
</dt> <dd>

<span data-ttu-id="43570-133">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="43570-133">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="43570-134">Nombre d’entrées dans la signature de sortie.</span><span class="sxs-lookup"><span data-stu-id="43570-134">Number of entries in the output signature.</span></span>

</dd> <dt>

<span data-ttu-id="43570-135">**NumPatchConstantSignatureEntries**</span><span class="sxs-lookup"><span data-stu-id="43570-135">**NumPatchConstantSignatureEntries**</span></span>
</dt> <dd>

<span data-ttu-id="43570-136">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="43570-136">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="43570-137">Nombre d’entrées dans la signature de constante de correctif.</span><span class="sxs-lookup"><span data-stu-id="43570-137">Number of entries in the patch constant signature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43570-138">Notes</span><span class="sxs-lookup"><span data-stu-id="43570-138">Remarks</span></span>

<span data-ttu-id="43570-139">Le \_ \_ nuanceur \_ d’effets D3DX11 DESC est utilisé avec [**ID3DX11EffectShaderVariable :: GetShaderDesc**](id3dx11effectshadervariable-getshaderdesc.md).</span><span class="sxs-lookup"><span data-stu-id="43570-139">D3DX11\_EFFECT\_SHADER\_DESC is used with [**ID3DX11EffectShaderVariable::GetShaderDesc**](id3dx11effectshadervariable-getshaderdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="43570-140">Spécifications</span><span class="sxs-lookup"><span data-stu-id="43570-140">Requirements</span></span>



| <span data-ttu-id="43570-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43570-141">Requirement</span></span> | <span data-ttu-id="43570-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="43570-142">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="43570-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="43570-143">Header</span></span><br/> | <dl> <span data-ttu-id="43570-144"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="43570-144"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43570-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43570-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43570-146">Effets 11 structures</span><span class="sxs-lookup"><span data-stu-id="43570-146">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

