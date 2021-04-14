---
title: Méthode ID3DX11EffectUnorderedAccessViewVariable SetUnorderedAccessView (D3dx11effect. h)
description: Définissez un mode d’accès non ordonné.
ms.assetid: a147879c-c5cf-4453-b27f-8716cb33962b
keywords:
- Méthode SetUnorderedAccessView Direct3D 11
- Méthode SetUnorderedAccessView Direct3D 11, interface ID3DX11EffectUnorderedAccessViewVariable
- Interface ID3DX11EffectUnorderedAccessViewVariable Direct3D 11, méthode SetUnorderedAccessView
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable.SetUnorderedAccessView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d665ab5b298e3a7549fb068cf0fcc4cce644765
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992160"
---
# <a name="id3dx11effectunorderedaccessviewvariablesetunorderedaccessview-method"></a><span data-ttu-id="6d856-106">ID3DX11EffectUnorderedAccessViewVariable :: SetUnorderedAccessView, méthode</span><span class="sxs-lookup"><span data-stu-id="6d856-106">ID3DX11EffectUnorderedAccessViewVariable::SetUnorderedAccessView method</span></span>

<span data-ttu-id="6d856-107">Définissez un mode d’accès non ordonné.</span><span class="sxs-lookup"><span data-stu-id="6d856-107">Set an unordered-access-view.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d856-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d856-108">Syntax</span></span>


```C++
HRESULT SetUnorderedAccessView(
   ID3D11UnorderedAccessView *pResource
);
```



## <a name="parameters"></a><span data-ttu-id="6d856-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d856-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d856-110">*Préversion*</span><span class="sxs-lookup"><span data-stu-id="6d856-110">*pResource*</span></span> 
</dt> <dd>

<span data-ttu-id="6d856-111">Type : **[ **ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\***</span><span class="sxs-lookup"><span data-stu-id="6d856-111">Type: **[**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\***</span></span>

<span data-ttu-id="6d856-112">Pointeur vers un [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview).</span><span class="sxs-lookup"><span data-stu-id="6d856-112">Pointer to an [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d856-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6d856-113">Return value</span></span>

<span data-ttu-id="6d856-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6d856-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6d856-115">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="6d856-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6d856-116">Notes</span><span class="sxs-lookup"><span data-stu-id="6d856-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6d856-117">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="6d856-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="6d856-118">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="6d856-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="6d856-119">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="6d856-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6d856-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6d856-120">Requirements</span></span>



| <span data-ttu-id="6d856-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d856-121">Requirement</span></span> | <span data-ttu-id="6d856-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d856-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d856-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="6d856-123">Header</span></span><br/>  | <dl> <span data-ttu-id="6d856-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d856-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="6d856-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6d856-125">Library</span></span><br/> | <dl> <span data-ttu-id="6d856-126"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="6d856-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d856-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d856-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d856-128">ID3DX11EffectUnorderedAccessViewVariable</span><span class="sxs-lookup"><span data-stu-id="6d856-128">ID3DX11EffectUnorderedAccessViewVariable</span></span>](id3dx11effectunorderedaccessviewvariable.md)
</dt> </dl>

 

 





