---
description: L’interface IDxtJpeg définit les propriétés de la transition de réinitialisation SMPTE. Cette interface est utilisée en interne par les services de modification DirectShow (DES) lors du rendu de la transition de réinitialisation SMPTE.
ms.assetid: ce1920d4-ebe5-42d1-a2eb-d71ddeaf14fe
title: Interface IDxtJpeg (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e9c32bee3f4041abaa9529036b7bc78250ac2487
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523973"
---
# <a name="idxtjpeg-interface"></a><span data-ttu-id="9e170-103">Interface IDxtJpeg</span><span class="sxs-lookup"><span data-stu-id="9e170-103">IDxtJpeg interface</span></span>

> [!Note]  
> <span data-ttu-id="9e170-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="9e170-104">\[Deprecated.</span></span> <span data-ttu-id="9e170-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9e170-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9e170-106">L' `IDxtJpeg` interface définit les propriétés de la transition de [réinitialisation SMPTE](smpte-wipe-transition.md) .</span><span class="sxs-lookup"><span data-stu-id="9e170-106">The `IDxtJpeg` interface sets properties on the [SMPTE Wipe](smpte-wipe-transition.md) transition.</span></span>

<span data-ttu-id="9e170-107">Cette interface est utilisée en interne par les services de modification DirectShow (DES) lors du rendu de la transition de réinitialisation SMPTE.</span><span class="sxs-lookup"><span data-stu-id="9e170-107">This interface is used internally by DirectShow Editing Services (DES) when it renders the SMPTE Wipe transition.</span></span> <span data-ttu-id="9e170-108">Les applications DES n’ont pas besoin d’utiliser cette interface.</span><span class="sxs-lookup"><span data-stu-id="9e170-108">DES applications do not need to use this interface.</span></span> <span data-ttu-id="9e170-109">Pour définir les propriétés d’une transition dans DES, utilisez l’interface [**IPropertySetter**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="9e170-109">To set the properties on a transition in DES, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="9e170-110">Membres</span><span class="sxs-lookup"><span data-stu-id="9e170-110">Members</span></span>

<span data-ttu-id="9e170-111">L’interface **IDxtJpeg** hérite de **IDXEffect**.</span><span class="sxs-lookup"><span data-stu-id="9e170-111">The **IDxtJpeg** interface inherits from **IDXEffect**.</span></span> <span data-ttu-id="9e170-112">**IDxtJpeg** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9e170-112">**IDxtJpeg** also has these types of members:</span></span>

-   [<span data-ttu-id="9e170-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9e170-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9e170-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9e170-114">Methods</span></span>

<span data-ttu-id="9e170-115">L’interface **IDxtJpeg** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="9e170-115">The **IDxtJpeg** interface has these methods.</span></span>



| <span data-ttu-id="9e170-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="9e170-116">Method</span></span>                                                     | <span data-ttu-id="9e170-117">Description</span><span class="sxs-lookup"><span data-stu-id="9e170-117">Description</span></span>                                                                               |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9e170-118">**ApplyChanges**</span><span class="sxs-lookup"><span data-stu-id="9e170-118">**ApplyChanges**</span></span>](idxtjpeg-applychanges.md)              | <span data-ttu-id="9e170-119">Applique toutes les propriétés qui ont été modifiées.</span><span class="sxs-lookup"><span data-stu-id="9e170-119">Applies any properties that have changed.</span></span><br/>                                      |
| [<span data-ttu-id="9e170-120">**Obtient la \_ CouleurBordure**</span><span class="sxs-lookup"><span data-stu-id="9e170-120">**get\_BorderColor**</span></span>](idxtjpeg-get-bordercolor.md)       | <span data-ttu-id="9e170-121">Récupère la couleur de la bordure autour des bords du motif de réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="9e170-121">Retrieves the color of the border around the edges of the wipe pattern.</span></span><br/>        |
| [<span data-ttu-id="9e170-122">**Obtient \_ BorderSoftness**</span><span class="sxs-lookup"><span data-stu-id="9e170-122">**get\_BorderSoftness**</span></span>](idxtjpeg-get-bordersoftness.md) | <span data-ttu-id="9e170-123">Récupère la largeur de la zone floue autour des bords du motif de réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="9e170-123">Retrieves the width of the blurry region around the edges of the wipe pattern.</span></span><br/> |
| [<span data-ttu-id="9e170-124">**accéder à \_ BorderWidth**</span><span class="sxs-lookup"><span data-stu-id="9e170-124">**get\_BorderWidth**</span></span>](idxtjpeg-get-borderwidth.md)       | <span data-ttu-id="9e170-125">Récupère la largeur de la bordure unie le long des bords du motif de réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="9e170-125">Retrieves the width of the solid border along the edges of the wipe pattern.</span></span><br/>   |
| [<span data-ttu-id="9e170-126">**Obtient \_ MaskName**</span><span class="sxs-lookup"><span data-stu-id="9e170-126">**get\_MaskName**</span></span>](idxtjpeg-get-maskname.md)             | <span data-ttu-id="9e170-127">Récupère le nom d’un fichier JPEG à utiliser comme masque de réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="9e170-127">Retrieves the name of a JPEG file to be used as the wipe mask.</span></span><br/>                 |
| [<span data-ttu-id="9e170-128">**Obtient \_ MaskNum**</span><span class="sxs-lookup"><span data-stu-id="9e170-128">**get\_MaskNum**</span></span>](idxtjpeg-get-masknum.md)               | <span data-ttu-id="9e170-129">Récupère le code de réinitialisation SMPTE de la réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="9e170-129">Retrieves the SMPTE wipe code of the wipe.</span></span><br/>                                     |
| [<span data-ttu-id="9e170-130">**Obtient les \_ offsets**</span><span class="sxs-lookup"><span data-stu-id="9e170-130">**get\_OffsetX**</span></span>](idxtjpeg-get-offsetx.md)               | <span data-ttu-id="9e170-131">Récupère le décalage horizontal de l’origine de la réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="9e170-131">Retrieves the horizontal offset of the wipe origin.</span></span><br/>                            |
| [<span data-ttu-id="9e170-132">**recevoir un \_ décalage**</span><span class="sxs-lookup"><span data-stu-id="9e170-132">**get\_OffsetY**</span></span>](idxtjpeg-get-offsety.md)               | <span data-ttu-id="9e170-133">Récupère le décalage vertical de l’origine de la réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="9e170-133">Retrieves the vertical offset of the wipe origin.</span></span><br/>                              |
| [<span data-ttu-id="9e170-134">**Obtient \_ ReplicateX**</span><span class="sxs-lookup"><span data-stu-id="9e170-134">**get\_ReplicateX**</span></span>](idxtjpeg-get-replicatex.md)         | <span data-ttu-id="9e170-135">Récupère le nombre de fois que le modèle de réinitialisation est répliqué horizontalement.</span><span class="sxs-lookup"><span data-stu-id="9e170-135">Retrieves the number of times the wipe pattern is replicated horizontally.</span></span><br/>     |
| [<span data-ttu-id="9e170-136">**être \_ répliqué**</span><span class="sxs-lookup"><span data-stu-id="9e170-136">**get\_ReplicateY**</span></span>](idxtjpeg-get-replicatey.md)         | <span data-ttu-id="9e170-137">Récupère le nombre de fois où le modèle de réinitialisation est répliqué verticalement.</span><span class="sxs-lookup"><span data-stu-id="9e170-137">Retrieves the number of times the wipe pattern is replicated vertically.</span></span><br/>       |
| [<span data-ttu-id="9e170-138">**récupération \_ ScaleX**</span><span class="sxs-lookup"><span data-stu-id="9e170-138">**get\_ScaleX**</span></span>](idxtjpeg-get-scalex.md)                 | <span data-ttu-id="9e170-139">Récupère la quantité d’étirement horizontal de la réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="9e170-139">Retrieves the amount by which the wipe is stretched horizontally.</span></span><br/>              |
| [<span data-ttu-id="9e170-140">**faire \_ évoluer**</span><span class="sxs-lookup"><span data-stu-id="9e170-140">**get\_ScaleY**</span></span>](idxtjpeg-get-scaley.md)                 | <span data-ttu-id="9e170-141">Récupère la valeur de l’étirement vertical de la réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="9e170-141">Retrieves the amount by which the wipe is stretched vertically.</span></span><br/>                |
| [<span data-ttu-id="9e170-142">**LoadDefSettings**</span><span class="sxs-lookup"><span data-stu-id="9e170-142">**LoadDefSettings**</span></span>](idxtjpeg-loaddefsettings.md)        | <span data-ttu-id="9e170-143">Restaure les paramètres par défaut de la transition de réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="9e170-143">Restores the default settings of the Wipe transition.</span></span><br/>                          |
| [<span data-ttu-id="9e170-144">**Placer la \_ CouleurBordure**</span><span class="sxs-lookup"><span data-stu-id="9e170-144">**put\_BorderColor**</span></span>](idxtjpeg-put-bordercolor.md)       | <span data-ttu-id="9e170-145">Spécifie la couleur de la bordure autour des bords du motif de la réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="9e170-145">Specifies the color of the border around the edges of the wipe pattern.</span></span><br/>        |
| [<span data-ttu-id="9e170-146">**put \_ BorderSoftness**</span><span class="sxs-lookup"><span data-stu-id="9e170-146">**put\_BorderSoftness**</span></span>](idxtjpeg-put-bordersoftness.md) | <span data-ttu-id="9e170-147">Spécifie la largeur de la zone floue autour des bords du motif de réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="9e170-147">Specifies the width of the blurry region around the edges of the wipe pattern.</span></span><br/> |
| [<span data-ttu-id="9e170-148">**placer \_ BorderWidth**</span><span class="sxs-lookup"><span data-stu-id="9e170-148">**put\_BorderWidth**</span></span>](idxtjpeg-put-borderwidth.md)       | <span data-ttu-id="9e170-149">Spécifie la largeur de la bordure unie le long des bords du motif de réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="9e170-149">Specifies the width of the solid border along the edges of the wipe pattern.</span></span><br/>   |
| [<span data-ttu-id="9e170-150">**put \_ MaskName**</span><span class="sxs-lookup"><span data-stu-id="9e170-150">**put\_MaskName**</span></span>](idxtjpeg-put-maskname.md)             | <span data-ttu-id="9e170-151">Spécifie le nom d’un fichier JPEG à utiliser comme masque de réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="9e170-151">Specifies the name of a JPEG file to use as the wipe mask.</span></span><br/>                     |
| [<span data-ttu-id="9e170-152">**put \_ MaskNum**</span><span class="sxs-lookup"><span data-stu-id="9e170-152">**put\_MaskNum**</span></span>](idxtjpeg-put-masknum.md)               | <span data-ttu-id="9e170-153">Spécifie le code de réinitialisation SMPTE de la réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="9e170-153">Specifies the SMPTE wipe code of the wipe.</span></span><br/>                                     |
| [<span data-ttu-id="9e170-154">**put \_ OffsetX**</span><span class="sxs-lookup"><span data-stu-id="9e170-154">**put\_OffsetX**</span></span>](idxtjpeg-put-offsetx.md)               | <span data-ttu-id="9e170-155">Spécifie le décalage horizontal de l’origine de la réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="9e170-155">Specifies the horizontal offset of the wipe origin.</span></span><br/>                            |
| [<span data-ttu-id="9e170-156">**placer un \_ décalage**</span><span class="sxs-lookup"><span data-stu-id="9e170-156">**put\_OffsetY**</span></span>](idxtjpeg-put-offsety.md)               | <span data-ttu-id="9e170-157">Spécifie le décalage vertical de l’origine de la réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="9e170-157">Specifies the vertical offset of the wipe origin.</span></span><br/>                              |
| [<span data-ttu-id="9e170-158">**put \_ ReplicateX**</span><span class="sxs-lookup"><span data-stu-id="9e170-158">**put\_ReplicateX**</span></span>](idxtjpeg-put-replicatex.md)         | <span data-ttu-id="9e170-159">Spécifie le nombre de fois que le modèle de réinitialisation est répliqué horizontalement.</span><span class="sxs-lookup"><span data-stu-id="9e170-159">Specifies the number of times the wipe pattern is replicated horizontally.</span></span><br/>     |
| [<span data-ttu-id="9e170-160">**mise en \_ réplique**</span><span class="sxs-lookup"><span data-stu-id="9e170-160">**put\_ReplicateY**</span></span>](idxtjpeg-put-replicatey.md)         | <span data-ttu-id="9e170-161">Spécifie le nombre de fois que le modèle de réinitialisation est répliqué verticalement.</span><span class="sxs-lookup"><span data-stu-id="9e170-161">Specifies the number of times the wipe pattern is replicated vertically.</span></span><br/>       |
| [<span data-ttu-id="9e170-162">**placer \_ ScaleX**</span><span class="sxs-lookup"><span data-stu-id="9e170-162">**put\_ScaleX**</span></span>](idxtjpeg-put-scalex.md)                 | <span data-ttu-id="9e170-163">Spécifie la quantité d’étirement horizontal de la réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="9e170-163">Specifies the amount by which the wipe is stretched horizontally.</span></span><br/>              |
| [<span data-ttu-id="9e170-164">**mettre à l' \_ échelle**</span><span class="sxs-lookup"><span data-stu-id="9e170-164">**put\_ScaleY**</span></span>](idxtjpeg-put-scaley.md)                 | <span data-ttu-id="9e170-165">Spécifie la quantité d’étirement vertical de la réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="9e170-165">Specifies the amount by which the wipe is stretched vertically.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="9e170-166">Notes</span><span class="sxs-lookup"><span data-stu-id="9e170-166">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9e170-167">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="9e170-167">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9e170-168">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9e170-168">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9e170-169">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9e170-169">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9e170-170">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e170-170">Requirements</span></span>



| <span data-ttu-id="9e170-171">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e170-171">Requirement</span></span> | <span data-ttu-id="9e170-172">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e170-172">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e170-173">En-tête</span><span class="sxs-lookup"><span data-stu-id="9e170-173">Header</span></span><br/>  | <dl> <span data-ttu-id="9e170-174"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e170-174"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9e170-175">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9e170-175">Library</span></span><br/> | <dl> <span data-ttu-id="9e170-176"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e170-176"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 




