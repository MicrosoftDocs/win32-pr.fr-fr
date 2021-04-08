---
title: Interface IVMMouse (VPCCOMInterfaces. h)
description: Contrôle le périphérique de la souris au sein d’une machine virtuelle.
ms.assetid: 13bbf980-aafd-4c63-b1cb-60f00b738d1f
keywords:
- Virtual PC de l’interface IVMMouse
- IVMMouse interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMMouse
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7041b8a28b924ffedc8ff23edd2b04afdaa78be2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844149"
---
# <a name="ivmmouse-interface"></a><span data-ttu-id="d6e5f-105">Interface IVMMouse</span><span class="sxs-lookup"><span data-stu-id="d6e5f-105">IVMMouse interface</span></span>

<span data-ttu-id="d6e5f-106">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d6e5f-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d6e5f-107">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d6e5f-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d6e5f-108">Contrôle l’appareil de la souris au sein d’une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="d6e5f-108">Controls the mouse device within a virtual machine (VM).</span></span> <span data-ttu-id="d6e5f-109">La **IVMMouse** d’un ordinateur virtuel peut être récupérée à l’aide de la propriété [**IVMVirtualMachine :: Mouse**](ivmvirtualmachine-mouse.md) .</span><span class="sxs-lookup"><span data-stu-id="d6e5f-109">The **IVMMouse** for a virtual machine can be retrieved using the [**IVMVirtualMachine::Mouse**](ivmvirtualmachine-mouse.md) property.</span></span> <span data-ttu-id="d6e5f-110">Les coordonnées du périphérique de la souris peuvent être représentées soit en coordonnées absolues, soit en coordonnées Delta.</span><span class="sxs-lookup"><span data-stu-id="d6e5f-110">Coordinates for the mouse device can be represented either in absolute coordinates or in delta coordinates.</span></span> <span data-ttu-id="d6e5f-111">Utilisez la propriété [**UsingAbsoluteCoordinates**](ivmmouse-usingabsolutecoordinates.md) pour faire la distinction entre les deux méthodes de représentation de coordonnées.</span><span class="sxs-lookup"><span data-stu-id="d6e5f-111">Use the [**UsingAbsoluteCoordinates**](ivmmouse-usingabsolutecoordinates.md) property to distinguish between the two methods of coordinate representation.</span></span> <span data-ttu-id="d6e5f-112">Notez que la récupération de la position actuelle du curseur et l’utilisation de coordonnées absolues sont prises en charge uniquement si les composants d’intégration sont installés sur le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="d6e5f-112">Note that retrieving the current cursor position and the use of absolute coordinates are only supported if the guest operating system has the integration components installed.</span></span>

## <a name="members"></a><span data-ttu-id="d6e5f-113">Membres</span><span class="sxs-lookup"><span data-stu-id="d6e5f-113">Members</span></span>

<span data-ttu-id="d6e5f-114">L’interface **IVMMouse** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="d6e5f-114">The **IVMMouse** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="d6e5f-115">**IVMMouse** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d6e5f-115">**IVMMouse** also has these types of members:</span></span>

-   [<span data-ttu-id="d6e5f-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d6e5f-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="d6e5f-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d6e5f-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d6e5f-118">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d6e5f-118">Methods</span></span>

<span data-ttu-id="d6e5f-119">L’interface **IVMMouse** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d6e5f-119">The **IVMMouse** interface has these methods.</span></span>



| <span data-ttu-id="d6e5f-120">Méthode</span><span class="sxs-lookup"><span data-stu-id="d6e5f-120">Method</span></span>                                  | <span data-ttu-id="d6e5f-121">Description</span><span class="sxs-lookup"><span data-stu-id="d6e5f-121">Description</span></span>                                                                        |
|:----------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="d6e5f-122">**Cliquez sur**</span><span class="sxs-lookup"><span data-stu-id="d6e5f-122">**Click**</span></span>](ivmmouse-click.md)         | <span data-ttu-id="d6e5f-123">Simule un clic sur le bouton de la souris.</span><span class="sxs-lookup"><span data-stu-id="d6e5f-123">Simulates a mouse button click.</span></span><br/>                                         |
| [<span data-ttu-id="d6e5f-124">**GetButton**</span><span class="sxs-lookup"><span data-stu-id="d6e5f-124">**GetButton**</span></span>](ivmmouse-getbutton.md) | <span data-ttu-id="d6e5f-125">Récupère l’état actuel (vers le haut ou vers le haut) du bouton spécifié de la souris.</span><span class="sxs-lookup"><span data-stu-id="d6e5f-125">Retrieves the current state (up or down) of the specified mouse button.</span></span><br/> |
| [<span data-ttu-id="d6e5f-126">**SetButton**</span><span class="sxs-lookup"><span data-stu-id="d6e5f-126">**SetButton**</span></span>](ivmmouse-setbutton.md) | <span data-ttu-id="d6e5f-127">Définit l’état actuel (vers le haut ou vers le haut) du bouton spécifié de la souris.</span><span class="sxs-lookup"><span data-stu-id="d6e5f-127">Sets the current state (up or down) of the specified mouse button.</span></span><br/>      |



 

### <a name="properties"></a><span data-ttu-id="d6e5f-128">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d6e5f-128">Properties</span></span>

<span data-ttu-id="d6e5f-129">L’interface **IVMMouse** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d6e5f-129">The **IVMMouse** interface has these properties.</span></span>



| <span data-ttu-id="d6e5f-130">Propriété</span><span class="sxs-lookup"><span data-stu-id="d6e5f-130">Property</span></span>                                                                         | <span data-ttu-id="d6e5f-131">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="d6e5f-131">Access type</span></span>           | <span data-ttu-id="d6e5f-132">Description</span><span class="sxs-lookup"><span data-stu-id="d6e5f-132">Description</span></span>                                                                                |
|:---------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6e5f-133">**HorizontalPosition**</span><span class="sxs-lookup"><span data-stu-id="d6e5f-133">**HorizontalPosition**</span></span>](ivmmouse-horizontalposition.md)<br/>             | <span data-ttu-id="d6e5f-134">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d6e5f-134">Read/write</span></span><br/> | <span data-ttu-id="d6e5f-135">Coordonnée x absolue de la souris.</span><span class="sxs-lookup"><span data-stu-id="d6e5f-135">The absolute x-coordinate of the mouse.</span></span><br/>                                         |
| [<span data-ttu-id="d6e5f-136">**ScrollWheelPosition**</span><span class="sxs-lookup"><span data-stu-id="d6e5f-136">**ScrollWheelPosition**</span></span>](ivmmouse-scrollwheelposition.md)<br/>           | <span data-ttu-id="d6e5f-137">Écriture seule</span><span class="sxs-lookup"><span data-stu-id="d6e5f-137">Write-only</span></span><br/> | <span data-ttu-id="d6e5f-138">Coordonnée z de la souris (relative uniquement).</span><span class="sxs-lookup"><span data-stu-id="d6e5f-138">The z-coordinate of the mouse (relative only).</span></span><br/>                                  |
| [<span data-ttu-id="d6e5f-139">**UsingAbsoluteCoordinates**</span><span class="sxs-lookup"><span data-stu-id="d6e5f-139">**UsingAbsoluteCoordinates**</span></span>](ivmmouse-usingabsolutecoordinates.md)<br/> | <span data-ttu-id="d6e5f-140">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d6e5f-140">Read/write</span></span><br/> | <span data-ttu-id="d6e5f-141">Indique si les coordonnées de la souris représentent des coordonnées absolues ou relatives.</span><span class="sxs-lookup"><span data-stu-id="d6e5f-141">Indicates whether mouse coordinates represent absolute or relative coordinates.</span></span><br/> |
| [<span data-ttu-id="d6e5f-142">**VerticalPosition**</span><span class="sxs-lookup"><span data-stu-id="d6e5f-142">**VerticalPosition**</span></span>](ivmmouse-verticalposition.md)<br/>                 | <span data-ttu-id="d6e5f-143">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d6e5f-143">Read/write</span></span><br/> | <span data-ttu-id="d6e5f-144">Coordonnée y absolue de la souris.</span><span class="sxs-lookup"><span data-stu-id="d6e5f-144">The absolute y-coordinate of the mouse.</span></span><br/>                                         |



 

## <a name="requirements"></a><span data-ttu-id="d6e5f-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6e5f-145">Requirements</span></span>



| <span data-ttu-id="d6e5f-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6e5f-146">Requirement</span></span> | <span data-ttu-id="d6e5f-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6e5f-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6e5f-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6e5f-148">Minimum supported client</span></span><br/> | <span data-ttu-id="d6e5f-149">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6e5f-149">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d6e5f-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6e5f-150">Minimum supported server</span></span><br/> | <span data-ttu-id="d6e5f-151">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6e5f-151">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d6e5f-152">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="d6e5f-152">End of client support</span></span><br/>    | <span data-ttu-id="d6e5f-153">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d6e5f-153">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d6e5f-154">Produit</span><span class="sxs-lookup"><span data-stu-id="d6e5f-154">Product</span></span><br/>                  | <span data-ttu-id="d6e5f-155">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d6e5f-155">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d6e5f-156">En-tête</span><span class="sxs-lookup"><span data-stu-id="d6e5f-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6e5f-157"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6e5f-157"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d6e5f-158">IID</span><span class="sxs-lookup"><span data-stu-id="d6e5f-158">IID</span></span><br/>                      | <span data-ttu-id="d6e5f-159">IID \_ IVMmouse est défini en tant que ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="d6e5f-159">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



 

