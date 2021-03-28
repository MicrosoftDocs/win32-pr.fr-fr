---
title: Méthode ID3DX11EffectBlendVariable SetBlendState (D3dx11effect. h)
description: Définit l’état de fusion d’un effet.
ms.assetid: 46100721-65a3-46de-aa22-3e7e2fb7b960
keywords:
- Méthode SetBlendState Direct3D 11
- Méthode SetBlendState Direct3D 11, interface ID3DX11EffectBlendVariable
- Interface ID3DX11EffectBlendVariable Direct3D 11, méthode SetBlendState
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.SetBlendState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ce781f29c521df7b81821cb19a56e6fd3999310
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762217"
---
# <a name="id3dx11effectblendvariablesetblendstate-method"></a><span data-ttu-id="68011-106">ID3DX11EffectBlendVariable :: SetBlendState, méthode</span><span class="sxs-lookup"><span data-stu-id="68011-106">ID3DX11EffectBlendVariable::SetBlendState method</span></span>

<span data-ttu-id="68011-107">Définit l’état de fusion d’un effet.</span><span class="sxs-lookup"><span data-stu-id="68011-107">Sets an effect's blend-state.</span></span>

## <a name="syntax"></a><span data-ttu-id="68011-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68011-108">Syntax</span></span>


```C++
HRESULT SetBlendState(
   UINT             Index,
   ID3D11BlendState *pBlendState
);
```



## <a name="parameters"></a><span data-ttu-id="68011-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="68011-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68011-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="68011-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="68011-111">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="68011-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="68011-112">Indexez dans un tableau d’interfaces d’état de fusion.</span><span class="sxs-lookup"><span data-stu-id="68011-112">Index into an array of blend-state interfaces.</span></span> <span data-ttu-id="68011-113">S’il n’existe qu’une seule interface d’état de fusion, utilisez 0.</span><span class="sxs-lookup"><span data-stu-id="68011-113">If there is only one blend-state interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="68011-114">*pBlendState*</span><span class="sxs-lookup"><span data-stu-id="68011-114">*pBlendState*</span></span> 
</dt> <dd>

<span data-ttu-id="68011-115">Type : **[ **ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)\***</span><span class="sxs-lookup"><span data-stu-id="68011-115">Type: **[**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)\***</span></span>

<span data-ttu-id="68011-116">Pointeur vers une interface [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate) contenant l’état de fusion à définir.</span><span class="sxs-lookup"><span data-stu-id="68011-116">A pointer to an [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate) interface containing the blend-state to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68011-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="68011-117">Return value</span></span>

<span data-ttu-id="68011-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="68011-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="68011-119">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="68011-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="68011-120">Notes</span><span class="sxs-lookup"><span data-stu-id="68011-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="68011-121">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="68011-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="68011-122">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="68011-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="68011-123">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="68011-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="68011-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="68011-124">Requirements</span></span>



| <span data-ttu-id="68011-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68011-125">Requirement</span></span> | <span data-ttu-id="68011-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="68011-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68011-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="68011-127">Header</span></span><br/>  | <dl> <span data-ttu-id="68011-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="68011-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="68011-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="68011-129">Library</span></span><br/> | <dl> <span data-ttu-id="68011-130"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="68011-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68011-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68011-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68011-132">ID3DX11EffectBlendVariable</span><span class="sxs-lookup"><span data-stu-id="68011-132">ID3DX11EffectBlendVariable</span></span>](id3dx11effectblendvariable.md)
</dt> </dl>

 

