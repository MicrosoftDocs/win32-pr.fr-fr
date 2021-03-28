---
title: Interface ID3DX11EffectScalarVariable (D3dx11effect. h)
description: Une interface de variable Effect-scalaire accède à des valeurs scalaires.
ms.assetid: 52e3b856-aa1b-4ed2-b140-7ae96ec1c94b
keywords:
- Interface ID3DX11EffectScalarVariable Direct3D 11
- Interface ID3DX11EffectScalarVariable Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d07f0d14ce37f9c84c20564189e1b8475e69887
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211694"
---
# <a name="id3dx11effectscalarvariable-interface"></a><span data-ttu-id="6690d-105">Interface ID3DX11EffectScalarVariable</span><span class="sxs-lookup"><span data-stu-id="6690d-105">ID3DX11EffectScalarVariable interface</span></span>

<span data-ttu-id="6690d-106">Une interface de variable Effect-scalaire accède à des valeurs scalaires.</span><span class="sxs-lookup"><span data-stu-id="6690d-106">An effect-scalar-variable interface accesses scalar values.</span></span>

## <a name="members"></a><span data-ttu-id="6690d-107">Membres</span><span class="sxs-lookup"><span data-stu-id="6690d-107">Members</span></span>

<span data-ttu-id="6690d-108">L’interface **ID3DX11EffectScalarVariable** hérite de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="6690d-108">The **ID3DX11EffectScalarVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="6690d-109">**ID3DX11EffectScalarVariable** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6690d-109">**ID3DX11EffectScalarVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="6690d-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6690d-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6690d-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6690d-111">Methods</span></span>

<span data-ttu-id="6690d-112">L’interface **ID3DX11EffectScalarVariable** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="6690d-112">The **ID3DX11EffectScalarVariable** interface has these methods.</span></span>



| <span data-ttu-id="6690d-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="6690d-113">Method</span></span>                                                             | <span data-ttu-id="6690d-114">Description</span><span class="sxs-lookup"><span data-stu-id="6690d-114">Description</span></span>                                          |
|:-------------------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="6690d-115">**GetBool**</span><span class="sxs-lookup"><span data-stu-id="6690d-115">**GetBool**</span></span>](id3dx11effectscalarvariable-getbool.md)             | <span data-ttu-id="6690d-116">Obtenir une variable booléenne.</span><span class="sxs-lookup"><span data-stu-id="6690d-116">Get a boolean variable.</span></span><br/>                   |
| [<span data-ttu-id="6690d-117">**GetBoolArray**</span><span class="sxs-lookup"><span data-stu-id="6690d-117">**GetBoolArray**</span></span>](id3dx11effectscalarvariable-getboolarray.md)   | <span data-ttu-id="6690d-118">Obtient un tableau de variables booléennes.</span><span class="sxs-lookup"><span data-stu-id="6690d-118">Get an array of boolean variables.</span></span><br/>        |
| [<span data-ttu-id="6690d-119">**GetFloat**</span><span class="sxs-lookup"><span data-stu-id="6690d-119">**GetFloat**</span></span>](id3dx11effectscalarvariable-getfloat.md)           | <span data-ttu-id="6690d-120">Obtenir une variable à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="6690d-120">Get a floating-point variable.</span></span><br/>            |
| [<span data-ttu-id="6690d-121">**GetFloatArray**</span><span class="sxs-lookup"><span data-stu-id="6690d-121">**GetFloatArray**</span></span>](id3dx11effectscalarvariable-getfloatarray.md) | <span data-ttu-id="6690d-122">Obtient un tableau de variables à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="6690d-122">Get an array of floating-point variables.</span></span><br/> |
| [<span data-ttu-id="6690d-123">**GetInt**</span><span class="sxs-lookup"><span data-stu-id="6690d-123">**GetInt**</span></span>](id3dx11effectscalarvariable-getint.md)               | <span data-ttu-id="6690d-124">Obtient une variable de type Integer.</span><span class="sxs-lookup"><span data-stu-id="6690d-124">Get an integer variable.</span></span><br/>                  |
| [<span data-ttu-id="6690d-125">**GetIntArray**</span><span class="sxs-lookup"><span data-stu-id="6690d-125">**GetIntArray**</span></span>](id3dx11effectscalarvariable-getintarray.md)     | <span data-ttu-id="6690d-126">Obtient un tableau de variables de type entier.</span><span class="sxs-lookup"><span data-stu-id="6690d-126">Get an array of integer variables.</span></span><br/>        |
| [<span data-ttu-id="6690d-127">**SetBool**</span><span class="sxs-lookup"><span data-stu-id="6690d-127">**SetBool**</span></span>](id3dx11effectscalarvariable-setbool.md)             | <span data-ttu-id="6690d-128">Définissez une variable booléenne.</span><span class="sxs-lookup"><span data-stu-id="6690d-128">Set a boolean variable.</span></span><br/>                   |
| [<span data-ttu-id="6690d-129">**SetBoolArray**</span><span class="sxs-lookup"><span data-stu-id="6690d-129">**SetBoolArray**</span></span>](id3dx11effectscalarvariable-setboolarray.md)   | <span data-ttu-id="6690d-130">Définissez un tableau de variables booléennes.</span><span class="sxs-lookup"><span data-stu-id="6690d-130">Set an array of boolean variables.</span></span><br/>        |
| [<span data-ttu-id="6690d-131">**SetFloat**</span><span class="sxs-lookup"><span data-stu-id="6690d-131">**SetFloat**</span></span>](id3dx11effectscalarvariable-setfloat.md)           | <span data-ttu-id="6690d-132">Définissez une variable à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="6690d-132">Set a floating-point variable.</span></span><br/>            |
| [<span data-ttu-id="6690d-133">**SetFloatArray**</span><span class="sxs-lookup"><span data-stu-id="6690d-133">**SetFloatArray**</span></span>](id3dx11effectscalarvariable-setfloatarray.md) | <span data-ttu-id="6690d-134">Définissez un tableau de variables à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="6690d-134">Set an array of floating-point variables.</span></span><br/> |
| [<span data-ttu-id="6690d-135">**SetInt**</span><span class="sxs-lookup"><span data-stu-id="6690d-135">**SetInt**</span></span>](id3dx11effectscalarvariable-setint.md)               | <span data-ttu-id="6690d-136">Définissez une variable de type entier.</span><span class="sxs-lookup"><span data-stu-id="6690d-136">Set an integer variable.</span></span><br/>                  |
| [<span data-ttu-id="6690d-137">**SetIntArray**</span><span class="sxs-lookup"><span data-stu-id="6690d-137">**SetIntArray**</span></span>](id3dx11effectscalarvariable-setintarray.md)     | <span data-ttu-id="6690d-138">Définissez un tableau de variables de type entier.</span><span class="sxs-lookup"><span data-stu-id="6690d-138">Set an array of integer variables.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="6690d-139">Notes</span><span class="sxs-lookup"><span data-stu-id="6690d-139">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6690d-140">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="6690d-140">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="6690d-141">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="6690d-141">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="6690d-142">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="6690d-142">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6690d-143">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6690d-143">Requirements</span></span>



| <span data-ttu-id="6690d-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6690d-144">Requirement</span></span> | <span data-ttu-id="6690d-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="6690d-145">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6690d-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="6690d-146">Header</span></span><br/>  | <dl> <span data-ttu-id="6690d-147"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6690d-147"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="6690d-148">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6690d-148">Library</span></span><br/> | <dl> <span data-ttu-id="6690d-149"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="6690d-149"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6690d-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6690d-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6690d-151">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="6690d-151">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="6690d-152">Effets 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="6690d-152">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="6690d-153">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="6690d-153">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





