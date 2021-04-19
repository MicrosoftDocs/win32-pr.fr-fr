---
description: Notez qu’au lieu d’utiliser cette fonction héritée, nous vous recommandons de compiler hors connexion à l’aide du compilateur de ligne de commande Fxc.exe ou d’utiliser l’API D3DCompile. Compilez un nuanceur ou un effet à partir d’une ressource.
ms.assetid: d291e47d-e04f-4e2d-9d05-9aef8e4fcf7e
title: D3DX10CompileFromResource, fonction (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CompileFromResource
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 6b698700804ca767c953343e6d5a5e540ca77555
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532430"
---
# <a name="d3dx10compilefromresource-function"></a><span data-ttu-id="b3618-104">D3DX10CompileFromResource fonction)</span><span class="sxs-lookup"><span data-stu-id="b3618-104">D3DX10CompileFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="b3618-105">Au lieu d’utiliser cette fonction héritée, nous vous recommandons de compiler hors connexion à l’aide du compilateur de ligne de commande Fxc.exe ou d’utiliser l’API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="b3618-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

<span data-ttu-id="b3618-106">Compilez un nuanceur ou un effet à partir d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="b3618-106">Compile a shader or an effect from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3618-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3618-107">Syntax</span></span>


```C++
HRESULT D3DX10CompileFromResource(
  _In_        HMODULE            hSrcModule,
  _In_        LPCTSTR            pSrcResource,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        LPCSTR             pFunctionName,
  _In_        LPCSTR             pProfile,
  _In_        UINT               Flags1,
  _In_        UINT               Flags2,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShader,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="b3618-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3618-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3618-109">*hSrcModule* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b3618-109">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3618-110">Type : **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3618-110">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3618-111">Handle du module de ressource contenant le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="b3618-111">Handle to the resource module containing the shader.</span></span> <span data-ttu-id="b3618-112">HMODULE peut être obtenu avec la [fonction GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="b3618-112">HMODULE can be obtained with [GetModuleHandle Function](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="b3618-113">*pSrcResource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b3618-113">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3618-114">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3618-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3618-115">Nom de la ressource contenant le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="b3618-115">Name of the resource containing the shader.</span></span> <span data-ttu-id="b3618-116">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="b3618-116">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="b3618-117">Dans le cas contraire, le type de données est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="b3618-117">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="b3618-118">*pSrcFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b3618-118">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3618-119">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3618-119">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3618-120">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="b3618-120">Optional.</span></span> <span data-ttu-id="b3618-121">Nom du fichier d’effet, qui est utilisé pour les messages d’erreur uniquement.</span><span class="sxs-lookup"><span data-stu-id="b3618-121">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="b3618-122">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="b3618-122">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b3618-123">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b3618-123">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3618-124">Type : **\* macro de [**\_ nuanceur \_ D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) const**</span><span class="sxs-lookup"><span data-stu-id="b3618-124">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="b3618-125">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="b3618-125">Optional.</span></span> <span data-ttu-id="b3618-126">Pointeur vers un tableau de définitions de macros (consultez la [**\_ \_ macro de nuanceur D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="b3618-126">Pointer to an array of macro definitions (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="b3618-127">La dernière structure du tableau sert de terminateur et doit avoir tous les membres définis sur 0.</span><span class="sxs-lookup"><span data-stu-id="b3618-127">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="b3618-128">S’il n’est pas utilisé, affectez la valeur **null** à *pDefines* .</span><span class="sxs-lookup"><span data-stu-id="b3618-128">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b3618-129">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b3618-129">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3618-130">Type : **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="b3618-130">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="b3618-131">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="b3618-131">Optional.</span></span> <span data-ttu-id="b3618-132">Pointeur vers une interface d' [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) pour la gestion des fichiers include.</span><span class="sxs-lookup"><span data-stu-id="b3618-132">Pointer to an [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) interface for handling include files.</span></span> <span data-ttu-id="b3618-133">Si vous affectez la **valeur null** , une erreur de compilation se produira si un nuanceur contient un \# include.</span><span class="sxs-lookup"><span data-stu-id="b3618-133">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="b3618-134">*pFunctionName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b3618-134">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3618-135">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3618-135">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3618-136">Nom de la fonction de point d’entrée du nuanceur où commence l’exécution du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="b3618-136">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="b3618-137">Quand vous compilez un effet, **D3DX10CompileFromResource** ignore *pFunctionName*; Nous vous recommandons de définir *pFunctionName* sur **null** , car il s’agit d’une bonne pratique de programmation qui consiste à définir un paramètre de pointeur sur la **valeur null** si la fonction appelée ne l’utilise pas.</span><span class="sxs-lookup"><span data-stu-id="b3618-137">When you compile an effect, **D3DX10CompileFromResource** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="b3618-138">*pProfile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b3618-138">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3618-139">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3618-139">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3618-140">Chaîne qui spécifie le modèle de nuanceur ; peut être n’importe quel profil dans le [Shader Model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [Shader Model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md)ou [Shader Model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span><span class="sxs-lookup"><span data-stu-id="b3618-140">A string that specifies the shader model; can be any profile in [shader model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [shader model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md), or [shader model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3618-141">*Flags1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b3618-141">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3618-142">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3618-142">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3618-143">[Indicateurs de compilation du nuanceur](d3d10-shader.md).</span><span class="sxs-lookup"><span data-stu-id="b3618-143">[Shader compile flags](d3d10-shader.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3618-144">*Flags2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b3618-144">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3618-145">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3618-145">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3618-146">[Indicateurs de compilation Effect](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b3618-146">[Effect compile flags](d3d10-graphics-reference-effect-constants.md).</span></span> <span data-ttu-id="b3618-147">Quand vous compilez un nuanceur et non un fichier Effect, **D3DX10CompileFromResource** ignore *flags2*; Nous vous recommandons de définir *flags2* sur zéro, car il s’agit d’une bonne pratique de programmation qui consiste à définir un paramètre de non-pointeur sur zéro si la fonction appelée ne l’utilise pas.</span><span class="sxs-lookup"><span data-stu-id="b3618-147">When you compile a shader and not an effect file, **D3DX10CompileFromResource** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="b3618-148">*pPump* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b3618-148">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3618-149">Type : **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="b3618-149">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="b3618-150">Pointeur vers une interface de pompage de thread (voir [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="b3618-150">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="b3618-151">Utilisez **null** pour spécifier que cette fonction ne doit pas être retournée tant qu’elle n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="b3618-151">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="b3618-152">*ppShader* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b3618-152">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3618-153">Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="b3618-153">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="b3618-154">Pointeur vers une [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) qui contient le nuanceur compilé, ainsi que toutes les informations de débogage et de table de symboles incorporées.</span><span class="sxs-lookup"><span data-stu-id="b3618-154">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="b3618-155">*ppErrorMsgs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b3618-155">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3618-156">Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="b3618-156">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="b3618-157">Pointeur vers une [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) qui contient une liste d’erreurs et d’avertissements qui se sont produits pendant la compilation.</span><span class="sxs-lookup"><span data-stu-id="b3618-157">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="b3618-158">Ces erreurs et avertissements sont identiques à la sortie de débogage d’un débogueur.</span><span class="sxs-lookup"><span data-stu-id="b3618-158">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="b3618-159">*pHResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b3618-159">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3618-160">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="b3618-160">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="b3618-161">Pointeur vers la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="b3618-161">A pointer to the return value.</span></span> <span data-ttu-id="b3618-162">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="b3618-162">May be **NULL**.</span></span> <span data-ttu-id="b3618-163">Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="b3618-163">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3618-164">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b3618-164">Return value</span></span>

<span data-ttu-id="b3618-165">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b3618-165">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b3618-166">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b3618-166">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3618-167">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3618-167">Requirements</span></span>



| <span data-ttu-id="b3618-168">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3618-168">Requirement</span></span> | <span data-ttu-id="b3618-169">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3618-169">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3618-170">En-tête</span><span class="sxs-lookup"><span data-stu-id="b3618-170">Header</span></span><br/> | <dl> <span data-ttu-id="b3618-171"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3618-171"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3618-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3618-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3618-173">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="b3618-173">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
