---
title: Méthode ID3DX11EffectPass GetDomainShaderDesc (D3dx11effect. h)
description: Obtenir une description du nuanceur de domaine.
ms.assetid: 02109930-0922-46b8-9381-bb75abd0c4a0
keywords:
- Méthode GetDomainShaderDesc Direct3D 11
- Méthode GetDomainShaderDesc Direct3D 11, interface ID3DX11EffectPass
- Interface ID3DX11EffectPass Direct3D 11, méthode GetDomainShaderDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetDomainShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2157134d97332fc9c76267f5e0db49d2c40e96a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974666"
---
# <a name="id3dx11effectpassgetdomainshaderdesc-method"></a><span data-ttu-id="337f9-106">ID3DX11EffectPass :: GetDomainShaderDesc, méthode</span><span class="sxs-lookup"><span data-stu-id="337f9-106">ID3DX11EffectPass::GetDomainShaderDesc method</span></span>

<span data-ttu-id="337f9-107">Obtenir une description du nuanceur de domaine.</span><span class="sxs-lookup"><span data-stu-id="337f9-107">Get a domain-shader description.</span></span>

## <a name="syntax"></a><span data-ttu-id="337f9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="337f9-108">Syntax</span></span>


```C++
HRESULT GetDomainShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="337f9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="337f9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="337f9-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="337f9-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="337f9-111">Type : **[ **D3DX11 \_ passe- \_ Shader \_ desc**](d3dx11-pass-shader-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="337f9-111">Type: **[**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)\***</span></span>

<span data-ttu-id="337f9-112">Pointeur vers une description du nuanceur de domaine (consultez [**D3DX11 \_ Pass \_ Shader \_ desc**](d3dx11-pass-shader-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="337f9-112">A pointer to a domain-shader description (see [**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="337f9-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="337f9-113">Return value</span></span>

<span data-ttu-id="337f9-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="337f9-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="337f9-115">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="337f9-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="337f9-116">Notes</span><span class="sxs-lookup"><span data-stu-id="337f9-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="337f9-117">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="337f9-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="337f9-118">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="337f9-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="337f9-119">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="337f9-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="337f9-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="337f9-120">Requirements</span></span>



| <span data-ttu-id="337f9-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="337f9-121">Requirement</span></span> | <span data-ttu-id="337f9-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="337f9-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="337f9-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="337f9-123">Header</span></span><br/>  | <dl> <span data-ttu-id="337f9-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="337f9-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="337f9-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="337f9-125">Library</span></span><br/> | <dl> <span data-ttu-id="337f9-126"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="337f9-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="337f9-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="337f9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="337f9-128">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="337f9-128">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





