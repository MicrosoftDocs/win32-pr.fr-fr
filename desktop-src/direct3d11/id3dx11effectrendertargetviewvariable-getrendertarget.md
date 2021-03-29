---
title: Méthode ID3DX11EffectRenderTargetViewVariable GetRenderTarget (D3dx11effect. h)
description: Obtenir une cible de rendu.
ms.assetid: 96984d0a-b8f4-444a-9683-3c37d8274d75
keywords:
- Méthode GetRenderTarget Direct3D 11
- Méthode GetRenderTarget Direct3D 11, interface ID3DX11EffectRenderTargetViewVariable
- Interface ID3DX11EffectRenderTargetViewVariable Direct3D 11, méthode GetRenderTarget
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable.GetRenderTarget
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfa86dd3a5c950e18ae97ba1987ee0f44b9f658c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996256"
---
# <a name="id3dx11effectrendertargetviewvariablegetrendertarget-method"></a><span data-ttu-id="01cd5-106">ID3DX11EffectRenderTargetViewVariable :: GetRenderTarget, méthode</span><span class="sxs-lookup"><span data-stu-id="01cd5-106">ID3DX11EffectRenderTargetViewVariable::GetRenderTarget method</span></span>

<span data-ttu-id="01cd5-107">Obtenir une cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="01cd5-107">Get a render-target.</span></span>

## <a name="syntax"></a><span data-ttu-id="01cd5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01cd5-108">Syntax</span></span>


```C++
HRESULT GetRenderTarget(
   ID3D11RenderTargetView **ppResource
);
```



## <a name="parameters"></a><span data-ttu-id="01cd5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01cd5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01cd5-110">*ppResource*</span><span class="sxs-lookup"><span data-stu-id="01cd5-110">*ppResource*</span></span> 
</dt> <dd>

<span data-ttu-id="01cd5-111">Type : **[ **ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\*\***</span><span class="sxs-lookup"><span data-stu-id="01cd5-111">Type: **[**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\*\***</span></span>

<span data-ttu-id="01cd5-112">Adresse d’un pointeur vers une interface de vue de rendu-cible.</span><span class="sxs-lookup"><span data-stu-id="01cd5-112">The address of a pointer to a render-target-view interface.</span></span> <span data-ttu-id="01cd5-113">Consultez [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span><span class="sxs-lookup"><span data-stu-id="01cd5-113">See [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01cd5-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="01cd5-114">Return value</span></span>

<span data-ttu-id="01cd5-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="01cd5-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="01cd5-116">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="01cd5-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="01cd5-117">Notes</span><span class="sxs-lookup"><span data-stu-id="01cd5-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="01cd5-118">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="01cd5-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="01cd5-119">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="01cd5-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="01cd5-120">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="01cd5-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="01cd5-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="01cd5-121">Requirements</span></span>



| <span data-ttu-id="01cd5-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01cd5-122">Requirement</span></span> | <span data-ttu-id="01cd5-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="01cd5-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01cd5-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="01cd5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="01cd5-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="01cd5-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="01cd5-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="01cd5-126">Library</span></span><br/> | <dl> <span data-ttu-id="01cd5-127"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="01cd5-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01cd5-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01cd5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01cd5-129">ID3DX11EffectRenderTargetViewVariable</span><span class="sxs-lookup"><span data-stu-id="01cd5-129">ID3DX11EffectRenderTargetViewVariable</span></span>](id3dx11effectrendertargetviewvariable.md)
</dt> </dl>

 

 





