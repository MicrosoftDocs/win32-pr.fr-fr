---
description: Notez qu’au lieu d’utiliser cette fonction héritée, nous vous recommandons d’utiliser l’API D3DPreprocess. Créer un nuanceur à partir de la mémoire sans le compiler.
ms.assetid: 099bc010-1269-4833-8a96-a7c78ed48206
title: D3DX10PreprocessShaderFromMemory, fonction (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10PreprocessShaderFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d1d06e46a5cd6b86420543b380f74273be032c17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762223"
---
# <a name="d3dx10preprocessshaderfrommemory-function"></a><span data-ttu-id="a416d-104">D3DX10PreprocessShaderFromMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="a416d-104">D3DX10PreprocessShaderFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="a416d-105">Au lieu d’utiliser cette fonction héritée, nous vous recommandons d’utiliser l’API [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="a416d-105">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

<span data-ttu-id="a416d-106">Créer un nuanceur à partir de la mémoire sans le compiler.</span><span class="sxs-lookup"><span data-stu-id="a416d-106">Create a shader from memory without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="a416d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a416d-107">Syntax</span></span>


```C++
HRESULT D3DX10PreprocessShaderFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataSize,
  _In_        LPCSTR             pFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="a416d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a416d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a416d-109">*pSrcData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a416d-109">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a416d-110">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a416d-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a416d-111">Pointeur vers la mémoire qui contient le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="a416d-111">Pointer to the memory containing the shader.</span></span>

</dd> <dt>

<span data-ttu-id="a416d-112">*SrcDataSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a416d-112">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a416d-113">Type : **[ **taille \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a416d-113">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a416d-114">Taille du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="a416d-114">Size of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="a416d-115">*pFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a416d-115">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a416d-116">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a416d-116">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a416d-117">Nom du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="a416d-117">Name of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="a416d-118">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a416d-118">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a416d-119">Type : **\* macro de [**\_ nuanceur \_ D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) const**</span><span class="sxs-lookup"><span data-stu-id="a416d-119">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="a416d-120">Tableau de macros de nuanceur se terminant par un caractère NULL (consultez la [**\_ \_ macro de nuanceur D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); définissez cette valeur sur **null** pour ne spécifier aucune macro.</span><span class="sxs-lookup"><span data-stu-id="a416d-120">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="a416d-121">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a416d-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a416d-122">Type : **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="a416d-122">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="a416d-123">Pointeur vers une interface include (voir [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Affectez-lui la valeur **null** pour spécifier qu’il n’y a aucun fichier include.</span><span class="sxs-lookup"><span data-stu-id="a416d-123">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="a416d-124">*pPump* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a416d-124">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a416d-125">Type : **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="a416d-125">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="a416d-126">Pointeur vers une interface de pompage de thread (voir [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="a416d-126">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="a416d-127">Utilisez **null** pour spécifier que cette fonction ne doit pas être retournée tant qu’elle n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="a416d-127">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="a416d-128">*ppShaderText* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a416d-128">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a416d-129">Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="a416d-129">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="a416d-130">Pointeur vers la mémoire (voir [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) qui contient le nuanceur non compilé.</span><span class="sxs-lookup"><span data-stu-id="a416d-130">A pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="a416d-131">*ppErrorMsgs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a416d-131">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a416d-132">Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="a416d-132">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="a416d-133">Adresse d’un pointeur vers la mémoire (voir [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) qui contient des erreurs de création d’effet, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="a416d-133">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect-creation errors, if any occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a416d-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a416d-134">Return value</span></span>

<span data-ttu-id="a416d-135">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a416d-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a416d-136">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="a416d-136">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a416d-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a416d-137">Requirements</span></span>



| <span data-ttu-id="a416d-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a416d-138">Requirement</span></span> | <span data-ttu-id="a416d-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="a416d-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a416d-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="a416d-140">Header</span></span><br/>  | <dl> <span data-ttu-id="a416d-141"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="a416d-141"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="a416d-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a416d-142">Library</span></span><br/> | <dl> <span data-ttu-id="a416d-143"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a416d-143"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a416d-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a416d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a416d-145">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="a416d-145">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
