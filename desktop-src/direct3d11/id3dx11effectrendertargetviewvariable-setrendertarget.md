---
title: Méthode ID3DX11EffectRenderTargetViewVariable SetRenderTarget (D3dx11effect. h)
description: Définissez une cible de rendu.
ms.assetid: caac7190-4f58-4a8e-9764-b6120ac14856
keywords:
- Méthode SetRenderTarget Direct3D 11
- Méthode SetRenderTarget Direct3D 11, interface ID3DX11EffectRenderTargetViewVariable
- Interface ID3DX11EffectRenderTargetViewVariable Direct3D 11, méthode SetRenderTarget
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable.SetRenderTarget
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb53f0dff19fcd8990575dc9b305b0fb2f7e149b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870209"
---
# <a name="id3dx11effectrendertargetviewvariablesetrendertarget-method"></a><span data-ttu-id="f05fa-106">ID3DX11EffectRenderTargetViewVariable :: SetRenderTarget, méthode</span><span class="sxs-lookup"><span data-stu-id="f05fa-106">ID3DX11EffectRenderTargetViewVariable::SetRenderTarget method</span></span>

<span data-ttu-id="f05fa-107">Définissez une cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="f05fa-107">Set a render-target.</span></span>

## <a name="syntax"></a><span data-ttu-id="f05fa-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f05fa-108">Syntax</span></span>


```C++
HRESULT SetRenderTarget(
   ID3D11RenderTargetView *pResource
);
```



## <a name="parameters"></a><span data-ttu-id="f05fa-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f05fa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f05fa-110">*Préversion*</span><span class="sxs-lookup"><span data-stu-id="f05fa-110">*pResource*</span></span> 
</dt> <dd>

<span data-ttu-id="f05fa-111">Type : **[ **ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\***</span><span class="sxs-lookup"><span data-stu-id="f05fa-111">Type: **[**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\***</span></span>

<span data-ttu-id="f05fa-112">Pointeur vers une interface de vue de rendu-cible.</span><span class="sxs-lookup"><span data-stu-id="f05fa-112">A pointer to a render-target-view interface.</span></span> <span data-ttu-id="f05fa-113">Consultez [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span><span class="sxs-lookup"><span data-stu-id="f05fa-113">See [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f05fa-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f05fa-114">Return value</span></span>

<span data-ttu-id="f05fa-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f05fa-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f05fa-116">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="f05fa-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f05fa-117">Notes</span><span class="sxs-lookup"><span data-stu-id="f05fa-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f05fa-118">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="f05fa-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f05fa-119">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="f05fa-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f05fa-120">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f05fa-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f05fa-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f05fa-121">Requirements</span></span>



| <span data-ttu-id="f05fa-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f05fa-122">Requirement</span></span> | <span data-ttu-id="f05fa-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f05fa-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f05fa-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="f05fa-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f05fa-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f05fa-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f05fa-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f05fa-126">Library</span></span><br/> | <dl> <span data-ttu-id="f05fa-127"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="f05fa-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f05fa-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f05fa-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f05fa-129">ID3DX11EffectRenderTargetViewVariable</span><span class="sxs-lookup"><span data-stu-id="f05fa-129">ID3DX11EffectRenderTargetViewVariable</span></span>](id3dx11effectrendertargetviewvariable.md)
</dt> </dl>

 

 





