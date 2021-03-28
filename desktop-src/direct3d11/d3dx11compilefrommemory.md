---
title: D3DX11CompileFromMemory, fonction (D3DX11async. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Remarque au lieu d’utiliser cette fonction, nous vous recommandons de compiler hors connexion à l’aide du compilateur de ligne de commande Fxc.exe ou d’utiliser l’une des API de compilation HLSL, comme l’API D3DCompile. Compilez un nuanceur ou un effet qui est chargé en mémoire.'
ms.assetid: 3396560f-f411-4c66-9f22-03c0050c74b0
keywords:
- Fonction D3DX11CompileFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CompileFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e10590c3db458a23bf4d52b6507146884630087
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974615"
---
# <a name="d3dx11compilefrommemory-function"></a><span data-ttu-id="bdcf4-106">D3DX11CompileFromMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="bdcf4-106">D3DX11CompileFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="bdcf4-107">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="bdcf4-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="bdcf4-108">Au lieu d’utiliser cette fonction, nous vous recommandons de compiler hors connexion à l’aide du compilateur de ligne de commande Fxc.exe ou d’utiliser l’une des API de compilation HLSL, comme l’API [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="bdcf4-108">Instead of using this function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) API.</span></span>

 

<span data-ttu-id="bdcf4-109">Compilez un nuanceur ou un effet qui est chargé en mémoire.</span><span class="sxs-lookup"><span data-stu-id="bdcf4-109">Compile a shader or an effect that is loaded in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdcf4-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bdcf4-110">Syntax</span></span>


```C++
HRESULT D3DX11CompileFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataLen,
  _In_        LPCSTR             pFileName,
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



## <a name="parameters"></a><span data-ttu-id="bdcf4-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bdcf4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdcf4-112">*pSrcData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bdcf4-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdcf4-113">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bdcf4-113">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bdcf4-114">Pointeur vers le nuanceur en mémoire.</span><span class="sxs-lookup"><span data-stu-id="bdcf4-114">Pointer to the shader in memory.</span></span>

</dd> <dt>

<span data-ttu-id="bdcf4-115">*SrcDataLen* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bdcf4-115">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdcf4-116">Type : **[ **taille \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bdcf4-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bdcf4-117">Taille du nuanceur en mémoire.</span><span class="sxs-lookup"><span data-stu-id="bdcf4-117">Size of the shader in memory.</span></span>

</dd> <dt>

<span data-ttu-id="bdcf4-118">*pFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bdcf4-118">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdcf4-119">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bdcf4-119">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bdcf4-120">Nom du fichier qui contient le code du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="bdcf4-120">The name of the file that contains the shader code.</span></span>

</dd> <dt>

<span data-ttu-id="bdcf4-121">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bdcf4-121">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdcf4-122">Type : **const [**D3D10 \_ Shader \_ macro**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="bdcf4-122">Type: **const [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="bdcf4-123">facultatif.</span><span class="sxs-lookup"><span data-stu-id="bdcf4-123">Optional.</span></span> <span data-ttu-id="bdcf4-124">Pointeur vers un tableau de définitions de macros (consultez la [**\_ \_ macro de nuanceur D3D10**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="bdcf4-124">Pointer to an array of macro definitions (see [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="bdcf4-125">La dernière structure du tableau sert de terminateur et doit avoir tous les membres définis sur 0.</span><span class="sxs-lookup"><span data-stu-id="bdcf4-125">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="bdcf4-126">S’il n’est pas utilisé, affectez la valeur **null** à *pDefines* .</span><span class="sxs-lookup"><span data-stu-id="bdcf4-126">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bdcf4-127">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bdcf4-127">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdcf4-128">Type : **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="bdcf4-128">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="bdcf4-129">facultatif.</span><span class="sxs-lookup"><span data-stu-id="bdcf4-129">Optional.</span></span> <span data-ttu-id="bdcf4-130">Pointeur vers une interface pour la gestion des fichiers include.</span><span class="sxs-lookup"><span data-stu-id="bdcf4-130">Pointer to an interface for handling include files.</span></span> <span data-ttu-id="bdcf4-131">Si vous affectez la **valeur null** , une erreur de compilation se produira si un nuanceur contient un \# include.</span><span class="sxs-lookup"><span data-stu-id="bdcf4-131">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="bdcf4-132">*pFunctionName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bdcf4-132">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdcf4-133">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bdcf4-133">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bdcf4-134">Nom de la fonction de point d’entrée du nuanceur où commence l’exécution du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="bdcf4-134">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="bdcf4-135">Quand vous compilez un effet, **D3DX11CompileFromMemory** ignore *pFunctionName*; Nous vous recommandons de définir *pFunctionName* sur **null** , car il s’agit d’une bonne pratique de programmation qui consiste à définir un paramètre de pointeur sur la **valeur null** si la fonction appelée ne l’utilise pas.</span><span class="sxs-lookup"><span data-stu-id="bdcf4-135">When you compile an effect, **D3DX11CompileFromMemory** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="bdcf4-136">*pProfile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bdcf4-136">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdcf4-137">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bdcf4-137">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bdcf4-138">Chaîne qui spécifie le modèle de nuanceur ; peut être n’importe quel profil dans le nuancier Model 2, Shader Model 3, Shader Model 4 ou Shader Model 5.</span><span class="sxs-lookup"><span data-stu-id="bdcf4-138">A string that specifies the shader model; can be any profile in shader model 2, shader model 3, shader model 4, or shader model 5.</span></span> <span data-ttu-id="bdcf4-139">Le profil peut également être pour le type d’effet (par exemple, FX \_ 4 \_ 1).</span><span class="sxs-lookup"><span data-stu-id="bdcf4-139">The profile can also be for effect type (for example, fx\_4\_1).</span></span>

</dd> <dt>

<span data-ttu-id="bdcf4-140">*Flags1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bdcf4-140">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdcf4-141">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bdcf4-141">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bdcf4-142">[**Indicateurs de compilation**](/windows/desktop/direct3dhlsl/d3dcompile-constants)du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="bdcf4-142">Shader [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-constants).</span></span>

</dd> <dt>

<span data-ttu-id="bdcf4-143">*Flags2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bdcf4-143">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdcf4-144">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bdcf4-144">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bdcf4-145">[**Indicateurs de compilation**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants)Effect.</span><span class="sxs-lookup"><span data-stu-id="bdcf4-145">Effect [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants).</span></span> <span data-ttu-id="bdcf4-146">Quand vous compilez un nuanceur et non un fichier Effect, **D3DX11CompileFromMemory** ignore *flags2*; Nous vous recommandons de définir *flags2* sur zéro, car il s’agit d’une bonne pratique de programmation qui consiste à définir un paramètre de non-pointeur sur zéro si la fonction appelée ne l’utilise pas.</span><span class="sxs-lookup"><span data-stu-id="bdcf4-146">When you compile a shader and not an effect file, **D3DX11CompileFromMemory** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="bdcf4-147">*pPump* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bdcf4-147">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdcf4-148">Type : **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="bdcf4-148">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="bdcf4-149">Pointeur vers une interface de pompage de thread (voir [**interface ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="bdcf4-149">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="bdcf4-150">Utilisez **null** pour spécifier que cette fonction ne doit pas être retournée tant qu’elle n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="bdcf4-150">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="bdcf4-151">*ppShader* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bdcf4-151">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bdcf4-152">Type : **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="bdcf4-152">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="bdcf4-153">Pointeur vers la mémoire qui contient le nuanceur compilé, ainsi que toutes les informations de débogage et de table de symboles incorporées.</span><span class="sxs-lookup"><span data-stu-id="bdcf4-153">A pointer to memory which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="bdcf4-154">*ppErrorMsgs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bdcf4-154">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bdcf4-155">Type : **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="bdcf4-155">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="bdcf4-156">Pointeur vers la mémoire qui contient une liste d’erreurs et d’avertissements qui se sont produits pendant la compilation.</span><span class="sxs-lookup"><span data-stu-id="bdcf4-156">A pointer to memory which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="bdcf4-157">Ces erreurs et avertissements sont identiques à la sortie de débogage d’un débogueur.</span><span class="sxs-lookup"><span data-stu-id="bdcf4-157">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="bdcf4-158">*pHResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bdcf4-158">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bdcf4-159">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="bdcf4-159">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="bdcf4-160">Pointeur vers la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="bdcf4-160">A pointer to the return value.</span></span> <span data-ttu-id="bdcf4-161">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="bdcf4-161">May be **NULL**.</span></span> <span data-ttu-id="bdcf4-162">Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="bdcf4-162">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdcf4-163">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bdcf4-163">Return value</span></span>

<span data-ttu-id="bdcf4-164">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bdcf4-164">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bdcf4-165">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="bdcf4-165">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

<span data-ttu-id="bdcf4-166">**D3DX11CompileFromMemory** retourne E \_ INVALIDARG si vous fournissez une valeur non **null** au paramètre *PHResult* lorsque vous fournissez la **valeur null** au paramètre *pPump* .</span><span class="sxs-lookup"><span data-stu-id="bdcf4-166">**D3DX11CompileFromMemory** returns E\_INVALIDARG if you supply non-**NULL** to the *pHResult* parameter when you supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="bdcf4-167">Pour plus d’informations sur cette situation, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="bdcf4-167">For more information about this situation, see Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdcf4-168">Notes</span><span class="sxs-lookup"><span data-stu-id="bdcf4-168">Remarks</span></span>

<span data-ttu-id="bdcf4-169">Pour plus d’informations sur **D3DX11CompileFromMemory**, consultez [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span><span class="sxs-lookup"><span data-stu-id="bdcf4-169">For more information about **D3DX11CompileFromMemory**, see [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span></span>

<span data-ttu-id="bdcf4-170">Vous devez fournir la **valeur null** au paramètre *pHResult* si vous fournissez également la **valeur null** au paramètre *pPump* .</span><span class="sxs-lookup"><span data-stu-id="bdcf4-170">You must supply **NULL** to the *pHResult* parameter if you also supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="bdcf4-171">Dans le cas contraire, vous ne pourrez pas créer par la suite un nuanceur à l’aide du code de nuanceur compilé que **D3DX11CompileFromMemory** retourne dans la mémoire vers laquelle pointe le paramètre *ppShader* .</span><span class="sxs-lookup"><span data-stu-id="bdcf4-171">Otherwise, you cannot subsequently create a shader by using the compiled shader code that **D3DX11CompileFromMemory** returns in the memory that the *ppShader* parameter points to.</span></span> <span data-ttu-id="bdcf4-172">Pour créer un nuanceur à partir d’un code de nuanceur conforme, vous appelez l’une des méthodes d’interface [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) suivantes :</span><span class="sxs-lookup"><span data-stu-id="bdcf4-172">To create a shader from complied shader code, you call one of the following [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface methods:</span></span>

-   [<span data-ttu-id="bdcf4-173">**CreateComputeShader**</span><span class="sxs-lookup"><span data-stu-id="bdcf4-173">**CreateComputeShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader)
-   [<span data-ttu-id="bdcf4-174">**CreateDomainShader**</span><span class="sxs-lookup"><span data-stu-id="bdcf4-174">**CreateDomainShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [<span data-ttu-id="bdcf4-175">**CreateGeometryShader**</span><span class="sxs-lookup"><span data-stu-id="bdcf4-175">**CreateGeometryShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [<span data-ttu-id="bdcf4-176">**CreateGeometryShaderWithStreamOutput**</span><span class="sxs-lookup"><span data-stu-id="bdcf4-176">**CreateGeometryShaderWithStreamOutput**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [<span data-ttu-id="bdcf4-177">**CreateHullShader**</span><span class="sxs-lookup"><span data-stu-id="bdcf4-177">**CreateHullShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [<span data-ttu-id="bdcf4-178">**CreatePixelShader**</span><span class="sxs-lookup"><span data-stu-id="bdcf4-178">**CreatePixelShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createpixelshader)
-   [<span data-ttu-id="bdcf4-179">**CreateVertexShader**</span><span class="sxs-lookup"><span data-stu-id="bdcf4-179">**CreateVertexShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

<span data-ttu-id="bdcf4-180">En outre, si vous fournissez une valeur non **null** à *pHResult* lorsque vous fournissez la valeur **null** à *pPump*, **D3DX11CompileFromMemory** retourne le code d’erreur de l’E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="bdcf4-180">In addition, if you supply a non-**NULL** value to *pHResult* when you supply **NULL** to *pPump*, **D3DX11CompileFromMemory** returns the E\_INVALIDARG error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdcf4-181">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bdcf4-181">Requirements</span></span>



| <span data-ttu-id="bdcf4-182">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bdcf4-182">Requirement</span></span> | <span data-ttu-id="bdcf4-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="bdcf4-183">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdcf4-184">En-tête</span><span class="sxs-lookup"><span data-stu-id="bdcf4-184">Header</span></span><br/>  | <dl> <span data-ttu-id="bdcf4-185"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdcf4-185"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="bdcf4-186">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bdcf4-186">Library</span></span><br/> | <dl> <span data-ttu-id="bdcf4-187"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bdcf4-187"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="bdcf4-188">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bdcf4-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdcf4-189">D3DX, fonctions</span><span class="sxs-lookup"><span data-stu-id="bdcf4-189">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

