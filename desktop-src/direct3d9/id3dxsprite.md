---
description: L’interface ID3DXSprite fournit un ensemble de méthodes qui simplifient le processus de dessin de sprites à l’aide de Microsoft Direct3D.
ms.assetid: ccf34fac-91a7-4734-bc62-aedaf4d66522
title: Interface ID3DXSprite (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3703132cd8a0f7744119d9b8cb5d9d48f260094c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870134"
---
# <a name="id3dxsprite-interface"></a><span data-ttu-id="3a410-103">Interface ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="3a410-103">ID3DXSprite interface</span></span>

<span data-ttu-id="3a410-104">L’interface ID3DXSprite fournit un ensemble de méthodes qui simplifient le processus de dessin de sprites à l’aide de Microsoft Direct3D.</span><span class="sxs-lookup"><span data-stu-id="3a410-104">The ID3DXSprite interface provides a set of methods that simplify the process of drawing sprites using Microsoft Direct3D.</span></span>

## <a name="members"></a><span data-ttu-id="3a410-105">Membres</span><span class="sxs-lookup"><span data-stu-id="3a410-105">Members</span></span>

<span data-ttu-id="3a410-106">L’interface **ID3DXSprite** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3a410-106">The **ID3DXSprite** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3a410-107">**ID3DXSprite** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3a410-107">**ID3DXSprite** also has these types of members:</span></span>

-   [<span data-ttu-id="3a410-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3a410-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3a410-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3a410-109">Methods</span></span>

<span data-ttu-id="3a410-110">L’interface **ID3DXSprite** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="3a410-110">The **ID3DXSprite** interface has these methods.</span></span>



| <span data-ttu-id="3a410-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="3a410-111">Method</span></span>                                                | <span data-ttu-id="3a410-112">Description</span><span class="sxs-lookup"><span data-stu-id="3a410-112">Description</span></span>                                                                                                                                                                                                                  |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3a410-113">**Début**</span><span class="sxs-lookup"><span data-stu-id="3a410-113">**Begin**</span></span>](id3dxsprite--begin.md)                   | <span data-ttu-id="3a410-114">Prépare un appareil pour le dessin des sprites.</span><span class="sxs-lookup"><span data-stu-id="3a410-114">Prepares a device for drawing sprites.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="3a410-115">**Dessin**</span><span class="sxs-lookup"><span data-stu-id="3a410-115">**Draw**</span></span>](id3dxsprite--draw.md)                     | <span data-ttu-id="3a410-116">Ajoute un sprite à la liste des sprites regroupés par lots.</span><span class="sxs-lookup"><span data-stu-id="3a410-116">Adds a sprite to the list of batched sprites.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="3a410-117">**Effet**</span><span class="sxs-lookup"><span data-stu-id="3a410-117">**End**</span></span>](id3dxsprite--end.md)                       | <span data-ttu-id="3a410-118">Appelle [**ID3DXSprite :: Flush**](id3dxsprite--flush.md) et restaure l’état de l’appareil pour qu’il se trouvait avant l’appel de [**ID3DXSprite :: Begin**](id3dxsprite--begin.md) .</span><span class="sxs-lookup"><span data-stu-id="3a410-118">Calls [**ID3DXSprite::Flush**](id3dxsprite--flush.md) and restores the device state to how it was before [**ID3DXSprite::Begin**](id3dxsprite--begin.md) was called.</span></span><br/>                                            |
| [<span data-ttu-id="3a410-119">**Purge**</span><span class="sxs-lookup"><span data-stu-id="3a410-119">**Flush**</span></span>](id3dxsprite--flush.md)                   | <span data-ttu-id="3a410-120">Force tous les sprites regroupés par lot à être envoyés à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3a410-120">Forces all batched sprites to be submitted to the device.</span></span> <span data-ttu-id="3a410-121">Les États des appareils restent tels qu’ils étaient après le dernier appel à [**ID3DXSprite :: Begin**](id3dxsprite--begin.md).</span><span class="sxs-lookup"><span data-stu-id="3a410-121">Device states remain as they were after the last call to [**ID3DXSprite::Begin**](id3dxsprite--begin.md).</span></span> <span data-ttu-id="3a410-122">La liste des sprites regroupés par lot est alors effacée.</span><span class="sxs-lookup"><span data-stu-id="3a410-122">The list of batched sprites is then cleared.</span></span><br/> |
| [<span data-ttu-id="3a410-123">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="3a410-123">**GetDevice**</span></span>](id3dxsprite--getdevice.md)           | <span data-ttu-id="3a410-124">Récupère l’appareil associé à l’objet Sprite.</span><span class="sxs-lookup"><span data-stu-id="3a410-124">Retrieves the device associated with the sprite object.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="3a410-125">**GetTransform**</span><span class="sxs-lookup"><span data-stu-id="3a410-125">**GetTransform**</span></span>](id3dxsprite--gettransform.md)     | <span data-ttu-id="3a410-126">Obtient la transformation de sprite.</span><span class="sxs-lookup"><span data-stu-id="3a410-126">Gets the sprite transform.</span></span><br/>                                                                                                                                                                                        |
| [<span data-ttu-id="3a410-127">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="3a410-127">**OnLostDevice**</span></span>](id3dxsprite--onlostdevice.md)     | <span data-ttu-id="3a410-128">Utilisez cette méthode pour libérer toutes les références aux ressources de la mémoire vidéo et supprimer tous les stateblocks.</span><span class="sxs-lookup"><span data-stu-id="3a410-128">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="3a410-129">Cette méthode doit être appelée chaque fois qu’un appareil est perdu ou avant de réinitialiser un appareil.</span><span class="sxs-lookup"><span data-stu-id="3a410-129">This method should be called whenever a device is lost or before resetting a device.</span></span><br/>                              |
| [<span data-ttu-id="3a410-130">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="3a410-130">**OnResetDevice**</span></span>](id3dxsprite--onresetdevice.md)   | <span data-ttu-id="3a410-131">Utilisez cette méthode pour acquérir à nouveau des ressources et enregistrer l’état initial.</span><span class="sxs-lookup"><span data-stu-id="3a410-131">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="3a410-132">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="3a410-132">**SetTransform**</span></span>](id3dxsprite--settransform.md)     | <span data-ttu-id="3a410-133">Définit la transformation Sprite.</span><span class="sxs-lookup"><span data-stu-id="3a410-133">Sets the sprite transform.</span></span><br/>                                                                                                                                                                                        |
| [<span data-ttu-id="3a410-134">**SetWorldViewLH**</span><span class="sxs-lookup"><span data-stu-id="3a410-134">**SetWorldViewLH**</span></span>](id3dxsprite--setworldviewlh.md) | <span data-ttu-id="3a410-135">Définit la transformation de vue universelle de gauche pour un sprite.</span><span class="sxs-lookup"><span data-stu-id="3a410-135">Sets the left-handed world-view transform for a sprite.</span></span> <span data-ttu-id="3a410-136">Un appel à cette méthode est requis avant d’effectuer un billboarding ou de trier des sprites.</span><span class="sxs-lookup"><span data-stu-id="3a410-136">A call to this method is required before billboarding or sorting sprites.</span></span><br/>                                                                                 |
| [<span data-ttu-id="3a410-137">**SetWorldViewRH**</span><span class="sxs-lookup"><span data-stu-id="3a410-137">**SetWorldViewRH**</span></span>](id3dxsprite--setworldviewrh.md) | <span data-ttu-id="3a410-138">Définit la transformation de la vue universelle droitier pour un sprite.</span><span class="sxs-lookup"><span data-stu-id="3a410-138">Sets the right-handed world-view transform for a sprite.</span></span> <span data-ttu-id="3a410-139">Un appel à cette méthode est requis avant d’effectuer un billboarding ou de trier des sprites.</span><span class="sxs-lookup"><span data-stu-id="3a410-139">A call to this method is required before billboarding or sorting sprites.</span></span><br/>                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="3a410-140">Notes</span><span class="sxs-lookup"><span data-stu-id="3a410-140">Remarks</span></span>

<span data-ttu-id="3a410-141">L’interface **ID3DXSprite** est obtenue en appelant la fonction [**D3DXCreateSprite**](d3dxcreatesprite.md) .</span><span class="sxs-lookup"><span data-stu-id="3a410-141">The **ID3DXSprite** interface is obtained by calling the [**D3DXCreateSprite**](d3dxcreatesprite.md) function.</span></span>

<span data-ttu-id="3a410-142">L’application appelle généralement en premier [**ID3DXSprite :: Begin**](id3dxsprite--begin.md), qui permet de contrôler l’état de rendu de l’appareil, la fusion alpha, la transformation et le tri des sprites.</span><span class="sxs-lookup"><span data-stu-id="3a410-142">The application typically first calls [**ID3DXSprite::Begin**](id3dxsprite--begin.md), which allows control over the device render state, alpha blending, and sprite transformation and sorting.</span></span> <span data-ttu-id="3a410-143">Ensuite, pour chaque sprite à afficher, appelez [**ID3DXSprite ::D RAW**](id3dxsprite--draw.md).</span><span class="sxs-lookup"><span data-stu-id="3a410-143">Then for each sprite to be displayed, call [**ID3DXSprite::Draw**](id3dxsprite--draw.md).</span></span> <span data-ttu-id="3a410-144">**ID3DXSprite ::D RAW** peut être appelé à plusieurs reprises pour stocker un nombre quelconque de sprites.</span><span class="sxs-lookup"><span data-stu-id="3a410-144">**ID3DXSprite::Draw** can be called repeatedly to store any number of sprites.</span></span> <span data-ttu-id="3a410-145">Pour afficher les sprites regroupés par lot sur l’appareil, appelez [**ID3DXSprite :: end**](id3dxsprite--end.md) ou [**ID3DXSprite :: Flush**](id3dxsprite--flush.md).</span><span class="sxs-lookup"><span data-stu-id="3a410-145">To display the batched sprites to the device, call [**ID3DXSprite::End**](id3dxsprite--end.md) or [**ID3DXSprite::Flush**](id3dxsprite--flush.md).</span></span>

<span data-ttu-id="3a410-146">Le type LPD3DXSPRITE est défini comme un pointeur vers l’interface **ID3DXSprite** .</span><span class="sxs-lookup"><span data-stu-id="3a410-146">The LPD3DXSPRITE type is defined as a pointer to the **ID3DXSprite** interface.</span></span>


```
typedef interface ID3DXSprite ID3DXSprite;
typedef interface ID3DXSprite *LPD3DXSPRITE;
```



## <a name="requirements"></a><span data-ttu-id="3a410-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a410-147">Requirements</span></span>



| <span data-ttu-id="3a410-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a410-148">Requirement</span></span> | <span data-ttu-id="3a410-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a410-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a410-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="3a410-150">Header</span></span><br/>  | <dl> <span data-ttu-id="3a410-151"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a410-151"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="3a410-152">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3a410-152">Library</span></span><br/> | <dl> <span data-ttu-id="3a410-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a410-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3a410-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a410-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a410-155">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="3a410-155">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
