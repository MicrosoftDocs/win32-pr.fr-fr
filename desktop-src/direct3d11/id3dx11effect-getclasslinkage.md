---
title: Méthode ID3DX11Effect GetClassLinkage (D3dx11effect. h)
description: Obtient une interface de liaison de classe.
ms.assetid: 006c900d-3464-4666-9fe9-d62ba8cb2b7f
keywords:
- Méthode GetClassLinkage Direct3D 11
- Méthode GetClassLinkage Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, méthode GetClassLinkage
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetClassLinkage
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47b19f14794186f85d0a51f21bc6b2759e512998
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953819"
---
# <a name="id3dx11effectgetclasslinkage-method"></a><span data-ttu-id="59135-106">ID3DX11Effect :: GetClassLinkage, méthode</span><span class="sxs-lookup"><span data-stu-id="59135-106">ID3DX11Effect::GetClassLinkage method</span></span>

<span data-ttu-id="59135-107">Obtient une interface de liaison de classe.</span><span class="sxs-lookup"><span data-stu-id="59135-107">Gets a class linkage interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="59135-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59135-108">Syntax</span></span>


```C++
ID3D11ClassLinkage* GetClassLinkage();
```



## <a name="parameters"></a><span data-ttu-id="59135-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59135-109">Parameters</span></span>

<span data-ttu-id="59135-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="59135-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="59135-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="59135-111">Return value</span></span>

<span data-ttu-id="59135-112">Type : **[ **ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage)\***</span><span class="sxs-lookup"><span data-stu-id="59135-112">Type: **[**ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage)\***</span></span>

<span data-ttu-id="59135-113">Retourne un pointeur vers une interface [**ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage) .</span><span class="sxs-lookup"><span data-stu-id="59135-113">Returns a pointer to an [**ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="59135-114">Notes</span><span class="sxs-lookup"><span data-stu-id="59135-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="59135-115">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="59135-115">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="59135-116">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="59135-116">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="59135-117">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="59135-117">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="59135-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="59135-118">Requirements</span></span>



| <span data-ttu-id="59135-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59135-119">Requirement</span></span> | <span data-ttu-id="59135-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="59135-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59135-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="59135-121">Header</span></span><br/>  | <dl> <span data-ttu-id="59135-122"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="59135-122"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="59135-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="59135-123">Library</span></span><br/> | <dl> <span data-ttu-id="59135-124"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="59135-124"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59135-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59135-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59135-126">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="59135-126">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

 





