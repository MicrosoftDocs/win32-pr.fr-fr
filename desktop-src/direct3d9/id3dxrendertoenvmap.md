---
description: L’interface ID3DXRenderToEnvMap est utilisée pour généraliser le processus de rendu des mappages d’environnement.
ms.assetid: d72db260-5493-4381-9269-521ad333f0b2
title: Interface ID3DXRenderToEnvMap (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c3fdfc37c206b6360fc0b7296bbf90c319652e28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106540932"
---
# <a name="id3dxrendertoenvmap-interface"></a><span data-ttu-id="8fd5b-103">Interface ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="8fd5b-103">ID3DXRenderToEnvMap interface</span></span>

<span data-ttu-id="8fd5b-104">L’interface ID3DXRenderToEnvMap est utilisée pour généraliser le processus de rendu des mappages d’environnement.</span><span class="sxs-lookup"><span data-stu-id="8fd5b-104">The ID3DXRenderToEnvMap interface is used to generalize the process of rendering to environment maps.</span></span>

## <a name="members"></a><span data-ttu-id="8fd5b-105">Membres</span><span class="sxs-lookup"><span data-stu-id="8fd5b-105">Members</span></span>

<span data-ttu-id="8fd5b-106">L’interface **ID3DXRenderToEnvMap** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8fd5b-106">The **ID3DXRenderToEnvMap** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8fd5b-107">**ID3DXRenderToEnvMap** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8fd5b-107">**ID3DXRenderToEnvMap** also has these types of members:</span></span>

-   [<span data-ttu-id="8fd5b-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8fd5b-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8fd5b-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8fd5b-109">Methods</span></span>

<span data-ttu-id="8fd5b-110">L’interface **ID3DXRenderToEnvMap** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="8fd5b-110">The **ID3DXRenderToEnvMap** interface has these methods.</span></span>



| <span data-ttu-id="8fd5b-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="8fd5b-111">Method</span></span>                                                          | <span data-ttu-id="8fd5b-112">Description</span><span class="sxs-lookup"><span data-stu-id="8fd5b-112">Description</span></span>                                                                                                                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8fd5b-113">**BeginCube**</span><span class="sxs-lookup"><span data-stu-id="8fd5b-113">**BeginCube**</span></span>](id3dxrendertoenvmap--begincube.md)             | <span data-ttu-id="8fd5b-114">Lancer le rendu d’une carte d’environnement cubique.</span><span class="sxs-lookup"><span data-stu-id="8fd5b-114">Initiate the rendering of a cubic environment map.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="8fd5b-115">**BeginHemisphere**</span><span class="sxs-lookup"><span data-stu-id="8fd5b-115">**BeginHemisphere**</span></span>](id3dxrendertoenvmap--beginhemisphere.md) | <span data-ttu-id="8fd5b-116">Lancer le rendu d’un mappage d’environnement hémisphérique.</span><span class="sxs-lookup"><span data-stu-id="8fd5b-116">Initiate the rendering of a hemispheric environment map.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="8fd5b-117">**BeginParabolic**</span><span class="sxs-lookup"><span data-stu-id="8fd5b-117">**BeginParabolic**</span></span>](id3dxrendertoenvmap--beginparabolic.md)   | <span data-ttu-id="8fd5b-118">Lancer le rendu d’un mappage d’environnement parabolique.</span><span class="sxs-lookup"><span data-stu-id="8fd5b-118">Initiate the rendering of a parabolic environment map.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="8fd5b-119">**BeginSphere**</span><span class="sxs-lookup"><span data-stu-id="8fd5b-119">**BeginSphere**</span></span>](id3dxrendertoenvmap--beginsphere.md)         | <span data-ttu-id="8fd5b-120">Lancer le rendu d’une carte d’environnement sphérique.</span><span class="sxs-lookup"><span data-stu-id="8fd5b-120">Initiate the rendering of a spherical environment map.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="8fd5b-121">**Effet**</span><span class="sxs-lookup"><span data-stu-id="8fd5b-121">**End**</span></span>](id3dxrendertoenvmap--end.md)                         | <span data-ttu-id="8fd5b-122">Restaurez toutes les cibles de rendu et, si nécessaire, composez toutes les faces rendues dans la surface de la carte de l’environnement.</span><span class="sxs-lookup"><span data-stu-id="8fd5b-122">Restore all render targets and, if needed, compose all the rendered faces into the environment map surface.</span></span><br/>                                                                           |
| [<span data-ttu-id="8fd5b-123">**Visage**</span><span class="sxs-lookup"><span data-stu-id="8fd5b-123">**Face**</span></span>](id3dxrendertoenvmap--face.md)                       | <span data-ttu-id="8fd5b-124">Initiez le dessin de chaque face d’une carte d’environnement.</span><span class="sxs-lookup"><span data-stu-id="8fd5b-124">Initiate the drawing of each face of an environment map.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="8fd5b-125">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="8fd5b-125">**GetDesc**</span></span>](id3dxrendertoenvmap--getdesc.md)                 | <span data-ttu-id="8fd5b-126">Récupère la description de la surface de rendu.</span><span class="sxs-lookup"><span data-stu-id="8fd5b-126">Retrieves the description of the render surface.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="8fd5b-127">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="8fd5b-127">**GetDevice**</span></span>](id3dxrendertoenvmap--getdevice.md)             | <span data-ttu-id="8fd5b-128">Récupère le périphérique Direct3D associé à la carte d’environnement.</span><span class="sxs-lookup"><span data-stu-id="8fd5b-128">Retrieves the Direct3D device associated with the environment map.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="8fd5b-129">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="8fd5b-129">**OnLostDevice**</span></span>](id3dxrendertoenvmap--onlostdevice.md)       | <span data-ttu-id="8fd5b-130">Utilisez cette méthode pour libérer toutes les références aux ressources de la mémoire vidéo et supprimer tous les stateblocks.</span><span class="sxs-lookup"><span data-stu-id="8fd5b-130">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="8fd5b-131">Cette méthode doit être appelée chaque fois qu’un appareil est perdu, ou avant de réinitialiser un appareil.</span><span class="sxs-lookup"><span data-stu-id="8fd5b-131">This method should be called whenever a device is lost, or before resetting a device.</span></span><br/> |
| [<span data-ttu-id="8fd5b-132">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="8fd5b-132">**OnResetDevice**</span></span>](id3dxrendertoenvmap--onresetdevice.md)     | <span data-ttu-id="8fd5b-133">Utilisez cette méthode pour acquérir à nouveau des ressources et enregistrer l’état initial.</span><span class="sxs-lookup"><span data-stu-id="8fd5b-133">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="8fd5b-134">Notes</span><span class="sxs-lookup"><span data-stu-id="8fd5b-134">Remarks</span></span>

<span data-ttu-id="8fd5b-135">Une carte d’environnement est utilisée pour la géométrie de la scène de texture pour fournir une scène plus sophistiquée sans utiliser de géométrie complexe.</span><span class="sxs-lookup"><span data-stu-id="8fd5b-135">An environment map is used to texture-map scene geometry to provide a more sophisticated scene without using complex geometry.</span></span> <span data-ttu-id="8fd5b-136">Cette interface prend en charge la création de surfaces pour les genres suivants de géométrie : cube, demi-sphère ou hémisphérique, parabolique ou sphère.</span><span class="sxs-lookup"><span data-stu-id="8fd5b-136">This interface supports creating surfaces for the following kinds of geometry: cube, half sphere or hemispheric, parabolic, or sphere.</span></span>

<span data-ttu-id="8fd5b-137">L’interface **ID3DXRenderToEnvMap** est obtenue en appelant la fonction [**D3DXCreateRenderToEnvMap**](d3dxcreaterendertoenvmap.md) .</span><span class="sxs-lookup"><span data-stu-id="8fd5b-137">The **ID3DXRenderToEnvMap** interface is obtained by calling the [**D3DXCreateRenderToEnvMap**](d3dxcreaterendertoenvmap.md) function.</span></span>

<span data-ttu-id="8fd5b-138">Le type LPD3DXRenderToEnvMap est défini comme un pointeur vers l’interface **ID3DXRenderToEnvMap** .</span><span class="sxs-lookup"><span data-stu-id="8fd5b-138">The LPD3DXRenderToEnvMap type is defined as a pointer to the **ID3DXRenderToEnvMap** interface.</span></span>


```
typedef interface ID3DXRenderToEnvMap ID3DXRenderToEnvMap;
typedef interface ID3DXRenderToEnvMap *LPD3DXRenderToEnvMap;
```



## <a name="requirements"></a><span data-ttu-id="8fd5b-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8fd5b-139">Requirements</span></span>



| <span data-ttu-id="8fd5b-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8fd5b-140">Requirement</span></span> | <span data-ttu-id="8fd5b-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fd5b-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fd5b-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="8fd5b-142">Header</span></span><br/>  | <dl> <span data-ttu-id="8fd5b-143"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fd5b-143"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="8fd5b-144">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8fd5b-144">Library</span></span><br/> | <dl> <span data-ttu-id="8fd5b-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8fd5b-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8fd5b-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fd5b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fd5b-147">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="8fd5b-147">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
