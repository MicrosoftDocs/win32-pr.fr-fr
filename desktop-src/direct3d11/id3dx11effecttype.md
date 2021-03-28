---
title: Interface ID3DX11EffectType (D3dx11effect. h)
description: L’interface ID3DX11EffectType accède aux variables d’effet par type. La durée de vie d’un objet ID3DX11EffectType est égale à la durée de vie de son objet ID3DX11Effect parent.
ms.assetid: 700076ee-a5fe-4af2-a5f4-053c05d8ddf0
keywords:
- Interface ID3DX11EffectType Direct3D 11
- Interface ID3DX11EffectType Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectType
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e3c210ca60abc9e55b8864a2b121cf92be369a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761983"
---
# <a name="id3dx11effecttype-interface"></a><span data-ttu-id="a29fb-105">Interface ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="a29fb-105">ID3DX11EffectType interface</span></span>

<span data-ttu-id="a29fb-106">L’interface **ID3DX11EffectType** accède aux variables d’effet par type.</span><span class="sxs-lookup"><span data-stu-id="a29fb-106">The **ID3DX11EffectType** interface accesses effect variables by type.</span></span>

<span data-ttu-id="a29fb-107">La durée de vie d’un objet **ID3DX11EffectType** est égale à la durée de vie de son objet [**ID3DX11Effect**](id3dx11effect.md) parent.</span><span class="sxs-lookup"><span data-stu-id="a29fb-107">The lifetime of an **ID3DX11EffectType** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="a29fb-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a29fb-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a29fb-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a29fb-109">Methods</span></span>

<span data-ttu-id="a29fb-110">L’interface **ID3DX11EffectType** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="a29fb-110">The **ID3DX11EffectType** interface has these methods.</span></span>



| <span data-ttu-id="a29fb-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="a29fb-111">Method</span></span>                                                                       | <span data-ttu-id="a29fb-112">Description</span><span class="sxs-lookup"><span data-stu-id="a29fb-112">Description</span></span>                                       |
|:-----------------------------------------------------------------------------|:--------------------------------------------------|
| [<span data-ttu-id="a29fb-113">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="a29fb-113">**GetDesc**</span></span>](id3dx11effecttype-getdesc.md)                                 | <span data-ttu-id="a29fb-114">Obtient une description de type d’effet.</span><span class="sxs-lookup"><span data-stu-id="a29fb-114">Get an effect-type description.</span></span><br/>        |
| [<span data-ttu-id="a29fb-115">**GetMemberName**</span><span class="sxs-lookup"><span data-stu-id="a29fb-115">**GetMemberName**</span></span>](id3dx11effecttype-getmembername.md)                     | <span data-ttu-id="a29fb-116">Obtient le nom d’un membre.</span><span class="sxs-lookup"><span data-stu-id="a29fb-116">Get the name of a member.</span></span><br/>              |
| [<span data-ttu-id="a29fb-117">**GetMemberSemantic**</span><span class="sxs-lookup"><span data-stu-id="a29fb-117">**GetMemberSemantic**</span></span>](id3dx11effecttype-getmembersemantic.md)             | <span data-ttu-id="a29fb-118">Obtient la sémantique attachée à un membre.</span><span class="sxs-lookup"><span data-stu-id="a29fb-118">Get the semantic attached to a member.</span></span><br/> |
| [<span data-ttu-id="a29fb-119">**GetMemberTypeByIndex**</span><span class="sxs-lookup"><span data-stu-id="a29fb-119">**GetMemberTypeByIndex**</span></span>](id3dx11effecttype-getmembertypebyindex.md)       | <span data-ttu-id="a29fb-120">Obtient un type de membre par index.</span><span class="sxs-lookup"><span data-stu-id="a29fb-120">Get a member type by index.</span></span><br/>            |
| [<span data-ttu-id="a29fb-121">**GetMemberTypeByName**</span><span class="sxs-lookup"><span data-stu-id="a29fb-121">**GetMemberTypeByName**</span></span>](id3dx11effecttype-getmembertypebyname.md)         | <span data-ttu-id="a29fb-122">Obtient un type de membre par nom.</span><span class="sxs-lookup"><span data-stu-id="a29fb-122">Get an member type by name.</span></span><br/>            |
| [<span data-ttu-id="a29fb-123">**GetMemberTypeBySemantic**</span><span class="sxs-lookup"><span data-stu-id="a29fb-123">**GetMemberTypeBySemantic**</span></span>](id3dx11effecttype-getmembertypebysemantic.md) | <span data-ttu-id="a29fb-124">Obtient un type de membre par sémantique.</span><span class="sxs-lookup"><span data-stu-id="a29fb-124">Get a member type by semantic.</span></span><br/>         |
| [<span data-ttu-id="a29fb-125">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="a29fb-125">**IsValid**</span></span>](id3dx11effecttype-isvalid.md)                                 | <span data-ttu-id="a29fb-126">Teste que le type d’effet est valide.</span><span class="sxs-lookup"><span data-stu-id="a29fb-126">Tests that the effect type is valid.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="a29fb-127">Notes</span><span class="sxs-lookup"><span data-stu-id="a29fb-127">Remarks</span></span>

<span data-ttu-id="a29fb-128">Pour obtenir des informations sur un type d’effet à partir d’une variable Effect, appelez [**ID3DX11EffectVariable :: GetType**](id3dx11effectvariable-gettype.md).</span><span class="sxs-lookup"><span data-stu-id="a29fb-128">To get information about an effect type from an effect variable, call [**ID3DX11EffectVariable::GetType**](id3dx11effectvariable-gettype.md).</span></span>

> [!Note]  
> <span data-ttu-id="a29fb-129">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="a29fb-129">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="a29fb-130">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="a29fb-130">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="a29fb-131">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="a29fb-131">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a29fb-132">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a29fb-132">Requirements</span></span>



| <span data-ttu-id="a29fb-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a29fb-133">Requirement</span></span> | <span data-ttu-id="a29fb-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="a29fb-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a29fb-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="a29fb-135">Header</span></span><br/>  | <dl> <span data-ttu-id="a29fb-136"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a29fb-136"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a29fb-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a29fb-137">Library</span></span><br/> | <dl> <span data-ttu-id="a29fb-138"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="a29fb-138"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a29fb-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a29fb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a29fb-140">Effets 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="a29fb-140">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="a29fb-141">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="a29fb-141">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





