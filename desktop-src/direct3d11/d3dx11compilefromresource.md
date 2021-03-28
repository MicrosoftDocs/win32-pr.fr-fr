---
title: D3DX11CompileFromResource, fonction (D3DX11async. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Notez qu’au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser des fonctions de ressource, puis de compiler hors connexion à l’aide du compilateur de ligne de commande Fxc.exe ou d’utiliser l’une des API de compilation HLSL, comme l’API D3DCompile. Compilez un nuanceur ou un effet à partir d’une ressource.'
ms.assetid: ececa469-f5e3-4cb3-befe-0ed1a5a57671
keywords:
- Fonction D3DX11CompileFromResource Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CompileFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b26eeb825a1d3b6bcda9f77eae24c99c3cec168b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953934"
---
# <a name="d3dx11compilefromresource-function"></a><span data-ttu-id="402c8-106">D3DX11CompileFromResource fonction)</span><span class="sxs-lookup"><span data-stu-id="402c8-106">D3DX11CompileFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="402c8-107">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="402c8-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="402c8-108">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser des [fonctions de ressource](/windows/desktop/menurc/resources-functions), puis de compiler hors connexion à l’aide du compilateur de ligne de commande Fxc.exe ou d’utiliser l’une des API de compilation HLSL, comme l’API [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="402c8-108">Instead of using this function, we recommend that you use [resource functions](/windows/desktop/menurc/resources-functions), then compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) API.</span></span>

 

<span data-ttu-id="402c8-109">Compilez un nuanceur ou un effet à partir d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="402c8-109">Compile a shader or an effect from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="402c8-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="402c8-110">Syntax</span></span>


```C++
HRESULT D3DX11CompileFromResource(
  _In_        HMODULE            hSrcModule,
  _In_        LPCTSTR            pSrcResource,
  _In_        LPCTSTR            pSrcFileName,
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



## <a name="parameters"></a><span data-ttu-id="402c8-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="402c8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="402c8-112">*hSrcModule* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="402c8-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="402c8-113">Type : **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="402c8-113">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="402c8-114">Handle du module de ressource contenant le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="402c8-114">Handle to the resource module containing the shader.</span></span> <span data-ttu-id="402c8-115">HMODULE peut être obtenu avec la [fonction GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="402c8-115">HMODULE can be obtained with [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="402c8-116">*pSrcResource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="402c8-116">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="402c8-117">Type : **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="402c8-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="402c8-118">Nom de la ressource contenant le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="402c8-118">Name of the resource containing the shader.</span></span> <span data-ttu-id="402c8-119">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="402c8-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="402c8-120">Dans le cas contraire, le type de données est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="402c8-120">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="402c8-121">*pSrcFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="402c8-121">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="402c8-122">Type : **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="402c8-122">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="402c8-123">facultatif.</span><span class="sxs-lookup"><span data-stu-id="402c8-123">Optional.</span></span> <span data-ttu-id="402c8-124">Nom du fichier d’effet, qui est utilisé pour les messages d’erreur uniquement.</span><span class="sxs-lookup"><span data-stu-id="402c8-124">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="402c8-125">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="402c8-125">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="402c8-126">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="402c8-126">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="402c8-127">Type : **const [**D3D10 \_ Shader \_ macro**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="402c8-127">Type: **const [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="402c8-128">facultatif.</span><span class="sxs-lookup"><span data-stu-id="402c8-128">Optional.</span></span> <span data-ttu-id="402c8-129">Pointeur vers un tableau de définitions de macros (consultez la [**\_ \_ macro de nuanceur D3D10**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="402c8-129">Pointer to an array of macro definitions (see [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="402c8-130">La dernière structure du tableau sert de terminateur et doit avoir tous les membres définis sur 0.</span><span class="sxs-lookup"><span data-stu-id="402c8-130">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="402c8-131">S’il n’est pas utilisé, affectez la valeur **null** à *pDefines* .</span><span class="sxs-lookup"><span data-stu-id="402c8-131">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="402c8-132">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="402c8-132">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="402c8-133">Type : **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="402c8-133">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="402c8-134">facultatif.</span><span class="sxs-lookup"><span data-stu-id="402c8-134">Optional.</span></span> <span data-ttu-id="402c8-135">Pointeur vers une interface pour la gestion des fichiers include.</span><span class="sxs-lookup"><span data-stu-id="402c8-135">Pointer to an interface for handling include files.</span></span> <span data-ttu-id="402c8-136">Si vous affectez la **valeur null** , une erreur de compilation se produira si un nuanceur contient un \# include.</span><span class="sxs-lookup"><span data-stu-id="402c8-136">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="402c8-137">*pFunctionName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="402c8-137">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="402c8-138">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="402c8-138">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="402c8-139">Nom de la fonction de point d’entrée du nuanceur où commence l’exécution du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="402c8-139">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="402c8-140">Quand vous compilez un effet, **D3DX11CompileFromResource** ignore *pFunctionName*; Nous vous recommandons de définir *pFunctionName* sur **null** , car il s’agit d’une bonne pratique de programmation qui consiste à définir un paramètre de pointeur sur la **valeur null** si la fonction appelée ne l’utilise pas.</span><span class="sxs-lookup"><span data-stu-id="402c8-140">When you compile an effect, **D3DX11CompileFromResource** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="402c8-141">*pProfile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="402c8-141">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="402c8-142">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="402c8-142">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="402c8-143">Chaîne qui spécifie le modèle de nuanceur ; peut être n’importe quel profil dans le nuancier Model 2, Shader Model 3, Shader Model 4 ou Shader Model 5.</span><span class="sxs-lookup"><span data-stu-id="402c8-143">A string that specifies the shader model; can be any profile in shader model 2, shader model 3, shader model 4, or shader model 5.</span></span> <span data-ttu-id="402c8-144">Le profil peut également être pour le type d’effet (par exemple, FX \_ 4 \_ 1).</span><span class="sxs-lookup"><span data-stu-id="402c8-144">The profile can also be for effect type (for example, fx\_4\_1).</span></span>

</dd> <dt>

<span data-ttu-id="402c8-145">*Flags1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="402c8-145">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="402c8-146">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="402c8-146">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="402c8-147">[**Indicateurs de compilation**](/windows/desktop/direct3dhlsl/d3dcompile-constants)du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="402c8-147">Shader [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-constants).</span></span>

</dd> <dt>

<span data-ttu-id="402c8-148">*Flags2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="402c8-148">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="402c8-149">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="402c8-149">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="402c8-150">[**Indicateurs de compilation**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants)Effect.</span><span class="sxs-lookup"><span data-stu-id="402c8-150">Effect [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants).</span></span> <span data-ttu-id="402c8-151">Quand vous compilez un nuanceur et non un fichier Effect, **D3DX11CompileFromResource** ignore *flags2*; Nous vous recommandons de définir *flags2* sur zéro, car il s’agit d’une bonne pratique de programmation qui consiste à définir un paramètre de non-pointeur sur zéro si la fonction appelée ne l’utilise pas.</span><span class="sxs-lookup"><span data-stu-id="402c8-151">When you compile a shader and not an effect file, **D3DX11CompileFromResource** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="402c8-152">*pPump* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="402c8-152">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="402c8-153">Type : **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="402c8-153">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="402c8-154">Pointeur vers une interface de pompage de thread (voir [**interface ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="402c8-154">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="402c8-155">Utilisez **null** pour spécifier que cette fonction ne doit pas être retournée tant qu’elle n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="402c8-155">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="402c8-156">*ppShader* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="402c8-156">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="402c8-157">Type : **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="402c8-157">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="402c8-158">Pointeur vers la mémoire qui contient le nuanceur compilé, ainsi que toutes les informations de débogage et de table de symboles incorporées.</span><span class="sxs-lookup"><span data-stu-id="402c8-158">A pointer to memory which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="402c8-159">*ppErrorMsgs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="402c8-159">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="402c8-160">Type : **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="402c8-160">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="402c8-161">Pointeur vers la mémoire qui contient une liste d’erreurs et d’avertissements qui se sont produits pendant la compilation.</span><span class="sxs-lookup"><span data-stu-id="402c8-161">A pointer to memory which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="402c8-162">Ces erreurs et avertissements sont identiques à la sortie de débogage d’un débogueur.</span><span class="sxs-lookup"><span data-stu-id="402c8-162">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="402c8-163">*pHResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="402c8-163">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="402c8-164">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="402c8-164">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="402c8-165">Pointeur vers la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="402c8-165">A pointer to the return value.</span></span> <span data-ttu-id="402c8-166">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="402c8-166">May be **NULL**.</span></span> <span data-ttu-id="402c8-167">Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="402c8-167">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="402c8-168">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="402c8-168">Return value</span></span>

<span data-ttu-id="402c8-169">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="402c8-169">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="402c8-170">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="402c8-170">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

<span data-ttu-id="402c8-171">**D3DX11CompileFromResource** retourne E \_ INVALIDARG si vous fournissez une valeur non **null** au paramètre *PHResult* lorsque vous fournissez la **valeur null** au paramètre *pPump* .</span><span class="sxs-lookup"><span data-stu-id="402c8-171">**D3DX11CompileFromResource** returns E\_INVALIDARG if you supply non-**NULL** to the *pHResult* parameter when you supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="402c8-172">Pour plus d’informations sur cette situation, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="402c8-172">For more information about this situation, see Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="402c8-173">Notes</span><span class="sxs-lookup"><span data-stu-id="402c8-173">Remarks</span></span>

<span data-ttu-id="402c8-174">Pour plus d’informations sur **D3DX11CompileFromResource**, consultez [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span><span class="sxs-lookup"><span data-stu-id="402c8-174">For more information about **D3DX11CompileFromResource**, see [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span></span>

<span data-ttu-id="402c8-175">Vous devez fournir la **valeur null** au paramètre *pHResult* si vous fournissez également la **valeur null** au paramètre *pPump* .</span><span class="sxs-lookup"><span data-stu-id="402c8-175">You must supply **NULL** to the *pHResult* parameter if you also supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="402c8-176">Dans le cas contraire, vous ne pourrez pas créer par la suite un nuanceur à l’aide du code de nuanceur compilé que **D3DX11CompileFromResource** retourne dans la mémoire vers laquelle pointe le paramètre *ppShader* .</span><span class="sxs-lookup"><span data-stu-id="402c8-176">Otherwise, you cannot subsequently create a shader by using the compiled shader code that **D3DX11CompileFromResource** returns in the memory that the *ppShader* parameter points to.</span></span> <span data-ttu-id="402c8-177">Pour créer un nuanceur à partir d’un code de nuanceur conforme, vous appelez l’une des méthodes d’interface [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) suivantes :</span><span class="sxs-lookup"><span data-stu-id="402c8-177">To create a shader from complied shader code, you call one of the following [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface methods:</span></span>

-   [<span data-ttu-id="402c8-178">**CreateComputeShader**</span><span class="sxs-lookup"><span data-stu-id="402c8-178">**CreateComputeShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader)
-   [<span data-ttu-id="402c8-179">**CreateDomainShader**</span><span class="sxs-lookup"><span data-stu-id="402c8-179">**CreateDomainShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [<span data-ttu-id="402c8-180">**CreateGeometryShader**</span><span class="sxs-lookup"><span data-stu-id="402c8-180">**CreateGeometryShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [<span data-ttu-id="402c8-181">**CreateGeometryShaderWithStreamOutput**</span><span class="sxs-lookup"><span data-stu-id="402c8-181">**CreateGeometryShaderWithStreamOutput**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [<span data-ttu-id="402c8-182">**CreateHullShader**</span><span class="sxs-lookup"><span data-stu-id="402c8-182">**CreateHullShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [<span data-ttu-id="402c8-183">**CreatePixelShader**</span><span class="sxs-lookup"><span data-stu-id="402c8-183">**CreatePixelShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createpixelshader)
-   [<span data-ttu-id="402c8-184">**CreateVertexShader**</span><span class="sxs-lookup"><span data-stu-id="402c8-184">**CreateVertexShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

<span data-ttu-id="402c8-185">En outre, si vous fournissez une valeur non **null** à *pHResult* lorsque vous fournissez la valeur **null** à *pPump*, **D3DX11CompileFromResource** retourne le code d’erreur de l’E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="402c8-185">In addition, if you supply a non-**NULL** value to *pHResult* when you supply **NULL** to *pPump*, **D3DX11CompileFromResource** returns the E\_INVALIDARG error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="402c8-186">Spécifications</span><span class="sxs-lookup"><span data-stu-id="402c8-186">Requirements</span></span>



| <span data-ttu-id="402c8-187">Condition requise</span><span class="sxs-lookup"><span data-stu-id="402c8-187">Requirement</span></span> | <span data-ttu-id="402c8-188">Valeur</span><span class="sxs-lookup"><span data-stu-id="402c8-188">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="402c8-189">En-tête</span><span class="sxs-lookup"><span data-stu-id="402c8-189">Header</span></span><br/>  | <dl> <span data-ttu-id="402c8-190"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="402c8-190"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="402c8-191">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="402c8-191">Library</span></span><br/> | <dl> <span data-ttu-id="402c8-192"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="402c8-192"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="402c8-193">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="402c8-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="402c8-194">D3DX, fonctions</span><span class="sxs-lookup"><span data-stu-id="402c8-194">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

