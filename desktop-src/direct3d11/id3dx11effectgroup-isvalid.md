---
title: ID3DX11EffectGroup IsValid, méthode (D3dx11effect. h)
description: Testez un effet pour voir s’il contient une syntaxe valide. | ID3DX11EffectGroup IsValid, méthode (D3dx11effect. h)
ms.assetid: 05829749-cef0-40ed-beab-556a65a1ac96
keywords:
- Méthode IsValid Direct3D 11
- Méthode IsValid Direct3D 11, interface ID3DX11EffectGroup
- Interface ID3DX11EffectGroup Direct3D 11, méthode IsValid
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0d1fd110a0f35f8a288517d72b69a6f5ad9f0ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974566"
---
# <a name="id3dx11effectgroupisvalid-method"></a><span data-ttu-id="63c8a-107">ID3DX11EffectGroup :: IsValid, méthode</span><span class="sxs-lookup"><span data-stu-id="63c8a-107">ID3DX11EffectGroup::IsValid method</span></span>

<span data-ttu-id="63c8a-108">Testez un effet pour voir s’il contient une syntaxe valide.</span><span class="sxs-lookup"><span data-stu-id="63c8a-108">Test an effect to see if it contains valid syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="63c8a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63c8a-109">Syntax</span></span>


```C++
BOOL IsValid();
```



## <a name="parameters"></a><span data-ttu-id="63c8a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63c8a-110">Parameters</span></span>

<span data-ttu-id="63c8a-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="63c8a-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="63c8a-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="63c8a-112">Return value</span></span>

<span data-ttu-id="63c8a-113">Type : **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="63c8a-113">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="63c8a-114">**True** si la syntaxe du code est valide ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="63c8a-114">**TRUE** if the code syntax is valid; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="63c8a-115">Notes</span><span class="sxs-lookup"><span data-stu-id="63c8a-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="63c8a-116">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="63c8a-116">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="63c8a-117">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="63c8a-117">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="63c8a-118">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="63c8a-118">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="63c8a-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="63c8a-119">Requirements</span></span>



| <span data-ttu-id="63c8a-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63c8a-120">Requirement</span></span> | <span data-ttu-id="63c8a-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="63c8a-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63c8a-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="63c8a-122">Header</span></span><br/>  | <dl> <span data-ttu-id="63c8a-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="63c8a-123"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="63c8a-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="63c8a-124">Library</span></span><br/> | <dl> <span data-ttu-id="63c8a-125"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="63c8a-125"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63c8a-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63c8a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63c8a-127">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="63c8a-127">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 

