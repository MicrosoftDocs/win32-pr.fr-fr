---
title: Méthode ID3DX11EffectDepthStencilVariable GetDepthStencilState (D3dx11effect. h)
description: Obtient un pointeur vers une interface de stencil de profondeur.
ms.assetid: 3e8f7fc6-960c-45f5-9276-9aa2a5e7a6c9
keywords:
- Méthode GetDepthStencilState Direct3D 11
- Méthode GetDepthStencilState Direct3D 11, interface ID3DX11EffectDepthStencilVariable
- Interface ID3DX11EffectDepthStencilVariable Direct3D 11, méthode GetDepthStencilState
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.GetDepthStencilState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e9276c7a126d5441361a4d449c4ee2ece70d995
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974682"
---
# <a name="id3dx11effectdepthstencilvariablegetdepthstencilstate-method"></a><span data-ttu-id="6db48-106">ID3DX11EffectDepthStencilVariable :: GetDepthStencilState, méthode</span><span class="sxs-lookup"><span data-stu-id="6db48-106">ID3DX11EffectDepthStencilVariable::GetDepthStencilState method</span></span>

<span data-ttu-id="6db48-107">Obtient un pointeur vers une interface de stencil de profondeur.</span><span class="sxs-lookup"><span data-stu-id="6db48-107">Get a pointer to a depth-stencil interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="6db48-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6db48-108">Syntax</span></span>


```C++
HRESULT GetDepthStencilState(
   UINT                    Index,
   ID3D11DepthStencilState **ppDepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="6db48-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6db48-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6db48-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="6db48-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="6db48-111">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6db48-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6db48-112">Index dans un tableau d’interfaces de stencil de profondeur.</span><span class="sxs-lookup"><span data-stu-id="6db48-112">Index into an array of depth-stencil interfaces.</span></span> <span data-ttu-id="6db48-113">S’il n’existe qu’une seule interface de stencil de profondeur, utilisez 0.</span><span class="sxs-lookup"><span data-stu-id="6db48-113">If there is only one depth-stencil interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="6db48-114">*ppDepthStencilState*</span><span class="sxs-lookup"><span data-stu-id="6db48-114">*ppDepthStencilState*</span></span> 
</dt> <dd>

<span data-ttu-id="6db48-115">Type : **[ **ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)\*\***</span><span class="sxs-lookup"><span data-stu-id="6db48-115">Type: **[**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)\*\***</span></span>

<span data-ttu-id="6db48-116">Adresse d’un pointeur vers une interface d’état de fusion (voir [**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)).</span><span class="sxs-lookup"><span data-stu-id="6db48-116">The address of a pointer to a blend-state interface (see [**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6db48-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6db48-117">Return value</span></span>

<span data-ttu-id="6db48-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6db48-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6db48-119">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="6db48-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6db48-120">Notes</span><span class="sxs-lookup"><span data-stu-id="6db48-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6db48-121">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="6db48-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="6db48-122">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="6db48-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="6db48-123">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="6db48-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6db48-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6db48-124">Requirements</span></span>



| <span data-ttu-id="6db48-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6db48-125">Requirement</span></span> | <span data-ttu-id="6db48-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="6db48-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6db48-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="6db48-127">Header</span></span><br/>  | <dl> <span data-ttu-id="6db48-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6db48-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="6db48-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6db48-129">Library</span></span><br/> | <dl> <span data-ttu-id="6db48-130"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="6db48-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6db48-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6db48-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6db48-132">ID3DX11EffectDepthStencilVariable</span><span class="sxs-lookup"><span data-stu-id="6db48-132">ID3DX11EffectDepthStencilVariable</span></span>](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

