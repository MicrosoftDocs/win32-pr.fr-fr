---
title: Méthode ID3DX11EffectUnorderedAccessViewVariable SetUnorderedAccessViewArray (D3dx11effect. h)
description: Définissez un tableau de vues d’accès non ordonnées.
ms.assetid: 12d0da06-990a-42b2-9566-cc5136f48781
keywords:
- Méthode SetUnorderedAccessViewArray Direct3D 11
- Méthode SetUnorderedAccessViewArray Direct3D 11, interface ID3DX11EffectUnorderedAccessViewVariable
- Interface ID3DX11EffectUnorderedAccessViewVariable Direct3D 11, méthode SetUnorderedAccessViewArray
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable.SetUnorderedAccessViewArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 053856f294906cf56acf1f38ca90663ebcc34051
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992157"
---
# <a name="id3dx11effectunorderedaccessviewvariablesetunorderedaccessviewarray-method"></a><span data-ttu-id="1fdcd-106">ID3DX11EffectUnorderedAccessViewVariable :: SetUnorderedAccessViewArray, méthode</span><span class="sxs-lookup"><span data-stu-id="1fdcd-106">ID3DX11EffectUnorderedAccessViewVariable::SetUnorderedAccessViewArray method</span></span>

<span data-ttu-id="1fdcd-107">Définissez un tableau de vues d’accès non ordonnées.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-107">Set an array of unordered-access-views.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fdcd-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1fdcd-108">Syntax</span></span>


```C++
HRESULT SetUnorderedAccessViewArray(
   ID3D11UnorderedAccessView **ppResources,
   UINT                      Offset,
   UINT                      Count
);
```



## <a name="parameters"></a><span data-ttu-id="1fdcd-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1fdcd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fdcd-110">*ppResources*</span><span class="sxs-lookup"><span data-stu-id="1fdcd-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="1fdcd-111">Type : **[ **ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span><span class="sxs-lookup"><span data-stu-id="1fdcd-111">Type: **[**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span></span>

<span data-ttu-id="1fdcd-112">Tableau de pointeurs [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) .</span><span class="sxs-lookup"><span data-stu-id="1fdcd-112">An array of [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) pointers.</span></span>

</dd> <dt>

<span data-ttu-id="1fdcd-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="1fdcd-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="1fdcd-114">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1fdcd-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1fdcd-115">Index du premier mode d’accès non ordonné.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-115">Index of the first unordered-access-view.</span></span>

</dd> <dt>

<span data-ttu-id="1fdcd-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="1fdcd-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="1fdcd-117">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1fdcd-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1fdcd-118">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-118">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fdcd-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1fdcd-119">Return value</span></span>

<span data-ttu-id="1fdcd-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1fdcd-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1fdcd-121">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1fdcd-122">Notes</span><span class="sxs-lookup"><span data-stu-id="1fdcd-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1fdcd-123">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="1fdcd-124">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="1fdcd-125">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="1fdcd-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1fdcd-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1fdcd-126">Requirements</span></span>



| <span data-ttu-id="1fdcd-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1fdcd-127">Requirement</span></span> | <span data-ttu-id="1fdcd-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="1fdcd-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fdcd-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="1fdcd-129">Header</span></span><br/>  | <dl> <span data-ttu-id="1fdcd-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fdcd-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="1fdcd-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1fdcd-131">Library</span></span><br/> | <dl> <span data-ttu-id="1fdcd-132"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="1fdcd-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fdcd-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1fdcd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fdcd-134">ID3DX11EffectUnorderedAccessViewVariable</span><span class="sxs-lookup"><span data-stu-id="1fdcd-134">ID3DX11EffectUnorderedAccessViewVariable</span></span>](id3dx11effectunorderedaccessviewvariable.md)
</dt> </dl>

 

