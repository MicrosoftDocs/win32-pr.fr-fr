---
title: Méthode ID3DX11EffectVariable AsShaderResource (D3dx11effect. h)
description: Obtenir une variable de nuanceur-ressource.
ms.assetid: 02db94eb-980a-4677-af89-3006aef6faca
keywords:
- Méthode AsShaderResource Direct3D 11
- Méthode AsShaderResource Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode AsShaderResource
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsShaderResource
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3af6236d25e8a2c652f5a551bf7199f3a78d8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996312"
---
# <a name="id3dx11effectvariableasshaderresource-method"></a><span data-ttu-id="4ebcc-106">ID3DX11EffectVariable :: AsShaderResource, méthode</span><span class="sxs-lookup"><span data-stu-id="4ebcc-106">ID3DX11EffectVariable::AsShaderResource method</span></span>

<span data-ttu-id="4ebcc-107">Obtenir une variable de nuanceur-ressource.</span><span class="sxs-lookup"><span data-stu-id="4ebcc-107">Get a shader-resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ebcc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4ebcc-108">Syntax</span></span>


```C++
ID3DX11EffectShaderResourceVariable* AsShaderResource();
```



## <a name="parameters"></a><span data-ttu-id="4ebcc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4ebcc-109">Parameters</span></span>

<span data-ttu-id="4ebcc-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="4ebcc-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4ebcc-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4ebcc-111">Return value</span></span>

<span data-ttu-id="4ebcc-112">Type : **[ **ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="4ebcc-112">Type: **[**ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md)\***</span></span>

<span data-ttu-id="4ebcc-113">Pointeur vers une variable de ressource de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="4ebcc-113">A pointer to a shader-resource variable.</span></span> <span data-ttu-id="4ebcc-114">Consultez [**ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md).</span><span class="sxs-lookup"><span data-stu-id="4ebcc-114">See [**ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4ebcc-115">Notes</span><span class="sxs-lookup"><span data-stu-id="4ebcc-115">Remarks</span></span>

<span data-ttu-id="4ebcc-116">AsShaderResource retourne une version de la variable Effect qui a été spécialisée pour une variable de ressource Shader.</span><span class="sxs-lookup"><span data-stu-id="4ebcc-116">AsShaderResource returns a version of the effect variable that has been specialized to a shader-resource variable.</span></span> <span data-ttu-id="4ebcc-117">Comme pour un cast, cette spécialisation retourne un objet non valide si la variable Effect ne contient pas de données de ressource de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="4ebcc-117">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain shader-resource data.</span></span>

<span data-ttu-id="4ebcc-118">Les applications peuvent tester la validité de l’objet retourné en appelant [**IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="4ebcc-118">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="4ebcc-119">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="4ebcc-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="4ebcc-120">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="4ebcc-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="4ebcc-121">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="4ebcc-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4ebcc-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4ebcc-122">Requirements</span></span>



| <span data-ttu-id="4ebcc-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4ebcc-123">Requirement</span></span> | <span data-ttu-id="4ebcc-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ebcc-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ebcc-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="4ebcc-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4ebcc-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ebcc-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4ebcc-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4ebcc-127">Library</span></span><br/> | <dl> <span data-ttu-id="4ebcc-128"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="4ebcc-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ebcc-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ebcc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ebcc-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="4ebcc-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





