---
title: Méthode ID3DX11EffectVariable AsDepthStencil (D3dx11effect. h)
description: Obtenir une variable de stencil de profondeur.
ms.assetid: 3526812b-6c43-492e-b529-12f61ecd20e3
keywords:
- Méthode AsDepthStencil Direct3D 11
- Méthode AsDepthStencil Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode AsDepthStencil
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsDepthStencil
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 980bd43f51d187252fab1872ba75d04f82820ef8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953898"
---
# <a name="id3dx11effectvariableasdepthstencil-method"></a><span data-ttu-id="98090-106">ID3DX11EffectVariable :: AsDepthStencil, méthode</span><span class="sxs-lookup"><span data-stu-id="98090-106">ID3DX11EffectVariable::AsDepthStencil method</span></span>

<span data-ttu-id="98090-107">Obtenir une variable de stencil de profondeur.</span><span class="sxs-lookup"><span data-stu-id="98090-107">Get a depth-stencil variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="98090-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98090-108">Syntax</span></span>


```C++
ID3DX11EffectDepthStencilVariable* AsDepthStencil();
```



## <a name="parameters"></a><span data-ttu-id="98090-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98090-109">Parameters</span></span>

<span data-ttu-id="98090-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="98090-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="98090-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="98090-111">Return value</span></span>

<span data-ttu-id="98090-112">Type : **[ **ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="98090-112">Type: **[**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md)\***</span></span>

<span data-ttu-id="98090-113">Pointeur vers une variable de stencil de profondeur.</span><span class="sxs-lookup"><span data-stu-id="98090-113">A pointer to a depth-stencil variable.</span></span> <span data-ttu-id="98090-114">Consultez [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md).</span><span class="sxs-lookup"><span data-stu-id="98090-114">See [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="98090-115">Notes</span><span class="sxs-lookup"><span data-stu-id="98090-115">Remarks</span></span>

<span data-ttu-id="98090-116">AsDepthStencil retourne une version de la variable Effect qui a été spécialisée pour une variable de stencil de profondeur.</span><span class="sxs-lookup"><span data-stu-id="98090-116">AsDepthStencil returns a version of the effect variable that has been specialized to a depth-stencil variable.</span></span> <span data-ttu-id="98090-117">Comme pour un cast, cette spécialisation retourne un objet non valide si la variable Effect ne contient pas de données de stencil de profondeur.</span><span class="sxs-lookup"><span data-stu-id="98090-117">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain depth-stencil data.</span></span>

<span data-ttu-id="98090-118">Les applications peuvent tester la validité de l’objet retourné en appelant [**IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="98090-118">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="98090-119">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="98090-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="98090-120">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="98090-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="98090-121">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="98090-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="98090-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="98090-122">Requirements</span></span>



| <span data-ttu-id="98090-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98090-123">Requirement</span></span> | <span data-ttu-id="98090-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="98090-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98090-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="98090-125">Header</span></span><br/>  | <dl> <span data-ttu-id="98090-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="98090-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="98090-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="98090-127">Library</span></span><br/> | <dl> <span data-ttu-id="98090-128"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="98090-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98090-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98090-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98090-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="98090-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





