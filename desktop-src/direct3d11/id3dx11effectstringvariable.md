---
title: Interface ID3DX11EffectStringVariable (D3dx11effect. h)
description: Une interface de variable de chaîne accède à une variable de chaîne.
ms.assetid: 8304d7cc-de30-41fe-af12-e11bf7ae32ce
keywords:
- Interface ID3DX11EffectStringVariable Direct3D 11
- Interface ID3DX11EffectStringVariable Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectStringVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a45eb5e0825bd8487396ed850c9d79665e5f1044
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992145"
---
# <a name="id3dx11effectstringvariable-interface"></a><span data-ttu-id="23271-105">Interface ID3DX11EffectStringVariable</span><span class="sxs-lookup"><span data-stu-id="23271-105">ID3DX11EffectStringVariable interface</span></span>

<span data-ttu-id="23271-106">Une interface de variable de chaîne accède à une variable de chaîne.</span><span class="sxs-lookup"><span data-stu-id="23271-106">A string-variable interface accesses a string variable.</span></span>

## <a name="members"></a><span data-ttu-id="23271-107">Membres</span><span class="sxs-lookup"><span data-stu-id="23271-107">Members</span></span>

<span data-ttu-id="23271-108">L’interface **ID3DX11EffectStringVariable** hérite de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="23271-108">The **ID3DX11EffectStringVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="23271-109">**ID3DX11EffectStringVariable** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="23271-109">**ID3DX11EffectStringVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="23271-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="23271-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="23271-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="23271-111">Methods</span></span>

<span data-ttu-id="23271-112">L’interface **ID3DX11EffectStringVariable** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="23271-112">The **ID3DX11EffectStringVariable** interface has these methods.</span></span>



| <span data-ttu-id="23271-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="23271-113">Method</span></span>                                                               | <span data-ttu-id="23271-114">Description</span><span class="sxs-lookup"><span data-stu-id="23271-114">Description</span></span>                         |
|:---------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="23271-115">**GetString**</span><span class="sxs-lookup"><span data-stu-id="23271-115">**GetString**</span></span>](id3dx11effectstringvariable-getstring.md)           | <span data-ttu-id="23271-116">Obtient la chaîne.</span><span class="sxs-lookup"><span data-stu-id="23271-116">Get the string.</span></span><br/>          |
| [<span data-ttu-id="23271-117">**GetStringArray**</span><span class="sxs-lookup"><span data-stu-id="23271-117">**GetStringArray**</span></span>](id3dx11effectstringvariable-getstringarray.md) | <span data-ttu-id="23271-118">Obtient un tableau de chaînes.</span><span class="sxs-lookup"><span data-stu-id="23271-118">Get an array of strings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="23271-119">Notes</span><span class="sxs-lookup"><span data-stu-id="23271-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="23271-120">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="23271-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="23271-121">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="23271-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="23271-122">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="23271-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="23271-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="23271-123">Requirements</span></span>



| <span data-ttu-id="23271-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23271-124">Requirement</span></span> | <span data-ttu-id="23271-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="23271-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23271-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="23271-126">Header</span></span><br/>  | <dl> <span data-ttu-id="23271-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="23271-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="23271-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="23271-128">Library</span></span><br/> | <dl> <span data-ttu-id="23271-129"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="23271-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23271-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23271-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23271-131">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="23271-131">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="23271-132">Effets 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="23271-132">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="23271-133">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="23271-133">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





