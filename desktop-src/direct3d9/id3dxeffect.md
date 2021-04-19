---
description: Utilisé pour définir et interroger des effets, et pour choisir des techniques. Un objet Effect peut contenir plusieurs techniques pour afficher le même effet.
ms.assetid: bffc64ab-12e7-44e9-b296-262b0459a68a
title: Interface ID3DXEffect (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 275376234739964940d70381a34331ff5b89f2dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106542149"
---
# <a name="id3dxeffect-interface"></a><span data-ttu-id="d6515-104">Interface ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="d6515-104">ID3DXEffect interface</span></span>

<span data-ttu-id="d6515-105">Utilisé pour définir et interroger des effets, et pour choisir des techniques.</span><span class="sxs-lookup"><span data-stu-id="d6515-105">Used to set and query effects, and to choose techniques.</span></span> <span data-ttu-id="d6515-106">Un objet Effect peut contenir plusieurs techniques pour afficher le même effet.</span><span class="sxs-lookup"><span data-stu-id="d6515-106">An effect object can contain multiple techniques to render the same effect.</span></span>

## <a name="members"></a><span data-ttu-id="d6515-107">Membres</span><span class="sxs-lookup"><span data-stu-id="d6515-107">Members</span></span>

<span data-ttu-id="d6515-108">L’interface **ID3DXEffect** hérite de [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span><span class="sxs-lookup"><span data-stu-id="d6515-108">The **ID3DXEffect** interface inherits from [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span></span> <span data-ttu-id="d6515-109">**ID3DXEffect** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d6515-109">**ID3DXEffect** also has these types of members:</span></span>

-   [<span data-ttu-id="d6515-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d6515-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d6515-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d6515-111">Methods</span></span>

<span data-ttu-id="d6515-112">L’interface **ID3DXEffect** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d6515-112">The **ID3DXEffect** interface has these methods.</span></span>



| <span data-ttu-id="d6515-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="d6515-113">Method</span></span>                                                                | <span data-ttu-id="d6515-114">Description</span><span class="sxs-lookup"><span data-stu-id="d6515-114">Description</span></span>                                                                                                                                                                                      |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6515-115">**ApplyParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="d6515-115">**ApplyParameterBlock**</span></span>](id3dxeffect--applyparameterblock.md)       | <span data-ttu-id="d6515-116">Appliquez les valeurs d’un bloc d’État à l’état du système d’effet actuel.</span><span class="sxs-lookup"><span data-stu-id="d6515-116">Apply the values in a state block to the current effect system state.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="d6515-117">**Début**</span><span class="sxs-lookup"><span data-stu-id="d6515-117">**Begin**</span></span>](id3dxeffect--begin.md)                                   | <span data-ttu-id="d6515-118">Démarre une technique active.</span><span class="sxs-lookup"><span data-stu-id="d6515-118">Starts an active technique.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="d6515-119">**BeginParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="d6515-119">**BeginParameterBlock**</span></span>](id3dxeffect--beginparameterblock.md)       | <span data-ttu-id="d6515-120">Démarrer la capture des modifications d’État dans un bloc de paramètres.</span><span class="sxs-lookup"><span data-stu-id="d6515-120">Start capturing state changes in a parameter block.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="d6515-121">**BeginPass**</span><span class="sxs-lookup"><span data-stu-id="d6515-121">**BeginPass**</span></span>](id3dxeffect--beginpass.md)                           | <span data-ttu-id="d6515-122">Commence une passe, dans la technique active.</span><span class="sxs-lookup"><span data-stu-id="d6515-122">Begins a pass, within the active technique.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="d6515-123">**CloneEffect**</span><span class="sxs-lookup"><span data-stu-id="d6515-123">**CloneEffect**</span></span>](id3dxeffect--cloneeffect.md)                       | <span data-ttu-id="d6515-124">Crée une copie d’un effet.</span><span class="sxs-lookup"><span data-stu-id="d6515-124">Creates a copy of an effect.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="d6515-125">**CommitChanges**</span><span class="sxs-lookup"><span data-stu-id="d6515-125">**CommitChanges**</span></span>](id3dxeffect--commitchanges.md)                   | <span data-ttu-id="d6515-126">Propage les modifications d’État qui se produisent à l’intérieur d’une passe active à l’appareil avant le rendu.</span><span class="sxs-lookup"><span data-stu-id="d6515-126">Propagate state changes that occur inside of an active pass to the device before rendering.</span></span><br/>                                                                                           |
| [<span data-ttu-id="d6515-127">**DeleteParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="d6515-127">**DeleteParameterBlock**</span></span>](id3dxeffect--deleteparameterblock.md)     | <span data-ttu-id="d6515-128">Supprimer un bloc de paramètres.</span><span class="sxs-lookup"><span data-stu-id="d6515-128">Delete a parameter block.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="d6515-129">**Effet**</span><span class="sxs-lookup"><span data-stu-id="d6515-129">**End**</span></span>](id3dxeffect--end.md)                                       | <span data-ttu-id="d6515-130">Met fin à une technique active.</span><span class="sxs-lookup"><span data-stu-id="d6515-130">Ends an active technique.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="d6515-131">**EndParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="d6515-131">**EndParameterBlock**</span></span>](id3dxeffect--endparameterblock.md)           | <span data-ttu-id="d6515-132">Arrêter la capture des modifications d’état des paramètres d’effet.</span><span class="sxs-lookup"><span data-stu-id="d6515-132">Stop capturing effect parameter state changes.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="d6515-133">**EndPass**</span><span class="sxs-lookup"><span data-stu-id="d6515-133">**EndPass**</span></span>](id3dxeffect--endpass.md)                               | <span data-ttu-id="d6515-134">Terminer une passe active.</span><span class="sxs-lookup"><span data-stu-id="d6515-134">End an active pass.</span></span><br/>                                                                                                                                                                   |
| [<span data-ttu-id="d6515-135">**FindNextValidTechnique**</span><span class="sxs-lookup"><span data-stu-id="d6515-135">**FindNextValidTechnique**</span></span>](id3dxeffect--findnextvalidtechnique.md) | <span data-ttu-id="d6515-136">Recherche la technique suivante valide, en commençant par la technique qui suit la technique spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d6515-136">Searches for the next valid technique, starting at the technique after the specified technique.</span></span><br/>                                                                                       |
| [<span data-ttu-id="d6515-137">**GetCurrentTechnique**</span><span class="sxs-lookup"><span data-stu-id="d6515-137">**GetCurrentTechnique**</span></span>](id3dxeffect--getcurrenttechnique.md)       | <span data-ttu-id="d6515-138">Obtient la technique actuelle.</span><span class="sxs-lookup"><span data-stu-id="d6515-138">Gets the current technique.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="d6515-139">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="d6515-139">**GetDevice**</span></span>](id3dxeffect--getdevice.md)                           | <span data-ttu-id="d6515-140">Récupère l’appareil associé à l’effet.</span><span class="sxs-lookup"><span data-stu-id="d6515-140">Retrieves the device associated with the effect.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="d6515-141">**GetPool**</span><span class="sxs-lookup"><span data-stu-id="d6515-141">**GetPool**</span></span>](id3dxeffect--getpool.md)                               | <span data-ttu-id="d6515-142">Obtient un pointeur vers le pool de paramètres partagés.</span><span class="sxs-lookup"><span data-stu-id="d6515-142">Gets a pointer to the pool of shared parameters.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="d6515-143">**GetStateManager**</span><span class="sxs-lookup"><span data-stu-id="d6515-143">**GetStateManager**</span></span>](id3dxeffect--getstatemanager.md)               | <span data-ttu-id="d6515-144">Obtient le gestionnaire d’état des effets.</span><span class="sxs-lookup"><span data-stu-id="d6515-144">Get the effect state manager.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="d6515-145">**IsParameterUsed**</span><span class="sxs-lookup"><span data-stu-id="d6515-145">**IsParameterUsed**</span></span>](id3dxeffect--isparameterused.md)               | <span data-ttu-id="d6515-146">Détermine si un paramètre est utilisé par la technique.</span><span class="sxs-lookup"><span data-stu-id="d6515-146">Determines if a parameter is used by the technique.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="d6515-147">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="d6515-147">**OnLostDevice**</span></span>](id3dxeffect--onlostdevice.md)                     | <span data-ttu-id="d6515-148">Utilisez cette méthode pour libérer toutes les références aux ressources de la mémoire vidéo et supprimer tous les stateblocks.</span><span class="sxs-lookup"><span data-stu-id="d6515-148">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="d6515-149">Cette méthode doit être appelée chaque fois qu’un appareil est perdu, ou avant de réinitialiser un appareil.</span><span class="sxs-lookup"><span data-stu-id="d6515-149">This method should be called whenever a device is lost, or before resetting a device.</span></span><br/> |
| [<span data-ttu-id="d6515-150">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="d6515-150">**OnResetDevice**</span></span>](id3dxeffect--onresetdevice.md)                   | <span data-ttu-id="d6515-151">Utilisez cette méthode pour acquérir à nouveau des ressources et enregistrer l’état initial.</span><span class="sxs-lookup"><span data-stu-id="d6515-151">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="d6515-152">**SetRawValue**</span><span class="sxs-lookup"><span data-stu-id="d6515-152">**SetRawValue**</span></span>](id3dxeffect--setrawvalue.md)                       | <span data-ttu-id="d6515-153">Définissez une plage contiguë de constantes de nuanceur avec une copie de mémoire.</span><span class="sxs-lookup"><span data-stu-id="d6515-153">Set a contiguous range of shader constants with a memory copy.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="d6515-154">**SetStateManager**</span><span class="sxs-lookup"><span data-stu-id="d6515-154">**SetStateManager**</span></span>](id3dxeffect--setstatemanager.md)               | <span data-ttu-id="d6515-155">Définissez le gestionnaire d’état des effets.</span><span class="sxs-lookup"><span data-stu-id="d6515-155">Set the effect state manager.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="d6515-156">**SetTechnique**</span><span class="sxs-lookup"><span data-stu-id="d6515-156">**SetTechnique**</span></span>](id3dxeffect--settechnique.md)                     | <span data-ttu-id="d6515-157">Définit la technique active.</span><span class="sxs-lookup"><span data-stu-id="d6515-157">Sets the active technique.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="d6515-158">**ValidateTechnique**</span><span class="sxs-lookup"><span data-stu-id="d6515-158">**ValidateTechnique**</span></span>](id3dxeffect--validatetechnique.md)           | <span data-ttu-id="d6515-159">Valider une technique.</span><span class="sxs-lookup"><span data-stu-id="d6515-159">Validate a technique.</span></span><br/>                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="d6515-160">Notes</span><span class="sxs-lookup"><span data-stu-id="d6515-160">Remarks</span></span>

<span data-ttu-id="d6515-161">L’interface ID3DXEffect est obtenue en appelant [**D3DXCreateEffect**](d3dxcreateeffect.md), [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md)ou [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md).</span><span class="sxs-lookup"><span data-stu-id="d6515-161">The ID3DXEffect interface is obtained by calling [**D3DXCreateEffect**](d3dxcreateeffect.md), [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md), or [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md).</span></span>

<span data-ttu-id="d6515-162">Le type LPD3DXEFFECT est défini en tant que pointeur vers cette interface.</span><span class="sxs-lookup"><span data-stu-id="d6515-162">The LPD3DXEFFECT type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXEffect ID3DXEffect;
typedef interface ID3DXEffect *LPD3DXEFFECT;
```



## <a name="requirements"></a><span data-ttu-id="d6515-163">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6515-163">Requirements</span></span>



| <span data-ttu-id="d6515-164">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6515-164">Requirement</span></span> | <span data-ttu-id="d6515-165">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6515-165">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6515-166">En-tête</span><span class="sxs-lookup"><span data-stu-id="d6515-166">Header</span></span><br/>  | <dl> <span data-ttu-id="d6515-167"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6515-167"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="d6515-168">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d6515-168">Library</span></span><br/> | <dl> <span data-ttu-id="d6515-169"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6515-169"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d6515-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6515-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6515-171">**ID3DXBaseEffect**</span><span class="sxs-lookup"><span data-stu-id="d6515-171">**ID3DXBaseEffect**</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="d6515-172">Interfaces d’effet</span><span class="sxs-lookup"><span data-stu-id="d6515-172">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[<span data-ttu-id="d6515-173">**D3DXCreateEffect**</span><span class="sxs-lookup"><span data-stu-id="d6515-173">**D3DXCreateEffect**</span></span>](d3dxcreateeffect.md)
</dt> <dt>

[<span data-ttu-id="d6515-174">**D3DXCreateEffectFromFile**</span><span class="sxs-lookup"><span data-stu-id="d6515-174">**D3DXCreateEffectFromFile**</span></span>](d3dxcreateeffectfromfile.md)
</dt> <dt>

[<span data-ttu-id="d6515-175">**D3DXCreateEffectFromResource**</span><span class="sxs-lookup"><span data-stu-id="d6515-175">**D3DXCreateEffectFromResource**</span></span>](d3dxcreateeffectfromresource.md)
</dt> </dl>

 

 




