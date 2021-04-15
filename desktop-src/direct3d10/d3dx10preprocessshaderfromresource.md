---
description: Notez qu’au lieu d’utiliser cette fonction héritée, nous vous recommandons d’utiliser l’API D3DPreprocess. Créez un nuanceur à partir d’une ressource sans le compiler.
ms.assetid: ca93e208-7627-4bf5-ab83-d4e906e149eb
title: D3DX10PreprocessShaderFromResource, fonction (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10PreprocessShaderFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 81a9f272cb0769d4313a4375f98bdc25b9e403e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394271"
---
# <a name="d3dx10preprocessshaderfromresource-function"></a><span data-ttu-id="15990-104">D3DX10PreprocessShaderFromResource fonction)</span><span class="sxs-lookup"><span data-stu-id="15990-104">D3DX10PreprocessShaderFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="15990-105">Au lieu d’utiliser cette fonction héritée, nous vous recommandons d’utiliser l’API [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="15990-105">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

<span data-ttu-id="15990-106">Créez un nuanceur à partir d’une ressource sans le compiler.</span><span class="sxs-lookup"><span data-stu-id="15990-106">Create a shader from a resource without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="15990-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15990-107">Syntax</span></span>


```C++
HRESULT D3DX10PreprocessShaderFromResource(
  _In_        HMODULE            hModule,
  _In_        LPCTSTR            pResourceName,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="15990-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="15990-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15990-109">*HMODULE* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="15990-109">*hModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15990-110">Type : **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="15990-110">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="15990-111">Handle du module de ressource contenant le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="15990-111">Handle to the resource module containing the shader.</span></span> <span data-ttu-id="15990-112">HMODULE peut être obtenu avec la [fonction GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="15990-112">HMODULE can be obtained with [GetModuleHandle Function](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="15990-113">*pResourceName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="15990-113">*pResourceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15990-114">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="15990-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="15990-115">Nom de la ressource côté hModule contenant le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="15990-115">The name of the resource in side hModule containing the shader.</span></span> <span data-ttu-id="15990-116">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="15990-116">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="15990-117">Dans le cas contraire, le type de données est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="15990-117">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="15990-118">*pSrcFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="15990-118">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15990-119">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="15990-119">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="15990-120">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="15990-120">Optional.</span></span> <span data-ttu-id="15990-121">Nom du fichier d’effet, qui est utilisé pour les messages d’erreur uniquement.</span><span class="sxs-lookup"><span data-stu-id="15990-121">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="15990-122">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="15990-122">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="15990-123">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="15990-123">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15990-124">Type : **\* macro de [**\_ nuanceur \_ D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) const**</span><span class="sxs-lookup"><span data-stu-id="15990-124">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="15990-125">Tableau de macros de nuanceur se terminant par un caractère NULL (consultez la [**\_ \_ macro de nuanceur D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); définissez cette valeur sur **null** pour ne spécifier aucune macro.</span><span class="sxs-lookup"><span data-stu-id="15990-125">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="15990-126">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="15990-126">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15990-127">Type : **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="15990-127">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="15990-128">Pointeur vers une interface include (voir [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Affectez-lui la valeur **null** pour spécifier qu’il n’y a aucun fichier include.</span><span class="sxs-lookup"><span data-stu-id="15990-128">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="15990-129">*pPump* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="15990-129">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15990-130">Type : **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="15990-130">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="15990-131">Pointeur vers une interface de pompage de thread (voir [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="15990-131">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="15990-132">Utilisez **null** pour spécifier que cette fonction ne doit pas être retournée tant qu’elle n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="15990-132">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="15990-133">*ppShaderText* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="15990-133">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15990-134">Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="15990-134">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="15990-135">Pointeur vers la mémoire (voir [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) qui contient le nuanceur non compilé.</span><span class="sxs-lookup"><span data-stu-id="15990-135">A pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="15990-136">*ppErrorMsgs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="15990-136">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15990-137">Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="15990-137">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="15990-138">Adresse d’un pointeur vers la mémoire (voir [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) qui contient des erreurs de création d’effet, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="15990-138">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect-creation errors, if any occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15990-139">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="15990-139">Return value</span></span>

<span data-ttu-id="15990-140">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="15990-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="15990-141">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="15990-141">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="15990-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15990-142">Requirements</span></span>



| <span data-ttu-id="15990-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="15990-143">Requirement</span></span> | <span data-ttu-id="15990-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="15990-144">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="15990-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="15990-145">Header</span></span><br/>  | <dl> <span data-ttu-id="15990-146"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="15990-146"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="15990-147">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="15990-147">Library</span></span><br/> | <dl> <span data-ttu-id="15990-148"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15990-148"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15990-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15990-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15990-150">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="15990-150">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
