---
description: Les applications utilisent les méthodes de l’interface ID3DXMATRIXStack pour manipuler une pile de matrice.
ms.assetid: 4d382d39-a9da-4a3b-b7b6-d6890357d467
title: Interface ID3DXMATRIXStack (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9446301ce057e788b4039f8ea3a144fb1fa19024
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106528573"
---
# <a name="id3dxmatrixstack-interface"></a><span data-ttu-id="8924d-103">Interface ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="8924d-103">ID3DXMATRIXStack interface</span></span>

<span data-ttu-id="8924d-104">Les applications utilisent les méthodes de l’interface ID3DXMATRIXStack pour manipuler une pile de matrice.</span><span class="sxs-lookup"><span data-stu-id="8924d-104">Applications use the methods of the ID3DXMATRIXStack interface to manipulate a matrix stack.</span></span>

## <a name="members"></a><span data-ttu-id="8924d-105">Membres</span><span class="sxs-lookup"><span data-stu-id="8924d-105">Members</span></span>

<span data-ttu-id="8924d-106">L’interface **ID3DXMATRIXStack** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8924d-106">The **ID3DXMATRIXStack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8924d-107">**ID3DXMATRIXStack** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8924d-107">**ID3DXMATRIXStack** also has these types of members:</span></span>

-   [<span data-ttu-id="8924d-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8924d-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8924d-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8924d-109">Methods</span></span>

<span data-ttu-id="8924d-110">L’interface **ID3DXMATRIXStack** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="8924d-110">The **ID3DXMATRIXStack** interface has these methods.</span></span>



| <span data-ttu-id="8924d-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="8924d-111">Method</span></span>                                                                       | <span data-ttu-id="8924d-112">Description</span><span class="sxs-lookup"><span data-stu-id="8924d-112">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8924d-113">**GetTop**</span><span class="sxs-lookup"><span data-stu-id="8924d-113">**GetTop**</span></span>](id3dxmatrixstack--gettop.md)                                   | <span data-ttu-id="8924d-114">Récupère la matrice actuelle en haut de la pile.</span><span class="sxs-lookup"><span data-stu-id="8924d-114">Retrieves the current matrix at the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="8924d-115">**LoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="8924d-115">**LoadIdentity**</span></span>](id3dxmatrixstack--loadidentity.md)                       | <span data-ttu-id="8924d-116">Charge l’identité dans la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="8924d-116">Loads identity in the current matrix.</span></span><br/>                                                                                           |
| [<span data-ttu-id="8924d-117">**LoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="8924d-117">**LoadMatrix**</span></span>](id3dxmatrixstack--loadmatrix.md)                           | <span data-ttu-id="8924d-118">Charge la matrice donnée dans la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="8924d-118">Loads the given matrix into the current matrix.</span></span><br/>                                                                                 |
| [<span data-ttu-id="8924d-119">**MultMatrix**</span><span class="sxs-lookup"><span data-stu-id="8924d-119">**MultMatrix**</span></span>](id3dxmatrixstack--multmatrix.md)                           | <span data-ttu-id="8924d-120">Détermine le produit de la matrice actuelle et de la matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="8924d-120">Determines the product of the current matrix and the given matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="8924d-121">**MultMatrixLocal**</span><span class="sxs-lookup"><span data-stu-id="8924d-121">**MultMatrixLocal**</span></span>](id3dxmatrixstack--multmatrixlocal.md)                 | <span data-ttu-id="8924d-122">Détermine le produit de la matrice donnée et de la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="8924d-122">Determines the product of the given matrix and the current matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="8924d-123">**Roulant**</span><span class="sxs-lookup"><span data-stu-id="8924d-123">**Pop**</span></span>](id3dxmatrixstack--pop.md)                                         | <span data-ttu-id="8924d-124">Supprime la matrice actuelle du haut de la pile.</span><span class="sxs-lookup"><span data-stu-id="8924d-124">Removes the current matrix from the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="8924d-125">**Souleve**</span><span class="sxs-lookup"><span data-stu-id="8924d-125">**Push**</span></span>](id3dxmatrixstack--push.md)                                       | <span data-ttu-id="8924d-126">Ajoute une matrice à la pile.</span><span class="sxs-lookup"><span data-stu-id="8924d-126">Adds a matrix to the stack.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="8924d-127">**RotateAxis**</span><span class="sxs-lookup"><span data-stu-id="8924d-127">**RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)                           | <span data-ttu-id="8924d-128">Pivote (par rapport à l’espace de coordonnées universelles) autour d’un axe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="8924d-128">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="8924d-129">**RotateAxisLocal**</span><span class="sxs-lookup"><span data-stu-id="8924d-129">**RotateAxisLocal**</span></span>](id3dxmatrixstack--rotateaxislocal.md)                 | <span data-ttu-id="8924d-130">Pivote (par rapport à l’espace de coordonnées local de l’objet) autour d’un axe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="8924d-130">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="8924d-131">**RotateYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="8924d-131">**RotateYawPitchRoll**</span></span>](id3dxmatrixstack--rotateyawpitchroll.md)           | <span data-ttu-id="8924d-132">Pivote (par rapport à l’espace de coordonnées universelles) autour d’un axe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="8924d-132">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="8924d-133">**RotateYawPitchRollLocal**</span><span class="sxs-lookup"><span data-stu-id="8924d-133">**RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack--rotateyawpitchrolllocal.md) | <span data-ttu-id="8924d-134">Pivote (par rapport à l’espace de coordonnées local de l’objet) autour d’un axe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="8924d-134">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="8924d-135">**Scale**</span><span class="sxs-lookup"><span data-stu-id="8924d-135">**Scale**</span></span>](id3dxmatrixstack--scale.md)                                     | <span data-ttu-id="8924d-136">Mettre à l’échelle la matrice actuelle sur l’origine de la coordonnée universelle.</span><span class="sxs-lookup"><span data-stu-id="8924d-136">Scale the current matrix about the world coordinate origin.</span></span><br/>                                                                     |
| [<span data-ttu-id="8924d-137">**ScaleLocal**</span><span class="sxs-lookup"><span data-stu-id="8924d-137">**ScaleLocal**</span></span>](id3dxmatrixstack--scalelocal.md)                           | <span data-ttu-id="8924d-138">Mettre à l’échelle la matrice actuelle sur l’origine de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8924d-138">Scale the current matrix about the object origin.</span></span><br/>                                                                               |
| [<span data-ttu-id="8924d-139">**Traduire**</span><span class="sxs-lookup"><span data-stu-id="8924d-139">**Translate**</span></span>](id3dxmatrixstack--translate.md)                             | <span data-ttu-id="8924d-140">Détermine le produit de la matrice actuelle et la matrice de translation calculée déterminée par les facteurs donnés (x, y et z).</span><span class="sxs-lookup"><span data-stu-id="8924d-140">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span><br/> |
| [<span data-ttu-id="8924d-141">**TranslateLocal**</span><span class="sxs-lookup"><span data-stu-id="8924d-141">**TranslateLocal**</span></span>](id3dxmatrixstack--translatelocal.md)                   | <span data-ttu-id="8924d-142">Détermine le produit de la matrice de traduction calculée, déterminé par les facteurs donnés (x, y et z) et la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="8924d-142">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8924d-143">Notes</span><span class="sxs-lookup"><span data-stu-id="8924d-143">Remarks</span></span>

<span data-ttu-id="8924d-144">L’interface **ID3DXMATRIXStack** est obtenue en appelant la fonction [**D3DXCreateMatrixStack**](d3dxcreatematrixstack.md) .</span><span class="sxs-lookup"><span data-stu-id="8924d-144">The **ID3DXMATRIXStack** interface is obtained by calling the [**D3DXCreateMatrixStack**](d3dxcreatematrixstack.md) function.</span></span>

<span data-ttu-id="8924d-145">Le type LPD3DXMATRIXSTACK est défini comme un pointeur vers l’interface **ID3DXMATRIXStack** .</span><span class="sxs-lookup"><span data-stu-id="8924d-145">The LPD3DXMATRIXSTACK type is defined as a pointer to the **ID3DXMATRIXStack** interface.</span></span>


```
typedef interface ID3DXMATRIXStack ID3DXMATRIXStack;
typedef interface ID3DXMATRIXStack *LPD3DXMATRIXSTACK;
```



## <a name="requirements"></a><span data-ttu-id="8924d-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8924d-146">Requirements</span></span>



| <span data-ttu-id="8924d-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8924d-147">Requirement</span></span> | <span data-ttu-id="8924d-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="8924d-148">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8924d-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="8924d-149">Header</span></span><br/>  | <dl> <span data-ttu-id="8924d-150"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8924d-150"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="8924d-151">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8924d-151">Library</span></span><br/> | <dl> <span data-ttu-id="8924d-152"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8924d-152"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8924d-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8924d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8924d-154">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="8924d-154">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
