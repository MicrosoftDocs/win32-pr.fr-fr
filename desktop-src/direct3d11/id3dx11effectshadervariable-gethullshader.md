---
title: Méthode ID3DX11EffectShaderVariable GetHullShader (D3dx11effect. h)
description: Obtenir un nuanceur de coque.
ms.assetid: 18b2a8fc-2c53-4858-9aaa-00d0dc86adee
keywords:
- Méthode GetHullShader Direct3D 11
- Méthode GetHullShader Direct3D 11, interface ID3DX11EffectShaderVariable
- Interface ID3DX11EffectShaderVariable Direct3D 11, méthode GetHullShader
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetHullShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7eac8e6e095eb1ddbba93d68bec87e85e0c4e22
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996288"
---
# <a name="id3dx11effectshadervariablegethullshader-method"></a><span data-ttu-id="0d815-106">ID3DX11EffectShaderVariable :: GetHullShader, méthode</span><span class="sxs-lookup"><span data-stu-id="0d815-106">ID3DX11EffectShaderVariable::GetHullShader method</span></span>

<span data-ttu-id="0d815-107">Obtenir un nuanceur de coque.</span><span class="sxs-lookup"><span data-stu-id="0d815-107">Get a hull shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d815-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d815-108">Syntax</span></span>


```C++
HRESULT GetHullShader(
   UINT             ShaderIndex,
   ID3D11HullShader **ppPS
);
```



## <a name="parameters"></a><span data-ttu-id="0d815-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d815-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d815-110">*ShaderIndex*</span><span class="sxs-lookup"><span data-stu-id="0d815-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="0d815-111">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0d815-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="0d815-112">Index du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="0d815-112">Index of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="0d815-113">*ppPS*</span><span class="sxs-lookup"><span data-stu-id="0d815-113">*ppPS*</span></span> 
</dt> <dd>

<span data-ttu-id="0d815-114">Type : **[ **ID3D11HullShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11hullshader)\*\***</span><span class="sxs-lookup"><span data-stu-id="0d815-114">Type: **[**ID3D11HullShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11hullshader)\*\***</span></span>

<span data-ttu-id="0d815-115">Pointeur vers un pointeur [**ID3D11HullShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11hullshader) qui sera défini sur le nuanceur de coque lors du retour.</span><span class="sxs-lookup"><span data-stu-id="0d815-115">A pointer to an [**ID3D11HullShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11hullshader) pointer that will be set to the hull shader on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d815-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0d815-116">Return value</span></span>

<span data-ttu-id="0d815-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0d815-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0d815-118">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="0d815-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0d815-119">Notes</span><span class="sxs-lookup"><span data-stu-id="0d815-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0d815-120">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="0d815-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="0d815-121">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="0d815-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="0d815-122">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="0d815-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0d815-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0d815-123">Requirements</span></span>



| <span data-ttu-id="0d815-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d815-124">Requirement</span></span> | <span data-ttu-id="0d815-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d815-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d815-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="0d815-126">Header</span></span><br/>  | <dl> <span data-ttu-id="0d815-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d815-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0d815-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0d815-128">Library</span></span><br/> | <dl> <span data-ttu-id="0d815-129"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="0d815-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d815-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d815-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d815-131">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="0d815-131">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

