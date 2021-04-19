---
description: Notez qu’au lieu d’utiliser cette fonction héritée, nous vous recommandons de compiler hors connexion à l’aide du compilateur de ligne de commande Fxc.exe ou d’utiliser l’API D3DCompile. Compilez un nuanceur ou un effet à partir d’un fichier.
ms.assetid: b0ca0b6a-3ff0-49ee-83de-14c4686a7104
title: D3DX10CompileFromFile, fonction (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CompileFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 571f8123a9834c95ecca6043c3495fb18fbaca47
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539168"
---
# <a name="d3dx10compilefromfile-function"></a><span data-ttu-id="546d6-104">D3DX10CompileFromFile fonction)</span><span class="sxs-lookup"><span data-stu-id="546d6-104">D3DX10CompileFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="546d6-105">Au lieu d’utiliser cette fonction héritée, nous vous recommandons de compiler hors connexion à l’aide du compilateur de ligne de commande Fxc.exe ou d’utiliser l’API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="546d6-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

<span data-ttu-id="546d6-106">Compilez un nuanceur ou un effet à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="546d6-106">Compile a shader or an effect from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="546d6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="546d6-107">Syntax</span></span>


```C++
HRESULT D3DX10CompileFromFile(
  _In_        LPCTSTR            pSrcFile,
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



## <a name="parameters"></a><span data-ttu-id="546d6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="546d6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="546d6-109">*pSrcFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="546d6-109">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="546d6-110">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="546d6-110">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="546d6-111">Nom du fichier qui contient le code du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="546d6-111">The name of the file that contains the shader code.</span></span> <span data-ttu-id="546d6-112">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="546d6-112">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="546d6-113">Dans le cas contraire, le type de données est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="546d6-113">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="546d6-114">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="546d6-114">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="546d6-115">Type : **\* macro de [**\_ nuanceur \_ D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) const**</span><span class="sxs-lookup"><span data-stu-id="546d6-115">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="546d6-116">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="546d6-116">Optional.</span></span> <span data-ttu-id="546d6-117">Pointeur vers un tableau de définitions de macros (consultez la [**\_ \_ macro de nuanceur D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="546d6-117">Pointer to an array of macro definitions (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="546d6-118">La dernière structure du tableau sert de terminateur et doit avoir tous les membres définis sur 0.</span><span class="sxs-lookup"><span data-stu-id="546d6-118">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="546d6-119">S’il n’est pas utilisé, affectez la valeur **null** à *pDefines* .</span><span class="sxs-lookup"><span data-stu-id="546d6-119">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="546d6-120">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="546d6-120">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="546d6-121">Type : **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="546d6-121">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="546d6-122">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="546d6-122">Optional.</span></span> <span data-ttu-id="546d6-123">Pointeur vers une interface d' [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) pour la gestion des fichiers include.</span><span class="sxs-lookup"><span data-stu-id="546d6-123">Pointer to an [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) interface for handling include files.</span></span> <span data-ttu-id="546d6-124">Si vous affectez la **valeur null** , une erreur de compilation se produira si un nuanceur contient un \# include.</span><span class="sxs-lookup"><span data-stu-id="546d6-124">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="546d6-125">*pFunctionName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="546d6-125">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="546d6-126">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="546d6-126">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="546d6-127">Nom de la fonction de point d’entrée du nuanceur où commence l’exécution du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="546d6-127">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="546d6-128">Quand vous compilez un effet, **D3DX10CompileFromFile** ignore *pFunctionName*; Nous vous recommandons de définir *pFunctionName* sur **null** , car il s’agit d’une bonne pratique de programmation qui consiste à définir un paramètre de pointeur sur la **valeur null** si la fonction appelée ne l’utilise pas.</span><span class="sxs-lookup"><span data-stu-id="546d6-128">When you compile an effect, **D3DX10CompileFromFile** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="546d6-129">*pProfile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="546d6-129">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="546d6-130">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="546d6-130">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="546d6-131">Chaîne qui spécifie le modèle de nuanceur ; peut être n’importe quel profil dans le [Shader Model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [Shader Model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md)ou [Shader Model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span><span class="sxs-lookup"><span data-stu-id="546d6-131">A string that specifies the shader model; can be any profile in [shader model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [shader model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md), or [shader model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span></span>

</dd> <dt>

<span data-ttu-id="546d6-132">*Flags1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="546d6-132">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="546d6-133">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="546d6-133">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="546d6-134">[Indicateurs de compilation du nuanceur](d3d10-shader.md).</span><span class="sxs-lookup"><span data-stu-id="546d6-134">[Shader compile flags](d3d10-shader.md).</span></span>

</dd> <dt>

<span data-ttu-id="546d6-135">*Flags2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="546d6-135">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="546d6-136">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="546d6-136">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="546d6-137">[Indicateurs de compilation Effect](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="546d6-137">[Effect compile flags](d3d10-graphics-reference-effect-constants.md).</span></span> <span data-ttu-id="546d6-138">Quand vous compilez un nuanceur et non un fichier Effect, **D3DX10CompileFromFile** ignore *flags2*; Nous vous recommandons de définir *flags2* sur zéro, car il s’agit d’une bonne pratique de programmation qui consiste à définir un paramètre de non-pointeur sur zéro si la fonction appelée ne l’utilise pas.</span><span class="sxs-lookup"><span data-stu-id="546d6-138">When you compile a shader and not an effect file, **D3DX10CompileFromFile** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="546d6-139">*pPump* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="546d6-139">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="546d6-140">Type : **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="546d6-140">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="546d6-141">Pointeur vers une interface de pompage de thread (voir [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="546d6-141">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="546d6-142">Utilisez **null** pour spécifier que cette fonction ne doit pas être retournée tant qu’elle n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="546d6-142">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="546d6-143">*ppShader* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="546d6-143">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="546d6-144">Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="546d6-144">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="546d6-145">Pointeur vers une [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) qui contient le nuanceur compilé, ainsi que toutes les informations de débogage et de table de symboles incorporées.</span><span class="sxs-lookup"><span data-stu-id="546d6-145">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="546d6-146">*ppErrorMsgs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="546d6-146">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="546d6-147">Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="546d6-147">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="546d6-148">Pointeur vers une [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) qui contient une liste d’erreurs et d’avertissements qui se sont produits pendant la compilation.</span><span class="sxs-lookup"><span data-stu-id="546d6-148">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="546d6-149">Ces erreurs et avertissements sont identiques à la sortie de débogage d’un débogueur.</span><span class="sxs-lookup"><span data-stu-id="546d6-149">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="546d6-150">*pHResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="546d6-150">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="546d6-151">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="546d6-151">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="546d6-152">Pointeur vers la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="546d6-152">A pointer to the return value.</span></span> <span data-ttu-id="546d6-153">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="546d6-153">May be **NULL**.</span></span> <span data-ttu-id="546d6-154">Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="546d6-154">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="546d6-155">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="546d6-155">Return value</span></span>

<span data-ttu-id="546d6-156">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="546d6-156">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="546d6-157">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="546d6-157">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="546d6-158">Notes</span><span class="sxs-lookup"><span data-stu-id="546d6-158">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="546d6-159">Spécifications</span><span class="sxs-lookup"><span data-stu-id="546d6-159">Requirements</span></span>



| <span data-ttu-id="546d6-160">Condition requise</span><span class="sxs-lookup"><span data-stu-id="546d6-160">Requirement</span></span> | <span data-ttu-id="546d6-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="546d6-161">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="546d6-162">En-tête</span><span class="sxs-lookup"><span data-stu-id="546d6-162">Header</span></span><br/> | <dl> <span data-ttu-id="546d6-163"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="546d6-163"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="546d6-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="546d6-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="546d6-165">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="546d6-165">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
