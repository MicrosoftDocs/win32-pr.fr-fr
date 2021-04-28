---
description: 'Interface ID3DXMatrixStack : les applications utilisent les méthodes de l’interface ID3DXMATRIXStack pour manipuler une pile de matrice.'
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
ms.openlocfilehash: 65e9a5cd041431e1939346fec79dcf94fccd4ae9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094407"
---
# <a name="id3dxmatrixstack-interface"></a><span data-ttu-id="3f20c-103">Interface ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="3f20c-103">ID3DXMatrixStack interface</span></span>

<span data-ttu-id="3f20c-104">Les applications utilisent les méthodes de l’interface ID3DXMATRIXStack pour manipuler une pile de matrice.</span><span class="sxs-lookup"><span data-stu-id="3f20c-104">Applications use the methods of the ID3DXMATRIXStack interface to manipulate a matrix stack.</span></span>

## <a name="members"></a><span data-ttu-id="3f20c-105">Membres</span><span class="sxs-lookup"><span data-stu-id="3f20c-105">Members</span></span>

<span data-ttu-id="3f20c-106">L’interface **ID3DXMatrixStack** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3f20c-106">The **ID3DXMatrixStack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3f20c-107">**ID3DXMatrixStack** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3f20c-107">**ID3DXMatrixStack** also has these types of members:</span></span>

-   [<span data-ttu-id="3f20c-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3f20c-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3f20c-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3f20c-109">Methods</span></span>

<span data-ttu-id="3f20c-110">L’interface **ID3DXMatrixStack** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="3f20c-110">The **ID3DXMatrixStack** interface has these methods.</span></span>



| <span data-ttu-id="3f20c-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="3f20c-111">Method</span></span>                                                                      | <span data-ttu-id="3f20c-112">Description</span><span class="sxs-lookup"><span data-stu-id="3f20c-112">Description</span></span>                                                                                                                                |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3f20c-113">**GetTop**</span><span class="sxs-lookup"><span data-stu-id="3f20c-113">**GetTop**</span></span>](id3dxmatrixstack-gettop.md)                                   | <span data-ttu-id="3f20c-114">Récupère la matrice actuelle en haut de la pile.</span><span class="sxs-lookup"><span data-stu-id="3f20c-114">Retrieves the current matrix at the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="3f20c-115">**LoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="3f20c-115">**LoadIdentity**</span></span>](id3dxmatrixstack-loadidentity.md)                       | <span data-ttu-id="3f20c-116">Charge l’identité dans la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="3f20c-116">Loads identity in the current matrix.</span></span><br/>                                                                                           |
| [<span data-ttu-id="3f20c-117">**LoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="3f20c-117">**LoadMatrix**</span></span>](id3dxmatrixstack-loadmatrix.md)                           | <span data-ttu-id="3f20c-118">Charge la matrice donnée dans la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="3f20c-118">Loads the given matrix into the current matrix.</span></span><br/>                                                                                 |
| [<span data-ttu-id="3f20c-119">**MultMatrix**</span><span class="sxs-lookup"><span data-stu-id="3f20c-119">**MultMatrix**</span></span>](id3dxmatrixstack-multmatrix.md)                           | <span data-ttu-id="3f20c-120">Détermine le produit de la matrice actuelle et de la matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="3f20c-120">Determines the product of the current matrix and the given matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="3f20c-121">**MultMatrixLocal**</span><span class="sxs-lookup"><span data-stu-id="3f20c-121">**MultMatrixLocal**</span></span>](id3dxmatrixstack-multmatrixlocal.md)                 | <span data-ttu-id="3f20c-122">Détermine le produit de la matrice donnée et de la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="3f20c-122">Determines the product of the given matrix and the current matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="3f20c-123">**Roulant**</span><span class="sxs-lookup"><span data-stu-id="3f20c-123">**Pop**</span></span>](id3dxmatrixstack-pop.md)                                         | <span data-ttu-id="3f20c-124">Supprime la matrice actuelle du haut de la pile.</span><span class="sxs-lookup"><span data-stu-id="3f20c-124">Removes the current matrix from the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="3f20c-125">**Souleve**</span><span class="sxs-lookup"><span data-stu-id="3f20c-125">**Push**</span></span>](id3dxmatrixstack-push.md)                                       | <span data-ttu-id="3f20c-126">Ajoute une matrice à la pile.</span><span class="sxs-lookup"><span data-stu-id="3f20c-126">Adds a matrix to the stack.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="3f20c-127">**RotateAxis**</span><span class="sxs-lookup"><span data-stu-id="3f20c-127">**RotateAxis**</span></span>](id3dxmatrixstack-rotateaxis.md)                           | <span data-ttu-id="3f20c-128">Pivote (par rapport à l’espace de coordonnées universelles) autour d’un axe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="3f20c-128">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="3f20c-129">**RotateAxisLocal**</span><span class="sxs-lookup"><span data-stu-id="3f20c-129">**RotateAxisLocal**</span></span>](id3dxmatrixstack-rotateaxislocal.md)                 | <span data-ttu-id="3f20c-130">Pivote (par rapport à l’espace de coordonnées local de l’objet) autour d’un axe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="3f20c-130">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="3f20c-131">**RotateYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="3f20c-131">**RotateYawPitchRoll**</span></span>](id3dxmatrixstack-rotateyawpitchroll.md)           | <span data-ttu-id="3f20c-132">Pivote (par rapport à l’espace de coordonnées universelles) autour d’un axe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="3f20c-132">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="3f20c-133">**RotateYawPitchRollLocal**</span><span class="sxs-lookup"><span data-stu-id="3f20c-133">**RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack-rotateyawpitchrolllocal.md) | <span data-ttu-id="3f20c-134">Pivote (par rapport à l’espace de coordonnées local de l’objet) autour d’un axe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="3f20c-134">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="3f20c-135">**Scale**</span><span class="sxs-lookup"><span data-stu-id="3f20c-135">**Scale**</span></span>](id3dxmatrixstack-scale.md)                                     | <span data-ttu-id="3f20c-136">Mettre à l’échelle la matrice actuelle sur l’origine de la coordonnée universelle.</span><span class="sxs-lookup"><span data-stu-id="3f20c-136">Scale the current matrix about the world coordinate origin.</span></span><br/>                                                                     |
| [<span data-ttu-id="3f20c-137">**ScaleLocal**</span><span class="sxs-lookup"><span data-stu-id="3f20c-137">**ScaleLocal**</span></span>](id3dxmatrixstack-scalelocal.md)                           | <span data-ttu-id="3f20c-138">Mettre à l’échelle la matrice actuelle sur l’origine de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3f20c-138">Scale the current matrix about the object origin.</span></span><br/>                                                                               |
| [<span data-ttu-id="3f20c-139">**Translate**</span><span class="sxs-lookup"><span data-stu-id="3f20c-139">**Translate**</span></span>](id3dxmatrixstack-translate.md)                             | <span data-ttu-id="3f20c-140">Détermine le produit de la matrice actuelle et la matrice de translation calculée déterminée par les facteurs donnés (x, y et z).</span><span class="sxs-lookup"><span data-stu-id="3f20c-140">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span><br/> |
| [<span data-ttu-id="3f20c-141">**TranslateLocal**</span><span class="sxs-lookup"><span data-stu-id="3f20c-141">**TranslateLocal**</span></span>](id3dxmatrixstack-translatelocal.md)                   | <span data-ttu-id="3f20c-142">Détermine le produit de la matrice de traduction calculée, déterminé par les facteurs donnés (x, y et z) et la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="3f20c-142">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3f20c-143">Notes </span><span class="sxs-lookup"><span data-stu-id="3f20c-143">Remarks</span></span>

<span data-ttu-id="3f20c-144">L’interface ID3DX10MATRIXStack est obtenue en appelant la fonction [**D3DXCreateMatrixStack**](d3d10-d3dxcreatematrixstack.md) .</span><span class="sxs-lookup"><span data-stu-id="3f20c-144">The ID3DX10MATRIXStack interface is obtained by calling the [**D3DXCreateMatrixStack**](d3d10-d3dxcreatematrixstack.md) function.</span></span>

<span data-ttu-id="3f20c-145">Le type LPD3DX10MATRIXSTACK est défini comme un pointeur vers l’interface **ID3DXMatrixStack** .</span><span class="sxs-lookup"><span data-stu-id="3f20c-145">The LPD3DX10MATRIXSTACK type is defined as a pointer to the **ID3DXMatrixStack** interface.</span></span>


```
typedef interface ID3DXMatrixStack ID3DXMatrixStack;
typedef interface ID3DXMatrixStack *LPD3DXMATRIXSTACK;
```



## <a name="requirements"></a><span data-ttu-id="3f20c-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3f20c-146">Requirements</span></span>



| <span data-ttu-id="3f20c-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3f20c-147">Requirement</span></span> | <span data-ttu-id="3f20c-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f20c-148">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3f20c-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="3f20c-149">Header</span></span><br/>  | <dl> <span data-ttu-id="3f20c-150"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f20c-150"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="3f20c-151">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3f20c-151">Library</span></span><br/> | <dl> <span data-ttu-id="3f20c-152"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f20c-152"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f20c-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f20c-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f20c-154">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="3f20c-154">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
