---
title: Méthode ID3DX11EffectVariable AsRenderTargetView (D3dx11effect. h)
description: Obtenir une variable Render-Target-View.
ms.assetid: 1eec342e-267a-4eab-886a-a309758065c7
keywords:
- Méthode AsRenderTargetView Direct3D 11
- Méthode AsRenderTargetView Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode AsRenderTargetView
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsRenderTargetView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ca6270503ff786b3f4a319e3f068ba76acada7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996320"
---
# <a name="id3dx11effectvariableasrendertargetview-method"></a><span data-ttu-id="619bc-106">ID3DX11EffectVariable :: AsRenderTargetView, méthode</span><span class="sxs-lookup"><span data-stu-id="619bc-106">ID3DX11EffectVariable::AsRenderTargetView method</span></span>

<span data-ttu-id="619bc-107">Obtenir une variable Render-Target-View.</span><span class="sxs-lookup"><span data-stu-id="619bc-107">Get a render-target-view variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="619bc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="619bc-108">Syntax</span></span>


```C++
ID3DX11EffectRenderTargetViewVariable* AsRenderTargetView();
```



## <a name="parameters"></a><span data-ttu-id="619bc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="619bc-109">Parameters</span></span>

<span data-ttu-id="619bc-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="619bc-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="619bc-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="619bc-111">Return value</span></span>

<span data-ttu-id="619bc-112">Type : **[ **ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="619bc-112">Type: **[**ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md)\***</span></span>

<span data-ttu-id="619bc-113">Pointeur vers une variable de vue de rendu-cible.</span><span class="sxs-lookup"><span data-stu-id="619bc-113">A pointer to a render-target-view variable.</span></span> <span data-ttu-id="619bc-114">Consultez [**ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md).</span><span class="sxs-lookup"><span data-stu-id="619bc-114">See [**ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="619bc-115">Notes</span><span class="sxs-lookup"><span data-stu-id="619bc-115">Remarks</span></span>

<span data-ttu-id="619bc-116">Cette méthode retourne une version de la variable Effect qui a été spécialisée pour une variable Render-Target-View.</span><span class="sxs-lookup"><span data-stu-id="619bc-116">This method returns a version of the effect variable that has been specialized to a render-target-view variable.</span></span> <span data-ttu-id="619bc-117">Comme pour un cast, cette spécialisation retourne un objet non valide si la variable Effect ne contient pas de données Render-Target-View.</span><span class="sxs-lookup"><span data-stu-id="619bc-117">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain render-target-view data.</span></span>

<span data-ttu-id="619bc-118">Les applications peuvent tester la validité de l’objet retourné en appelant [**IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="619bc-118">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="619bc-119">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="619bc-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="619bc-120">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="619bc-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="619bc-121">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="619bc-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="619bc-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="619bc-122">Requirements</span></span>



| <span data-ttu-id="619bc-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="619bc-123">Requirement</span></span> | <span data-ttu-id="619bc-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="619bc-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="619bc-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="619bc-125">Header</span></span><br/>  | <dl> <span data-ttu-id="619bc-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="619bc-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="619bc-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="619bc-127">Library</span></span><br/> | <dl> <span data-ttu-id="619bc-128"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="619bc-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="619bc-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="619bc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="619bc-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="619bc-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





