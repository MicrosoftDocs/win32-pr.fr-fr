---
title: Méthode ID3DX11EffectDepthStencilViewVariable SetDepthStencil (D3dx11effect. h)
description: Définissez une ressource de vue de gabarit de profondeur.
ms.assetid: 35cbcd3b-6fc8-448d-a82e-724f91038d07
keywords:
- Méthode SetDepthStencil Direct3D 11
- Méthode SetDepthStencil Direct3D 11, interface ID3DX11EffectDepthStencilViewVariable
- Interface ID3DX11EffectDepthStencilViewVariable Direct3D 11, méthode SetDepthStencil
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.SetDepthStencil
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 723be51bc769982acf43c19482978bd581cafa13
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992248"
---
# <a name="id3dx11effectdepthstencilviewvariablesetdepthstencil-method"></a><span data-ttu-id="9d39a-106">ID3DX11EffectDepthStencilViewVariable :: SetDepthStencil, méthode</span><span class="sxs-lookup"><span data-stu-id="9d39a-106">ID3DX11EffectDepthStencilViewVariable::SetDepthStencil method</span></span>

<span data-ttu-id="9d39a-107">Définissez une ressource de vue de gabarit de profondeur.</span><span class="sxs-lookup"><span data-stu-id="9d39a-107">Set a depth-stencil-view resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d39a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d39a-108">Syntax</span></span>


```C++
HRESULT SetDepthStencil(
   ID3D11DepthStencilView *pResource
);
```



## <a name="parameters"></a><span data-ttu-id="9d39a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d39a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d39a-110">*Préversion*</span><span class="sxs-lookup"><span data-stu-id="9d39a-110">*pResource*</span></span> 
</dt> <dd>

<span data-ttu-id="9d39a-111">Type : **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\***</span><span class="sxs-lookup"><span data-stu-id="9d39a-111">Type: **[**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\***</span></span>

<span data-ttu-id="9d39a-112">Pointeur vers une interface de vue de stencil-profondeur.</span><span class="sxs-lookup"><span data-stu-id="9d39a-112">A pointer to a depth-stencil-view interface.</span></span> <span data-ttu-id="9d39a-113">Consultez [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span><span class="sxs-lookup"><span data-stu-id="9d39a-113">See [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d39a-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9d39a-114">Return value</span></span>

<span data-ttu-id="9d39a-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9d39a-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9d39a-116">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="9d39a-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9d39a-117">Notes</span><span class="sxs-lookup"><span data-stu-id="9d39a-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9d39a-118">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="9d39a-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9d39a-119">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="9d39a-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9d39a-120">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="9d39a-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9d39a-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9d39a-121">Requirements</span></span>



| <span data-ttu-id="9d39a-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d39a-122">Requirement</span></span> | <span data-ttu-id="9d39a-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d39a-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d39a-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="9d39a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9d39a-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d39a-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9d39a-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9d39a-126">Library</span></span><br/> | <dl> <span data-ttu-id="9d39a-127"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="9d39a-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d39a-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d39a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d39a-129">ID3DX11EffectDepthStencilViewVariable</span><span class="sxs-lookup"><span data-stu-id="9d39a-129">ID3DX11EffectDepthStencilViewVariable</span></span>](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 

 





