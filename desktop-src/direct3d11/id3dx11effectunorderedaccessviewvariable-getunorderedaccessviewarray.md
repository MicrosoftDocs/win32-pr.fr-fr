---
title: Méthode ID3DX11EffectUnorderedAccessViewVariable GetUnorderedAccessViewArray (D3dx11effect. h)
description: Obtient un tableau de vues d’accès non ordonnées.
ms.assetid: 38f838bb-cdcb-43c2-8b98-a188f479e93d
keywords:
- Méthode GetUnorderedAccessViewArray Direct3D 11
- Méthode GetUnorderedAccessViewArray Direct3D 11, interface ID3DX11EffectUnorderedAccessViewVariable
- Interface ID3DX11EffectUnorderedAccessViewVariable Direct3D 11, méthode GetUnorderedAccessViewArray
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable.GetUnorderedAccessViewArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c264b5652287676d0792027f4f0ea8921bdb92f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211837"
---
# <a name="id3dx11effectunorderedaccessviewvariablegetunorderedaccessviewarray-method"></a><span data-ttu-id="af632-106">ID3DX11EffectUnorderedAccessViewVariable :: GetUnorderedAccessViewArray, méthode</span><span class="sxs-lookup"><span data-stu-id="af632-106">ID3DX11EffectUnorderedAccessViewVariable::GetUnorderedAccessViewArray method</span></span>

<span data-ttu-id="af632-107">Obtient un tableau de vues d’accès non ordonnées.</span><span class="sxs-lookup"><span data-stu-id="af632-107">Get an array of unordered-access-views.</span></span>

## <a name="syntax"></a><span data-ttu-id="af632-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af632-108">Syntax</span></span>


```C++
HRESULT GetUnorderedAccessViewArray(
   ID3D11UnorderedAccessView **ppResources,
   UINT                      Offset,
   UINT                      Count
);
```



## <a name="parameters"></a><span data-ttu-id="af632-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af632-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af632-110">*ppResources*</span><span class="sxs-lookup"><span data-stu-id="af632-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="af632-111">Type : **[ **ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span><span class="sxs-lookup"><span data-stu-id="af632-111">Type: **[**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span></span>

<span data-ttu-id="af632-112">Pointeur vers un pointeur [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) qui sera défini sur le tableau UAV lors du retour.</span><span class="sxs-lookup"><span data-stu-id="af632-112">Pointer to an [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) pointer that will be set to the UAV array on return.</span></span>

</dd> <dt>

<span data-ttu-id="af632-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="af632-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="af632-114">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="af632-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="af632-115">Index de la première interface.</span><span class="sxs-lookup"><span data-stu-id="af632-115">Index of the first interface.</span></span>

</dd> <dt>

<span data-ttu-id="af632-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="af632-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="af632-117">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="af632-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="af632-118">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="af632-118">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af632-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="af632-119">Return value</span></span>

<span data-ttu-id="af632-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="af632-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="af632-121">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="af632-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="af632-122">Notes</span><span class="sxs-lookup"><span data-stu-id="af632-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="af632-123">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="af632-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="af632-124">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="af632-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="af632-125">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="af632-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="af632-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="af632-126">Requirements</span></span>



| <span data-ttu-id="af632-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af632-127">Requirement</span></span> | <span data-ttu-id="af632-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="af632-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af632-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="af632-129">Header</span></span><br/>  | <dl> <span data-ttu-id="af632-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="af632-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="af632-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="af632-131">Library</span></span><br/> | <dl> <span data-ttu-id="af632-132"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="af632-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af632-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af632-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af632-134">ID3DX11EffectUnorderedAccessViewVariable</span><span class="sxs-lookup"><span data-stu-id="af632-134">ID3DX11EffectUnorderedAccessViewVariable</span></span>](id3dx11effectunorderedaccessviewvariable.md)
</dt> </dl>

 

