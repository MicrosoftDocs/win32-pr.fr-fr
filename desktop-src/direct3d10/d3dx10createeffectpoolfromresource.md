---
description: Créer un pool d’effets à partir d’une ressource.
ms.assetid: 594ab788-fd96-4ea9-ad93-ef02fefa5d61
title: D3DX10CreateEffectPoolFromResource, fonction (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectPoolFromResource
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 1fccc9c399a4573440318b92d1157738589da8a4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523177"
---
# <a name="d3dx10createeffectpoolfromresource-function"></a><span data-ttu-id="c320e-103">D3DX10CreateEffectPoolFromResource fonction)</span><span class="sxs-lookup"><span data-stu-id="c320e-103">D3DX10CreateEffectPoolFromResource function</span></span>

<span data-ttu-id="c320e-104">Créer un pool d’effets à partir d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="c320e-104">Create an effect pool from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="c320e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c320e-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectPoolFromResource(
  _In_        HMODULE            hModule,
  _In_        LPCTSTR            pResourceName,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        ID3D10Include      *pInclude,
  _In_        LPCSTR             pProfile,
  _In_        UINT               HLSLFlags,
  _In_        UINT               FXFlags,
  _In_        ID3D10Device       *pDevice,
  _In_        ID3DX10ThreadPump  *pPump,
  _In_        ID3D10EffectPool   **ppEffectPool,
  _In_        ID3D10Blob         **ppErrors,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="c320e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c320e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c320e-107">*HMODULE* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c320e-107">*hModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c320e-108">Type : **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c320e-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c320e-109">Handle du module de ressource contenant l’effet.</span><span class="sxs-lookup"><span data-stu-id="c320e-109">A handle to the resource module containing the effect.</span></span> <span data-ttu-id="c320e-110">HMODULE peut être obtenu avec la [fonction GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="c320e-110">HMODULE can be obtained with [GetModuleHandle Function](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="c320e-111">*pResourceName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c320e-111">*pResourceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c320e-112">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c320e-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c320e-113">Nom de la ressource dans hModule.</span><span class="sxs-lookup"><span data-stu-id="c320e-113">The name of the resource in hModule.</span></span> <span data-ttu-id="c320e-114">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="c320e-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="c320e-115">Dans le cas contraire, le type de données est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="c320e-115">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="c320e-116">*pSrcFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c320e-116">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c320e-117">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c320e-117">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c320e-118">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="c320e-118">Optional.</span></span> <span data-ttu-id="c320e-119">Nom du fichier d’effet, qui est utilisé pour les messages d’erreur uniquement.</span><span class="sxs-lookup"><span data-stu-id="c320e-119">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="c320e-120">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="c320e-120">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c320e-121">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c320e-121">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c320e-122">Type : **\* macro de [**\_ nuanceur \_ D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) const**</span><span class="sxs-lookup"><span data-stu-id="c320e-122">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="c320e-123">Tableau de macros de nuanceur se terminant par un caractère NULL (consultez la [**\_ \_ macro de nuanceur D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); définissez cette valeur sur **null** pour ne spécifier aucune macro.</span><span class="sxs-lookup"><span data-stu-id="c320e-123">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="c320e-124">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c320e-124">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c320e-125">Type : **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="c320e-125">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="c320e-126">Pointeur vers une interface include (voir [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="c320e-126">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="c320e-127">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c320e-127">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c320e-128">*pProfile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c320e-128">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c320e-129">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c320e-129">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c320e-130">Chaîne qui spécifie le [profil de nuanceur](../direct3dhlsl/dx-graphics-hlsl-models.md)ou le modèle de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="c320e-130">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="c320e-131">*HLSLFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c320e-131">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c320e-132">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c320e-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c320e-133">Options de compilation HLSL ( [consultez \_ constantes de nuanceur D3D10](d3d10-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="c320e-133">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="c320e-134">*FXFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c320e-134">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c320e-135">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c320e-135">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c320e-136">Appliquer des options de compilation (voir [indicateurs de compilation et d’effet](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="c320e-136">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="c320e-137">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c320e-137">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c320e-138">Type : **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="c320e-138">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="c320e-139">Pointeur vers l’appareil (voir [**interface ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) qui utilisera les ressources.</span><span class="sxs-lookup"><span data-stu-id="c320e-139">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="c320e-140">*pPump* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c320e-140">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c320e-141">Type : **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="c320e-141">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="c320e-142">Pointeur vers une interface de pompage de thread (voir [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="c320e-142">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="c320e-143">Utilisez **null** pour spécifier que cette fonction ne doit pas être retournée tant qu’elle n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="c320e-143">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="c320e-144">*ppEffectPool* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c320e-144">*ppEffectPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c320e-145">Type : **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span><span class="sxs-lookup"><span data-stu-id="c320e-145">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span></span>

<span data-ttu-id="c320e-146">Adresse d’un pointeur vers le pool d’effets (consultez [**ID3D10EffectPool interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span><span class="sxs-lookup"><span data-stu-id="c320e-146">The address of a pointer to the effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span></span>

</dd> <dt>

<span data-ttu-id="c320e-147">*ppErrors* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c320e-147">*ppErrors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c320e-148">Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="c320e-148">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="c320e-149">Adresse d’un pointeur vers la mémoire (voir [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) qui contient des erreurs d’effet de compilation, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="c320e-149">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="c320e-150">*pHResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c320e-150">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c320e-151">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="c320e-151">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="c320e-152">Pointeur vers la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="c320e-152">A pointer to the return value.</span></span> <span data-ttu-id="c320e-153">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="c320e-153">May be **NULL**.</span></span> <span data-ttu-id="c320e-154">Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="c320e-154">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c320e-155">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c320e-155">Return value</span></span>

<span data-ttu-id="c320e-156">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c320e-156">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c320e-157">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c320e-157">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c320e-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c320e-158">Requirements</span></span>



| <span data-ttu-id="c320e-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c320e-159">Requirement</span></span> | <span data-ttu-id="c320e-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="c320e-160">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c320e-161">En-tête</span><span class="sxs-lookup"><span data-stu-id="c320e-161">Header</span></span><br/> | <dl> <span data-ttu-id="c320e-162"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="c320e-162"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c320e-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c320e-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c320e-164">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="c320e-164">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
