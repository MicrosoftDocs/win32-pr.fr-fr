---
description: Créer un pool d’effets à partir d’un effet en mémoire.
ms.assetid: 634bcb23-a73f-4493-b805-e2aa5420fa2a
title: D3DX10CreateEffectPoolFromMemory, fonction (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectPoolFromMemory
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 7dc93b7e73f336e75432debfe9bde6659ea4707c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545272"
---
# <a name="d3dx10createeffectpoolfrommemory-function"></a><span data-ttu-id="92b58-103">D3DX10CreateEffectPoolFromMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="92b58-103">D3DX10CreateEffectPoolFromMemory function</span></span>

<span data-ttu-id="92b58-104">Créer un pool d’effets à partir d’un effet en mémoire.</span><span class="sxs-lookup"><span data-stu-id="92b58-104">Create an effect pool from an effect in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="92b58-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="92b58-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectPoolFromMemory(
  _In_        LPCVOID            pData,
  _In_        SIZE_T             DataLength,
  _In_        LPCSTR             pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        ID3D10Include      *pInclude,
  _In_        LPCSTR             pProfile,
  _In_        UINT               HLSLFlags,
  _In_        UINT               FXFlags,
  _In_        ID3D10Device       *pDevice,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10EffectPool   **ppEffectPool,
  _Out_       ID3D10Blob         **ppErrors,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="92b58-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="92b58-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92b58-107">*pData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="92b58-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92b58-108">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92b58-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="92b58-109">Pointeur vers l’effet.</span><span class="sxs-lookup"><span data-stu-id="92b58-109">A pointer to the effect.</span></span>

</dd> <dt>

<span data-ttu-id="92b58-110">*DATALENGTH* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="92b58-110">*DataLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92b58-111">Type : **[ **taille \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92b58-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="92b58-112">Taille de l’effet.</span><span class="sxs-lookup"><span data-stu-id="92b58-112">The size of the effect.</span></span>

</dd> <dt>

<span data-ttu-id="92b58-113">*pSrcFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="92b58-113">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92b58-114">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92b58-114">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="92b58-115">Nom du fichier d’effet.</span><span class="sxs-lookup"><span data-stu-id="92b58-115">The name of the effect file.</span></span>

</dd> <dt>

<span data-ttu-id="92b58-116">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="92b58-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92b58-117">Type : **\* macro de [**\_ nuanceur \_ D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) const**</span><span class="sxs-lookup"><span data-stu-id="92b58-117">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="92b58-118">Tableau de macros de nuanceur se terminant par un caractère NULL (consultez la [**\_ \_ macro de nuanceur D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); définissez cette valeur sur **null** pour ne spécifier aucune macro.</span><span class="sxs-lookup"><span data-stu-id="92b58-118">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="92b58-119">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="92b58-119">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92b58-120">Type : **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="92b58-120">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="92b58-121">Pointeur vers une interface include (voir [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="92b58-121">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="92b58-122">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="92b58-122">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="92b58-123">*pProfile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="92b58-123">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92b58-124">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92b58-124">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="92b58-125">Chaîne qui spécifie le [profil de nuanceur](../direct3dhlsl/dx-graphics-hlsl-models.md)ou le modèle de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="92b58-125">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="92b58-126">*HLSLFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="92b58-126">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92b58-127">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92b58-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="92b58-128">Options de compilation HLSL ( [consultez \_ constantes de nuanceur D3D10](d3d10-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="92b58-128">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="92b58-129">*FXFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="92b58-129">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92b58-130">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92b58-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="92b58-131">Appliquer des options de compilation (voir [indicateurs de compilation et d’effet](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="92b58-131">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="92b58-132">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="92b58-132">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92b58-133">Type : **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="92b58-133">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="92b58-134">Pointeur vers l’appareil (voir [**interface ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) qui utilisera les ressources.</span><span class="sxs-lookup"><span data-stu-id="92b58-134">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="92b58-135">*pPump* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="92b58-135">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92b58-136">Type : **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="92b58-136">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="92b58-137">Pointeur vers une interface de pompage de thread (voir [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="92b58-137">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="92b58-138">Utilisez **null** pour spécifier que cette fonction ne doit pas être retournée tant qu’elle n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="92b58-138">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="92b58-139">*ppEffectPool* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="92b58-139">*ppEffectPool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92b58-140">Type : **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span><span class="sxs-lookup"><span data-stu-id="92b58-140">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span></span>

<span data-ttu-id="92b58-141">Adresse d’un pointeur vers le pool d’effets (consultez [**ID3D10EffectPool interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span><span class="sxs-lookup"><span data-stu-id="92b58-141">The address of a pointer to the effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span></span>

</dd> <dt>

<span data-ttu-id="92b58-142">*ppErrors* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="92b58-142">*ppErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92b58-143">Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="92b58-143">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="92b58-144">Adresse d’un pointeur vers la mémoire (voir [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) qui contient des erreurs d’effet de compilation, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="92b58-144">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="92b58-145">*pHResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="92b58-145">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92b58-146">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="92b58-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="92b58-147">Pointeur vers la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="92b58-147">A pointer to the return value.</span></span> <span data-ttu-id="92b58-148">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="92b58-148">May be **NULL**.</span></span> <span data-ttu-id="92b58-149">Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="92b58-149">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92b58-150">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="92b58-150">Return value</span></span>

<span data-ttu-id="92b58-151">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="92b58-151">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="92b58-152">Retourne l’un des [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="92b58-152">Returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="92b58-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92b58-153">Requirements</span></span>



| <span data-ttu-id="92b58-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92b58-154">Requirement</span></span> | <span data-ttu-id="92b58-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="92b58-155">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="92b58-156">En-tête</span><span class="sxs-lookup"><span data-stu-id="92b58-156">Header</span></span><br/> | <dl> <span data-ttu-id="92b58-157"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="92b58-157"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92b58-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92b58-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92b58-159">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="92b58-159">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
