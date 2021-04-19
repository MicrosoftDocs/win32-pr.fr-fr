---
description: Notez qu’au lieu d’utiliser cette fonction héritée, nous vous recommandons d’utiliser l’API D3DPreprocess. Créer un nuanceur à partir d’un fichier sans le compiler.
ms.assetid: 9f609aa5-5ee7-45fb-9693-69de130b6cc0
title: D3DX10PreprocessShaderFromFile, fonction (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10PreprocessShaderFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: e6222febd378b262d9fb9e87a6224968c2d04038
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539465"
---
# <a name="d3dx10preprocessshaderfromfile-function"></a><span data-ttu-id="ed93a-104">D3DX10PreprocessShaderFromFile fonction)</span><span class="sxs-lookup"><span data-stu-id="ed93a-104">D3DX10PreprocessShaderFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="ed93a-105">Au lieu d’utiliser cette fonction héritée, nous vous recommandons d’utiliser l’API [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="ed93a-105">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

<span data-ttu-id="ed93a-106">Créer un nuanceur à partir d’un fichier sans le compiler.</span><span class="sxs-lookup"><span data-stu-id="ed93a-106">Create a shader from a file without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed93a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed93a-107">Syntax</span></span>


```C++
HRESULT D3DX10PreprocessShaderFromFile(
  _In_        LPCTSTR            pFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="ed93a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ed93a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed93a-109">*pFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ed93a-109">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed93a-110">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed93a-110">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed93a-111">Nom du fichier de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="ed93a-111">Name of the shader file.</span></span>

</dd> <dt>

<span data-ttu-id="ed93a-112">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ed93a-112">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed93a-113">Type : **\* macro de [**\_ nuanceur \_ D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) const**</span><span class="sxs-lookup"><span data-stu-id="ed93a-113">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="ed93a-114">Tableau de macros de nuanceur se terminant par un caractère NULL (consultez la [**\_ \_ macro de nuanceur D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); définissez cette valeur sur **null** pour ne spécifier aucune macro.</span><span class="sxs-lookup"><span data-stu-id="ed93a-114">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="ed93a-115">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ed93a-115">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed93a-116">Type : **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="ed93a-116">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="ed93a-117">Pointeur vers une interface include (voir [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Affectez-lui la valeur **null** pour spécifier qu’il n’y a aucun fichier include.</span><span class="sxs-lookup"><span data-stu-id="ed93a-117">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="ed93a-118">*pPump* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ed93a-118">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed93a-119">Type : **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="ed93a-119">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="ed93a-120">Pointeur vers une interface de pompage de thread (voir [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="ed93a-120">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="ed93a-121">Utilisez **null** pour spécifier que cette fonction ne doit pas être retournée tant qu’elle n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="ed93a-121">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="ed93a-122">*ppShaderText* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ed93a-122">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed93a-123">Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="ed93a-123">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="ed93a-124">Pointeur vers la mémoire (voir [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) qui contient le nuanceur non compilé.</span><span class="sxs-lookup"><span data-stu-id="ed93a-124">A pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="ed93a-125">*ppErrorMsgs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ed93a-125">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed93a-126">Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="ed93a-126">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="ed93a-127">Adresse d’un pointeur vers la mémoire (voir [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) qui contient des erreurs de création d’effet, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="ed93a-127">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect-creation errors, if any occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed93a-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ed93a-128">Return value</span></span>

<span data-ttu-id="ed93a-129">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ed93a-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ed93a-130">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ed93a-130">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ed93a-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ed93a-131">Requirements</span></span>



| <span data-ttu-id="ed93a-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ed93a-132">Requirement</span></span> | <span data-ttu-id="ed93a-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed93a-133">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed93a-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="ed93a-134">Header</span></span><br/> | <dl> <span data-ttu-id="ed93a-135"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed93a-135"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed93a-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed93a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed93a-137">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="ed93a-137">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
