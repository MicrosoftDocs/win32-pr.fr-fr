---
title: Interface ID3DX11EffectClassInstanceVariable (D3dx11effect. h)
description: Accède à une instance de classe.
ms.assetid: 64bbae01-1b54-4b3c-9115-80d7b8911ff8
keywords:
- Interface ID3DX11EffectClassInstanceVariable Direct3D 11
- Interface ID3DX11EffectClassInstanceVariable Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectClassInstanceVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56e8b6c7ca76dd595363fa0cd80753fce0b66b2e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323370"
---
# <a name="id3dx11effectclassinstancevariable-interface"></a><span data-ttu-id="aaaa4-105">Interface ID3DX11EffectClassInstanceVariable</span><span class="sxs-lookup"><span data-stu-id="aaaa4-105">ID3DX11EffectClassInstanceVariable interface</span></span>

<span data-ttu-id="aaaa4-106">Accède à une instance de classe.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-106">Accesses a class instance.</span></span>

## <a name="members"></a><span data-ttu-id="aaaa4-107">Membres</span><span class="sxs-lookup"><span data-stu-id="aaaa4-107">Members</span></span>

<span data-ttu-id="aaaa4-108">L’interface **ID3DX11EffectClassInstanceVariable** hérite de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="aaaa4-108">The **ID3DX11EffectClassInstanceVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="aaaa4-109">**ID3DX11EffectClassInstanceVariable** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="aaaa4-109">**ID3DX11EffectClassInstanceVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="aaaa4-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="aaaa4-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="aaaa4-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="aaaa4-111">Methods</span></span>

<span data-ttu-id="aaaa4-112">L’interface **ID3DX11EffectClassInstanceVariable** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-112">The **ID3DX11EffectClassInstanceVariable** interface has these methods.</span></span>



| <span data-ttu-id="aaaa4-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="aaaa4-113">Method</span></span>                                                                          | <span data-ttu-id="aaaa4-114">Description</span><span class="sxs-lookup"><span data-stu-id="aaaa4-114">Description</span></span>                       |
|:--------------------------------------------------------------------------------|:----------------------------------|
| [<span data-ttu-id="aaaa4-115">**GetClassInstance**</span><span class="sxs-lookup"><span data-stu-id="aaaa4-115">**GetClassInstance**</span></span>](id3dx11effectclassinstancevariable-getclassinstance.md) | <span data-ttu-id="aaaa4-116">Obtient une instance de classe.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-116">Gets a class instance.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="aaaa4-117">Notes</span><span class="sxs-lookup"><span data-stu-id="aaaa4-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="aaaa4-118">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="aaaa4-119">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="aaaa4-120">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="aaaa4-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="aaaa4-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="aaaa4-121">Requirements</span></span>



| <span data-ttu-id="aaaa4-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aaaa4-122">Requirement</span></span> | <span data-ttu-id="aaaa4-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="aaaa4-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aaaa4-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="aaaa4-124">Header</span></span><br/>  | <dl> <span data-ttu-id="aaaa4-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="aaaa4-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="aaaa4-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="aaaa4-126">Library</span></span><br/> | <dl> <span data-ttu-id="aaaa4-127"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="aaaa4-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aaaa4-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aaaa4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaaa4-129">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="aaaa4-129">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="aaaa4-130">Effets 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="aaaa4-130">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="aaaa4-131">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="aaaa4-131">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





