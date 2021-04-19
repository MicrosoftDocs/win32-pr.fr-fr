---
description: L’interface IDxtCompositor définit les propriétés de la transition du compositeur. Cette interface est utilisée en interne par les services de modification DirectShow (DES) lors du rendu de la transition de compositeur.
ms.assetid: 519f1e00-4b67-4014-906b-043f2478baa7
title: Interface IDxtCompositor (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c2e19f555fe01cbec3763bc1dc76d11aeb5f5ecb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521688"
---
# <a name="idxtcompositor-interface"></a><span data-ttu-id="a2da8-103">Interface IDxtCompositor</span><span class="sxs-lookup"><span data-stu-id="a2da8-103">IDxtCompositor interface</span></span>

> [!Note]  
> <span data-ttu-id="a2da8-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="a2da8-104">\[Deprecated.</span></span> <span data-ttu-id="a2da8-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a2da8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a2da8-106">L' `IDxtCompositor` interface définit les propriétés de la transition du [compositeur](compositor-transition.md) .</span><span class="sxs-lookup"><span data-stu-id="a2da8-106">The `IDxtCompositor` interface sets properties on the [Compositor](compositor-transition.md) transition.</span></span>

<span data-ttu-id="a2da8-107">Cette interface est utilisée en interne par les services de modification DirectShow (DES) lors du rendu de la transition de compositeur.</span><span class="sxs-lookup"><span data-stu-id="a2da8-107">This interface is used internally by DirectShow Editing Services (DES) when it renders the Compositor transition.</span></span> <span data-ttu-id="a2da8-108">Les applications DES n’ont pas besoin d’utiliser cette interface.</span><span class="sxs-lookup"><span data-stu-id="a2da8-108">DES applications do not have to use this interface.</span></span> <span data-ttu-id="a2da8-109">Pour définir les propriétés d’une transition dans DES, utilisez l’interface [**IPropertySetter**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="a2da8-109">To set the properties on a transition in DES, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

<span data-ttu-id="a2da8-110">La transition de compositeur composite une image de premier plan sur une image d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="a2da8-110">The Compositor transition composites a foreground image onto a background image.</span></span> <span data-ttu-id="a2da8-111">Le *rectangle source* définit la section de l’image de premier plan qui est composite.</span><span class="sxs-lookup"><span data-stu-id="a2da8-111">The *source rectangle* defines the section of the foreground image that is composited.</span></span> <span data-ttu-id="a2da8-112">Le *rectangle de destination* définit la section de l’image d’arrière-plan qui reçoit l’image de premier plan.</span><span class="sxs-lookup"><span data-stu-id="a2da8-112">The *destination rectangle* defines the section of the background image that receives the foreground image.</span></span> <span data-ttu-id="a2da8-113">Le diagramme suivant illustre ces rectangles.</span><span class="sxs-lookup"><span data-stu-id="a2da8-113">The following diagram illustrates these rectangles.</span></span>

![Propriétés de transition du compositeur](images/compmeasure.png)

## <a name="members"></a><span data-ttu-id="a2da8-115">Membres</span><span class="sxs-lookup"><span data-stu-id="a2da8-115">Members</span></span>

<span data-ttu-id="a2da8-116">L’interface **IDxtCompositor** hérite de **IDXEffect**.</span><span class="sxs-lookup"><span data-stu-id="a2da8-116">The **IDxtCompositor** interface inherits from **IDXEffect**.</span></span> <span data-ttu-id="a2da8-117">**IDxtCompositor** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a2da8-117">**IDxtCompositor** also has these types of members:</span></span>

-   [<span data-ttu-id="a2da8-118">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a2da8-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a2da8-119">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a2da8-119">Methods</span></span>

<span data-ttu-id="a2da8-120">L’interface **IDxtCompositor** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="a2da8-120">The **IDxtCompositor** interface has these methods.</span></span>



| <span data-ttu-id="a2da8-121">Méthode</span><span class="sxs-lookup"><span data-stu-id="a2da8-121">Method</span></span>                                                   | <span data-ttu-id="a2da8-122">Description</span><span class="sxs-lookup"><span data-stu-id="a2da8-122">Description</span></span>                                                         |
|:---------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="a2da8-123">**afficher la \_ hauteur**</span><span class="sxs-lookup"><span data-stu-id="a2da8-123">**get\_Height**</span></span>](idxtcompositor-get-height.md)         | <span data-ttu-id="a2da8-124">Récupère la hauteur du rectangle cible.</span><span class="sxs-lookup"><span data-stu-id="a2da8-124">Retrieves the height of the target rectangle.</span></span><br/>            |
| [<span data-ttu-id="a2da8-125">**Obtient les \_ offsets**</span><span class="sxs-lookup"><span data-stu-id="a2da8-125">**get\_OffsetX**</span></span>](idxtcompositor-get-offsetx.md)       | <span data-ttu-id="a2da8-126">Récupère le décalage horizontal du rectangle cible.</span><span class="sxs-lookup"><span data-stu-id="a2da8-126">Retrieves the horizontal offset of the target rectangle.</span></span><br/> |
| [<span data-ttu-id="a2da8-127">**recevoir un \_ décalage**</span><span class="sxs-lookup"><span data-stu-id="a2da8-127">**get\_OffsetY**</span></span>](idxtcompositor-get-offsety.md)       | <span data-ttu-id="a2da8-128">Récupère le décalage vertical du rectangle cible.</span><span class="sxs-lookup"><span data-stu-id="a2da8-128">Retrieves the vertical offset of the target rectangle.</span></span><br/>   |
| [<span data-ttu-id="a2da8-129">**Obtient \_ SrcHeight**</span><span class="sxs-lookup"><span data-stu-id="a2da8-129">**get\_SrcHeight**</span></span>](idxtcompositor-get-srcheight.md)   | <span data-ttu-id="a2da8-130">Récupère la hauteur du rectangle source.</span><span class="sxs-lookup"><span data-stu-id="a2da8-130">Retrieves the height of the source rectangle.</span></span><br/>            |
| [<span data-ttu-id="a2da8-131">**Obtient \_ SrcOffsetX**</span><span class="sxs-lookup"><span data-stu-id="a2da8-131">**get\_SrcOffsetX**</span></span>](idxtcompositor-get-srcoffsetx.md) | <span data-ttu-id="a2da8-132">Récupère le décalage horizontal du rectangle source.</span><span class="sxs-lookup"><span data-stu-id="a2da8-132">Retrieves the horizontal offset of the source rectangle.</span></span><br/> |
| [<span data-ttu-id="a2da8-133">**Obtient \_ SrcOffsetY**</span><span class="sxs-lookup"><span data-stu-id="a2da8-133">**get\_SrcOffsetY**</span></span>](idxtcompositor-get-srcoffsety.md) | <span data-ttu-id="a2da8-134">Récupère le décalage vertical du rectangle source.</span><span class="sxs-lookup"><span data-stu-id="a2da8-134">Retrieves the vertical offset of the source rectangle.</span></span><br/>   |
| [<span data-ttu-id="a2da8-135">**Obtient \_ SrcWidth**</span><span class="sxs-lookup"><span data-stu-id="a2da8-135">**get\_SrcWidth**</span></span>](idxtcompositor-get-srcwidth.md)     | <span data-ttu-id="a2da8-136">Récupère la largeur du rectangle source.</span><span class="sxs-lookup"><span data-stu-id="a2da8-136">Retrieves the width of the source rectangle.</span></span><br/>             |
| [<span data-ttu-id="a2da8-137">**afficher la \_ largeur**</span><span class="sxs-lookup"><span data-stu-id="a2da8-137">**get\_Width**</span></span>](idxtcompositor-get-width.md)           | <span data-ttu-id="a2da8-138">Récupère la largeur du rectangle cible.</span><span class="sxs-lookup"><span data-stu-id="a2da8-138">Retrieves the width of the target rectangle.</span></span><br/>             |
| [<span data-ttu-id="a2da8-139">**Placer la \_ hauteur**</span><span class="sxs-lookup"><span data-stu-id="a2da8-139">**put\_Height**</span></span>](idxtcompositor-put-height.md)         | <span data-ttu-id="a2da8-140">Spécifie la hauteur du rectangle cible.</span><span class="sxs-lookup"><span data-stu-id="a2da8-140">Specifies the height of the target rectangle.</span></span><br/>            |
| [<span data-ttu-id="a2da8-141">**put \_ OffsetX**</span><span class="sxs-lookup"><span data-stu-id="a2da8-141">**put\_OffsetX**</span></span>](idxtcompositor-put-offsetx.md)       | <span data-ttu-id="a2da8-142">Spécifie le décalage horizontal du rectangle cible.</span><span class="sxs-lookup"><span data-stu-id="a2da8-142">Specifies the horizontal offset of the target rectangle.</span></span><br/> |
| [<span data-ttu-id="a2da8-143">**placer un \_ décalage**</span><span class="sxs-lookup"><span data-stu-id="a2da8-143">**put\_OffsetY**</span></span>](idxtcompositor-put-offsety.md)       | <span data-ttu-id="a2da8-144">Spécifie le décalage vertical du rectangle cible.</span><span class="sxs-lookup"><span data-stu-id="a2da8-144">Specifies the vertical offset of the target rectangle.</span></span><br/>   |
| [<span data-ttu-id="a2da8-145">**put \_ SrcHeight**</span><span class="sxs-lookup"><span data-stu-id="a2da8-145">**put\_SrcHeight**</span></span>](idxtcompositor-put-srcheight.md)   | <span data-ttu-id="a2da8-146">Spécifie la hauteur du rectangle source.</span><span class="sxs-lookup"><span data-stu-id="a2da8-146">Specifies the height of the source rectangle.</span></span><br/>            |
| [<span data-ttu-id="a2da8-147">**put \_ SrcOffsetX**</span><span class="sxs-lookup"><span data-stu-id="a2da8-147">**put\_SrcOffsetX**</span></span>](idxtcompositor-put-srcoffsetx.md) | <span data-ttu-id="a2da8-148">Spécifie le décalage horizontal du rectangle source.</span><span class="sxs-lookup"><span data-stu-id="a2da8-148">Specifies the horizontal offset of the source rectangle.</span></span><br/> |
| [<span data-ttu-id="a2da8-149">**put \_ SrcOffsetY**</span><span class="sxs-lookup"><span data-stu-id="a2da8-149">**put\_SrcOffsetY**</span></span>](idxtcompositor-put-srcoffsety.md) | <span data-ttu-id="a2da8-150">Spécifie le décalage vertical du rectangle source.</span><span class="sxs-lookup"><span data-stu-id="a2da8-150">Specifies the vertical offset of the source rectangle.</span></span><br/>   |
| [<span data-ttu-id="a2da8-151">**put \_ SrcWidth**</span><span class="sxs-lookup"><span data-stu-id="a2da8-151">**put\_SrcWidth**</span></span>](idxtcompositor-put-srcwidth.md)     | <span data-ttu-id="a2da8-152">Spécifie la largeur du rectangle source.</span><span class="sxs-lookup"><span data-stu-id="a2da8-152">Specifies the width of the source rectangle.</span></span><br/>             |
| [<span data-ttu-id="a2da8-153">**mettre la \_ largeur**</span><span class="sxs-lookup"><span data-stu-id="a2da8-153">**put\_Width**</span></span>](idxtcompositor-put-width.md)           | <span data-ttu-id="a2da8-154">Spécifie la largeur du rectangle cible.</span><span class="sxs-lookup"><span data-stu-id="a2da8-154">Specifies the width of the target rectangle.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="a2da8-155">Notes</span><span class="sxs-lookup"><span data-stu-id="a2da8-155">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a2da8-156">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="a2da8-156">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a2da8-157">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a2da8-157">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a2da8-158">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a2da8-158">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a2da8-159">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2da8-159">Requirements</span></span>



| <span data-ttu-id="a2da8-160">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2da8-160">Requirement</span></span> | <span data-ttu-id="a2da8-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2da8-161">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2da8-162">En-tête</span><span class="sxs-lookup"><span data-stu-id="a2da8-162">Header</span></span><br/>  | <dl> <span data-ttu-id="a2da8-163"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2da8-163"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a2da8-164">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a2da8-164">Library</span></span><br/> | <dl> <span data-ttu-id="a2da8-165"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2da8-165"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 




