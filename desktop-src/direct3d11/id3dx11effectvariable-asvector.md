---
title: Méthode ID3DX11EffectVariable AsVector (D3dx11effect. h)
description: Obtenir une variable vectorielle.
ms.assetid: 995bd9f3-1417-4048-9a23-4dcb3864c77d
keywords:
- Méthode AsVector Direct3D 11
- Méthode AsVector Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode AsVector
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8df994536c818461b0307cdee726e704aaaf8a43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996232"
---
# <a name="id3dx11effectvariableasvector-method"></a><span data-ttu-id="0e11d-106">ID3DX11EffectVariable :: AsVector, méthode</span><span class="sxs-lookup"><span data-stu-id="0e11d-106">ID3DX11EffectVariable::AsVector method</span></span>

<span data-ttu-id="0e11d-107">Obtenir une variable vectorielle.</span><span class="sxs-lookup"><span data-stu-id="0e11d-107">Get a vector variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e11d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e11d-108">Syntax</span></span>


```C++
ID3DX11EffectVectorVariable* AsVector();
```



## <a name="parameters"></a><span data-ttu-id="0e11d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e11d-109">Parameters</span></span>

<span data-ttu-id="0e11d-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="0e11d-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0e11d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0e11d-111">Return value</span></span>

<span data-ttu-id="0e11d-112">Type : **[ **ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="0e11d-112">Type: **[**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md)\***</span></span>

<span data-ttu-id="0e11d-113">Pointeur vers une variable vectorielle.</span><span class="sxs-lookup"><span data-stu-id="0e11d-113">A pointer to a vector variable.</span></span> <span data-ttu-id="0e11d-114">Consultez [**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md).</span><span class="sxs-lookup"><span data-stu-id="0e11d-114">See [**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0e11d-115">Notes</span><span class="sxs-lookup"><span data-stu-id="0e11d-115">Remarks</span></span>

<span data-ttu-id="0e11d-116">AsVector retourne une version de la variable Effect qui a été spécialisée pour une variable Vector.</span><span class="sxs-lookup"><span data-stu-id="0e11d-116">AsVector returns a version of the effect variable that has been specialized to a vector variable.</span></span> <span data-ttu-id="0e11d-117">Comme pour un cast, cette spécialisation retourne un objet non valide si la variable Effect ne contient pas de données vectorielles.</span><span class="sxs-lookup"><span data-stu-id="0e11d-117">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain vector data.</span></span>

<span data-ttu-id="0e11d-118">Les applications peuvent tester la validité de l’objet retourné en appelant [**IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="0e11d-118">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="0e11d-119">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="0e11d-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="0e11d-120">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="0e11d-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="0e11d-121">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="0e11d-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0e11d-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0e11d-122">Requirements</span></span>



| <span data-ttu-id="0e11d-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e11d-123">Requirement</span></span> | <span data-ttu-id="0e11d-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e11d-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e11d-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="0e11d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="0e11d-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e11d-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0e11d-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0e11d-127">Library</span></span><br/> | <dl> <span data-ttu-id="0e11d-128"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="0e11d-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e11d-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e11d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e11d-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="0e11d-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





