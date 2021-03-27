---
title: Méthode ID3DX11EffectShaderVariable GetDomainShader (D3dx11effect. h)
description: Obtenir un nuanceur de domaine.
ms.assetid: fd95a4f0-7df3-4098-843f-0a1e22209603
keywords:
- Méthode GetDomainShader Direct3D 11
- Méthode GetDomainShader Direct3D 11, interface ID3DX11EffectShaderVariable
- Interface ID3DX11EffectShaderVariable Direct3D 11, méthode GetDomainShader
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetDomainShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b7f097fb950b60aaa9c7fa2d5b763b393d5e275
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211967"
---
# <a name="id3dx11effectshadervariablegetdomainshader-method"></a><span data-ttu-id="23240-106">ID3DX11EffectShaderVariable :: GetDomainShader, méthode</span><span class="sxs-lookup"><span data-stu-id="23240-106">ID3DX11EffectShaderVariable::GetDomainShader method</span></span>

<span data-ttu-id="23240-107">Obtenir un nuanceur de domaine.</span><span class="sxs-lookup"><span data-stu-id="23240-107">Get a domain shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="23240-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23240-108">Syntax</span></span>


```C++
HRESULT GetDomainShader(
   UINT               ShaderIndex,
   ID3D11DomainShader **ppPS
);
```



## <a name="parameters"></a><span data-ttu-id="23240-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23240-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23240-110">*ShaderIndex*</span><span class="sxs-lookup"><span data-stu-id="23240-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="23240-111">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="23240-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="23240-112">Index du nuanceur de domaine.</span><span class="sxs-lookup"><span data-stu-id="23240-112">Index of the domain shader.</span></span>

</dd> <dt>

<span data-ttu-id="23240-113">*ppPS*</span><span class="sxs-lookup"><span data-stu-id="23240-113">*ppPS*</span></span> 
</dt> <dd>

<span data-ttu-id="23240-114">Type : **[ **ID3D11DomainShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11domainshader)\*\***</span><span class="sxs-lookup"><span data-stu-id="23240-114">Type: **[**ID3D11DomainShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11domainshader)\*\***</span></span>

<span data-ttu-id="23240-115">Pointeur vers un pointeur [**ID3D11DomainShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11domainshader) qui sera défini sur le nuanceur de domaine lors du retour.</span><span class="sxs-lookup"><span data-stu-id="23240-115">Pointer to an [**ID3D11DomainShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11domainshader) pointer that will be set to the domain shader on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23240-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="23240-116">Return value</span></span>

<span data-ttu-id="23240-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="23240-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="23240-118">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="23240-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="23240-119">Notes</span><span class="sxs-lookup"><span data-stu-id="23240-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="23240-120">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="23240-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="23240-121">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="23240-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="23240-122">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="23240-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="23240-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="23240-123">Requirements</span></span>



| <span data-ttu-id="23240-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23240-124">Requirement</span></span> | <span data-ttu-id="23240-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="23240-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23240-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="23240-126">Header</span></span><br/>  | <dl> <span data-ttu-id="23240-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="23240-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="23240-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="23240-128">Library</span></span><br/> | <dl> <span data-ttu-id="23240-129"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="23240-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23240-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23240-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23240-131">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="23240-131">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

