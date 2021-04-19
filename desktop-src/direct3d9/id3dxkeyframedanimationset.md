---
description: Une application utilise les méthodes de cette interface pour implémenter un ensemble d’animations d’image clé.
ms.assetid: eeb7acd8-1017-4aca-9813-188fc6703837
title: Interface ID3DXKeyframedAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0e45ab69b3a91461c947ce9c8a63885bb5ab0a8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529633"
---
# <a name="id3dxkeyframedanimationset-interface"></a><span data-ttu-id="33e51-103">Interface ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="33e51-103">ID3DXKeyframedAnimationSet interface</span></span>

<span data-ttu-id="33e51-104">Une application utilise les méthodes de cette interface pour implémenter un ensemble d’animations d’image clé.</span><span class="sxs-lookup"><span data-stu-id="33e51-104">An application uses the methods of this interface to implement a key frame animation set.</span></span>

## <a name="members"></a><span data-ttu-id="33e51-105">Membres</span><span class="sxs-lookup"><span data-stu-id="33e51-105">Members</span></span>

<span data-ttu-id="33e51-106">L’interface **ID3DXKeyframedAnimationSet** hérite de [**ID3DXAnimationSet**](id3dxanimationset.md).</span><span class="sxs-lookup"><span data-stu-id="33e51-106">The **ID3DXKeyframedAnimationSet** interface inherits from [**ID3DXAnimationSet**](id3dxanimationset.md).</span></span> <span data-ttu-id="33e51-107">**ID3DXKeyframedAnimationSet** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="33e51-107">**ID3DXKeyframedAnimationSet** also has these types of members:</span></span>

-   [<span data-ttu-id="33e51-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="33e51-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="33e51-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="33e51-109">Methods</span></span>

<span data-ttu-id="33e51-110">L’interface **ID3DXKeyframedAnimationSet** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="33e51-110">The **ID3DXKeyframedAnimationSet** interface has these methods.</span></span>



| <span data-ttu-id="33e51-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="33e51-111">Method</span></span>                                                                                   | <span data-ttu-id="33e51-112">Description</span><span class="sxs-lookup"><span data-stu-id="33e51-112">Description</span></span>                                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="33e51-113">**Dens**</span><span class="sxs-lookup"><span data-stu-id="33e51-113">**Compress**</span></span>](id3dxkeyframedanimationset--compress.md)                                 | <span data-ttu-id="33e51-114">Transforme les animations dans une animation définie dans un format compressé et retourne un pointeur vers la mémoire tampon qui stocke les données compressées.</span><span class="sxs-lookup"><span data-stu-id="33e51-114">Transforms animations in an animation set into a compressed format and returns a pointer to the buffer that stores the compressed data.</span></span><br/> |
| [<span data-ttu-id="33e51-115">**GetCallbackKey**</span><span class="sxs-lookup"><span data-stu-id="33e51-115">**GetCallbackKey**</span></span>](id3dxkeyframedanimationset--getcallbackkey.md)                     | <span data-ttu-id="33e51-116">Obtient des informations sur un rappel spécifique dans l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="33e51-116">Gets information about a specific callback in the animation set.</span></span><br/>                                                                        |
| [<span data-ttu-id="33e51-117">**GetCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="33e51-117">**GetCallbackKeys**</span></span>](id3dxkeyframedanimationset--getcallbackkeys.md)                   | <span data-ttu-id="33e51-118">Remplit un tableau avec les données de clé de rappel utilisées pour l’animation d’image clé.</span><span class="sxs-lookup"><span data-stu-id="33e51-118">Fills an array with callback key data used for key frame animation.</span></span><br/>                                                                     |
| [<span data-ttu-id="33e51-119">**GetNumCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="33e51-119">**GetNumCallbackKeys**</span></span>](id3dxkeyframedanimationset--getnumcallbackkeys.md)             | <span data-ttu-id="33e51-120">Obtient le nombre de clés de rappel dans l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="33e51-120">Gets the number of callback keys in the animation set.</span></span><br/>                                                                                  |
| [<span data-ttu-id="33e51-121">**GetNumRotationKeys**</span><span class="sxs-lookup"><span data-stu-id="33e51-121">**GetNumRotationKeys**</span></span>](id3dxkeyframedanimationset--getnumrotationkeys.md)             | <span data-ttu-id="33e51-122">Obtient le nombre de clés de rotation dans l’animation d’image clé spécifiée.</span><span class="sxs-lookup"><span data-stu-id="33e51-122">Gets the number of rotation keys in the specified key frame animation.</span></span><br/>                                                                  |
| [<span data-ttu-id="33e51-123">**GetNumScaleKeys**</span><span class="sxs-lookup"><span data-stu-id="33e51-123">**GetNumScaleKeys**</span></span>](id3dxkeyframedanimationset--getnumscalekeys.md)                   | <span data-ttu-id="33e51-124">Obtient le nombre de clés de mise à l’échelle dans l’animation d’image clé spécifiée.</span><span class="sxs-lookup"><span data-stu-id="33e51-124">Gets the number of scale keys in the specified key frame animation.</span></span><br/>                                                                     |
| [<span data-ttu-id="33e51-125">**GetNumTranslationKeys**</span><span class="sxs-lookup"><span data-stu-id="33e51-125">**GetNumTranslationKeys**</span></span>](id3dxkeyframedanimationset--getnumtranslationkeys.md)       | <span data-ttu-id="33e51-126">Obtient le nombre de clés de traduction dans l’animation d’image clé spécifiée.</span><span class="sxs-lookup"><span data-stu-id="33e51-126">Gets the number of translation keys in the specified key frame animation.</span></span><br/>                                                               |
| [<span data-ttu-id="33e51-127">**GetPlaybackType**</span><span class="sxs-lookup"><span data-stu-id="33e51-127">**GetPlaybackType**</span></span>](id3dxkeyframedanimationset--getplaybacktype.md)                   | <span data-ttu-id="33e51-128">Obtient le type de la boucle de lecture du jeu d’animations.</span><span class="sxs-lookup"><span data-stu-id="33e51-128">Gets the type of the animation set playback loop.</span></span><br/>                                                                                       |
| [<span data-ttu-id="33e51-129">**GetRotationKey**</span><span class="sxs-lookup"><span data-stu-id="33e51-129">**GetRotationKey**</span></span>](id3dxkeyframedanimationset--getrotationkey.md)                     | <span data-ttu-id="33e51-130">Obtient des informations de rotation pour une image clé spécifique dans l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="33e51-130">Get rotation information for a specific key frame in the animation set.</span></span><br/>                                                                 |
| [<span data-ttu-id="33e51-131">**GetRotationKeys**</span><span class="sxs-lookup"><span data-stu-id="33e51-131">**GetRotationKeys**</span></span>](id3dxkeyframedanimationset--getrotationkeys.md)                   | <span data-ttu-id="33e51-132">Remplit un tableau avec les données de clé de rotation utilisées pour l’animation d’image clé.</span><span class="sxs-lookup"><span data-stu-id="33e51-132">Fills an array with rotational key data used for key frame animation.</span></span><br/>                                                                   |
| [<span data-ttu-id="33e51-133">**GetScaleKey**</span><span class="sxs-lookup"><span data-stu-id="33e51-133">**GetScaleKey**</span></span>](id3dxkeyframedanimationset--getscalekey.md)                           | <span data-ttu-id="33e51-134">Obtenir des informations de mise à l’échelle pour une image clé spécifique dans l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="33e51-134">Get scale information for a specific key frame in the animation set.</span></span><br/>                                                                    |
| [<span data-ttu-id="33e51-135">**GetScaleKeys**</span><span class="sxs-lookup"><span data-stu-id="33e51-135">**GetScaleKeys**</span></span>](id3dxkeyframedanimationset--getscalekeys.md)                         | <span data-ttu-id="33e51-136">Remplit un tableau avec les données de la clé de mise à l’échelle utilisées pour l’animation d’image clé.</span><span class="sxs-lookup"><span data-stu-id="33e51-136">Fills an array with scale key data used for key frame animation.</span></span><br/>                                                                        |
| [<span data-ttu-id="33e51-137">**GetSourceTicksPerSecond**</span><span class="sxs-lookup"><span data-stu-id="33e51-137">**GetSourceTicksPerSecond**</span></span>](id3dxkeyframedanimationset--getsourcetickspersecond.md)   | <span data-ttu-id="33e51-138">Obtient le nombre de graduations d’image clé d’animation qui se produisent par seconde.</span><span class="sxs-lookup"><span data-stu-id="33e51-138">Gets the number of animation key frame ticks that occur per second.</span></span><br/>                                                                     |
| [<span data-ttu-id="33e51-139">**GetTranslationKey**</span><span class="sxs-lookup"><span data-stu-id="33e51-139">**GetTranslationKey**</span></span>](id3dxkeyframedanimationset--gettranslationkey.md)               | <span data-ttu-id="33e51-140">Obtenir des informations de traduction pour une image clé spécifique dans l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="33e51-140">Get translation information for a specific key frame in the animation set.</span></span><br/>                                                              |
| [<span data-ttu-id="33e51-141">**GetTranslationKeys**</span><span class="sxs-lookup"><span data-stu-id="33e51-141">**GetTranslationKeys**</span></span>](id3dxkeyframedanimationset--gettranslationkeys.md)             | <span data-ttu-id="33e51-142">Remplit un tableau avec les données de clé de traduction utilisées pour l’animation d’image clé.</span><span class="sxs-lookup"><span data-stu-id="33e51-142">Fills an array with translational key data used for key frame animation.</span></span><br/>                                                                |
| [<span data-ttu-id="33e51-143">**RegisterAnimationSRTKeys**</span><span class="sxs-lookup"><span data-stu-id="33e51-143">**RegisterAnimationSRTKeys**</span></span>](id3dxkeyframedanimationset--registeranimationsrtkeys.md) | <span data-ttu-id="33e51-144">Enregistre les données de l’image clé de l’échelle, de rotation et de translation (SRT) pour une animation.</span><span class="sxs-lookup"><span data-stu-id="33e51-144">Register the scale, rotate, and translate (SRT) key frame data for an animation.</span></span><br/>                                                        |
| [<span data-ttu-id="33e51-145">**SetCallbackKey**</span><span class="sxs-lookup"><span data-stu-id="33e51-145">**SetCallbackKey**</span></span>](id3dxkeyframedanimationset--setcallbackkey.md)                     | <span data-ttu-id="33e51-146">Définit des informations sur un rappel spécifique dans l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="33e51-146">Sets information about a specific callback in the animation set.</span></span><br/>                                                                        |
| [<span data-ttu-id="33e51-147">**SetRotationKey**</span><span class="sxs-lookup"><span data-stu-id="33e51-147">**SetRotationKey**</span></span>](id3dxkeyframedanimationset--setrotationkey.md)                     | <span data-ttu-id="33e51-148">Définissez les informations de rotation pour une image clé spécifique dans l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="33e51-148">Set rotation information for a specific key frame in the animation set.</span></span><br/>                                                                 |
| [<span data-ttu-id="33e51-149">**SetScaleKey**</span><span class="sxs-lookup"><span data-stu-id="33e51-149">**SetScaleKey**</span></span>](id3dxkeyframedanimationset--setscalekey.md)                           | <span data-ttu-id="33e51-150">Définir les informations de mise à l’échelle d’une image clé spécifique dans l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="33e51-150">Set scale information for a specific key frame in the animation set.</span></span><br/>                                                                    |
| [<span data-ttu-id="33e51-151">**SetTranslationKey**</span><span class="sxs-lookup"><span data-stu-id="33e51-151">**SetTranslationKey**</span></span>](id3dxkeyframedanimationset--settranslationkey.md)               | <span data-ttu-id="33e51-152">Définissez les informations de traduction pour une image clé spécifique dans l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="33e51-152">Set translation information for a specific key frame in the animation set.</span></span><br/>                                                              |
| [<span data-ttu-id="33e51-153">**UnregisterAnimation**</span><span class="sxs-lookup"><span data-stu-id="33e51-153">**UnregisterAnimation**</span></span>](id3dxkeyframedanimationset--unregisteranimation.md)           | <span data-ttu-id="33e51-154">Supprimez les données d’animation du jeu d’animations.</span><span class="sxs-lookup"><span data-stu-id="33e51-154">Remove the animation data from the animation set.</span></span><br/>                                                                                       |
| [<span data-ttu-id="33e51-155">**UnregisterRotationKey**</span><span class="sxs-lookup"><span data-stu-id="33e51-155">**UnregisterRotationKey**</span></span>](id3dxkeyframedanimationset--unregisterrotationkey.md)       | <span data-ttu-id="33e51-156">Supprime les données de rotation au niveau de l’image clé spécifiée.</span><span class="sxs-lookup"><span data-stu-id="33e51-156">Removes the rotation data at the specified key frame.</span></span><br/>                                                                                   |
| [<span data-ttu-id="33e51-157">**UnregisterScaleKey**</span><span class="sxs-lookup"><span data-stu-id="33e51-157">**UnregisterScaleKey**</span></span>](id3dxkeyframedanimationset--unregisterscalekey.md)             | <span data-ttu-id="33e51-158">Supprime les données de mise à l’échelle au niveau de l’image clé spécifiée.</span><span class="sxs-lookup"><span data-stu-id="33e51-158">Removes the scale data at the specified key frame.</span></span><br/>                                                                                      |
| [<span data-ttu-id="33e51-159">**UnregisterTranslationKey**</span><span class="sxs-lookup"><span data-stu-id="33e51-159">**UnregisterTranslationKey**</span></span>](id3dxkeyframedanimationset--unregistertranslationkey.md) | <span data-ttu-id="33e51-160">Supprime les données de traduction au niveau de l’image clé spécifiée.</span><span class="sxs-lookup"><span data-stu-id="33e51-160">Removes the translation data at the specified key frame.</span></span><br/>                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="33e51-161">Notes</span><span class="sxs-lookup"><span data-stu-id="33e51-161">Remarks</span></span>

<span data-ttu-id="33e51-162">Créer une animation avec image clé définie avec [**D3DXCreateKeyframedAnimationSet**](d3dxcreatekeyframedanimationset.md).</span><span class="sxs-lookup"><span data-stu-id="33e51-162">Create a keyframed animation set with [**D3DXCreateKeyframedAnimationSet**](d3dxcreatekeyframedanimationset.md).</span></span>

<span data-ttu-id="33e51-163">Le type LPD3DXKEYFRAMEDANIMATIONSET est défini en tant que pointeur vers cette interface.</span><span class="sxs-lookup"><span data-stu-id="33e51-163">The LPD3DXKEYFRAMEDANIMATIONSET type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXKeyframedAnimationSet ID3DXKeyframedAnimationSet;
typedef interface ID3DXKeyframedAnimationSet *LPD3DXKEYFRAMEDANIMATIONSET;
```



## <a name="requirements"></a><span data-ttu-id="33e51-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33e51-164">Requirements</span></span>



| <span data-ttu-id="33e51-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33e51-165">Requirement</span></span> | <span data-ttu-id="33e51-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="33e51-166">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="33e51-167">En-tête</span><span class="sxs-lookup"><span data-stu-id="33e51-167">Header</span></span><br/>  | <dl> <span data-ttu-id="33e51-168"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="33e51-168"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="33e51-169">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="33e51-169">Library</span></span><br/> | <dl> <span data-ttu-id="33e51-170"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="33e51-170"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="33e51-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33e51-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33e51-172">**ID3DXAnimationSet**</span><span class="sxs-lookup"><span data-stu-id="33e51-172">**ID3DXAnimationSet**</span></span>](id3dxanimationset.md)
</dt> <dt>

[<span data-ttu-id="33e51-173">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="33e51-173">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 




