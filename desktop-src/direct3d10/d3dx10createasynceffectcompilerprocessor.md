---
description: Créer un processeur de données asynchrones pour un effet.
ms.assetid: 90a0dcd1-e495-4068-9f28-e2645370b984
title: D3DX10CreateAsyncEffectCompilerProcessor, fonction (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncEffectCompilerProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 9e1e5716228537d505adc4f48179ec7027b57198
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525889"
---
# <a name="d3dx10createasynceffectcompilerprocessor-function"></a><span data-ttu-id="fb6ea-103">D3DX10CreateAsyncEffectCompilerProcessor fonction)</span><span class="sxs-lookup"><span data-stu-id="fb6ea-103">D3DX10CreateAsyncEffectCompilerProcessor function</span></span>

<span data-ttu-id="fb6ea-104">Créer un processeur de données asynchrones pour un effet.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-104">Create an asynchronous-data processor for an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb6ea-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb6ea-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncEffectCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        UINT                 Flags,
  _In_        UINT                 FXFlags,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="fb6ea-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fb6ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb6ea-107">*pFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fb6ea-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb6ea-108">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb6ea-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fb6ea-109">Chaîne qui contient le nom de fichier de l’effet.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-109">A string that contains the effect filename.</span></span>

</dd> <dt>

<span data-ttu-id="fb6ea-110">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fb6ea-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb6ea-111">Type : **\* macro de [**\_ nuanceur \_ D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) const**</span><span class="sxs-lookup"><span data-stu-id="fb6ea-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="fb6ea-112">Tableau de macros de nuanceur se terminant par un caractère NULL (consultez la [**\_ \_ macro de nuanceur D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); définissez cette valeur sur **null** pour ne spécifier aucune macro.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="fb6ea-113">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fb6ea-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb6ea-114">Type : **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="fb6ea-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="fb6ea-115">Pointeur vers une interface include (voir [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="fb6ea-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="fb6ea-116">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-116">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fb6ea-117">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="fb6ea-117">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb6ea-118">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb6ea-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fb6ea-119">[Options de compilation HLSL](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="fb6ea-119">[HLSL compile options](d3d10-graphics-reference-effect-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="fb6ea-120">*FXFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fb6ea-120">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb6ea-121">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb6ea-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fb6ea-122">[Appliquer les options de compilation](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="fb6ea-122">[Effect compile options](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="fb6ea-123">*ppCompiledShader* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fb6ea-123">*ppCompiledShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb6ea-124">Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="fb6ea-124">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="fb6ea-125">Adresse d’un pointeur vers la mémoire tampon (voir [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) qui contient l’effet compilé.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-125">Address of a pointer to buffer (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains the compiled effect.</span></span>

</dd> <dt>

<span data-ttu-id="fb6ea-126">*ppErrorBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fb6ea-126">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb6ea-127">Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="fb6ea-127">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="fb6ea-128">Adresse d’un pointeur vers une mémoire tampon (voir [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) qui contient des erreurs de compilation.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-128">Address of a pointer to a buffer (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains compile errors.</span></span>

</dd> <dt>

<span data-ttu-id="fb6ea-129">*ppDataProcessor* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fb6ea-129">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb6ea-130">Type : **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="fb6ea-130">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="fb6ea-131">Adresse d’un pointeur vers une mémoire tampon qui contient le processeur de données créé (voir [**interface ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="fb6ea-131">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb6ea-132">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fb6ea-132">Return value</span></span>

<span data-ttu-id="fb6ea-133">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fb6ea-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fb6ea-134">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="fb6ea-134">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb6ea-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb6ea-135">Requirements</span></span>



| <span data-ttu-id="fb6ea-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb6ea-136">Requirement</span></span> | <span data-ttu-id="fb6ea-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb6ea-137">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb6ea-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="fb6ea-138">Header</span></span><br/> | <dl> <span data-ttu-id="fb6ea-139"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb6ea-139"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb6ea-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb6ea-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb6ea-141">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="fb6ea-141">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
