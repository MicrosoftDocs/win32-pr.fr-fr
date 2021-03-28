---
title: Méthode ID3DX11EffectVariable AsUnorderedAccessView (D3dx11effect. h)
description: Obtenir une variable de vue d’accès non ordonnée.
ms.assetid: e8b7c104-09f7-4bfb-9980-a5603550b723
keywords:
- Méthode AsUnorderedAccessView Direct3D 11
- Méthode AsUnorderedAccessView Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode AsUnorderedAccessView
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsUnorderedAccessView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8b9ce7dbbc99ef16ef3290ec1ba3135a8d2cb05
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762386"
---
# <a name="id3dx11effectvariableasunorderedaccessview-method"></a><span data-ttu-id="c35da-106">ID3DX11EffectVariable :: AsUnorderedAccessView, méthode</span><span class="sxs-lookup"><span data-stu-id="c35da-106">ID3DX11EffectVariable::AsUnorderedAccessView method</span></span>

<span data-ttu-id="c35da-107">Obtenir une variable de vue d’accès non ordonnée.</span><span class="sxs-lookup"><span data-stu-id="c35da-107">Get an unordered-access-view variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="c35da-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c35da-108">Syntax</span></span>


```C++
ID3DX11EffectUnorderedAccessViewVariable* AsUnorderedAccessView();
```



## <a name="parameters"></a><span data-ttu-id="c35da-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c35da-109">Parameters</span></span>

<span data-ttu-id="c35da-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c35da-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c35da-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c35da-111">Return value</span></span>

<span data-ttu-id="c35da-112">Type : **[ **ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="c35da-112">Type: **[**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md)\***</span></span>

<span data-ttu-id="c35da-113">Pointeur vers une variable d’affichage d’accès non ordonnée.</span><span class="sxs-lookup"><span data-stu-id="c35da-113">A pointer to an unordered-access-view variable.</span></span> <span data-ttu-id="c35da-114">Consultez [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md).</span><span class="sxs-lookup"><span data-stu-id="c35da-114">See [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c35da-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c35da-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c35da-116">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="c35da-116">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c35da-117">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="c35da-117">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c35da-118">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c35da-118">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c35da-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c35da-119">Requirements</span></span>



| <span data-ttu-id="c35da-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c35da-120">Requirement</span></span> | <span data-ttu-id="c35da-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c35da-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c35da-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="c35da-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c35da-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c35da-123"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c35da-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c35da-124">Library</span></span><br/> | <dl> <span data-ttu-id="c35da-125"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="c35da-125"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c35da-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c35da-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c35da-127">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="c35da-127">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





