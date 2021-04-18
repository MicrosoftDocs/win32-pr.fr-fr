---
description: Les applications utilisent les méthodes de l’interface ID3DXMATRIXStack pour manipuler une pile de matrice.
ms.assetid: 6c76f9e0-5f59-4cf3-b34a-2475536af6c7
title: Interface ID3DXMatrixStack (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMatrixStack
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3d6956a6764683378c732c4ed859bfa13e537422
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323233"
---
# <a name="id3dxmatrixstack-interface"></a><span data-ttu-id="8de74-103">Interface ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="8de74-103">ID3DXMatrixStack interface</span></span>

<span data-ttu-id="8de74-104">Les applications utilisent les méthodes de l’interface ID3DXMATRIXStack pour manipuler une pile de matrice.</span><span class="sxs-lookup"><span data-stu-id="8de74-104">Applications use the methods of the ID3DXMATRIXStack interface to manipulate a matrix stack.</span></span>

## <a name="members"></a><span data-ttu-id="8de74-105">Membres</span><span class="sxs-lookup"><span data-stu-id="8de74-105">Members</span></span>

<span data-ttu-id="8de74-106">L’interface **ID3DXMatrixStack** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8de74-106">The **ID3DXMatrixStack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8de74-107">**ID3DXMatrixStack** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8de74-107">**ID3DXMatrixStack** also has these types of members:</span></span>

-   [<span data-ttu-id="8de74-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8de74-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8de74-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8de74-109">Methods</span></span>

<span data-ttu-id="8de74-110">L’interface **ID3DXMatrixStack** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="8de74-110">The **ID3DXMatrixStack** interface has these methods.</span></span>



| <span data-ttu-id="8de74-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="8de74-111">Method</span></span>                                                                      | <span data-ttu-id="8de74-112">Description</span><span class="sxs-lookup"><span data-stu-id="8de74-112">Description</span></span>                                                                                                                                |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8de74-113">**GetTop**</span><span class="sxs-lookup"><span data-stu-id="8de74-113">**GetTop**</span></span>](id3dxmatrixstack-gettop.md)                                   | <span data-ttu-id="8de74-114">Récupère la matrice actuelle en haut de la pile.</span><span class="sxs-lookup"><span data-stu-id="8de74-114">Retrieves the current matrix at the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="8de74-115">**LoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="8de74-115">**LoadIdentity**</span></span>](id3dxmatrixstack-loadidentity.md)                       | <span data-ttu-id="8de74-116">Charge l’identité dans la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="8de74-116">Loads identity in the current matrix.</span></span><br/>                                                                                           |
| [<span data-ttu-id="8de74-117">**LoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="8de74-117">**LoadMatrix**</span></span>](id3dxmatrixstack-loadmatrix.md)                           | <span data-ttu-id="8de74-118">Charge la matrice donnée dans la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="8de74-118">Loads the given matrix into the current matrix.</span></span><br/>                                                                                 |
| [<span data-ttu-id="8de74-119">**MultMatrix**</span><span class="sxs-lookup"><span data-stu-id="8de74-119">**MultMatrix**</span></span>](id3dxmatrixstack-multmatrix.md)                           | <span data-ttu-id="8de74-120">Détermine le produit de la matrice actuelle et de la matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="8de74-120">Determines the product of the current matrix and the given matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="8de74-121">**MultMatrixLocal**</span><span class="sxs-lookup"><span data-stu-id="8de74-121">**MultMatrixLocal**</span></span>](id3dxmatrixstack-multmatrixlocal.md)                 | <span data-ttu-id="8de74-122">Détermine le produit de la matrice donnée et de la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="8de74-122">Determines the product of the given matrix and the current matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="8de74-123">**Roulant**</span><span class="sxs-lookup"><span data-stu-id="8de74-123">**Pop**</span></span>](id3dxmatrixstack-pop.md)                                         | <span data-ttu-id="8de74-124">Supprime la matrice actuelle du haut de la pile.</span><span class="sxs-lookup"><span data-stu-id="8de74-124">Removes the current matrix from the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="8de74-125">**Souleve**</span><span class="sxs-lookup"><span data-stu-id="8de74-125">**Push**</span></span>](id3dxmatrixstack-push.md)                                       | <span data-ttu-id="8de74-126">Ajoute une matrice à la pile.</span><span class="sxs-lookup"><span data-stu-id="8de74-126">Adds a matrix to the stack.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="8de74-127">**RotateAxis**</span><span class="sxs-lookup"><span data-stu-id="8de74-127">**RotateAxis**</span></span>](id3dxmatrixstack-rotateaxis.md)                           | <span data-ttu-id="8de74-128">Pivote (par rapport à l’espace de coordonnées universelles) autour d’un axe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="8de74-128">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="8de74-129">**RotateAxisLocal**</span><span class="sxs-lookup"><span data-stu-id="8de74-129">**RotateAxisLocal**</span></span>](id3dxmatrixstack-rotateaxislocal.md)                 | <span data-ttu-id="8de74-130">Pivote (par rapport à l’espace de coordonnées local de l’objet) autour d’un axe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="8de74-130">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="8de74-131">**RotateYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="8de74-131">**RotateYawPitchRoll**</span></span>](id3dxmatrixstack-rotateyawpitchroll.md)           | <span data-ttu-id="8de74-132">Pivote (par rapport à l’espace de coordonnées universelles) autour d’un axe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="8de74-132">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="8de74-133">**RotateYawPitchRollLocal**</span><span class="sxs-lookup"><span data-stu-id="8de74-133">**RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack-rotateyawpitchrolllocal.md) | <span data-ttu-id="8de74-134">Pivote (par rapport à l’espace de coordonnées local de l’objet) autour d’un axe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="8de74-134">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="8de74-135">**Scale**</span><span class="sxs-lookup"><span data-stu-id="8de74-135">**Scale**</span></span>](id3dxmatrixstack-scale.md)                                     | <span data-ttu-id="8de74-136">Mettre à l’échelle la matrice actuelle sur l’origine de la coordonnée universelle.</span><span class="sxs-lookup"><span data-stu-id="8de74-136">Scale the current matrix about the world coordinate origin.</span></span><br/>                                                                     |
| [<span data-ttu-id="8de74-137">**ScaleLocal**</span><span class="sxs-lookup"><span data-stu-id="8de74-137">**ScaleLocal**</span></span>](id3dxmatrixstack-scalelocal.md)                           | <span data-ttu-id="8de74-138">Mettre à l’échelle la matrice actuelle sur l’origine de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8de74-138">Scale the current matrix about the object origin.</span></span><br/>                                                                               |
| [<span data-ttu-id="8de74-139">**Traduire**</span><span class="sxs-lookup"><span data-stu-id="8de74-139">**Translate**</span></span>](id3dxmatrixstack-translate.md)                             | <span data-ttu-id="8de74-140">Détermine le produit de la matrice actuelle et la matrice de translation calculée déterminée par les facteurs donnés (x, y et z).</span><span class="sxs-lookup"><span data-stu-id="8de74-140">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span><br/> |
| [<span data-ttu-id="8de74-141">**TranslateLocal**</span><span class="sxs-lookup"><span data-stu-id="8de74-141">**TranslateLocal**</span></span>](id3dxmatrixstack-translatelocal.md)                   | <span data-ttu-id="8de74-142">Détermine le produit de la matrice de traduction calculée, déterminé par les facteurs donnés (x, y et z) et la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="8de74-142">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8de74-143">Notes</span><span class="sxs-lookup"><span data-stu-id="8de74-143">Remarks</span></span>

<span data-ttu-id="8de74-144">L’interface ID3DX10MATRIXStack est obtenue en appelant la fonction [**D3DXCreateMatrixStack**](d3d10-d3dxcreatematrixstack.md) .</span><span class="sxs-lookup"><span data-stu-id="8de74-144">The ID3DX10MATRIXStack interface is obtained by calling the [**D3DXCreateMatrixStack**](d3d10-d3dxcreatematrixstack.md) function.</span></span>

<span data-ttu-id="8de74-145">Le type LPD3DX10MATRIXSTACK est défini comme un pointeur vers l’interface **ID3DXMatrixStack** .</span><span class="sxs-lookup"><span data-stu-id="8de74-145">The LPD3DX10MATRIXSTACK type is defined as a pointer to the **ID3DXMatrixStack** interface.</span></span>


```
typedef interface ID3DXMatrixStack ID3DXMatrixStack;
typedef interface ID3DXMatrixStack *LPD3DXMATRIXSTACK;
```



## <a name="requirements"></a><span data-ttu-id="8de74-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8de74-146">Requirements</span></span>



| <span data-ttu-id="8de74-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8de74-147">Requirement</span></span> | <span data-ttu-id="8de74-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="8de74-148">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8de74-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="8de74-149">Header</span></span><br/>  | <dl> <span data-ttu-id="8de74-150"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="8de74-150"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="8de74-151">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8de74-151">Library</span></span><br/> | <dl> <span data-ttu-id="8de74-152"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8de74-152"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8de74-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8de74-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8de74-154">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="8de74-154">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
