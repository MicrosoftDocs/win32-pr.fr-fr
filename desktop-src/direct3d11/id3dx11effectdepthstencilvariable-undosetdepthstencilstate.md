---
title: Méthode ID3DX11EffectDepthStencilVariable UndoSetDepthStencilState (D3dx11effect. h)
description: Rétablit un État du stencil de profondeur précédemment défini.
ms.assetid: 558bc777-a520-4235-84d3-db2d9f1ce4b6
keywords:
- Méthode UndoSetDepthStencilState Direct3D 11
- Méthode UndoSetDepthStencilState Direct3D 11, interface ID3DX11EffectDepthStencilVariable
- Interface ID3DX11EffectDepthStencilVariable Direct3D 11, méthode UndoSetDepthStencilState
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.UndoSetDepthStencilState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bd44d486d2613406617f0534046c54818267dd9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996144"
---
# <a name="id3dx11effectdepthstencilvariableundosetdepthstencilstate-method"></a><span data-ttu-id="91461-106">ID3DX11EffectDepthStencilVariable :: UndoSetDepthStencilState, méthode</span><span class="sxs-lookup"><span data-stu-id="91461-106">ID3DX11EffectDepthStencilVariable::UndoSetDepthStencilState method</span></span>

<span data-ttu-id="91461-107">Rétablit un État du stencil de profondeur précédemment défini.</span><span class="sxs-lookup"><span data-stu-id="91461-107">Reverts a previously set depth stencil state.</span></span>

## <a name="syntax"></a><span data-ttu-id="91461-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91461-108">Syntax</span></span>


```C++
HRESULT UndoSetDepthStencilState(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="91461-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91461-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91461-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="91461-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="91461-111">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="91461-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="91461-112">Index dans un tableau d’interfaces de stencil de profondeur.</span><span class="sxs-lookup"><span data-stu-id="91461-112">Index into an array of depth-stencil interfaces.</span></span> <span data-ttu-id="91461-113">S’il n’existe qu’une seule interface de stencil de profondeur, utilisez 0.</span><span class="sxs-lookup"><span data-stu-id="91461-113">If there is only one depth-stencil interface, use 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91461-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="91461-114">Return value</span></span>

<span data-ttu-id="91461-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="91461-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="91461-116">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="91461-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="91461-117">Notes</span><span class="sxs-lookup"><span data-stu-id="91461-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="91461-118">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="91461-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="91461-119">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="91461-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="91461-120">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="91461-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="91461-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="91461-121">Requirements</span></span>



| <span data-ttu-id="91461-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91461-122">Requirement</span></span> | <span data-ttu-id="91461-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="91461-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91461-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="91461-124">Header</span></span><br/>  | <dl> <span data-ttu-id="91461-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="91461-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="91461-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="91461-126">Library</span></span><br/> | <dl> <span data-ttu-id="91461-127"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="91461-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91461-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91461-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91461-129">ID3DX11EffectDepthStencilVariable</span><span class="sxs-lookup"><span data-stu-id="91461-129">ID3DX11EffectDepthStencilVariable</span></span>](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

