---
title: D3DX11CompileFromFile, fonction (D3DX11async. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Remarque au lieu d’utiliser cette fonction, nous vous recommandons de compiler hors connexion à l’aide du compilateur de ligne de commande Fxc.exe ou d’utiliser l’une des API de compilation HLSL, comme l’API D3DCompileFromFile. Compilez un nuanceur ou un effet à partir d’un fichier.'
ms.assetid: 91a1a339-50da-4f86-9b55-6af246a60482
keywords:
- Fonction D3DX11CompileFromFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CompileFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89c9194eb54652304c220e5a4de0ee12a26ea1a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116258"
---
# <a name="d3dx11compilefromfile-function"></a><span data-ttu-id="fe862-106">D3DX11CompileFromFile fonction)</span><span class="sxs-lookup"><span data-stu-id="fe862-106">D3DX11CompileFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="fe862-107">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="fe862-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="fe862-108">Au lieu d’utiliser cette fonction, nous vous recommandons de compiler hors connexion à l’aide du compilateur de ligne de commande Fxc.exe ou d’utiliser l’une des API de compilation HLSL, comme l’API [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) .</span><span class="sxs-lookup"><span data-stu-id="fe862-108">Instead of using this function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) API.</span></span>

 

<span data-ttu-id="fe862-109">Compilez un nuanceur ou un effet à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="fe862-109">Compile a shader or an effect from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe862-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe862-110">Syntax</span></span>


```C++
HRESULT D3DX11CompileFromFile(
  _In_        LPCTSTR            pSrcFile,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        LPCSTR             pFunctionName,
  _In_        LPCSTR             pProfile,
  _In_        UINT               Flags1,
  _In_        UINT               Flags2,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShader,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="fe862-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe862-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe862-112">*pSrcFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fe862-112">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe862-113">Type : **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fe862-113">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fe862-114">Nom du fichier qui contient le code du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="fe862-114">The name of the file that contains the shader code.</span></span> <span data-ttu-id="fe862-115">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="fe862-115">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="fe862-116">Dans le cas contraire, le type de données est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="fe862-116">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="fe862-117">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fe862-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe862-118">Type : **const [**D3D10 \_ Shader \_ macro**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="fe862-118">Type: **const [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="fe862-119">facultatif.</span><span class="sxs-lookup"><span data-stu-id="fe862-119">Optional.</span></span> <span data-ttu-id="fe862-120">Pointeur vers un tableau de définitions de macros (consultez la [**\_ \_ macro de nuanceur D3D10**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="fe862-120">Pointer to an array of macro definitions (see [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="fe862-121">La dernière structure du tableau sert de terminateur et doit avoir tous les membres définis sur 0.</span><span class="sxs-lookup"><span data-stu-id="fe862-121">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="fe862-122">S’il n’est pas utilisé, affectez la valeur **null** à *pDefines* .</span><span class="sxs-lookup"><span data-stu-id="fe862-122">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fe862-123">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fe862-123">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe862-124">Type : **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="fe862-124">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="fe862-125">facultatif.</span><span class="sxs-lookup"><span data-stu-id="fe862-125">Optional.</span></span> <span data-ttu-id="fe862-126">Pointeur vers une interface pour la gestion des fichiers include.</span><span class="sxs-lookup"><span data-stu-id="fe862-126">Pointer to an interface for handling include files.</span></span> <span data-ttu-id="fe862-127">Si vous affectez la **valeur null** , une erreur de compilation se produira si un nuanceur contient un \# include.</span><span class="sxs-lookup"><span data-stu-id="fe862-127">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="fe862-128">*pFunctionName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fe862-128">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe862-129">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fe862-129">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fe862-130">Nom de la fonction de point d’entrée du nuanceur où commence l’exécution du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="fe862-130">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="fe862-131">Quand vous compilez un effet, **D3DX11CompileFromFile** ignore *pFunctionName*; Nous vous recommandons de définir *pFunctionName* sur **null** , car il s’agit d’une bonne pratique de programmation qui consiste à définir un paramètre de pointeur sur la **valeur null** si la fonction appelée ne l’utilise pas.</span><span class="sxs-lookup"><span data-stu-id="fe862-131">When you compile an effect, **D3DX11CompileFromFile** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="fe862-132">*pProfile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fe862-132">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe862-133">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fe862-133">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fe862-134">Chaîne qui spécifie le modèle de nuanceur ; peut être n’importe quel profil dans le nuancier Model 2, Shader Model 3, Shader Model 4 ou Shader Model 5.</span><span class="sxs-lookup"><span data-stu-id="fe862-134">A string that specifies the shader model; can be any profile in shader model 2, shader model 3, shader model 4, or shader model 5.</span></span> <span data-ttu-id="fe862-135">Le profil peut également être pour le type d’effet (par exemple, FX \_ 4 \_ 1).</span><span class="sxs-lookup"><span data-stu-id="fe862-135">The profile can also be for effect type (for example, fx\_4\_1).</span></span>

</dd> <dt>

<span data-ttu-id="fe862-136">*Flags1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fe862-136">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe862-137">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fe862-137">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fe862-138">[**Indicateurs de compilation**](/windows/desktop/direct3dhlsl/d3dcompile-constants)du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="fe862-138">Shader [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-constants).</span></span>

</dd> <dt>

<span data-ttu-id="fe862-139">*Flags2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fe862-139">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe862-140">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fe862-140">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fe862-141">[**Indicateurs de compilation**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants)Effect.</span><span class="sxs-lookup"><span data-stu-id="fe862-141">Effect [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants).</span></span> <span data-ttu-id="fe862-142">Quand vous compilez un nuanceur et non un fichier Effect, **D3DX11CompileFromFile** ignore *flags2*; Nous vous recommandons de définir *flags2* sur zéro, car il s’agit d’une bonne pratique de programmation qui consiste à définir un paramètre de non-pointeur sur zéro si la fonction appelée ne l’utilise pas.</span><span class="sxs-lookup"><span data-stu-id="fe862-142">When you compile a shader and not an effect file, **D3DX11CompileFromFile** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="fe862-143">*pPump* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fe862-143">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe862-144">Type : **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="fe862-144">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="fe862-145">Pointeur vers une interface de pompage de thread (voir [**interface ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="fe862-145">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="fe862-146">Utilisez **null** pour spécifier que cette fonction ne doit pas être retournée tant qu’elle n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="fe862-146">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="fe862-147">*ppShader* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fe862-147">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe862-148">Type : **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="fe862-148">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="fe862-149">Pointeur vers la mémoire qui contient le nuanceur compilé, ainsi que toutes les informations de débogage et de table de symboles incorporées.</span><span class="sxs-lookup"><span data-stu-id="fe862-149">A pointer to memory which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="fe862-150">*ppErrorMsgs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fe862-150">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe862-151">Type : **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="fe862-151">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="fe862-152">Pointeur vers la mémoire qui contient une liste d’erreurs et d’avertissements qui se sont produits pendant la compilation.</span><span class="sxs-lookup"><span data-stu-id="fe862-152">A pointer to memory which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="fe862-153">Ces erreurs et avertissements sont identiques à la sortie de débogage d’un débogueur.</span><span class="sxs-lookup"><span data-stu-id="fe862-153">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="fe862-154">*pHResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fe862-154">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe862-155">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="fe862-155">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="fe862-156">Pointeur vers la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="fe862-156">A pointer to the return value.</span></span> <span data-ttu-id="fe862-157">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="fe862-157">May be **NULL**.</span></span> <span data-ttu-id="fe862-158">Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="fe862-158">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe862-159">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fe862-159">Return value</span></span>

<span data-ttu-id="fe862-160">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fe862-160">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fe862-161">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="fe862-161">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

<span data-ttu-id="fe862-162">**D3DX11CompileFromFile** retourne E \_ INVALIDARG si vous fournissez une valeur non **null** au paramètre *pHResult* lorsque vous fournissez la valeur **null** au paramètre *pPump* .</span><span class="sxs-lookup"><span data-stu-id="fe862-162">**D3DX11CompileFromFile** returns E\_INVALIDARG if you supply a non-**NULL** value to the *pHResult* parameter when you supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="fe862-163">Pour plus d’informations sur cette situation, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="fe862-163">For more information about this situation, see Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe862-164">Notes</span><span class="sxs-lookup"><span data-stu-id="fe862-164">Remarks</span></span>

<span data-ttu-id="fe862-165">Pour plus d’informations sur **D3DX11CompileFromFile**, consultez [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span><span class="sxs-lookup"><span data-stu-id="fe862-165">For more information about **D3DX11CompileFromFile**, see [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span></span>

<span data-ttu-id="fe862-166">Vous devez fournir la **valeur null** au paramètre *pHResult* si vous fournissez également la **valeur null** au paramètre *pPump* .</span><span class="sxs-lookup"><span data-stu-id="fe862-166">You must supply **NULL** to the *pHResult* parameter if you also supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="fe862-167">Dans le cas contraire, vous ne pouvez pas créer de nuanceur à l’aide du code de nuanceur compilé que **D3DX11CompileFromFile** retourne dans la mémoire vers laquelle pointe le paramètre *ppShader* .</span><span class="sxs-lookup"><span data-stu-id="fe862-167">Otherwise, you cannot create a shader by using the compiled shader code that **D3DX11CompileFromFile** returns in the memory that the *ppShader* parameter points to.</span></span> <span data-ttu-id="fe862-168">Pour créer un nuanceur à partir d’un code de nuanceur conforme, vous appelez l’une des méthodes d’interface [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) suivantes :</span><span class="sxs-lookup"><span data-stu-id="fe862-168">To create a shader from complied shader code, you call one of the following [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface methods:</span></span>

-   [<span data-ttu-id="fe862-169">**CreateComputeShader**</span><span class="sxs-lookup"><span data-stu-id="fe862-169">**CreateComputeShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader)
-   [<span data-ttu-id="fe862-170">**CreateDomainShader**</span><span class="sxs-lookup"><span data-stu-id="fe862-170">**CreateDomainShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [<span data-ttu-id="fe862-171">**CreateGeometryShader**</span><span class="sxs-lookup"><span data-stu-id="fe862-171">**CreateGeometryShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [<span data-ttu-id="fe862-172">**CreateGeometryShaderWithStreamOutput**</span><span class="sxs-lookup"><span data-stu-id="fe862-172">**CreateGeometryShaderWithStreamOutput**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [<span data-ttu-id="fe862-173">**CreateHullShader**</span><span class="sxs-lookup"><span data-stu-id="fe862-173">**CreateHullShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [<span data-ttu-id="fe862-174">**CreatePixelShader**</span><span class="sxs-lookup"><span data-stu-id="fe862-174">**CreatePixelShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createpixelshader)
-   [<span data-ttu-id="fe862-175">**CreateVertexShader**</span><span class="sxs-lookup"><span data-stu-id="fe862-175">**CreateVertexShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

<span data-ttu-id="fe862-176">En outre, si vous fournissez une valeur non **null** à *pHResult* lorsque vous fournissez la valeur **null** à *pPump*, **D3DX11CompileFromFile** retourne le code d’erreur de l’E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="fe862-176">In addition, if you supply a non-**NULL** value to *pHResult* when you supply **NULL** to *pPump*, **D3DX11CompileFromFile** returns the E\_INVALIDARG error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe862-177">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fe862-177">Requirements</span></span>



| <span data-ttu-id="fe862-178">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe862-178">Requirement</span></span> | <span data-ttu-id="fe862-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe862-179">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe862-180">En-tête</span><span class="sxs-lookup"><span data-stu-id="fe862-180">Header</span></span><br/>  | <dl> <span data-ttu-id="fe862-181"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe862-181"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="fe862-182">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fe862-182">Library</span></span><br/> | <dl> <span data-ttu-id="fe862-183"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe862-183"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="fe862-184">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe862-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe862-185">D3DX, fonctions</span><span class="sxs-lookup"><span data-stu-id="fe862-185">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

