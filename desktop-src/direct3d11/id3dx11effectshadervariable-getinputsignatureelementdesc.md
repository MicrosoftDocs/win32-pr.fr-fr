---
title: Méthode ID3DX11EffectShaderVariable GetInputSignatureElementDesc (D3dx11effect. h)
description: Obtient une description de la signature d’entrée.
ms.assetid: 45b1fd25-1005-48fd-8a61-561ea2c273e5
keywords:
- Méthode GetInputSignatureElementDesc Direct3D 11
- Méthode GetInputSignatureElementDesc Direct3D 11, interface ID3DX11EffectShaderVariable
- Interface ID3DX11EffectShaderVariable Direct3D 11, méthode GetInputSignatureElementDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetInputSignatureElementDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf788370c26da1ba773d797de544b1a64750d90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116306"
---
# <a name="id3dx11effectshadervariablegetinputsignatureelementdesc-method"></a><span data-ttu-id="749eb-106">ID3DX11EffectShaderVariable :: GetInputSignatureElementDesc, méthode</span><span class="sxs-lookup"><span data-stu-id="749eb-106">ID3DX11EffectShaderVariable::GetInputSignatureElementDesc method</span></span>

<span data-ttu-id="749eb-107">Obtient une description de la signature d’entrée.</span><span class="sxs-lookup"><span data-stu-id="749eb-107">Get an input-signature description.</span></span>

## <a name="syntax"></a><span data-ttu-id="749eb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="749eb-108">Syntax</span></span>


```C++
HRESULT GetInputSignatureElementDesc(
   UINT                           ShaderIndex,
   UINT                           Element,
   D3D11_SIGNATURE_PARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="749eb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="749eb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="749eb-110">*ShaderIndex*</span><span class="sxs-lookup"><span data-stu-id="749eb-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="749eb-111">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="749eb-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="749eb-112">Index de nuanceur de base zéro.</span><span class="sxs-lookup"><span data-stu-id="749eb-112">A zero-based shader index.</span></span>

</dd> <dt>

<span data-ttu-id="749eb-113">*Element*</span><span class="sxs-lookup"><span data-stu-id="749eb-113">*Element*</span></span> 
</dt> <dd>

<span data-ttu-id="749eb-114">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="749eb-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="749eb-115">Index d’élément de nuanceur de base zéro.</span><span class="sxs-lookup"><span data-stu-id="749eb-115">A zero-based shader-element index.</span></span>

</dd> <dt>

<span data-ttu-id="749eb-116">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="749eb-116">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="749eb-117">Type : **[ **\_ paramètre de signature d3d11 \_ \_ desc**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***</span><span class="sxs-lookup"><span data-stu-id="749eb-117">Type: **[**D3D11\_SIGNATURE\_PARAMETER\_DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***</span></span>

<span data-ttu-id="749eb-118">Pointeur vers une description de paramètre (consultez [**d3d11 \_ signature \_ Parameter \_ desc**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).</span><span class="sxs-lookup"><span data-stu-id="749eb-118">A pointer to a parameter description (see [**D3D11\_SIGNATURE\_PARAMETER\_DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="749eb-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="749eb-119">Return value</span></span>

<span data-ttu-id="749eb-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="749eb-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="749eb-121">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="749eb-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="749eb-122">Notes</span><span class="sxs-lookup"><span data-stu-id="749eb-122">Remarks</span></span>

<span data-ttu-id="749eb-123">Un effet contient un ou plusieurs nuanceurs ; chaque nuanceur a une signature d’entrée et de sortie ; chaque signature contient un ou plusieurs éléments (ou paramètres).</span><span class="sxs-lookup"><span data-stu-id="749eb-123">An effect contains one or more shaders; each shader has an input and output signature; each signature contains one or more elements (or parameters).</span></span> <span data-ttu-id="749eb-124">L’index du nuanceur identifie le nuanceur et l’index de l’élément identifie l’élément (ou le paramètre) dans la signature du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="749eb-124">The shader index identifies the shader and the element index identifies the element (or parameter) in the shader signature.</span></span>

> [!Note]  
> <span data-ttu-id="749eb-125">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="749eb-125">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="749eb-126">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="749eb-126">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="749eb-127">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="749eb-127">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="749eb-128">Spécifications</span><span class="sxs-lookup"><span data-stu-id="749eb-128">Requirements</span></span>



| <span data-ttu-id="749eb-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="749eb-129">Requirement</span></span> | <span data-ttu-id="749eb-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="749eb-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="749eb-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="749eb-131">Header</span></span><br/>  | <dl> <span data-ttu-id="749eb-132"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="749eb-132"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="749eb-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="749eb-133">Library</span></span><br/> | <dl> <span data-ttu-id="749eb-134"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="749eb-134"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="749eb-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="749eb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="749eb-136">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="749eb-136">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

