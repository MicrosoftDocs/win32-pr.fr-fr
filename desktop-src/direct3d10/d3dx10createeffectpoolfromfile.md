---
description: Créer un pool d’effets à partir d’un fichier d’effet.
ms.assetid: be738374-a91e-43d3-9cec-14882e6317ee
title: D3DX10CreateEffectFromFile, fonction (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectPoolFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 418ea287b9bbf2021f3b2e5379b209cf87745a69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537245"
---
# <a name="d3dx10createeffectpoolfromfile-function"></a><span data-ttu-id="3b7c7-103">D3DX10CreateEffectPoolFromFile fonction)</span><span class="sxs-lookup"><span data-stu-id="3b7c7-103">D3DX10CreateEffectPoolFromFile function</span></span>

<span data-ttu-id="3b7c7-104">Créer un pool d’effets à partir d’un fichier d’effet.</span><span class="sxs-lookup"><span data-stu-id="3b7c7-104">Create an effect pool from an effect file.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b7c7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b7c7-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectPoolFromFile(
  _In_        LPCTSTR            pFileName,
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



## <a name="parameters"></a><span data-ttu-id="3b7c7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b7c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b7c7-107">*pFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3b7c7-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b7c7-108">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3b7c7-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3b7c7-109">Nom du fichier d’effet.</span><span class="sxs-lookup"><span data-stu-id="3b7c7-109">The effect filename.</span></span> <span data-ttu-id="3b7c7-110">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="3b7c7-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="3b7c7-111">Dans le cas contraire, le type de données est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="3b7c7-111">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="3b7c7-112">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3b7c7-112">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b7c7-113">Type : **\* macro de [**\_ nuanceur \_ D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) const**</span><span class="sxs-lookup"><span data-stu-id="3b7c7-113">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="3b7c7-114">Tableau de macros de nuanceur se terminant par un caractère NULL (consultez la [**\_ \_ macro de nuanceur D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); définissez cette valeur sur **null** pour ne spécifier aucune macro.</span><span class="sxs-lookup"><span data-stu-id="3b7c7-114">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="3b7c7-115">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3b7c7-115">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b7c7-116">Type : **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="3b7c7-116">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="3b7c7-117">Pointeur vers une interface include (voir [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="3b7c7-117">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="3b7c7-118">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3b7c7-118">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3b7c7-119">*pProfile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3b7c7-119">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b7c7-120">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3b7c7-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3b7c7-121">Chaîne qui spécifie le [profil de nuanceur](../direct3dhlsl/dx-graphics-hlsl-models.md)ou le modèle de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="3b7c7-121">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="3b7c7-122">*HLSLFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3b7c7-122">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b7c7-123">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3b7c7-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3b7c7-124">Options de compilation HLSL ( [consultez \_ constantes de nuanceur D3D10](d3d10-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="3b7c7-124">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="3b7c7-125">*FXFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3b7c7-125">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b7c7-126">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3b7c7-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3b7c7-127">Appliquer des options de compilation (voir [indicateurs de compilation et d’effet](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="3b7c7-127">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="3b7c7-128">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3b7c7-128">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b7c7-129">Type : **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="3b7c7-129">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="3b7c7-130">Pointeur vers l’appareil (voir [**interface ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) qui utilisera les ressources.</span><span class="sxs-lookup"><span data-stu-id="3b7c7-130">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="3b7c7-131">*pPump* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3b7c7-131">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b7c7-132">Type : **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="3b7c7-132">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="3b7c7-133">Pointeur vers une interface de pompage de thread (voir [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="3b7c7-133">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="3b7c7-134">Utilisez **null** pour spécifier que cette fonction ne doit pas être retournée tant qu’elle n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="3b7c7-134">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="3b7c7-135">*ppEffectPool* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3b7c7-135">*ppEffectPool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b7c7-136">Type : **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span><span class="sxs-lookup"><span data-stu-id="3b7c7-136">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span></span>

<span data-ttu-id="3b7c7-137">Adresse d’un pointeur vers le pool d’effets (consultez [**ID3D10EffectPool interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span><span class="sxs-lookup"><span data-stu-id="3b7c7-137">The address of a pointer to the effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span></span>

</dd> <dt>

<span data-ttu-id="3b7c7-138">*ppErrors* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3b7c7-138">*ppErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b7c7-139">Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="3b7c7-139">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="3b7c7-140">Adresse d’un pointeur vers la mémoire (voir [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) qui contient des erreurs d’effet de compilation, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="3b7c7-140">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="3b7c7-141">*pHResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3b7c7-141">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b7c7-142">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="3b7c7-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="3b7c7-143">Pointeur vers la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="3b7c7-143">A pointer to the return value.</span></span> <span data-ttu-id="3b7c7-144">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="3b7c7-144">May be **NULL**.</span></span> <span data-ttu-id="3b7c7-145">Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="3b7c7-145">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b7c7-146">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3b7c7-146">Return value</span></span>

<span data-ttu-id="3b7c7-147">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3b7c7-147">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3b7c7-148">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="3b7c7-148">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3b7c7-149">Notes</span><span class="sxs-lookup"><span data-stu-id="3b7c7-149">Remarks</span></span>

<span data-ttu-id="3b7c7-150">Cet exemple crée un pool d’effets à partir de l’effet utilisé dans l' [exemple BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="3b7c7-150">This example creates an effect pool from the effect used in the [BasicHLSL10 Sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).</span></span>


```
   
// Create an effect pool from an effect in memory
ID3D10EffectPool * l_pEffectPool = NULL;
ID3D10Blob* l_pBlob_Errors = NULL;
WCHAR str[MAX_PATH];
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
hr = D3DX10CreateEffectPoolFromFile( str, 
    NULL, NULL, D3D10_SHADER_ENABLE_STRICTNESS, 
    0, pd3dDevice, NULL, &l_pEffectPool,
    &l_pBlob_Errors );
```



## <a name="requirements"></a><span data-ttu-id="3b7c7-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b7c7-151">Requirements</span></span>



| <span data-ttu-id="3b7c7-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b7c7-152">Requirement</span></span> | <span data-ttu-id="3b7c7-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b7c7-153">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b7c7-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="3b7c7-154">Header</span></span><br/> | <dl> <span data-ttu-id="3b7c7-155"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b7c7-155"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b7c7-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b7c7-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b7c7-157">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="3b7c7-157">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
