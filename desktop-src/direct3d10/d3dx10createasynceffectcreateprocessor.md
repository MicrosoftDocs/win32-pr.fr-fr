---
description: Créer un pool d’effets de manière asynchrone.
ms.assetid: 50c55751-26de-4002-9a89-8e5ab59dda79
title: D3DX10CreateAsyncEffectCreateProcessor, fonction (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncEffectCreateProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 573efc51214031afe66f6cfd552bbda634d15142
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522344"
---
# <a name="d3dx10createasynceffectcreateprocessor-function"></a><span data-ttu-id="23a35-103">D3DX10CreateAsyncEffectCreateProcessor fonction)</span><span class="sxs-lookup"><span data-stu-id="23a35-103">D3DX10CreateAsyncEffectCreateProcessor function</span></span>

<span data-ttu-id="23a35-104">Créer un pool d’effets de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="23a35-104">Create an effect pool asynchronously.</span></span>

## <a name="syntax"></a><span data-ttu-id="23a35-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23a35-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncEffectCreateProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags,
  _In_        UINT                 FXFlags,
  _In_        ID3D10Device         *pDevice,
  _In_        ID3D10EffectPool     *pPool,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="23a35-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23a35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23a35-107">*pFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="23a35-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23a35-108">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="23a35-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="23a35-109">Chaîne qui contient le nom de fichier de l’effet.</span><span class="sxs-lookup"><span data-stu-id="23a35-109">A string that contains the effect filename.</span></span>

</dd> <dt>

<span data-ttu-id="23a35-110">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="23a35-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23a35-111">Type : **\* macro de [**\_ nuanceur \_ D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) const**</span><span class="sxs-lookup"><span data-stu-id="23a35-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="23a35-112">Tableau de macros de nuanceur se terminant par un caractère NULL (consultez la [**\_ \_ macro de nuanceur D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); définissez cette valeur sur **null** pour ne spécifier aucune macro.</span><span class="sxs-lookup"><span data-stu-id="23a35-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="23a35-113">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="23a35-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23a35-114">Type : **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="23a35-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="23a35-115">Pointeur vers une interface include (voir [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Affectez-lui la valeur **null** pour spécifier qu’il n’y a aucun fichier include.</span><span class="sxs-lookup"><span data-stu-id="23a35-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="23a35-116">*pProfile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="23a35-116">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23a35-117">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="23a35-117">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="23a35-118">Chaîne qui spécifie le [profil de nuanceur](../direct3dhlsl/dx-graphics-hlsl-models.md) ou le modèle de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="23a35-118">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md) or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="23a35-119">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="23a35-119">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23a35-120">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="23a35-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="23a35-121">Options de compilation HLSL (voir [indicateurs de nuanceur](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="23a35-121">HLSL compile options (see [Shader Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="23a35-122">*FXFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="23a35-122">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23a35-123">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="23a35-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="23a35-124">Appliquer des options de compilation (voir [indicateurs de compilation et d’effet](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="23a35-124">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="23a35-125">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="23a35-125">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23a35-126">Type : **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="23a35-126">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="23a35-127">Pointeur vers l’appareil (voir [**interface ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) qui utilisera les ressources.</span><span class="sxs-lookup"><span data-stu-id="23a35-127">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="23a35-128">*pPool* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="23a35-128">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23a35-129">Type : **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span><span class="sxs-lookup"><span data-stu-id="23a35-129">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span></span>

<span data-ttu-id="23a35-130">Pointeur vers un pool d’effets (voir [**interface ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) pour le partage de variables entre les effets.</span><span class="sxs-lookup"><span data-stu-id="23a35-130">A pointer to an effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) for sharing variables between effects.</span></span>

</dd> <dt>

<span data-ttu-id="23a35-131">*ppErrorBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="23a35-131">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23a35-132">Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="23a35-132">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="23a35-133">Adresse d’un pointeur vers la mémoire (voir [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) qui contient des erreurs d’effet de compilation, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="23a35-133">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="23a35-134">*ppProcessor* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="23a35-134">*ppProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23a35-135">Type : **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="23a35-135">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="23a35-136">Adresse d’un pointeur vers le processeur de données asynchrones (voir [**interface ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="23a35-136">The address of a pointer to the asynchronous-data processor (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23a35-137">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="23a35-137">Return value</span></span>

<span data-ttu-id="23a35-138">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="23a35-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="23a35-139">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="23a35-139">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="23a35-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="23a35-140">Requirements</span></span>



| <span data-ttu-id="23a35-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23a35-141">Requirement</span></span> | <span data-ttu-id="23a35-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="23a35-142">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="23a35-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="23a35-143">Header</span></span><br/> | <dl> <span data-ttu-id="23a35-144"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="23a35-144"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23a35-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23a35-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23a35-146">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="23a35-146">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
