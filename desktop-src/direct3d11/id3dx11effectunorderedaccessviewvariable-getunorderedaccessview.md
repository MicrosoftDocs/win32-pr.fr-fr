---
title: Méthode ID3DX11EffectUnorderedAccessViewVariable GetUnorderedAccessView (D3dx11effect. h)
description: Obtenir un mode d’accès non ordonné.
ms.assetid: 46f61c4f-b3ee-4058-99b9-a43ca6944fb2
keywords:
- Méthode GetUnorderedAccessView Direct3D 11
- Méthode GetUnorderedAccessView Direct3D 11, interface ID3DX11EffectUnorderedAccessViewVariable
- Interface ID3DX11EffectUnorderedAccessViewVariable Direct3D 11, méthode GetUnorderedAccessView
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable.GetUnorderedAccessView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7743d15c2380ff4e38bdcae1d38bbd8905cbccda
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996184"
---
# <a name="id3dx11effectunorderedaccessviewvariablegetunorderedaccessview-method"></a><span data-ttu-id="a246f-106">ID3DX11EffectUnorderedAccessViewVariable :: GetUnorderedAccessView, méthode</span><span class="sxs-lookup"><span data-stu-id="a246f-106">ID3DX11EffectUnorderedAccessViewVariable::GetUnorderedAccessView method</span></span>

<span data-ttu-id="a246f-107">Obtenir un mode d’accès non ordonné.</span><span class="sxs-lookup"><span data-stu-id="a246f-107">Get an unordered-access-view.</span></span>

## <a name="syntax"></a><span data-ttu-id="a246f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a246f-108">Syntax</span></span>


```C++
HRESULT GetUnorderedAccessView(
   ID3D11UnorderedAccessView **ppResource
);
```



## <a name="parameters"></a><span data-ttu-id="a246f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a246f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a246f-110">*ppResource*</span><span class="sxs-lookup"><span data-stu-id="a246f-110">*ppResource*</span></span> 
</dt> <dd>

<span data-ttu-id="a246f-111">Type : **[ **ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span><span class="sxs-lookup"><span data-stu-id="a246f-111">Type: **[**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span></span>

<span data-ttu-id="a246f-112">Pointeur vers un pointeur [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) qui sera défini lors du retour.</span><span class="sxs-lookup"><span data-stu-id="a246f-112">Pointer to an [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) pointer that will be set on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a246f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a246f-113">Return value</span></span>

<span data-ttu-id="a246f-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a246f-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a246f-115">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="a246f-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a246f-116">Notes</span><span class="sxs-lookup"><span data-stu-id="a246f-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a246f-117">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="a246f-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="a246f-118">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="a246f-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="a246f-119">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="a246f-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a246f-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a246f-120">Requirements</span></span>



| <span data-ttu-id="a246f-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a246f-121">Requirement</span></span> | <span data-ttu-id="a246f-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="a246f-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a246f-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="a246f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a246f-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a246f-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a246f-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a246f-125">Library</span></span><br/> | <dl> <span data-ttu-id="a246f-126"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="a246f-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a246f-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a246f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a246f-128">ID3DX11EffectUnorderedAccessViewVariable</span><span class="sxs-lookup"><span data-stu-id="a246f-128">ID3DX11EffectUnorderedAccessViewVariable</span></span>](id3dx11effectunorderedaccessviewvariable.md)
</dt> </dl>

 

 





