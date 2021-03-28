---
title: Méthode ID3DX11EffectVariable AsSampler (D3dx11effect. h)
description: Obtenir une variable d’échantillonneur.
ms.assetid: dff699f7-758a-442b-93eb-23a09468251f
keywords:
- Méthode AsSampler Direct3D 11
- Méthode AsSampler Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode AsSampler
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsSampler
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1213320950377f6981348a158c3d8c8ef4d4fd0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996317"
---
# <a name="id3dx11effectvariableassampler-method"></a><span data-ttu-id="eb8b5-106">ID3DX11EffectVariable :: AsSampler, méthode</span><span class="sxs-lookup"><span data-stu-id="eb8b5-106">ID3DX11EffectVariable::AsSampler method</span></span>

<span data-ttu-id="eb8b5-107">Obtenir une variable d’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="eb8b5-107">Get a sampler variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb8b5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb8b5-108">Syntax</span></span>


```C++
ID3DX11EffectSamplerVariable* AsSampler();
```



## <a name="parameters"></a><span data-ttu-id="eb8b5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb8b5-109">Parameters</span></span>

<span data-ttu-id="eb8b5-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="eb8b5-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eb8b5-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eb8b5-111">Return value</span></span>

<span data-ttu-id="eb8b5-112">Type : **[ **ID3DX11EffectSamplerVariable**](id3dx11effectsamplervariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="eb8b5-112">Type: **[**ID3DX11EffectSamplerVariable**](id3dx11effectsamplervariable.md)\***</span></span>

<span data-ttu-id="eb8b5-113">Pointeur vers une variable d’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="eb8b5-113">A pointer to a sampler variable.</span></span> <span data-ttu-id="eb8b5-114">Consultez [**ID3DX11EffectSamplerVariable**](id3dx11effectsamplervariable.md).</span><span class="sxs-lookup"><span data-stu-id="eb8b5-114">See [**ID3DX11EffectSamplerVariable**](id3dx11effectsamplervariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="eb8b5-115">Notes</span><span class="sxs-lookup"><span data-stu-id="eb8b5-115">Remarks</span></span>

<span data-ttu-id="eb8b5-116">AsSampler retourne une version de la variable Effect qui a été spécialisée pour une variable d’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="eb8b5-116">AsSampler returns a version of the effect variable that has been specialized to a sampler variable.</span></span> <span data-ttu-id="eb8b5-117">Comme pour un cast, cette spécialisation retourne un objet non valide si la variable Effect ne contient pas de données d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="eb8b5-117">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain sampler data.</span></span>

<span data-ttu-id="eb8b5-118">Les applications peuvent tester la validité de l’objet retourné en appelant [**IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="eb8b5-118">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="eb8b5-119">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="eb8b5-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="eb8b5-120">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="eb8b5-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="eb8b5-121">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="eb8b5-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="eb8b5-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="eb8b5-122">Requirements</span></span>



| <span data-ttu-id="eb8b5-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb8b5-123">Requirement</span></span> | <span data-ttu-id="eb8b5-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb8b5-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb8b5-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="eb8b5-125">Header</span></span><br/>  | <dl> <span data-ttu-id="eb8b5-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb8b5-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="eb8b5-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="eb8b5-127">Library</span></span><br/> | <dl> <span data-ttu-id="eb8b5-128"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="eb8b5-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb8b5-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb8b5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb8b5-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="eb8b5-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





