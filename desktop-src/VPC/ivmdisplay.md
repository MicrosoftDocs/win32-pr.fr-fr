---
title: Interface IVMDisplay (VPCCOMInterfaces. h)
description: Contrôle les paramètres d’affichage d’un ordinateur virtuel. L’interface IVMDisplay pour un ordinateur virtuel peut être récupérée à l’aide de la propriété d’affichage IVMVirtualMachine.
ms.assetid: b2eafd86-459c-4807-aa77-8b9125bce53e
keywords:
- Virtual PC de l’interface IVMDisplay
- IVMDisplay interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMDisplay
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0f410e49682d2fa9f5f8511d96e3b9ce9a1094
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942507"
---
# <a name="ivmdisplay-interface"></a><span data-ttu-id="c3397-106">Interface IVMDisplay</span><span class="sxs-lookup"><span data-stu-id="c3397-106">IVMDisplay interface</span></span>

<span data-ttu-id="c3397-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c3397-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c3397-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c3397-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c3397-109">Contrôle les paramètres d’affichage d’un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="c3397-109">Controls the display settings of a virtual machine.</span></span> <span data-ttu-id="c3397-110">L’interface **IVMDisplay** pour un ordinateur virtuel peut être récupérée à l’aide de la propriété [**IVMVirtualMachine ::D**](ivmvirtualmachine-display.md) .</span><span class="sxs-lookup"><span data-stu-id="c3397-110">The **IVMDisplay** interface for a virtual machine can be retrieved using the [**IVMVirtualMachine::Display**](ivmvirtualmachine-display.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="c3397-111">Membres</span><span class="sxs-lookup"><span data-stu-id="c3397-111">Members</span></span>

<span data-ttu-id="c3397-112">L’interface **IVMDisplay** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="c3397-112">The **IVMDisplay** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="c3397-113">**IVMDisplay** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c3397-113">**IVMDisplay** also has these types of members:</span></span>

-   [<span data-ttu-id="c3397-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c3397-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="c3397-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c3397-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c3397-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c3397-116">Methods</span></span>

<span data-ttu-id="c3397-117">L’interface **IVMDisplay** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="c3397-117">The **IVMDisplay** interface has these methods.</span></span>



| <span data-ttu-id="c3397-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="c3397-118">Method</span></span>                                                       | <span data-ttu-id="c3397-119">Description</span><span class="sxs-lookup"><span data-stu-id="c3397-119">Description</span></span>                                                                                             |
|:-------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c3397-120">**\_GenerateThumbnail**</span><span class="sxs-lookup"><span data-stu-id="c3397-120">**\_GenerateThumbnail**</span></span>](ivmdisplay--generatethumbnail.md) | <span data-ttu-id="c3397-121">Récupère un tableau de pixels représentant une image miniature de l’écran de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="c3397-121">Retrieves an array of pixels representing a thumbnail image of the virtual machine's screen.</span></span><br/> |
| [<span data-ttu-id="c3397-122">**SetDimensions**</span><span class="sxs-lookup"><span data-stu-id="c3397-122">**SetDimensions**</span></span>](ivmdisplay-setdimensions.md)            | <span data-ttu-id="c3397-123">Définit, en pixels, la hauteur et la largeur de l’affichage de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="c3397-123">Sets the height and width of the virtual machine's display, in pixels.</span></span><br/>                       |



 

### <a name="properties"></a><span data-ttu-id="c3397-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c3397-124">Properties</span></span>

<span data-ttu-id="c3397-125">L’interface **IVMDisplay** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c3397-125">The **IVMDisplay** interface has these properties.</span></span>



| <span data-ttu-id="c3397-126">Propriété</span><span class="sxs-lookup"><span data-stu-id="c3397-126">Property</span></span>                                             | <span data-ttu-id="c3397-127">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="c3397-127">Access type</span></span>          | <span data-ttu-id="c3397-128">Description</span><span class="sxs-lookup"><span data-stu-id="c3397-128">Description</span></span>                                                                                   |
|:-----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c3397-129">**CanResize**</span><span class="sxs-lookup"><span data-stu-id="c3397-129">**CanResize**</span></span>](ivmdisplay-canresize.md)<br/> | <span data-ttu-id="c3397-130">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3397-130">Read-only</span></span><br/> | <span data-ttu-id="c3397-131">Indique si l’invité autorise les modifications de résolution.</span><span class="sxs-lookup"><span data-stu-id="c3397-131">Indicates whether the Guest allows resolution changes.</span></span><br/>                             |
| [<span data-ttu-id="c3397-132">**Height**</span><span class="sxs-lookup"><span data-stu-id="c3397-132">**Height**</span></span>](ivmdisplay-height.md)<br/>       | <span data-ttu-id="c3397-133">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3397-133">Read-only</span></span><br/> | <span data-ttu-id="c3397-134">Hauteur de l’affichage de l’ordinateur virtuel, en pixels.</span><span class="sxs-lookup"><span data-stu-id="c3397-134">The height of the virtual machine's display, in pixels.</span></span><br/>                            |
| [<span data-ttu-id="c3397-135">**Thumbnail**</span><span class="sxs-lookup"><span data-stu-id="c3397-135">**Thumbnail**</span></span>](ivmdisplay-thumbnail.md)<br/> | <span data-ttu-id="c3397-136">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3397-136">Read-only</span></span><br/> | <span data-ttu-id="c3397-137">Tableau de pixels représentant une image miniature de l’écran de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="c3397-137">An array of pixels representing a thumbnail image of the virtual machine's screen.</span></span><br/> |
| [<span data-ttu-id="c3397-138">**VideoMode**</span><span class="sxs-lookup"><span data-stu-id="c3397-138">**VideoMode**</span></span>](ivmdisplay-videomode.md)<br/> | <span data-ttu-id="c3397-139">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3397-139">Read-only</span></span><br/> | <span data-ttu-id="c3397-140">Mode vidéo actuel (texte, VGA, SVGA, etc.).</span><span class="sxs-lookup"><span data-stu-id="c3397-140">The current video mode (Text, VGA, SVGA, and so on).</span></span><br/>                               |
| [<span data-ttu-id="c3397-141">**Width**</span><span class="sxs-lookup"><span data-stu-id="c3397-141">**Width**</span></span>](ivmdisplay-width.md)<br/>         | <span data-ttu-id="c3397-142">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3397-142">Read-only</span></span><br/> | <span data-ttu-id="c3397-143">Largeur de l’affichage de l’ordinateur virtuel, en pixels.</span><span class="sxs-lookup"><span data-stu-id="c3397-143">The width of the virtual machine's display, in pixels.</span></span><br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="c3397-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3397-144">Requirements</span></span>



| <span data-ttu-id="c3397-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3397-145">Requirement</span></span> | <span data-ttu-id="c3397-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3397-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3397-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3397-147">Minimum supported client</span></span><br/> | <span data-ttu-id="c3397-148">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3397-148">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c3397-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3397-149">Minimum supported server</span></span><br/> | <span data-ttu-id="c3397-150">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3397-150">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c3397-151">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="c3397-151">End of client support</span></span><br/>    | <span data-ttu-id="c3397-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c3397-152">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c3397-153">Produit</span><span class="sxs-lookup"><span data-stu-id="c3397-153">Product</span></span><br/>                  | <span data-ttu-id="c3397-154">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c3397-154">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c3397-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3397-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3397-156"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3397-156"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c3397-157">IID</span><span class="sxs-lookup"><span data-stu-id="c3397-157">IID</span></span><br/>                      | <span data-ttu-id="c3397-158">IID \_ IVMDisplay est défini en tant que 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="c3397-158">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



 

