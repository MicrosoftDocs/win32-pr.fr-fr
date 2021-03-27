---
title: Méthode ID3DX11EffectVariable AsScalar (D3dx11effect. h)
description: Obtenir une variable scalaire.
ms.assetid: 5cc02fb3-351a-4309-9145-1ed7d759a650
keywords:
- Méthode AsScalar Direct3D 11
- Méthode AsScalar Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode AsScalar
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsScalar
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e455250ae99075af449793d634fd6b3c2fafc4b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762391"
---
# <a name="id3dx11effectvariableasscalar-method"></a><span data-ttu-id="2fdee-106">ID3DX11EffectVariable :: AsScalar, méthode</span><span class="sxs-lookup"><span data-stu-id="2fdee-106">ID3DX11EffectVariable::AsScalar method</span></span>

<span data-ttu-id="2fdee-107">Obtenir une variable scalaire.</span><span class="sxs-lookup"><span data-stu-id="2fdee-107">Get a scalar variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fdee-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2fdee-108">Syntax</span></span>


```C++
ID3DX11EffectScalarVariable* AsScalar();
```



## <a name="parameters"></a><span data-ttu-id="2fdee-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2fdee-109">Parameters</span></span>

<span data-ttu-id="2fdee-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="2fdee-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2fdee-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2fdee-111">Return value</span></span>

<span data-ttu-id="2fdee-112">Type : **[ **ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="2fdee-112">Type: **[**ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md)\***</span></span>

<span data-ttu-id="2fdee-113">Pointeur vers une variable scalaire.</span><span class="sxs-lookup"><span data-stu-id="2fdee-113">A pointer to a scalar variable.</span></span> <span data-ttu-id="2fdee-114">Consultez [**ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md).</span><span class="sxs-lookup"><span data-stu-id="2fdee-114">See [**ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2fdee-115">Notes</span><span class="sxs-lookup"><span data-stu-id="2fdee-115">Remarks</span></span>

<span data-ttu-id="2fdee-116">AsScalar retourne une version de la variable Effect qui a été spécialisée pour une variable scalaire.</span><span class="sxs-lookup"><span data-stu-id="2fdee-116">AsScalar returns a version of the effect variable that has been specialized to a scalar variable.</span></span> <span data-ttu-id="2fdee-117">Comme pour un cast, cette spécialisation retourne un objet non valide si la variable Effect ne contient pas de données scalaires.</span><span class="sxs-lookup"><span data-stu-id="2fdee-117">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain scalar data.</span></span>

<span data-ttu-id="2fdee-118">Les applications peuvent tester la validité de l’objet retourné en appelant [**IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="2fdee-118">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="2fdee-119">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="2fdee-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="2fdee-120">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="2fdee-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="2fdee-121">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="2fdee-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2fdee-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2fdee-122">Requirements</span></span>



| <span data-ttu-id="2fdee-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2fdee-123">Requirement</span></span> | <span data-ttu-id="2fdee-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="2fdee-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fdee-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="2fdee-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2fdee-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fdee-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="2fdee-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2fdee-127">Library</span></span><br/> | <dl> <span data-ttu-id="2fdee-128"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="2fdee-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fdee-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2fdee-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fdee-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="2fdee-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





