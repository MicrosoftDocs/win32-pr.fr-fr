---
title: Méthode ID3DX11EffectVariable AsClassInstance (D3dx11effect. h)
description: Obtenir une variable d’instance de classe.
ms.assetid: c1d4adb5-7cd2-4ba2-9a91-3d03f9596a10
keywords:
- Méthode AsClassInstance Direct3D 11
- Méthode AsClassInstance Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode AsClassInstance
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17dc9124f4b9a24ead503694c10a4a2d2205ed3b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992144"
---
# <a name="id3dx11effectvariableasclassinstance-method"></a><span data-ttu-id="217d0-106">ID3DX11EffectVariable :: AsClassInstance, méthode</span><span class="sxs-lookup"><span data-stu-id="217d0-106">ID3DX11EffectVariable::AsClassInstance method</span></span>

<span data-ttu-id="217d0-107">Obtenir une variable d’instance de classe.</span><span class="sxs-lookup"><span data-stu-id="217d0-107">Get a class-instance variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="217d0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="217d0-108">Syntax</span></span>


```C++
ID3DX11EffectClassInstanceVariable* AsClassInstance();
```



## <a name="parameters"></a><span data-ttu-id="217d0-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="217d0-109">Parameters</span></span>

<span data-ttu-id="217d0-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="217d0-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="217d0-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="217d0-111">Return value</span></span>

<span data-ttu-id="217d0-112">Type : **[ **ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="217d0-112">Type: **[**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\***</span></span>

<span data-ttu-id="217d0-113">Pointeur vers une variable d’instance de classe.</span><span class="sxs-lookup"><span data-stu-id="217d0-113">A pointer to class-instance variable.</span></span> <span data-ttu-id="217d0-114">Consultez [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md).</span><span class="sxs-lookup"><span data-stu-id="217d0-114">See [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="217d0-115">Notes</span><span class="sxs-lookup"><span data-stu-id="217d0-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="217d0-116">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="217d0-116">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="217d0-117">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="217d0-117">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="217d0-118">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="217d0-118">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="217d0-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="217d0-119">Requirements</span></span>



| <span data-ttu-id="217d0-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="217d0-120">Requirement</span></span> | <span data-ttu-id="217d0-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="217d0-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="217d0-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="217d0-122">Header</span></span><br/>  | <dl> <span data-ttu-id="217d0-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="217d0-123"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="217d0-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="217d0-124">Library</span></span><br/> | <dl> <span data-ttu-id="217d0-125"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="217d0-125"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="217d0-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="217d0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="217d0-127">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="217d0-127">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





