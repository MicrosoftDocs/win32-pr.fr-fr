---
title: Méthode ID3DX11EffectVariable GetParentConstantBuffer (D3dx11effect. h)
description: Obtient une mémoire tampon constante. | Méthode ID3DX11EffectVariable GetParentConstantBuffer (D3dx11effect. h)
ms.assetid: 43b46b05-951e-4c52-8bc7-4bb5f657ea78
keywords:
- Méthode GetParentConstantBuffer Direct3D 11
- Méthode GetParentConstantBuffer Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode GetParentConstantBuffer
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetParentConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa424b91b72dca5539fd0f96a1380e86d1f23f58
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996248"
---
# <a name="id3dx11effectvariablegetparentconstantbuffer-method"></a><span data-ttu-id="0da21-107">ID3DX11EffectVariable :: GetParentConstantBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="0da21-107">ID3DX11EffectVariable::GetParentConstantBuffer method</span></span>

<span data-ttu-id="0da21-108">Obtient une mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="0da21-108">Get a constant buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="0da21-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0da21-109">Syntax</span></span>


```C++
ID3DX11EffectConstantBuffer* GetParentConstantBuffer();
```



## <a name="parameters"></a><span data-ttu-id="0da21-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0da21-110">Parameters</span></span>

<span data-ttu-id="0da21-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="0da21-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0da21-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0da21-112">Return value</span></span>

<span data-ttu-id="0da21-113">Type : **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0da21-113">Type: **[**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span></span>

<span data-ttu-id="0da21-114">Pointeur vers un [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="0da21-114">A pointer to a [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0da21-115">Notes</span><span class="sxs-lookup"><span data-stu-id="0da21-115">Remarks</span></span>

<span data-ttu-id="0da21-116">Les variables d’effet sont lues ou écrites dans une mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="0da21-116">Effect variables are read-from or written-to a constant buffer.</span></span>

> [!Note]  
> <span data-ttu-id="0da21-117">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="0da21-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="0da21-118">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="0da21-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="0da21-119">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="0da21-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0da21-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0da21-120">Requirements</span></span>



| <span data-ttu-id="0da21-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0da21-121">Requirement</span></span> | <span data-ttu-id="0da21-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="0da21-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0da21-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="0da21-123">Header</span></span><br/>  | <dl> <span data-ttu-id="0da21-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0da21-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0da21-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0da21-125">Library</span></span><br/> | <dl> <span data-ttu-id="0da21-126"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="0da21-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0da21-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0da21-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0da21-128">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="0da21-128">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





