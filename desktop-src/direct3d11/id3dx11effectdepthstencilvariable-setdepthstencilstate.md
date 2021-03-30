---
title: Méthode ID3DX11EffectDepthStencilVariable SetDepthStencilState (D3dx11effect. h)
description: Définit l’état du stencil de profondeur.
ms.assetid: 4ece246f-4466-4790-8f38-450b67fff7c6
keywords:
- Méthode SetDepthStencilState Direct3D 11
- Méthode SetDepthStencilState Direct3D 11, interface ID3DX11EffectDepthStencilVariable
- Interface ID3DX11EffectDepthStencilVariable Direct3D 11, méthode SetDepthStencilState
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.SetDepthStencilState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b82fac869cb15bced76fdc1335967c6f7d017f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974679"
---
# <a name="id3dx11effectdepthstencilvariablesetdepthstencilstate-method"></a><span data-ttu-id="4fc45-106">ID3DX11EffectDepthStencilVariable :: SetDepthStencilState, méthode</span><span class="sxs-lookup"><span data-stu-id="4fc45-106">ID3DX11EffectDepthStencilVariable::SetDepthStencilState method</span></span>

<span data-ttu-id="4fc45-107">Définit l’état du stencil de profondeur.</span><span class="sxs-lookup"><span data-stu-id="4fc45-107">Sets the depth stencil state.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fc45-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4fc45-108">Syntax</span></span>


```C++
HRESULT SetDepthStencilState(
   UINT                    Index,
   ID3D11DepthStencilState *pDepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="4fc45-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4fc45-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fc45-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="4fc45-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="4fc45-111">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4fc45-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4fc45-112">Index dans un tableau d’interfaces de stencil de profondeur.</span><span class="sxs-lookup"><span data-stu-id="4fc45-112">Index into an array of depth-stencil interfaces.</span></span> <span data-ttu-id="4fc45-113">S’il n’existe qu’une seule interface de stencil de profondeur, utilisez 0.</span><span class="sxs-lookup"><span data-stu-id="4fc45-113">If there is only one depth-stencil interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="4fc45-114">*pDepthStencilState*</span><span class="sxs-lookup"><span data-stu-id="4fc45-114">*pDepthStencilState*</span></span> 
</dt> <dd>

<span data-ttu-id="4fc45-115">Type : **[ **ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)\***</span><span class="sxs-lookup"><span data-stu-id="4fc45-115">Type: **[**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)\***</span></span>

<span data-ttu-id="4fc45-116">Pointeur vers une interface [**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate) contenant le nouvel État du stencil de profondeur.</span><span class="sxs-lookup"><span data-stu-id="4fc45-116">Pointer to an [**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate) interface containing the new depth stencil state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fc45-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4fc45-117">Return value</span></span>

<span data-ttu-id="4fc45-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4fc45-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4fc45-119">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="4fc45-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4fc45-120">Notes</span><span class="sxs-lookup"><span data-stu-id="4fc45-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4fc45-121">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="4fc45-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="4fc45-122">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="4fc45-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="4fc45-123">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="4fc45-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4fc45-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4fc45-124">Requirements</span></span>



| <span data-ttu-id="4fc45-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4fc45-125">Requirement</span></span> | <span data-ttu-id="4fc45-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="4fc45-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fc45-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="4fc45-127">Header</span></span><br/>  | <dl> <span data-ttu-id="4fc45-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fc45-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4fc45-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4fc45-129">Library</span></span><br/> | <dl> <span data-ttu-id="4fc45-130"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="4fc45-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fc45-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fc45-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fc45-132">ID3DX11EffectDepthStencilVariable</span><span class="sxs-lookup"><span data-stu-id="4fc45-132">ID3DX11EffectDepthStencilVariable</span></span>](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

