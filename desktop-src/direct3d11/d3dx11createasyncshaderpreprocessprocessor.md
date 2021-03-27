---
title: D3DX11CreateAsyncShaderPreprocessProcessor, fonction (D3DX11async. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Consultez la section Notes. Créer un processeur de données pour un nuanceur de manière asynchrone.'
ms.assetid: a7e9754b-acc1-49d0-bd8e-b116bc3c7e3a
keywords:
- Fonction D3DX11CreateAsyncShaderPreprocessProcessor Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncShaderPreprocessProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46e58b267f186e5fd0104b10e9f9423f407aaf13
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953932"
---
# <a name="d3dx11createasyncshaderpreprocessprocessor-function"></a><span data-ttu-id="19a6d-106">D3DX11CreateAsyncShaderPreprocessProcessor fonction)</span><span class="sxs-lookup"><span data-stu-id="19a6d-106">D3DX11CreateAsyncShaderPreprocessProcessor function</span></span>

> [!Note]  
> <span data-ttu-id="19a6d-107">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="19a6d-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="19a6d-108">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="19a6d-108">See Remarks.</span></span>

 

<span data-ttu-id="19a6d-109">Créer un processeur de données pour un nuanceur de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="19a6d-109">Create a data processor for a shader asynchronously.</span></span>

## <a name="syntax"></a><span data-ttu-id="19a6d-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19a6d-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncShaderPreprocessProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D11_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _Out_       ID3D10Blob           **ppShaderText,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX11DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="19a6d-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19a6d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19a6d-112">*pFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="19a6d-112">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19a6d-113">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="19a6d-113">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="19a6d-114">Chaîne qui contient le nom de fichier du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="19a6d-114">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="19a6d-115">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="19a6d-115">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19a6d-116">Type : **const d3d11 \_ Shader \_ macro \***</span><span class="sxs-lookup"><span data-stu-id="19a6d-116">Type: **const D3D11\_SHADER\_MACRO\***</span></span>

<span data-ttu-id="19a6d-117">Tableau de macros de nuanceur se terminant par un caractère NULL ; Affectez-lui la valeur **null** pour ne spécifier aucune macro.</span><span class="sxs-lookup"><span data-stu-id="19a6d-117">A NULL-terminated array of shader macros; set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="19a6d-118">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="19a6d-118">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19a6d-119">Type : **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="19a6d-119">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="19a6d-120">Pointeur vers une interface include ; Affectez-lui la valeur **null** pour spécifier qu’il n’y a aucun fichier include.</span><span class="sxs-lookup"><span data-stu-id="19a6d-120">A pointer to an include interface; set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="19a6d-121">*ppShaderText* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="19a6d-121">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19a6d-122">Type : **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="19a6d-122">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="19a6d-123">Adresse d’un pointeur vers une mémoire tampon qui contient le texte ASCII du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="19a6d-123">Address of a pointer to a buffer that contains the ASCII text of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="19a6d-124">*ppErrorBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="19a6d-124">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19a6d-125">Type : **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="19a6d-125">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="19a6d-126">Adresse d’un pointeur vers une mémoire tampon qui contient des erreurs de compilation.</span><span class="sxs-lookup"><span data-stu-id="19a6d-126">Address of a pointer to a buffer that contains compile errors.</span></span>

</dd> <dt>

<span data-ttu-id="19a6d-127">*ppDataProcessor* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="19a6d-127">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19a6d-128">Type : **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="19a6d-128">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span></span>

<span data-ttu-id="19a6d-129">Adresse d’un pointeur vers une mémoire tampon qui contient le processeur de données créé (voir [**interface ID3DX11DataProcessor**](id3dx11dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="19a6d-129">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19a6d-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="19a6d-130">Return value</span></span>

<span data-ttu-id="19a6d-131">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="19a6d-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="19a6d-132">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="19a6d-132">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="19a6d-133">Notes</span><span class="sxs-lookup"><span data-stu-id="19a6d-133">Remarks</span></span>

<span data-ttu-id="19a6d-134">Il n’y a aucune implémentation du chargeur asynchrone en dehors de D3DX 10 et D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="19a6d-134">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="19a6d-135">Pour les applications du Windows Store, les exemples DirectX (par exemple, l' [exemple de didacticiel Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) incluent le module **BasicLoader** qui utilise le modèle de programmation asynchrone Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="19a6d-135">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="19a6d-136">Pour les applications de bureau Win32, vous pouvez utiliser le [Runtime d’accès concurrentiel](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) pour implémenter un modèle semblable au Windows Runtime modèle de programmation asynchrone.</span><span class="sxs-lookup"><span data-stu-id="19a6d-136">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="19a6d-137">Spécifications</span><span class="sxs-lookup"><span data-stu-id="19a6d-137">Requirements</span></span>



| <span data-ttu-id="19a6d-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19a6d-138">Requirement</span></span> | <span data-ttu-id="19a6d-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="19a6d-139">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="19a6d-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="19a6d-140">Header</span></span><br/>  | <dl> <span data-ttu-id="19a6d-141"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="19a6d-141"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="19a6d-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="19a6d-142">Library</span></span><br/> | <dl> <span data-ttu-id="19a6d-143"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19a6d-143"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="19a6d-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19a6d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19a6d-145">D3DX, fonctions</span><span class="sxs-lookup"><span data-stu-id="19a6d-145">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

