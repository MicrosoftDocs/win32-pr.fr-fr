---
title: D3DX11PreprocessShaderFromResource, fonction (D3DX11async. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Notez qu’au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser l’API D3DPreprocess. Créez un nuanceur à partir d’une ressource sans le compiler.'
ms.assetid: 13362ad6-f02e-4899-8962-4f7d4750ff69
keywords:
- Fonction D3DX11PreprocessShaderFromResource Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11PreprocessShaderFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 645d872e983cabbcd81aab05a59ee8f1f83cc403
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992264"
---
# <a name="d3dx11preprocessshaderfromresource-function"></a><span data-ttu-id="65618-106">D3DX11PreprocessShaderFromResource fonction)</span><span class="sxs-lookup"><span data-stu-id="65618-106">D3DX11PreprocessShaderFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="65618-107">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="65618-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="65618-108">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser l’API [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="65618-108">Instead of using this function, we recommend that you use the [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) API.</span></span>

 

<span data-ttu-id="65618-109">Créez un nuanceur à partir d’une ressource sans le compiler.</span><span class="sxs-lookup"><span data-stu-id="65618-109">Create a shader from a resource without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="65618-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65618-110">Syntax</span></span>


```C++
HRESULT D3DX11PreprocessShaderFromResource(
  _In_        HMODULE            hModule,
  _In_        LPCTSTR            pResourceName,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D11_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="65618-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65618-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65618-112">*HMODULE* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="65618-112">*hModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65618-113">Type : **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="65618-113">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="65618-114">Handle du module de ressource contenant le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="65618-114">Handle to the resource module containing the shader.</span></span> <span data-ttu-id="65618-115">HMODULE peut être obtenu avec la [fonction GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="65618-115">HMODULE can be obtained with [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="65618-116">*pResourceName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="65618-116">*pResourceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65618-117">Type : **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="65618-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="65618-118">Nom de la ressource côté hModule contenant le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="65618-118">The name of the resource in side hModule containing the shader.</span></span> <span data-ttu-id="65618-119">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="65618-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="65618-120">Dans le cas contraire, le type de données est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="65618-120">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="65618-121">*pSrcFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="65618-121">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65618-122">Type : **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="65618-122">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="65618-123">facultatif.</span><span class="sxs-lookup"><span data-stu-id="65618-123">Optional.</span></span> <span data-ttu-id="65618-124">Nom du fichier d’effet, qui est utilisé pour les messages d’erreur uniquement.</span><span class="sxs-lookup"><span data-stu-id="65618-124">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="65618-125">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="65618-125">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="65618-126">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="65618-126">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65618-127">Type : **const d3d11 \_ Shader \_ macro \***</span><span class="sxs-lookup"><span data-stu-id="65618-127">Type: **const D3D11\_SHADER\_MACRO\***</span></span>

<span data-ttu-id="65618-128">Tableau de macros de nuanceur se terminant par un caractère NULL ; Affectez-lui la valeur **null** pour ne spécifier aucune macro.</span><span class="sxs-lookup"><span data-stu-id="65618-128">A NULL-terminated array of shader macros; set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="65618-129">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="65618-129">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65618-130">Type : **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="65618-130">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="65618-131">Pointeur vers une interface include ; Affectez-lui la valeur **null** pour spécifier qu’il n’y a aucun fichier include.</span><span class="sxs-lookup"><span data-stu-id="65618-131">A pointer to an include interface; set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="65618-132">*pPump* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="65618-132">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65618-133">Type : **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="65618-133">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="65618-134">Pointeur vers une interface de pompage de thread (voir [**interface ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="65618-134">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="65618-135">Utilisez **null** pour spécifier que cette fonction ne doit pas être retournée tant qu’elle n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="65618-135">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="65618-136">*ppShaderText* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="65618-136">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65618-137">Type : **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="65618-137">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="65618-138">Pointeur vers la mémoire qui contient le nuanceur non compilé.</span><span class="sxs-lookup"><span data-stu-id="65618-138">A pointer to memory that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="65618-139">*ppErrorMsgs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="65618-139">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65618-140">Type : **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="65618-140">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="65618-141">Adresse d’un pointeur vers la mémoire qui contient des erreurs de création d’effet, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="65618-141">The address of a pointer to memory that contains effect-creation errors, if any occurred.</span></span>

</dd> <dt>

<span data-ttu-id="65618-142">*pHResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="65618-142">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65618-143">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="65618-143">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="65618-144">Pointeur vers la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="65618-144">A pointer to the return value.</span></span> <span data-ttu-id="65618-145">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="65618-145">May be **NULL**.</span></span> <span data-ttu-id="65618-146">Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="65618-146">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65618-147">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="65618-147">Return value</span></span>

<span data-ttu-id="65618-148">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="65618-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="65618-149">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="65618-149">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="65618-150">Spécifications</span><span class="sxs-lookup"><span data-stu-id="65618-150">Requirements</span></span>



| <span data-ttu-id="65618-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65618-151">Requirement</span></span> | <span data-ttu-id="65618-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="65618-152">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="65618-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="65618-153">Header</span></span><br/>  | <dl> <span data-ttu-id="65618-154"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="65618-154"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="65618-155">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="65618-155">Library</span></span><br/> | <dl> <span data-ttu-id="65618-156"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65618-156"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="65618-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65618-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65618-158">D3DX, fonctions</span><span class="sxs-lookup"><span data-stu-id="65618-158">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

