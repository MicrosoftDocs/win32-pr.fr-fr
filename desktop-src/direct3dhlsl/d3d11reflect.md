---
title: D3D11Reflect fonction)
description: Obtient un pointeur vers une interface de réflexion.
ms.assetid: 855097c7-988b-4ab6-90c5-e5dd0bc9e1e0
keywords:
- D3D11Reflect fonction HLSL
topic_type:
- apiref
api_name:
- D3D11Reflect
api_location:
- D3dcompiler_47.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e54a1f388ebb122398ad33c3a8d942496fa55393
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116282"
---
# <a name="d3d11reflect-function"></a><span data-ttu-id="930d7-104">D3D11Reflect fonction)</span><span class="sxs-lookup"><span data-stu-id="930d7-104">D3D11Reflect function</span></span>

<span data-ttu-id="930d7-105">Obtient un pointeur vers une interface de réflexion.</span><span class="sxs-lookup"><span data-stu-id="930d7-105">Gets a pointer to a reflection interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="930d7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="930d7-106">Syntax</span></span>

``` syntax
HRESULT D3D11Reflect(
  in  LPCVOID pSrcData,
  in  SIZE_T SrcDataSize,
  out ID3D11ShaderReflection ppReflector
);
```

## <a name="parameters"></a><span data-ttu-id="930d7-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="930d7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="930d7-108">*pSrcData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="930d7-108">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="930d7-109">Type : **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="930d7-109">Type: **[**LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="930d7-110">Pointeur vers les données sources comme code HLSL compilé.</span><span class="sxs-lookup"><span data-stu-id="930d7-110">A pointer to source data as compiled HLSL code.</span></span>

</dd> <dt>

<span data-ttu-id="930d7-111">*SrcDataSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="930d7-111">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="930d7-112">Type : **[ **taille \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="930d7-112">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="930d7-113">Longueur de *pSrcData*.</span><span class="sxs-lookup"><span data-stu-id="930d7-113">Length of *pSrcData*.</span></span>

</dd> <dt>

<span data-ttu-id="930d7-114">*ppReflector* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="930d7-114">*ppReflector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="930d7-115">Type : **[ **ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection)\*\***</span><span class="sxs-lookup"><span data-stu-id="930d7-115">Type: **[**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection)\*\***</span></span>

<span data-ttu-id="930d7-116">Adresse d’un pointeur vers l’interface [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) .</span><span class="sxs-lookup"><span data-stu-id="930d7-116">The address of a pointer to the [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="930d7-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="930d7-117">Return value</span></span>

<span data-ttu-id="930d7-118">Type : **[ **HRESULT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="930d7-118">Type: **[**HRESULT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="930d7-119">Retourne l’un des codes de retour décrits dans la rubrique [codes de retour Direct3D 11](/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues).</span><span class="sxs-lookup"><span data-stu-id="930d7-119">Returns one of the return codes described in the topic [Direct3D 11 Return Codes](/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues).</span></span>

## <a name="remarks"></a><span data-ttu-id="930d7-120">Notes</span><span class="sxs-lookup"><span data-stu-id="930d7-120">Remarks</span></span>

<span data-ttu-id="930d7-121">La fonction de compilateur inline **D3D11Reflect** est un wrapper pour la fonction de compilateur [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) .</span><span class="sxs-lookup"><span data-stu-id="930d7-121">The inline **D3D11Reflect** compiler function is a wrapper for the [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) compiler function.</span></span> <span data-ttu-id="930d7-122">**D3D11Reflect** peut récupérer uniquement une interface [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) à partir d’un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="930d7-122">**D3D11Reflect** can retrieve only a [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) interface from a shader.</span></span> <span data-ttu-id="930d7-123">**D3DReflect** peut récupérer une interface **ID3D11ShaderReflection** ou une interface de réflexion direct3d 10 ou Direct3D 10,1, par exemple, [**ID3D10ShaderReflection**](/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflection).</span><span class="sxs-lookup"><span data-stu-id="930d7-123">**D3DReflect** can retrieve a **ID3D11ShaderReflection** interface or a Direct3D 10 or Direct3D 10.1 reflection interface, for example, [**ID3D10ShaderReflection**](/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflection).</span></span>

<span data-ttu-id="930d7-124">Le code du nuanceur contient des métadonnées qui peuvent être inspectées à l’aide des API de réflexion.</span><span class="sxs-lookup"><span data-stu-id="930d7-124">Shader code contains metadata that can be inspected using the reflection APIs.</span></span>

<span data-ttu-id="930d7-125">Le code suivant montre comment récupérer une interface [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) à partir d’un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="930d7-125">The following code shows how to retrieve a [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) interface from a shader.</span></span>


```C++
pd3dDevice->CreatePixelShader( pPixelShaderBuffer->GetBufferPointer(),
                               pPixelShaderBuffer->GetBufferSize(), g_pPSClassLinkage, &g_pPixelShader );

ID3D11ShaderReflection* pReflector = NULL; 
D3D11Reflect( pPixelShaderBuffer->GetBufferPointer(), pPixelShaderBuffer->GetBufferSize(), 
            &pReflector);
```



## <a name="requirements"></a><span data-ttu-id="930d7-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="930d7-126">Requirements</span></span>



| <span data-ttu-id="930d7-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="930d7-127">Requirement</span></span> | <span data-ttu-id="930d7-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="930d7-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="930d7-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="930d7-129">Header</span></span><br/>  | <dl> <span data-ttu-id="930d7-130"><dt>D3DCompiler. inl</dt></span><span class="sxs-lookup"><span data-stu-id="930d7-130"><dt>D3DCompiler.inl</dt></span></span> </dl>     |
| <span data-ttu-id="930d7-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="930d7-131">Library</span></span><br/> | <dl> <span data-ttu-id="930d7-132"><dt>D3dcompiler \_ 47. lib</dt></span><span class="sxs-lookup"><span data-stu-id="930d7-132"><dt>D3dcompiler\_47.lib</dt></span></span> </dl> |
| <span data-ttu-id="930d7-133">DLL</span><span class="sxs-lookup"><span data-stu-id="930d7-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="930d7-134"><dt>D3dcompiler \_47.dll</dt></span><span class="sxs-lookup"><span data-stu-id="930d7-134"><dt>D3dcompiler\_47.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="930d7-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="930d7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="930d7-136">Fonctions</span><span class="sxs-lookup"><span data-stu-id="930d7-136">Functions</span></span>](dx-graphics-d3dcompiler-reference-functions.md)
</dt> </dl>

 

