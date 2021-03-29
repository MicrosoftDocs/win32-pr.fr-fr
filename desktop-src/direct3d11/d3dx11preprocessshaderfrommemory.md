---
title: D3DX11PreprocessShaderFromMemory, fonction (D3DX11async. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Notez qu’au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser l’API D3DPreprocess. Créer un nuanceur à partir de la mémoire sans le compiler.'
ms.assetid: 3c646914-9334-44fe-a8a0-b84d0dc1a16e
keywords:
- Fonction D3DX11PreprocessShaderFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11PreprocessShaderFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71a94633270fe0f4e462e60915de862be8693daa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992265"
---
# <a name="d3dx11preprocessshaderfrommemory-function"></a><span data-ttu-id="4c811-106">D3DX11PreprocessShaderFromMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="4c811-106">D3DX11PreprocessShaderFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="4c811-107">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c811-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="4c811-108">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser l’API [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="4c811-108">Instead of using this function, we recommend that you use the [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) API.</span></span>

 

<span data-ttu-id="4c811-109">Créer un nuanceur à partir de la mémoire sans le compiler.</span><span class="sxs-lookup"><span data-stu-id="4c811-109">Create a shader from memory without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c811-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4c811-110">Syntax</span></span>


```C++
HRESULT D3DX11PreprocessShaderFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataSize,
  _In_        LPCSTR             pFileName,
  _In_  const D3D11_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="4c811-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4c811-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c811-112">*pSrcData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4c811-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c811-113">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4c811-113">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4c811-114">Pointeur vers la mémoire qui contient le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="4c811-114">Pointer to the memory containing the shader.</span></span>

</dd> <dt>

<span data-ttu-id="4c811-115">*SrcDataSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4c811-115">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c811-116">Type : **[ **taille \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4c811-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4c811-117">Taille du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="4c811-117">Size of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="4c811-118">*pFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4c811-118">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c811-119">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4c811-119">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4c811-120">Nom du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="4c811-120">Name of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="4c811-121">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4c811-121">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c811-122">Type : **const d3d11 \_ Shader \_ macro \***</span><span class="sxs-lookup"><span data-stu-id="4c811-122">Type: **const D3D11\_SHADER\_MACRO\***</span></span>

<span data-ttu-id="4c811-123">Tableau de macros de nuanceur se terminant par un caractère NULL ; Affectez-lui la valeur **null** pour ne spécifier aucune macro.</span><span class="sxs-lookup"><span data-stu-id="4c811-123">A NULL-terminated array of shader macros; set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="4c811-124">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4c811-124">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c811-125">Type : **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="4c811-125">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="4c811-126">Pointeur vers une interface include ; Affectez-lui la valeur **null** pour spécifier qu’il n’y a aucun fichier include.</span><span class="sxs-lookup"><span data-stu-id="4c811-126">A pointer to an include interface; set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="4c811-127">*pPump* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4c811-127">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c811-128">Type : **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="4c811-128">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="4c811-129">Pointeur vers une interface de pompage de thread (voir [**interface ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="4c811-129">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="4c811-130">Utilisez **null** pour spécifier que cette fonction ne doit pas être retournée tant qu’elle n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="4c811-130">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="4c811-131">*ppShaderText* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4c811-131">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c811-132">Type : **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="4c811-132">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="4c811-133">Pointeur vers la mémoire qui contient le nuanceur non compilé.</span><span class="sxs-lookup"><span data-stu-id="4c811-133">A pointer to memory that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="4c811-134">*ppErrorMsgs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4c811-134">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c811-135">Type : **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="4c811-135">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="4c811-136">Adresse d’un pointeur vers la mémoire qui contient des erreurs de création d’effet, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="4c811-136">The address of a pointer to memory that contains effect-creation errors, if any occurred.</span></span>

</dd> <dt>

<span data-ttu-id="4c811-137">*pHResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4c811-137">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c811-138">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="4c811-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="4c811-139">Pointeur vers la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="4c811-139">A pointer to the return value.</span></span> <span data-ttu-id="4c811-140">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="4c811-140">May be **NULL**.</span></span> <span data-ttu-id="4c811-141">Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="4c811-141">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c811-142">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4c811-142">Return value</span></span>

<span data-ttu-id="4c811-143">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4c811-143">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4c811-144">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="4c811-144">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c811-145">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4c811-145">Requirements</span></span>



| <span data-ttu-id="4c811-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4c811-146">Requirement</span></span> | <span data-ttu-id="4c811-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c811-147">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c811-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="4c811-148">Header</span></span><br/>  | <dl> <span data-ttu-id="4c811-149"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c811-149"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="4c811-150">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4c811-150">Library</span></span><br/> | <dl> <span data-ttu-id="4c811-151"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c811-151"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="4c811-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c811-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c811-153">D3DX, fonctions</span><span class="sxs-lookup"><span data-stu-id="4c811-153">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

