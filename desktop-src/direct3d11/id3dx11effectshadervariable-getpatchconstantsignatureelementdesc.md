---
title: Méthode ID3DX11EffectShaderVariable GetPatchConstantSignatureElementDesc (D3dx11effect. h)
description: Obtenir une description de la signature constante de patch.
ms.assetid: 72a86cf6-ace2-4306-ac5c-37d888c087f7
keywords:
- Méthode GetPatchConstantSignatureElementDesc Direct3D 11
- Méthode GetPatchConstantSignatureElementDesc Direct3D 11, interface ID3DX11EffectShaderVariable
- Interface ID3DX11EffectShaderVariable Direct3D 11, méthode GetPatchConstantSignatureElementDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetPatchConstantSignatureElementDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4fcbc8f7c1bc34b0da42dd08c255a04a6d2fc83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996160"
---
# <a name="id3dx11effectshadervariablegetpatchconstantsignatureelementdesc-method"></a><span data-ttu-id="096ed-106">ID3DX11EffectShaderVariable :: GetPatchConstantSignatureElementDesc, méthode</span><span class="sxs-lookup"><span data-stu-id="096ed-106">ID3DX11EffectShaderVariable::GetPatchConstantSignatureElementDesc method</span></span>

<span data-ttu-id="096ed-107">Obtenir une description de la signature constante de patch.</span><span class="sxs-lookup"><span data-stu-id="096ed-107">Get a patch constant signature description.</span></span>

## <a name="syntax"></a><span data-ttu-id="096ed-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="096ed-108">Syntax</span></span>


```C++
HRESULT GetPatchConstantSignatureElementDesc(
   UINT                           ShaderIndex,
   UINT                           Element,
   D3D11_SIGNATURE_PARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="096ed-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="096ed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="096ed-110">*ShaderIndex*</span><span class="sxs-lookup"><span data-stu-id="096ed-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="096ed-111">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="096ed-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="096ed-112">Index de nuanceur de base zéro.</span><span class="sxs-lookup"><span data-stu-id="096ed-112">A zero-based shader index.</span></span>

</dd> <dt>

<span data-ttu-id="096ed-113">*Element*</span><span class="sxs-lookup"><span data-stu-id="096ed-113">*Element*</span></span> 
</dt> <dd>

<span data-ttu-id="096ed-114">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="096ed-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="096ed-115">Index de base zéro de l’élément.</span><span class="sxs-lookup"><span data-stu-id="096ed-115">A zero-based element index.</span></span>

</dd> <dt>

<span data-ttu-id="096ed-116">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="096ed-116">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="096ed-117">Type : **[ **\_ paramètre de signature d3d11 \_ \_ desc**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***</span><span class="sxs-lookup"><span data-stu-id="096ed-117">Type: **[**D3D11\_SIGNATURE\_PARAMETER\_DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***</span></span>

<span data-ttu-id="096ed-118">Pointeur vers une description de paramètre (consultez [**d3d11 \_ signature \_ Parameter \_ desc**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).</span><span class="sxs-lookup"><span data-stu-id="096ed-118">A pointer to a parameter description (see [**D3D11\_SIGNATURE\_PARAMETER\_DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="096ed-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="096ed-119">Return value</span></span>

<span data-ttu-id="096ed-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="096ed-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="096ed-121">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="096ed-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="096ed-122">Notes</span><span class="sxs-lookup"><span data-stu-id="096ed-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="096ed-123">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="096ed-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="096ed-124">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="096ed-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="096ed-125">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="096ed-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="096ed-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="096ed-126">Requirements</span></span>



| <span data-ttu-id="096ed-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="096ed-127">Requirement</span></span> | <span data-ttu-id="096ed-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="096ed-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="096ed-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="096ed-129">Header</span></span><br/>  | <dl> <span data-ttu-id="096ed-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="096ed-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="096ed-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="096ed-131">Library</span></span><br/> | <dl> <span data-ttu-id="096ed-132"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="096ed-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="096ed-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="096ed-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="096ed-134">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="096ed-134">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

