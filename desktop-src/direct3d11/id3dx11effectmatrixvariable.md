---
title: Interface ID3DX11EffectMatrixVariable (D3dx11effect. h)
description: Une interface à matrice variable accède à une matrice.
ms.assetid: 44f30d1a-3ec1-49d7-92c0-475cf2fa4d2a
keywords:
- Interface ID3DX11EffectMatrixVariable Direct3D 11
- Interface ID3DX11EffectMatrixVariable Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5c4c89a231d429fc0a1f8fecbcbb4d06db35cb5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974622"
---
# <a name="id3dx11effectmatrixvariable-interface"></a><span data-ttu-id="1aa16-105">Interface ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="1aa16-105">ID3DX11EffectMatrixVariable interface</span></span>

<span data-ttu-id="1aa16-106">Une interface à matrice variable accède à une matrice.</span><span class="sxs-lookup"><span data-stu-id="1aa16-106">A matrix-variable interface accesses a matrix.</span></span>

## <a name="members"></a><span data-ttu-id="1aa16-107">Membres</span><span class="sxs-lookup"><span data-stu-id="1aa16-107">Members</span></span>

<span data-ttu-id="1aa16-108">L’interface **ID3DX11EffectMatrixVariable** hérite de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="1aa16-108">The **ID3DX11EffectMatrixVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="1aa16-109">**ID3DX11EffectMatrixVariable** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1aa16-109">**ID3DX11EffectMatrixVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="1aa16-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1aa16-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1aa16-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1aa16-111">Methods</span></span>

<span data-ttu-id="1aa16-112">L’interface **ID3DX11EffectMatrixVariable** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="1aa16-112">The **ID3DX11EffectMatrixVariable** interface has these methods.</span></span>



| <span data-ttu-id="1aa16-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="1aa16-113">Method</span></span>                                                                                 | <span data-ttu-id="1aa16-114">Description</span><span class="sxs-lookup"><span data-stu-id="1aa16-114">Description</span></span>                                                       |
|:---------------------------------------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="1aa16-115">**GetMatrix**</span><span class="sxs-lookup"><span data-stu-id="1aa16-115">**GetMatrix**</span></span>](id3dx11effectmatrixvariable-getmatrix.md)                             | <span data-ttu-id="1aa16-116">Obtenir une matrice.</span><span class="sxs-lookup"><span data-stu-id="1aa16-116">Get a matrix.</span></span><br/>                                          |
| [<span data-ttu-id="1aa16-117">**GetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="1aa16-117">**GetMatrixArray**</span></span>](id3dx11effectmatrixvariable-getmatrixarray.md)                   | <span data-ttu-id="1aa16-118">Obtient un tableau de matrices.</span><span class="sxs-lookup"><span data-stu-id="1aa16-118">Get an array of matrices.</span></span><br/>                              |
| [<span data-ttu-id="1aa16-119">**GetMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="1aa16-119">**GetMatrixTranspose**</span></span>](id3dx11effectmatrixvariable-getmatrixtranspose.md)           | <span data-ttu-id="1aa16-120">Transposez et récupérez une matrice à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="1aa16-120">Transpose and get a floating-point matrix.</span></span><br/>             |
| [<span data-ttu-id="1aa16-121">**GetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="1aa16-121">**GetMatrixTransposeArray**</span></span>](id3dx11effectmatrixvariable-getmatrixtransposearray.md) | <span data-ttu-id="1aa16-122">Transposez et récupérez un tableau de matrices à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="1aa16-122">Transpose and get an array of floating-point matrices.</span></span><br/> |
| [<span data-ttu-id="1aa16-123">**SetMatrix**</span><span class="sxs-lookup"><span data-stu-id="1aa16-123">**SetMatrix**</span></span>](id3dx11effectmatrixvariable-setmatrix.md)                             | <span data-ttu-id="1aa16-124">Définissez une matrice à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="1aa16-124">Set a floating-point matrix.</span></span><br/>                           |
| [<span data-ttu-id="1aa16-125">**SetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="1aa16-125">**SetMatrixArray**</span></span>](id3dx11effectmatrixvariable-setmatrixarray.md)                   | <span data-ttu-id="1aa16-126">Définissez un tableau de matrices à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="1aa16-126">Set an array of floating-point matrices.</span></span><br/>               |
| [<span data-ttu-id="1aa16-127">**SetMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="1aa16-127">**SetMatrixTranspose**</span></span>](id3dx11effectmatrixvariable-setmatrixtranspose.md)           | <span data-ttu-id="1aa16-128">Transposez et définissez une matrice à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="1aa16-128">Transpose and set a floating-point matrix.</span></span><br/>             |
| [<span data-ttu-id="1aa16-129">**SetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="1aa16-129">**SetMatrixTransposeArray**</span></span>](id3dx11effectmatrixvariable-setmatrixtransposearray.md) | <span data-ttu-id="1aa16-130">Transposez et définissez un tableau de matrices à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="1aa16-130">Transpose and set an array of floating-point matrices.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1aa16-131">Notes</span><span class="sxs-lookup"><span data-stu-id="1aa16-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1aa16-132">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="1aa16-132">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="1aa16-133">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="1aa16-133">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="1aa16-134">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="1aa16-134">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1aa16-135">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1aa16-135">Requirements</span></span>



| <span data-ttu-id="1aa16-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1aa16-136">Requirement</span></span> | <span data-ttu-id="1aa16-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="1aa16-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1aa16-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="1aa16-138">Header</span></span><br/>  | <dl> <span data-ttu-id="1aa16-139"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="1aa16-139"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="1aa16-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1aa16-140">Library</span></span><br/> | <dl> <span data-ttu-id="1aa16-141"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="1aa16-141"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1aa16-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1aa16-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1aa16-143">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="1aa16-143">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="1aa16-144">Effets 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="1aa16-144">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="1aa16-145">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="1aa16-145">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





