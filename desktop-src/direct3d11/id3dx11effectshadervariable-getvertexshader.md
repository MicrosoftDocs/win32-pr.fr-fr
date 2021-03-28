---
title: Méthode ID3DX11EffectShaderVariable GetVertexShader (D3dx11effect. h)
description: Obtenir un nuanceur de sommets.
ms.assetid: 31a250ae-154b-43ce-97e3-6480f23dc4e2
keywords:
- Méthode GetVertexShader Direct3D 11
- Méthode GetVertexShader Direct3D 11, interface ID3DX11EffectShaderVariable
- Interface ID3DX11EffectShaderVariable Direct3D 11, méthode GetVertexShader
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetVertexShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7977da5fc36a0c339069526db723e2c479b49d55
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531023"
---
# <a name="id3dx11effectshadervariablegetvertexshader-method"></a><span data-ttu-id="ba8cc-106">ID3DX11EffectShaderVariable :: GetVertexShader, méthode</span><span class="sxs-lookup"><span data-stu-id="ba8cc-106">ID3DX11EffectShaderVariable::GetVertexShader method</span></span>

<span data-ttu-id="ba8cc-107">Obtenir un nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="ba8cc-107">Get a vertex shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba8cc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba8cc-108">Syntax</span></span>


```C++
HRESULT GetVertexShader(
   UINT               ShaderIndex,
   ID3D11VertexShader **ppVS
);
```



## <a name="parameters"></a><span data-ttu-id="ba8cc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ba8cc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba8cc-110">*ShaderIndex*</span><span class="sxs-lookup"><span data-stu-id="ba8cc-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="ba8cc-111">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ba8cc-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ba8cc-112">Index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="ba8cc-112">A zero-based index.</span></span>

</dd> <dt>

<span data-ttu-id="ba8cc-113">*ppVS*</span><span class="sxs-lookup"><span data-stu-id="ba8cc-113">*ppVS*</span></span> 
</dt> <dd>

<span data-ttu-id="ba8cc-114">Type : **[ **ID3D11VertexShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11vertexshader)\*\***</span><span class="sxs-lookup"><span data-stu-id="ba8cc-114">Type: **[**ID3D11VertexShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11vertexshader)\*\***</span></span>

<span data-ttu-id="ba8cc-115">Pointeur vers un pointeur [**ID3D11VertexShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11vertexshader) qui sera défini sur le nuanceur de sommets lors du retour.</span><span class="sxs-lookup"><span data-stu-id="ba8cc-115">A pointer to an [**ID3D11VertexShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11vertexshader) pointer that will be set to the vertex shader on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba8cc-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ba8cc-116">Return value</span></span>

<span data-ttu-id="ba8cc-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ba8cc-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ba8cc-118">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="ba8cc-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ba8cc-119">Notes</span><span class="sxs-lookup"><span data-stu-id="ba8cc-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ba8cc-120">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="ba8cc-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ba8cc-121">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="ba8cc-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ba8cc-122">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="ba8cc-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ba8cc-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ba8cc-123">Requirements</span></span>



| <span data-ttu-id="ba8cc-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba8cc-124">Requirement</span></span> | <span data-ttu-id="ba8cc-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba8cc-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba8cc-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="ba8cc-126">Header</span></span><br/>  | <dl> <span data-ttu-id="ba8cc-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba8cc-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ba8cc-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ba8cc-128">Library</span></span><br/> | <dl> <span data-ttu-id="ba8cc-129"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="ba8cc-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba8cc-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba8cc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba8cc-131">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="ba8cc-131">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

