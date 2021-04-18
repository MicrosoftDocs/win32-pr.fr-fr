---
description: Créer un processeur de données asynchrones pour un pool de mémoire.
ms.assetid: 3985a5e5-492e-4003-9d10-6e34620de69f
title: D3DX10CreateAsyncEffectPoolCreateProcessor, fonction (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncEffectPoolCreateProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 32e7c60f28a823c624b3866a8cdd46db659f8a49
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211820"
---
# <a name="d3dx10createasynceffectpoolcreateprocessor-function"></a><span data-ttu-id="882bc-103">D3DX10CreateAsyncEffectPoolCreateProcessor fonction)</span><span class="sxs-lookup"><span data-stu-id="882bc-103">D3DX10CreateAsyncEffectPoolCreateProcessor function</span></span>

<span data-ttu-id="882bc-104">Créer un processeur de données asynchrones pour un pool de mémoire.</span><span class="sxs-lookup"><span data-stu-id="882bc-104">Create an asynchronous-data processor for a memory pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="882bc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="882bc-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncEffectPoolCreateProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags,
  _In_        UINT                 FXFlags,
  _In_        ID3D10Device         *pDevice,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="882bc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="882bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="882bc-107">*pFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="882bc-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="882bc-108">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="882bc-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="882bc-109">Chaîne qui contient le nom de fichier de l’effet.</span><span class="sxs-lookup"><span data-stu-id="882bc-109">A string that contains the effect filename.</span></span>

</dd> <dt>

<span data-ttu-id="882bc-110">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="882bc-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="882bc-111">Type : **\* macro de [**\_ nuanceur \_ D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) const**</span><span class="sxs-lookup"><span data-stu-id="882bc-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="882bc-112">Tableau de macros de nuanceur se terminant par un caractère NULL (consultez la [**\_ \_ macro de nuanceur D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); définissez cette valeur sur **null** pour ne spécifier aucune macro.</span><span class="sxs-lookup"><span data-stu-id="882bc-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="882bc-113">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="882bc-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="882bc-114">Type : **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="882bc-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="882bc-115">Pointeur vers une interface include (voir [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Affectez-lui la valeur **null** pour spécifier qu’il n’y a aucun fichier include.</span><span class="sxs-lookup"><span data-stu-id="882bc-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="882bc-116">*pProfile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="882bc-116">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="882bc-117">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="882bc-117">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="882bc-118">Chaîne qui spécifie le [profil de nuanceur](../direct3dhlsl/dx-graphics-hlsl-models.md) ou le modèle de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="882bc-118">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md) or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="882bc-119">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="882bc-119">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="882bc-120">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="882bc-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="882bc-121">Options de compilation HLSL (voir [indicateurs de nuanceur](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="882bc-121">HLSL compile options (see [Shader Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="882bc-122">*FXFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="882bc-122">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="882bc-123">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="882bc-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="882bc-124">Appliquer des options de compilation (voir [indicateurs de compilation et d’effet](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="882bc-124">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="882bc-125">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="882bc-125">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="882bc-126">Type : **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="882bc-126">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="882bc-127">Pointeur vers l’appareil (voir [**interface ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) qui utilisera les ressources.</span><span class="sxs-lookup"><span data-stu-id="882bc-127">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="882bc-128">*ppErrorBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="882bc-128">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="882bc-129">Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="882bc-129">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="882bc-130">Adresse d’un pointeur vers la mémoire (voir [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) qui contient des erreurs d’effet de compilation, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="882bc-130">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="882bc-131">*ppDataProcessor* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="882bc-131">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="882bc-132">Type : **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="882bc-132">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="882bc-133">Adresse d’un pointeur vers une mémoire tampon qui contient le processeur de données créé (voir [**interface ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="882bc-133">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="882bc-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="882bc-134">Return value</span></span>

<span data-ttu-id="882bc-135">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="882bc-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="882bc-136">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="882bc-136">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="882bc-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="882bc-137">Requirements</span></span>



| <span data-ttu-id="882bc-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="882bc-138">Requirement</span></span> | <span data-ttu-id="882bc-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="882bc-139">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="882bc-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="882bc-140">Header</span></span><br/> | <dl> <span data-ttu-id="882bc-141"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="882bc-141"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="882bc-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="882bc-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="882bc-143">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="882bc-143">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
