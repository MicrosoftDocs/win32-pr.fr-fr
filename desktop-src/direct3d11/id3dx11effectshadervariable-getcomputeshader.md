---
title: Méthode ID3DX11EffectShaderVariable GetComputeShader (D3dx11effect. h)
description: Obtenir un nuanceur de calcul.
ms.assetid: 16a48be1-4e73-4206-837f-615f8d624086
keywords:
- Méthode GetComputeShader Direct3D 11
- Méthode GetComputeShader Direct3D 11, interface ID3DX11EffectShaderVariable
- Interface ID3DX11EffectShaderVariable Direct3D 11, méthode GetComputeShader
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetComputeShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c9312a7d603370d53c0721574623733c9e75da8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211968"
---
# <a name="id3dx11effectshadervariablegetcomputeshader-method"></a><span data-ttu-id="1476f-106">ID3DX11EffectShaderVariable :: GetComputeShader, méthode</span><span class="sxs-lookup"><span data-stu-id="1476f-106">ID3DX11EffectShaderVariable::GetComputeShader method</span></span>

<span data-ttu-id="1476f-107">Obtenir un nuanceur de calcul.</span><span class="sxs-lookup"><span data-stu-id="1476f-107">Get a compute shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="1476f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1476f-108">Syntax</span></span>


```C++
HRESULT GetComputeShader(
   UINT                ShaderIndex,
   ID3D11ComputeShader **ppPS
);
```



## <a name="parameters"></a><span data-ttu-id="1476f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1476f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1476f-110">*ShaderIndex*</span><span class="sxs-lookup"><span data-stu-id="1476f-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="1476f-111">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1476f-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1476f-112">Index du nuanceur de calcul.</span><span class="sxs-lookup"><span data-stu-id="1476f-112">Index of the compute shader.</span></span>

</dd> <dt>

<span data-ttu-id="1476f-113">*ppPS*</span><span class="sxs-lookup"><span data-stu-id="1476f-113">*ppPS*</span></span> 
</dt> <dd>

<span data-ttu-id="1476f-114">Type : **[ **ID3D11ComputeShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11computeshader)\*\***</span><span class="sxs-lookup"><span data-stu-id="1476f-114">Type: **[**ID3D11ComputeShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11computeshader)\*\***</span></span>

<span data-ttu-id="1476f-115">Pointeur vers un pointeur [**ID3D11ComputeShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11computeshader) qui sera défini sur le nuanceur de calcul lors du retour.</span><span class="sxs-lookup"><span data-stu-id="1476f-115">Pointer to an [**ID3D11ComputeShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11computeshader) pointer that will be set to the compute shader on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1476f-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1476f-116">Return value</span></span>

<span data-ttu-id="1476f-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1476f-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1476f-118">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="1476f-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1476f-119">Notes</span><span class="sxs-lookup"><span data-stu-id="1476f-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1476f-120">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="1476f-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="1476f-121">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="1476f-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="1476f-122">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="1476f-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1476f-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1476f-123">Requirements</span></span>



| <span data-ttu-id="1476f-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1476f-124">Requirement</span></span> | <span data-ttu-id="1476f-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="1476f-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1476f-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="1476f-126">Header</span></span><br/>  | <dl> <span data-ttu-id="1476f-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="1476f-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="1476f-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1476f-128">Library</span></span><br/> | <dl> <span data-ttu-id="1476f-129"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="1476f-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1476f-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1476f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1476f-131">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="1476f-131">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

