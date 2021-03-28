---
title: Méthode ID3DX11EffectBlendVariable GetBackingStore (D3dx11effect. h)
description: Obtient un pointeur vers une variable d’état de fusion.
ms.assetid: 809daaad-9bf0-48fb-ae91-f237c43db324
keywords:
- Méthode GetBackingStore Direct3D 11
- Méthode GetBackingStore Direct3D 11, interface ID3DX11EffectBlendVariable
- Interface ID3DX11EffectBlendVariable Direct3D 11, méthode GetBackingStore
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0220481b58931edace2a5dfe7298d83f7bd1325
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211890"
---
# <a name="id3dx11effectblendvariablegetbackingstore-method"></a><span data-ttu-id="abbcc-106">ID3DX11EffectBlendVariable :: GetBackingStore, méthode</span><span class="sxs-lookup"><span data-stu-id="abbcc-106">ID3DX11EffectBlendVariable::GetBackingStore method</span></span>

<span data-ttu-id="abbcc-107">Obtient un pointeur vers une variable d’état de fusion.</span><span class="sxs-lookup"><span data-stu-id="abbcc-107">Get a pointer to a blend-state variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="abbcc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="abbcc-108">Syntax</span></span>


```C++
HRESULT GetBackingStore(
   UINT             Index,
   D3D11_BLEND_DESC *pBlendDesc
);
```



## <a name="parameters"></a><span data-ttu-id="abbcc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="abbcc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abbcc-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="abbcc-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="abbcc-111">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="abbcc-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="abbcc-112">Index dans un tableau de descriptions d’état de fusion.</span><span class="sxs-lookup"><span data-stu-id="abbcc-112">Index into an array of blend-state descriptions.</span></span> <span data-ttu-id="abbcc-113">S’il n’existe qu’une seule variable d’état de fusion dans l’effet, utilisez 0.</span><span class="sxs-lookup"><span data-stu-id="abbcc-113">If there is only one blend-state variable in the effect, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="abbcc-114">*pBlendDesc*</span><span class="sxs-lookup"><span data-stu-id="abbcc-114">*pBlendDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="abbcc-115">Type : **[ **d3d11 \_ Blend \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)\***</span><span class="sxs-lookup"><span data-stu-id="abbcc-115">Type: **[**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)\***</span></span>

<span data-ttu-id="abbcc-116">Pointeur vers une description d’état de fusion (consultez [**d3d11 \_ Blend \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)).</span><span class="sxs-lookup"><span data-stu-id="abbcc-116">A pointer to a blend-state description (see [**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abbcc-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="abbcc-117">Return value</span></span>

<span data-ttu-id="abbcc-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="abbcc-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="abbcc-119">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="abbcc-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="abbcc-120">Notes</span><span class="sxs-lookup"><span data-stu-id="abbcc-120">Remarks</span></span>

<span data-ttu-id="abbcc-121">Les variables d’effet sont enregistrées en mémoire dans le magasin de stockage ; Quand une technique est appliquée, les valeurs du magasin de stockage sont copiées sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="abbcc-121">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="abbcc-122">Les données du magasin de stockage peuvent être utilisées pour recréer la variable si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="abbcc-122">Backing store data can used to recreate the variable when necessary.</span></span>

> [!Note]  
> <span data-ttu-id="abbcc-123">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="abbcc-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="abbcc-124">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="abbcc-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="abbcc-125">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="abbcc-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="abbcc-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="abbcc-126">Requirements</span></span>



| <span data-ttu-id="abbcc-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="abbcc-127">Requirement</span></span> | <span data-ttu-id="abbcc-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="abbcc-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abbcc-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="abbcc-129">Header</span></span><br/>  | <dl> <span data-ttu-id="abbcc-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="abbcc-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="abbcc-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="abbcc-131">Library</span></span><br/> | <dl> <span data-ttu-id="abbcc-132"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="abbcc-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abbcc-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abbcc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abbcc-134">ID3DX11EffectBlendVariable</span><span class="sxs-lookup"><span data-stu-id="abbcc-134">ID3DX11EffectBlendVariable</span></span>](id3dx11effectblendvariable.md)
</dt> </dl>

 

