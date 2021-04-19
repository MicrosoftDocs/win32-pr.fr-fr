---
description: Créez un effet à partir de la mémoire.
ms.assetid: 6903a695-bb87-45fe-9913-25beeaf17233
title: D3DX10CreateEffectFromMemory, fonction (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectFromMemory
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 03cbbc70e633f8289f99e094602cb1a912b711c5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527117"
---
# <a name="d3dx10createeffectfrommemory-function"></a><span data-ttu-id="4ac0d-103">D3DX10CreateEffectFromMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="4ac0d-103">D3DX10CreateEffectFromMemory function</span></span>

<span data-ttu-id="4ac0d-104">Créez un effet à partir de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="4ac0d-104">Create an effect from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ac0d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4ac0d-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectFromMemory(
  _In_        LPCVOID            pData,
  _In_        SIZE_T             DataLength,
  _In_        LPCSTR             pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        ID3D10Include      *pInclude,
  _In_        LPCSTR             pProfile,
  _In_        UINT               HLSLFlags,
  _In_        UINT               FXFlags,
  _In_        ID3D10Device       *pDevice,
  _In_        ID3D10EffectPool   *pEffectPool,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Effect       **ppEffect,
  _Out_       ID3D10Blob         **ppErrors,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="4ac0d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4ac0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ac0d-107">*pData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4ac0d-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ac0d-108">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4ac0d-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4ac0d-109">Pointeur vers l’effet en mémoire.</span><span class="sxs-lookup"><span data-stu-id="4ac0d-109">Pointer to the effect in memory.</span></span>

</dd> <dt>

<span data-ttu-id="4ac0d-110">*DATALENGTH* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4ac0d-110">*DataLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ac0d-111">Type : **[ **taille \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4ac0d-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4ac0d-112">Taille de l’effet en mémoire.</span><span class="sxs-lookup"><span data-stu-id="4ac0d-112">Size of the effect in memory.</span></span>

</dd> <dt>

<span data-ttu-id="4ac0d-113">*pSrcFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4ac0d-113">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ac0d-114">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4ac0d-114">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4ac0d-115">Nom du fichier d’effet en mémoire.</span><span class="sxs-lookup"><span data-stu-id="4ac0d-115">Name of the effect file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="4ac0d-116">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4ac0d-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ac0d-117">Type : **\* macro de [**\_ nuanceur \_ D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) const**</span><span class="sxs-lookup"><span data-stu-id="4ac0d-117">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="4ac0d-118">Tableau de macros de nuanceur se terminant par un caractère NULL (consultez la [**\_ \_ macro de nuanceur D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); définissez cette valeur sur **null** pour ne spécifier aucune macro.</span><span class="sxs-lookup"><span data-stu-id="4ac0d-118">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="4ac0d-119">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4ac0d-119">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ac0d-120">Type : **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="4ac0d-120">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="4ac0d-121">Pointeur vers une interface include (voir [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="4ac0d-121">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="4ac0d-122">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4ac0d-122">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4ac0d-123">*pProfile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4ac0d-123">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ac0d-124">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4ac0d-124">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4ac0d-125">Chaîne qui spécifie le [profil de nuanceur](../direct3dhlsl/dx-graphics-hlsl-models.md)ou le modèle de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="4ac0d-125">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="4ac0d-126">*HLSLFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4ac0d-126">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ac0d-127">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4ac0d-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4ac0d-128">Options de compilation HLSL ( [consultez \_ constantes de nuanceur D3D10](d3d10-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="4ac0d-128">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="4ac0d-129">*FXFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4ac0d-129">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ac0d-130">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4ac0d-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4ac0d-131">Appliquer des options de compilation (consultez [D3D10 \_ Effect, constantes](d3d10-effect.md)).</span><span class="sxs-lookup"><span data-stu-id="4ac0d-131">Effect compile options (see [D3D10\_EFFECT Constants](d3d10-effect.md)).</span></span>

</dd> <dt>

<span data-ttu-id="4ac0d-132">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4ac0d-132">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ac0d-133">Type : **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="4ac0d-133">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="4ac0d-134">Pointeur vers l’appareil (voir [**interface ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) qui utilisera les ressources.</span><span class="sxs-lookup"><span data-stu-id="4ac0d-134">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="4ac0d-135">*pEffectPool* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4ac0d-135">*pEffectPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ac0d-136">Type : **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span><span class="sxs-lookup"><span data-stu-id="4ac0d-136">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span></span>

<span data-ttu-id="4ac0d-137">Pointeur vers un pool d’effets (voir [**interface ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) pour le partage de variables entre les effets.</span><span class="sxs-lookup"><span data-stu-id="4ac0d-137">Pointer to an effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) for sharing variables between effects.</span></span>

</dd> <dt>

<span data-ttu-id="4ac0d-138">*pPump* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4ac0d-138">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ac0d-139">Type : **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="4ac0d-139">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="4ac0d-140">Pointeur vers une interface de pompage de thread (voir [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="4ac0d-140">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="4ac0d-141">Utilisez **null** pour spécifier que cette fonction ne doit pas être retournée tant qu’elle n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="4ac0d-141">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="4ac0d-142">*ppEffect* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4ac0d-142">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ac0d-143">Type : **[ **ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span><span class="sxs-lookup"><span data-stu-id="4ac0d-143">Type: **[**ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span></span>

<span data-ttu-id="4ac0d-144">Adresse d’un pointeur vers l’effet (voir [**interface ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)) créé.</span><span class="sxs-lookup"><span data-stu-id="4ac0d-144">Address of a pointer to the effect (see [**ID3D10Effect Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)) that is created.</span></span>

</dd> <dt>

<span data-ttu-id="4ac0d-145">*ppErrors* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4ac0d-145">*ppErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ac0d-146">Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="4ac0d-146">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="4ac0d-147">Adresse d’un pointeur vers la mémoire (voir [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) qui contient des erreurs d’effet de compilation, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="4ac0d-147">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="4ac0d-148">*pHResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4ac0d-148">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ac0d-149">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="4ac0d-149">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="4ac0d-150">Pointeur vers la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="4ac0d-150">A pointer to the return value.</span></span> <span data-ttu-id="4ac0d-151">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="4ac0d-151">May be **NULL**.</span></span> <span data-ttu-id="4ac0d-152">Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="4ac0d-152">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ac0d-153">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4ac0d-153">Return value</span></span>

<span data-ttu-id="4ac0d-154">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4ac0d-154">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4ac0d-155">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="4ac0d-155">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ac0d-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4ac0d-156">Requirements</span></span>



| <span data-ttu-id="4ac0d-157">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4ac0d-157">Requirement</span></span> | <span data-ttu-id="4ac0d-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ac0d-158">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ac0d-159">En-tête</span><span class="sxs-lookup"><span data-stu-id="4ac0d-159">Header</span></span><br/> | <dl> <span data-ttu-id="4ac0d-160"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ac0d-160"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ac0d-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ac0d-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ac0d-162">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="4ac0d-162">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
