---
description: Créer un effet à partir d’un fichier.
ms.assetid: 1418857e-bda1-4ffb-bbb9-dfa3709313b1
title: D3DX10CreateEffectFromFile, fonction (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 60bc52e5b149a2fa69cc4a16f12900b12ab81db8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523850"
---
# <a name="d3dx10createeffectfromfile-function"></a><span data-ttu-id="eb3cd-103">D3DX10CreateEffectFromFile fonction)</span><span class="sxs-lookup"><span data-stu-id="eb3cd-103">D3DX10CreateEffectFromFile function</span></span>

<span data-ttu-id="eb3cd-104">Créer un effet à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="eb3cd-104">Create an effect from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb3cd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb3cd-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectFromFile(
  _In_        LPCTSTR            pFileName,
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



## <a name="parameters"></a><span data-ttu-id="eb3cd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb3cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb3cd-107">*pFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb3cd-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb3cd-108">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb3cd-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb3cd-109">Nom du fichier d’effet ASCII.</span><span class="sxs-lookup"><span data-stu-id="eb3cd-109">Name of the ASCII effect file.</span></span> <span data-ttu-id="eb3cd-110">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="eb3cd-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="eb3cd-111">Dans le cas contraire, le type de données est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="eb3cd-111">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="eb3cd-112">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb3cd-112">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb3cd-113">Type : **\* macro de [**\_ nuanceur \_ D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) const**</span><span class="sxs-lookup"><span data-stu-id="eb3cd-113">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="eb3cd-114">Tableau de macros de nuanceur se terminant par un caractère NULL (consultez la [**\_ \_ macro de nuanceur D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); définissez cette valeur sur **null** pour ne spécifier aucune macro.</span><span class="sxs-lookup"><span data-stu-id="eb3cd-114">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="eb3cd-115">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb3cd-115">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb3cd-116">Type : **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="eb3cd-116">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="eb3cd-117">Pointeur vers une interface include (voir [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="eb3cd-117">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="eb3cd-118">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="eb3cd-118">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="eb3cd-119">*pProfile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb3cd-119">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb3cd-120">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb3cd-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb3cd-121">Chaîne qui spécifie le [profil de nuanceur](../direct3dhlsl/dx-graphics-hlsl-models.md)ou le modèle de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="eb3cd-121">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="eb3cd-122">*HLSLFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb3cd-122">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb3cd-123">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb3cd-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb3cd-124">Options de compilation HLSL ( [consultez \_ constantes de nuanceur D3D10](d3d10-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="eb3cd-124">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="eb3cd-125">*FXFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb3cd-125">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb3cd-126">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb3cd-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb3cd-127">Appliquer des options de compilation (voir [indicateurs de compilation et d’effet](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="eb3cd-127">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="eb3cd-128">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb3cd-128">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb3cd-129">Type : **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="eb3cd-129">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="eb3cd-130">Pointeur vers l’appareil (voir [**interface ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) qui utilisera les ressources.</span><span class="sxs-lookup"><span data-stu-id="eb3cd-130">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="eb3cd-131">*pEffectPool* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb3cd-131">*pEffectPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb3cd-132">Type : **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span><span class="sxs-lookup"><span data-stu-id="eb3cd-132">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span></span>

<span data-ttu-id="eb3cd-133">Pointeur vers un pool d’effets (voir [**interface ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) pour le partage de variables entre les effets.</span><span class="sxs-lookup"><span data-stu-id="eb3cd-133">Pointer to an effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) for sharing variables between effects.</span></span>

</dd> <dt>

<span data-ttu-id="eb3cd-134">*pPump* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb3cd-134">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb3cd-135">Type : **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="eb3cd-135">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="eb3cd-136">Pointeur vers une interface de pompage de thread (voir [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="eb3cd-136">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="eb3cd-137">Utilisez **null** pour spécifier que cette fonction ne doit pas être retournée tant qu’elle n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="eb3cd-137">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="eb3cd-138">*ppEffect* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="eb3cd-138">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb3cd-139">Type : **[ **ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span><span class="sxs-lookup"><span data-stu-id="eb3cd-139">Type: **[**ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span></span>

<span data-ttu-id="eb3cd-140">Adresse d’un pointeur vers l’effet (voir [**interface ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)) créé.</span><span class="sxs-lookup"><span data-stu-id="eb3cd-140">Address of a pointer to the effect (see [**ID3D10Effect Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)) that is created.</span></span>

</dd> <dt>

<span data-ttu-id="eb3cd-141">*ppErrors* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="eb3cd-141">*ppErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb3cd-142">Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="eb3cd-142">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="eb3cd-143">Adresse d’un pointeur vers la mémoire (voir [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) qui contient des erreurs d’effet de compilation, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="eb3cd-143">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="eb3cd-144">*pHResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="eb3cd-144">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb3cd-145">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="eb3cd-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="eb3cd-146">Pointeur vers la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="eb3cd-146">A pointer to the return value.</span></span> <span data-ttu-id="eb3cd-147">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="eb3cd-147">May be **NULL**.</span></span> <span data-ttu-id="eb3cd-148">Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="eb3cd-148">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb3cd-149">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eb3cd-149">Return value</span></span>

<span data-ttu-id="eb3cd-150">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eb3cd-150">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eb3cd-151">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="eb3cd-151">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb3cd-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb3cd-152">Requirements</span></span>



| <span data-ttu-id="eb3cd-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb3cd-153">Requirement</span></span> | <span data-ttu-id="eb3cd-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb3cd-154">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb3cd-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="eb3cd-155">Header</span></span><br/> | <dl> <span data-ttu-id="eb3cd-156"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb3cd-156"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb3cd-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb3cd-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb3cd-158">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="eb3cd-158">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
