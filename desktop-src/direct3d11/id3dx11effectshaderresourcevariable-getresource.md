---
title: ID3DX11EffectShaderResourceVariable GetResource, méthode (D3dx11effect. h)
description: Obtenir une ressource de nuanceur.
ms.assetid: 7c56aba0-ce60-4b50-9c1a-802bf1d73c6b
keywords:
- GetResource, méthode Direct3D 11
- GetResource méthode Direct3D 11, interface ID3DX11EffectShaderResourceVariable
- ID3DX11EffectShaderResourceVariable interface Direct3D 11, GetResource, méthode
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable.GetResource
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cea841ae63646958603396d5b65305c242961942
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211693"
---
# <a name="id3dx11effectshaderresourcevariablegetresource-method"></a><span data-ttu-id="78964-106">ID3DX11EffectShaderResourceVariable :: GetResource, méthode</span><span class="sxs-lookup"><span data-stu-id="78964-106">ID3DX11EffectShaderResourceVariable::GetResource method</span></span>

<span data-ttu-id="78964-107">Obtenir une ressource de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="78964-107">Get a shader resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="78964-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="78964-108">Syntax</span></span>


```C++
HRESULT GetResource(
   ID3D11ShaderResourceView **ppResource
);
```



## <a name="parameters"></a><span data-ttu-id="78964-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="78964-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78964-110">*ppResource*</span><span class="sxs-lookup"><span data-stu-id="78964-110">*ppResource*</span></span> 
</dt> <dd>

<span data-ttu-id="78964-111">Type : **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="78964-111">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span></span>

<span data-ttu-id="78964-112">Adresse d’un pointeur vers une interface Shader-Resource-View.</span><span class="sxs-lookup"><span data-stu-id="78964-112">The address of a pointer to a shader-resource-view interface.</span></span> <span data-ttu-id="78964-113">Consultez [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="78964-113">See [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78964-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="78964-114">Return value</span></span>

<span data-ttu-id="78964-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="78964-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="78964-116">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="78964-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="78964-117">Notes</span><span class="sxs-lookup"><span data-stu-id="78964-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="78964-118">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="78964-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="78964-119">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="78964-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="78964-120">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="78964-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="78964-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="78964-121">Requirements</span></span>



| <span data-ttu-id="78964-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78964-122">Requirement</span></span> | <span data-ttu-id="78964-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="78964-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78964-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="78964-124">Header</span></span><br/>  | <dl> <span data-ttu-id="78964-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="78964-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="78964-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="78964-126">Library</span></span><br/> | <dl> <span data-ttu-id="78964-127"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="78964-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78964-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78964-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78964-129">ID3DX11EffectShaderResourceVariable</span><span class="sxs-lookup"><span data-stu-id="78964-129">ID3DX11EffectShaderResourceVariable</span></span>](id3dx11effectshaderresourcevariable.md)
</dt> </dl>

 

 





