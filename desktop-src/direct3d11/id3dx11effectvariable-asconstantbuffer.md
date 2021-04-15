---
title: Méthode ID3DX11EffectVariable AsConstantBuffer (D3dx11effect. h)
description: Obtient une mémoire tampon constante. | Méthode ID3DX11EffectVariable AsConstantBuffer (D3dx11effect. h)
ms.assetid: b8d8b43c-4626-43b6-8a49-8ffa7cb48427
keywords:
- Méthode AsConstantBuffer Direct3D 11
- Méthode AsConstantBuffer Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode AsConstantBuffer
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee4caca60216df0c04a773da22150dbc6f7be717
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992217"
---
# <a name="id3dx11effectvariableasconstantbuffer-method"></a><span data-ttu-id="23a20-107">ID3DX11EffectVariable :: AsConstantBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="23a20-107">ID3DX11EffectVariable::AsConstantBuffer method</span></span>

<span data-ttu-id="23a20-108">Obtient une mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="23a20-108">Get a constant buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="23a20-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23a20-109">Syntax</span></span>


```C++
ID3DX11EffectConstantBuffer* AsConstantBuffer();
```



## <a name="parameters"></a><span data-ttu-id="23a20-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23a20-110">Parameters</span></span>

<span data-ttu-id="23a20-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="23a20-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="23a20-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="23a20-112">Return value</span></span>

<span data-ttu-id="23a20-113">Type : **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="23a20-113">Type: **[**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span></span>

<span data-ttu-id="23a20-114">Pointeur vers une mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="23a20-114">A pointer to a constant buffer.</span></span> <span data-ttu-id="23a20-115">Consultez [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="23a20-115">See [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="23a20-116">Notes</span><span class="sxs-lookup"><span data-stu-id="23a20-116">Remarks</span></span>

<span data-ttu-id="23a20-117">AsConstantBuffer retourne une version de la variable Effect qui a été spécialisée dans une mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="23a20-117">AsConstantBuffer returns a version of the effect variable that has been specialized to a constant buffer.</span></span> <span data-ttu-id="23a20-118">Comme pour un cast, cette spécialisation retourne un objet non valide si la variable Effect ne contient pas de données de mémoire tampon constantes.</span><span class="sxs-lookup"><span data-stu-id="23a20-118">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain constant buffer data.</span></span>

<span data-ttu-id="23a20-119">Les applications peuvent tester la validité de l’objet retourné en appelant [**IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="23a20-119">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="23a20-120">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="23a20-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="23a20-121">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="23a20-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="23a20-122">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="23a20-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="23a20-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="23a20-123">Requirements</span></span>



| <span data-ttu-id="23a20-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23a20-124">Requirement</span></span> | <span data-ttu-id="23a20-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="23a20-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23a20-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="23a20-126">Header</span></span><br/>  | <dl> <span data-ttu-id="23a20-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="23a20-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="23a20-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="23a20-128">Library</span></span><br/> | <dl> <span data-ttu-id="23a20-129"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="23a20-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23a20-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23a20-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23a20-131">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="23a20-131">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





