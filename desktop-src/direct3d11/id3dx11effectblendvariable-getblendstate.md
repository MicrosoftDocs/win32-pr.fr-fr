---
title: Méthode ID3DX11EffectBlendVariable GetBlendState (D3dx11effect. h)
description: Obtient un pointeur vers une interface d’état de fusion.
ms.assetid: ab4ee765-b5ad-4dc3-9b00-48052528d3bd
keywords:
- Méthode GetBlendState Direct3D 11
- Méthode GetBlendState Direct3D 11, interface ID3DX11EffectBlendVariable
- Interface ID3DX11EffectBlendVariable Direct3D 11, méthode GetBlendState
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.GetBlendState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48092b496fa8a38be7c9dd8aea67a26e8b56f4f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323186"
---
# <a name="id3dx11effectblendvariablegetblendstate-method"></a><span data-ttu-id="26922-106">ID3DX11EffectBlendVariable :: GetBlendState, méthode</span><span class="sxs-lookup"><span data-stu-id="26922-106">ID3DX11EffectBlendVariable::GetBlendState method</span></span>

<span data-ttu-id="26922-107">Obtient un pointeur vers une interface d’état de fusion.</span><span class="sxs-lookup"><span data-stu-id="26922-107">Get a pointer to a blend-state interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="26922-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26922-108">Syntax</span></span>


```C++
HRESULT GetBlendState(
   UINT             Index,
   ID3D11BlendState **ppBlendState
);
```



## <a name="parameters"></a><span data-ttu-id="26922-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26922-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26922-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="26922-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="26922-111">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="26922-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="26922-112">Indexez dans un tableau d’interfaces d’état de fusion.</span><span class="sxs-lookup"><span data-stu-id="26922-112">Index into an array of blend-state interfaces.</span></span> <span data-ttu-id="26922-113">S’il n’existe qu’une seule interface d’état de fusion, utilisez 0.</span><span class="sxs-lookup"><span data-stu-id="26922-113">If there is only one blend-state interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="26922-114">*ppBlendState*</span><span class="sxs-lookup"><span data-stu-id="26922-114">*ppBlendState*</span></span> 
</dt> <dd>

<span data-ttu-id="26922-115">Type : **[ **ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)\*\***</span><span class="sxs-lookup"><span data-stu-id="26922-115">Type: **[**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)\*\***</span></span>

<span data-ttu-id="26922-116">Adresse d’un pointeur vers une interface d’état de fusion (voir [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)).</span><span class="sxs-lookup"><span data-stu-id="26922-116">The address of a pointer to a blend-state interface (see [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26922-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="26922-117">Return value</span></span>

<span data-ttu-id="26922-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="26922-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="26922-119">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="26922-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="26922-120">Notes</span><span class="sxs-lookup"><span data-stu-id="26922-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="26922-121">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="26922-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="26922-122">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="26922-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="26922-123">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="26922-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="26922-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="26922-124">Requirements</span></span>



| <span data-ttu-id="26922-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26922-125">Requirement</span></span> | <span data-ttu-id="26922-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="26922-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26922-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="26922-127">Header</span></span><br/>  | <dl> <span data-ttu-id="26922-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="26922-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="26922-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="26922-129">Library</span></span><br/> | <dl> <span data-ttu-id="26922-130"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="26922-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26922-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26922-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26922-132">ID3DX11EffectBlendVariable</span><span class="sxs-lookup"><span data-stu-id="26922-132">ID3DX11EffectBlendVariable</span></span>](id3dx11effectblendvariable.md)
</dt> </dl>

 

