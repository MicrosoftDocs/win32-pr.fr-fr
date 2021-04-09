---
description: L’interface ID3DXLine implémente le dessin de lignes à l’aide de triangles texturés.
ms.assetid: 87472618-d3e4-4008-9009-ae17fc7b696d
title: Interface ID3DXLine (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1c535ff736e9a26e8316e4715f4be4022a6417df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043194"
---
# <a name="id3dxline-interface"></a><span data-ttu-id="d277f-103">Interface ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="d277f-103">ID3DXLine interface</span></span>

<span data-ttu-id="d277f-104">L’interface ID3DXLine implémente le dessin de lignes à l’aide de triangles texturés.</span><span class="sxs-lookup"><span data-stu-id="d277f-104">The ID3DXLine interface implements line drawing using textured triangles.</span></span>

## <a name="members"></a><span data-ttu-id="d277f-105">Membres</span><span class="sxs-lookup"><span data-stu-id="d277f-105">Members</span></span>

<span data-ttu-id="d277f-106">L’interface **ID3DXLine** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d277f-106">The **ID3DXLine** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d277f-107">**ID3DXLine** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d277f-107">**ID3DXLine** also has these types of members:</span></span>

-   [<span data-ttu-id="d277f-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d277f-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d277f-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d277f-109">Methods</span></span>

<span data-ttu-id="d277f-110">L’interface **ID3DXLine** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d277f-110">The **ID3DXLine** interface has these methods.</span></span>



| <span data-ttu-id="d277f-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="d277f-111">Method</span></span>                                                | <span data-ttu-id="d277f-112">Description</span><span class="sxs-lookup"><span data-stu-id="d277f-112">Description</span></span>                                                                                                                                                                                      |
|:------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d277f-113">**Début**</span><span class="sxs-lookup"><span data-stu-id="d277f-113">**Begin**</span></span>](id3dxline--begin.md)                     | <span data-ttu-id="d277f-114">Prépare un appareil pour le dessin de lignes.</span><span class="sxs-lookup"><span data-stu-id="d277f-114">Prepares a device for drawing lines.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="d277f-115">**Dessin**</span><span class="sxs-lookup"><span data-stu-id="d277f-115">**Draw**</span></span>](id3dxline--draw.md)                       | <span data-ttu-id="d277f-116">Dessine une bande en courbes dans l’espace à l’écran.</span><span class="sxs-lookup"><span data-stu-id="d277f-116">Draws a line strip in screen space.</span></span> <span data-ttu-id="d277f-117">L’entrée se présente sous la forme d’un tableau qui définit les points (of [**D3DXVECTOR2**](d3dxvector2.md)) sur la bande.</span><span class="sxs-lookup"><span data-stu-id="d277f-117">Input is in the form of an array that defines points (of [**D3DXVECTOR2**](d3dxvector2.md)) on the line strip.</span></span><br/>                                   |
| [<span data-ttu-id="d277f-118">**DrawTransform**</span><span class="sxs-lookup"><span data-stu-id="d277f-118">**DrawTransform**</span></span>](id3dxline--drawtransform.md)     | <span data-ttu-id="d277f-119">Dessine une bande de courbes dans l’espace à l’écran avec une matrice de transformation d’entrée spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d277f-119">Draws a line strip in screen space with a specified input transformation matrix.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="d277f-120">**Effet**</span><span class="sxs-lookup"><span data-stu-id="d277f-120">**End**</span></span>](id3dxline--end.md)                         | <span data-ttu-id="d277f-121">Restaure l’état de l’appareil sur la manière dont il se trouvait lors de l’appel de [**ID3DXLine :: Begin**](id3dxline--begin.md) .</span><span class="sxs-lookup"><span data-stu-id="d277f-121">Restores the device state to how it was when [**ID3DXLine::Begin**](id3dxline--begin.md) was called.</span></span><br/>                                                                                 |
| [<span data-ttu-id="d277f-122">**GetAntialias**</span><span class="sxs-lookup"><span data-stu-id="d277f-122">**GetAntialias**</span></span>](id3dxline--getantialias.md)       | <span data-ttu-id="d277f-123">Obtient l’état de l’anticrénelage de ligne.</span><span class="sxs-lookup"><span data-stu-id="d277f-123">Gets the line antialiasing state.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="d277f-124">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="d277f-124">**GetDevice**</span></span>](id3dxline--getdevice.md)             | <span data-ttu-id="d277f-125">Récupère le périphérique Direct3D associé à l’objet Line.</span><span class="sxs-lookup"><span data-stu-id="d277f-125">Retrieves the Direct3D device associated with the line object.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="d277f-126">**GetGLLines**</span><span class="sxs-lookup"><span data-stu-id="d277f-126">**GetGLLines**</span></span>](id3dxline--getgllines.md)           | <span data-ttu-id="d277f-127">Obtient le mode de dessin de lignes de style OpenGL.</span><span class="sxs-lookup"><span data-stu-id="d277f-127">Gets the OpenGL-style line-drawing mode.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="d277f-128">**GetPattern**</span><span class="sxs-lookup"><span data-stu-id="d277f-128">**GetPattern**</span></span>](id3dxline--getpattern.md)           | <span data-ttu-id="d277f-129">Obtient le modèle de stipple de la ligne.</span><span class="sxs-lookup"><span data-stu-id="d277f-129">Gets the line stipple pattern.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="d277f-130">**GetPatternScale**</span><span class="sxs-lookup"><span data-stu-id="d277f-130">**GetPatternScale**</span></span>](id3dxline--getpatternscale.md) | <span data-ttu-id="d277f-131">Obtient la valeur de mise à l’échelle du modèle stipple.</span><span class="sxs-lookup"><span data-stu-id="d277f-131">Gets the stipple-pattern scale value.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="d277f-132">**GetWidth**</span><span class="sxs-lookup"><span data-stu-id="d277f-132">**GetWidth**</span></span>](id3dxline--getwidth.md)               | <span data-ttu-id="d277f-133">Obtient l’épaisseur de la ligne.</span><span class="sxs-lookup"><span data-stu-id="d277f-133">Gets the thickness of the line.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="d277f-134">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="d277f-134">**OnLostDevice**</span></span>](id3dxline--onlostdevice.md)       | <span data-ttu-id="d277f-135">Utilisez cette méthode pour libérer toutes les références aux ressources de la mémoire vidéo et supprimer tous les stateblocks.</span><span class="sxs-lookup"><span data-stu-id="d277f-135">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="d277f-136">Cette méthode doit être appelée chaque fois qu’un appareil est perdu, ou avant de réinitialiser un appareil.</span><span class="sxs-lookup"><span data-stu-id="d277f-136">This method should be called whenever a device is lost, or before resetting a device.</span></span><br/> |
| [<span data-ttu-id="d277f-137">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="d277f-137">**OnResetDevice**</span></span>](id3dxline--onresetdevice.md)     | <span data-ttu-id="d277f-138">Utilisez cette méthode pour acquérir à nouveau des ressources et enregistrer l’état initial.</span><span class="sxs-lookup"><span data-stu-id="d277f-138">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="d277f-139">**SetAntialias**</span><span class="sxs-lookup"><span data-stu-id="d277f-139">**SetAntialias**</span></span>](id3dxline--setantialias.md)       | <span data-ttu-id="d277f-140">Active ou désactive l’anticrénelage de ligne.</span><span class="sxs-lookup"><span data-stu-id="d277f-140">Toggles line antialiasing.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="d277f-141">**SetGLLines**</span><span class="sxs-lookup"><span data-stu-id="d277f-141">**SetGLLines**</span></span>](id3dxline--setgllines.md)           | <span data-ttu-id="d277f-142">Active/désactive le mode de dessin des lignes de style OpenGL.</span><span class="sxs-lookup"><span data-stu-id="d277f-142">Toggles the mode to draw OpenGL-style lines.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="d277f-143">**SetPattern**</span><span class="sxs-lookup"><span data-stu-id="d277f-143">**SetPattern**</span></span>](id3dxline--setpattern.md)           | <span data-ttu-id="d277f-144">Applique un modèle de stipple à la ligne.</span><span class="sxs-lookup"><span data-stu-id="d277f-144">Applies a stipple pattern to the line.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="d277f-145">**SetPatternScale**</span><span class="sxs-lookup"><span data-stu-id="d277f-145">**SetPatternScale**</span></span>](id3dxline--setpatternscale.md) | <span data-ttu-id="d277f-146">Étire le modèle stipple le long de la direction de la ligne.</span><span class="sxs-lookup"><span data-stu-id="d277f-146">Stretches the stipple pattern along the line direction.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="d277f-147">**SetWidth**</span><span class="sxs-lookup"><span data-stu-id="d277f-147">**SetWidth**</span></span>](id3dxline--setwidth.md)               | <span data-ttu-id="d277f-148">Spécifie l’épaisseur de la ligne.</span><span class="sxs-lookup"><span data-stu-id="d277f-148">Specifies the thickness of the line.</span></span><br/>                                                                                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="d277f-149">Notes</span><span class="sxs-lookup"><span data-stu-id="d277f-149">Remarks</span></span>

<span data-ttu-id="d277f-150">Créez un objet de dessin de ligne avec [**D3DXCreateLine**](d3dxcreateline.md).</span><span class="sxs-lookup"><span data-stu-id="d277f-150">Create a line drawing object with [**D3DXCreateLine**](d3dxcreateline.md).</span></span>

<span data-ttu-id="d277f-151">Le type LPD3DXLINE est défini comme un pointeur vers l’interface **ID3DXLine** .</span><span class="sxs-lookup"><span data-stu-id="d277f-151">The LPD3DXLINE type is defined as a pointer to the **ID3DXLine** interface.</span></span>


```
typedef interface ID3DXLine ID3DXLine;
typedef interface ID3DXLine *LPD3DXLINE;
```



## <a name="requirements"></a><span data-ttu-id="d277f-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d277f-152">Requirements</span></span>



| <span data-ttu-id="d277f-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d277f-153">Requirement</span></span> | <span data-ttu-id="d277f-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="d277f-154">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d277f-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="d277f-155">Header</span></span><br/>  | <dl> <span data-ttu-id="d277f-156"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="d277f-156"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="d277f-157">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d277f-157">Library</span></span><br/> | <dl> <span data-ttu-id="d277f-158"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d277f-158"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d277f-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d277f-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d277f-160">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="d277f-160">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
