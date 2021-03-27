---
title: Méthode ID3DX11EffectVariable AsDepthStencilView (D3dx11effect. h)
description: Obtenir une variable de vue de gabarit de profondeur.
ms.assetid: 491ca6e1-a74c-4996-a25c-ea40910f0f36
keywords:
- Méthode AsDepthStencilView Direct3D 11
- Méthode AsDepthStencilView Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode AsDepthStencilView
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsDepthStencilView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 432ba5018f1e233e7fb1b4ad4efae1d4f27cb141
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211728"
---
# <a name="id3dx11effectvariableasdepthstencilview-method"></a><span data-ttu-id="42ede-106">ID3DX11EffectVariable :: AsDepthStencilView, méthode</span><span class="sxs-lookup"><span data-stu-id="42ede-106">ID3DX11EffectVariable::AsDepthStencilView method</span></span>

<span data-ttu-id="42ede-107">Obtenir une variable de vue de gabarit de profondeur.</span><span class="sxs-lookup"><span data-stu-id="42ede-107">Get a depth-stencil-view variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="42ede-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="42ede-108">Syntax</span></span>


```C++
ID3DX11EffectDepthStencilViewVariable* AsDepthStencilView();
```



## <a name="parameters"></a><span data-ttu-id="42ede-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42ede-109">Parameters</span></span>

<span data-ttu-id="42ede-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="42ede-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="42ede-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="42ede-111">Return value</span></span>

<span data-ttu-id="42ede-112">Type : **[ **ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="42ede-112">Type: **[**ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md)\***</span></span>

<span data-ttu-id="42ede-113">Pointeur vers une variable de vue de stencil de profondeur.</span><span class="sxs-lookup"><span data-stu-id="42ede-113">A pointer to a depth-stencil-view variable.</span></span> <span data-ttu-id="42ede-114">Consultez [**ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md).</span><span class="sxs-lookup"><span data-stu-id="42ede-114">See [**ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="42ede-115">Notes</span><span class="sxs-lookup"><span data-stu-id="42ede-115">Remarks</span></span>

<span data-ttu-id="42ede-116">Cette méthode retourne une version de la variable Effect qui a été spécialisée pour une variable de vue de stencil de profondeur.</span><span class="sxs-lookup"><span data-stu-id="42ede-116">This method returns a version of the effect variable that has been specialized to a depth-stencil-view variable.</span></span> <span data-ttu-id="42ede-117">Comme pour un cast, cette spécialisation retourne un objet non valide si la variable Effect ne contient pas de données Depth-View-View.</span><span class="sxs-lookup"><span data-stu-id="42ede-117">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain depth-stencil-view data.</span></span>

<span data-ttu-id="42ede-118">Les applications peuvent tester la validité de l’objet retourné en appelant [**IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="42ede-118">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="42ede-119">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="42ede-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="42ede-120">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="42ede-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="42ede-121">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="42ede-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="42ede-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="42ede-122">Requirements</span></span>



| <span data-ttu-id="42ede-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42ede-123">Requirement</span></span> | <span data-ttu-id="42ede-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="42ede-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42ede-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="42ede-125">Header</span></span><br/>  | <dl> <span data-ttu-id="42ede-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="42ede-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="42ede-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="42ede-127">Library</span></span><br/> | <dl> <span data-ttu-id="42ede-128"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="42ede-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42ede-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42ede-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42ede-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="42ede-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





