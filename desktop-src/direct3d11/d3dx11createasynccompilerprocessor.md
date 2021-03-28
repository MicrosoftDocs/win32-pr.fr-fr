---
title: D3DX11CreateAsyncCompilerProcessor, fonction (D3DX11async. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Consultez la section Notes. Créer un processeur de données asynchrones pour un nuanceur.'
ms.assetid: 90756ac3-946d-49fa-9f97-70dc5da812c6
keywords:
- Fonction D3DX11CreateAsyncCompilerProcessor Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncCompilerProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 533e487e65640b8c17a0ff8d061388e8b5a6c0f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992305"
---
# <a name="d3dx11createasynccompilerprocessor-function"></a><span data-ttu-id="c870b-106">D3DX11CreateAsyncCompilerProcessor fonction)</span><span class="sxs-lookup"><span data-stu-id="c870b-106">D3DX11CreateAsyncCompilerProcessor function</span></span>

> [!Note]  
> <span data-ttu-id="c870b-107">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="c870b-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="c870b-108">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="c870b-108">See Remarks.</span></span>

 

<span data-ttu-id="c870b-109">Créer un processeur de données asynchrones pour un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="c870b-109">Create an asynchronous-data processor for a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="c870b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c870b-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D11_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pFunctionName,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags1,
  _In_        UINT                 Flags2,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX11DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="c870b-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c870b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c870b-112">*pFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c870b-112">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c870b-113">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c870b-113">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c870b-114">Chaîne qui contient le nom de fichier du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="c870b-114">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="c870b-115">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c870b-115">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c870b-116">Type : **const d3d11 \_ Shader \_ macro \***</span><span class="sxs-lookup"><span data-stu-id="c870b-116">Type: **const D3D11\_SHADER\_MACRO\***</span></span>

<span data-ttu-id="c870b-117">Tableau de macros de nuanceur se terminant par un caractère NULL ; Affectez-lui la valeur **null** pour ne spécifier aucune macro.</span><span class="sxs-lookup"><span data-stu-id="c870b-117">A NULL-terminated array of shader macros; set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="c870b-118">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c870b-118">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c870b-119">Type : **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="c870b-119">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="c870b-120">Pointeur vers une interface include.</span><span class="sxs-lookup"><span data-stu-id="c870b-120">A pointer to an include interface.</span></span> <span data-ttu-id="c870b-121">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c870b-121">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c870b-122">*pFunctionName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c870b-122">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c870b-123">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c870b-123">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c870b-124">Nom de la fonction de point d’entrée du nuanceur où commence l’exécution du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="c870b-124">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="c870b-125">Quand vous compilez un effet, **D3DX11CreateAsyncCompilerProcessor** ignore *pFunctionName*; Nous vous recommandons de définir *pFunctionName* sur **null** , car il s’agit d’une bonne pratique de programmation qui consiste à définir un paramètre de pointeur sur la **valeur null** si la fonction appelée ne l’utilise pas..</span><span class="sxs-lookup"><span data-stu-id="c870b-125">When you compile an effect, **D3DX11CreateAsyncCompilerProcessor** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it..</span></span>

</dd> <dt>

<span data-ttu-id="c870b-126">*pProfile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c870b-126">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c870b-127">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c870b-127">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c870b-128">Chaîne qui spécifie le profil de nuanceur ou le modèle de nuanceur ; peut être n’importe quel profil dans le nuancier Model 2, Shader Model 3, Shader Model 4 ou Shader Model 5.</span><span class="sxs-lookup"><span data-stu-id="c870b-128">A string that specifies the shader profile or shader model; can be any profile in shader model 2, shader model 3, shader model 4, or shader model 5.</span></span> <span data-ttu-id="c870b-129">Le profil peut également être pour le type d’effet (par exemple, FX \_ 4 \_ 1).</span><span class="sxs-lookup"><span data-stu-id="c870b-129">The profile can also be for effect type (for example, fx\_4\_1).</span></span>

</dd> <dt>

<span data-ttu-id="c870b-130">*Flags1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c870b-130">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c870b-131">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c870b-131">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c870b-132">Indicateurs de compilation du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="c870b-132">Shader compile flags.</span></span>

</dd> <dt>

<span data-ttu-id="c870b-133">*Flags2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c870b-133">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c870b-134">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c870b-134">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c870b-135">Indicateurs de compilation Effect.</span><span class="sxs-lookup"><span data-stu-id="c870b-135">Effect compile flags.</span></span> <span data-ttu-id="c870b-136">Quand vous compilez un nuanceur et non un fichier Effect, **D3DX11CreateAsyncCompilerProcessor** ignore *flags2*; Nous vous recommandons de définir *flags2* sur zéro, car il s’agit d’une bonne pratique de programmation qui consiste à définir un paramètre de non-pointeur sur zéro si la fonction appelée ne l’utilise pas.</span><span class="sxs-lookup"><span data-stu-id="c870b-136">When you compile a shader and not an effect file, **D3DX11CreateAsyncCompilerProcessor** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="c870b-137">*ppCompiledShader* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c870b-137">*ppCompiledShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c870b-138">Type : **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="c870b-138">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="c870b-139">Adresse d’un pointeur vers l’effet compilé.</span><span class="sxs-lookup"><span data-stu-id="c870b-139">Address of a pointer to the compiled effect.</span></span>

</dd> <dt>

<span data-ttu-id="c870b-140">*ppErrorBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c870b-140">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c870b-141">Type : **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="c870b-141">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="c870b-142">Adresse d’un pointeur vers des erreurs de compilation.</span><span class="sxs-lookup"><span data-stu-id="c870b-142">Address of a pointer to compile errors.</span></span>

</dd> <dt>

<span data-ttu-id="c870b-143">*ppDataProcessor* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c870b-143">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c870b-144">Type : **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="c870b-144">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span></span>

<span data-ttu-id="c870b-145">Adresse d’un pointeur vers une mémoire tampon qui contient le processeur de données créé (voir [**interface ID3DX11DataProcessor**](id3dx11dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="c870b-145">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c870b-146">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c870b-146">Return value</span></span>

<span data-ttu-id="c870b-147">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c870b-147">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c870b-148">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c870b-148">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c870b-149">Notes</span><span class="sxs-lookup"><span data-stu-id="c870b-149">Remarks</span></span>

<span data-ttu-id="c870b-150">Il n’y a aucune implémentation du chargeur asynchrone en dehors de D3DX 10 et D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="c870b-150">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="c870b-151">Pour les applications du Windows Store, les exemples DirectX (par exemple, l' [exemple de didacticiel Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) incluent le module **BasicLoader** qui utilise le modèle de programmation asynchrone Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="c870b-151">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="c870b-152">Pour les applications de bureau Win32, vous pouvez utiliser le [Runtime d’accès concurrentiel](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) pour implémenter un modèle semblable au Windows Runtime modèle de programmation asynchrone.</span><span class="sxs-lookup"><span data-stu-id="c870b-152">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="c870b-153">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c870b-153">Requirements</span></span>



| <span data-ttu-id="c870b-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c870b-154">Requirement</span></span> | <span data-ttu-id="c870b-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="c870b-155">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c870b-156">En-tête</span><span class="sxs-lookup"><span data-stu-id="c870b-156">Header</span></span><br/>  | <dl> <span data-ttu-id="c870b-157"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="c870b-157"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="c870b-158">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c870b-158">Library</span></span><br/> | <dl> <span data-ttu-id="c870b-159"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c870b-159"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="c870b-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c870b-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c870b-161">D3DX, fonctions</span><span class="sxs-lookup"><span data-stu-id="c870b-161">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

