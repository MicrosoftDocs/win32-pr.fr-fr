---
title: Modification de l’appareil pointeur
description: Valeurs qui peuvent être passées dans le paramètre wParam du message WM_POINTERDEVICECHANGE.
ms.assetid: B95191D7-820B-445A-A3A4-811F9F1A8C4F
topic_type:
- apiref
api_name:
- PDC_ARRIVAL
- PDC_REMOVAL
- PDC_ORIENTATION_0
- PDC_ORIENTATION_90
- PDC_ORIENTATION_180
- PDC_ORIENTATION_270
- PDC_MODE_DEFAULT
- PDC_MODE_CENTERED
- PDC_MAPPING_CHANGE
- PDC_RESOLUTION
- PDC_ORIGIN
- PDC_MODE_ASPECTRATIOPRESERVED
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5e4b85c17adcd2db7c0f2f672e27ca467b346b0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942498"
---
# <a name="pointer-device-change"></a><span data-ttu-id="9dcc7-103">Modification de l’appareil pointeur</span><span class="sxs-lookup"><span data-stu-id="9dcc7-103">Pointer Device Change</span></span>

<span data-ttu-id="9dcc7-104">Valeurs qui peuvent être passées dans le paramètre *wParam* du message [**WM_POINTERDEVICECHANGE**](wm-pointerdevicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="9dcc7-104">Values that can be passed in the *wParam* parameter of the [**WM_POINTERDEVICECHANGE**](wm-pointerdevicechange.md) message.</span></span>

<dl> <dt>

<span data-ttu-id="9dcc7-105"><span id="PDC_ARRIVAL"></span><span id="pdc_arrival"></span>**PDC_ARRIVAL**</span><span class="sxs-lookup"><span data-stu-id="9dcc7-105"><span id="PDC_ARRIVAL"></span><span id="pdc_arrival"></span>**PDC_ARRIVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dcc7-106">0x001</span><span class="sxs-lookup"><span data-stu-id="9dcc7-106">0x001</span></span>
</dt> <dt>



<span data-ttu-id="9dcc7-107">Un nouvel appareil est attaché.</span><span class="sxs-lookup"><span data-stu-id="9dcc7-107">A new device is attached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dcc7-108"><span id="PDC_REMOVAL"></span><span id="pdc_removal"></span>**PDC_REMOVAL**</span><span class="sxs-lookup"><span data-stu-id="9dcc7-108"><span id="PDC_REMOVAL"></span><span id="pdc_removal"></span>**PDC_REMOVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dcc7-109">0x002</span><span class="sxs-lookup"><span data-stu-id="9dcc7-109">0x002</span></span>
</dt> <dt>



<span data-ttu-id="9dcc7-110">Un appareil a été détaché.</span><span class="sxs-lookup"><span data-stu-id="9dcc7-110">A device has been detached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dcc7-111"><span id="PDC_ORIENTATION_0"></span><span id="pdc_orientation_0"></span>**PDC_ORIENTATION_0**</span><span class="sxs-lookup"><span data-stu-id="9dcc7-111"><span id="PDC_ORIENTATION_0"></span><span id="pdc_orientation_0"></span>**PDC_ORIENTATION_0**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dcc7-112">0x004</span><span class="sxs-lookup"><span data-stu-id="9dcc7-112">0x004</span></span>
</dt> <dt>



<span data-ttu-id="9dcc7-113">Orientation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9dcc7-113">Orientation of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dcc7-114"><span id="PDC_ORIENTATION_90"></span><span id="pdc_orientation_90"></span>**PDC_ORIENTATION_90**</span><span class="sxs-lookup"><span data-stu-id="9dcc7-114"><span id="PDC_ORIENTATION_90"></span><span id="pdc_orientation_90"></span>**PDC_ORIENTATION_90**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dcc7-115">0x008</span><span class="sxs-lookup"><span data-stu-id="9dcc7-115">0x008</span></span>
</dt> <dt>



<span data-ttu-id="9dcc7-116">Orientation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9dcc7-116">Orientation of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dcc7-117"><span id="PDC_ORIENTATION_180"></span><span id="pdc_orientation_180"></span>**PDC_ORIENTATION_180**</span><span class="sxs-lookup"><span data-stu-id="9dcc7-117"><span id="PDC_ORIENTATION_180"></span><span id="pdc_orientation_180"></span>**PDC_ORIENTATION_180**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dcc7-118">0x010</span><span class="sxs-lookup"><span data-stu-id="9dcc7-118">0x010</span></span>
</dt> <dt>



<span data-ttu-id="9dcc7-119">Orientation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9dcc7-119">Orientation of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dcc7-120"><span id="PDC_ORIENTATION_270"></span><span id="pdc_orientation_270"></span>**PDC_ORIENTATION_270**</span><span class="sxs-lookup"><span data-stu-id="9dcc7-120"><span id="PDC_ORIENTATION_270"></span><span id="pdc_orientation_270"></span>**PDC_ORIENTATION_270**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dcc7-121">0x020</span><span class="sxs-lookup"><span data-stu-id="9dcc7-121">0x020</span></span>
</dt> <dt>



<span data-ttu-id="9dcc7-122">Orientation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9dcc7-122">Orientation of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dcc7-123"><span id="PDC_MODE_DEFAULT"></span><span id="pdc_mode_default"></span>**PDC_MODE_DEFAULT**</span><span class="sxs-lookup"><span data-stu-id="9dcc7-123"><span id="PDC_MODE_DEFAULT"></span><span id="pdc_mode_default"></span>**PDC_MODE_DEFAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dcc7-124">0x040</span><span class="sxs-lookup"><span data-stu-id="9dcc7-124">0x040</span></span>
</dt> <dt>



<span data-ttu-id="9dcc7-125">Mode d’affichage par défaut.</span><span class="sxs-lookup"><span data-stu-id="9dcc7-125">The default display mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dcc7-126"><span id="PDC_MODE_CENTERED"></span><span id="pdc_mode_centered"></span>**PDC_MODE_CENTERED**</span><span class="sxs-lookup"><span data-stu-id="9dcc7-126"><span id="PDC_MODE_CENTERED"></span><span id="pdc_mode_centered"></span>**PDC_MODE_CENTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dcc7-127">0x080</span><span class="sxs-lookup"><span data-stu-id="9dcc7-127">0x080</span></span>
</dt> <dt>



<span data-ttu-id="9dcc7-128">Mode d’affichage centré.</span><span class="sxs-lookup"><span data-stu-id="9dcc7-128">Centered display mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dcc7-129"><span id="PDC_MAPPING_CHANGE"></span><span id="pdc_mapping_change"></span>**PDC_MAPPING_CHANGE**</span><span class="sxs-lookup"><span data-stu-id="9dcc7-129"><span id="PDC_MAPPING_CHANGE"></span><span id="pdc_mapping_change"></span>**PDC_MAPPING_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dcc7-130">0x100</span><span class="sxs-lookup"><span data-stu-id="9dcc7-130">0x100</span></span>
</dt> <dt>



<span data-ttu-id="9dcc7-131">Modification de l’affichage du mappage du digitaliseur.</span><span class="sxs-lookup"><span data-stu-id="9dcc7-131">The change in display to digitizer mapping.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dcc7-132"><span id="PDC_RESOLUTION"></span><span id="pdc_resolution"></span>**PDC_RESOLUTION**</span><span class="sxs-lookup"><span data-stu-id="9dcc7-132"><span id="PDC_RESOLUTION"></span><span id="pdc_resolution"></span>**PDC_RESOLUTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dcc7-133">0x200</span><span class="sxs-lookup"><span data-stu-id="9dcc7-133">0x200</span></span>
</dt> <dt>



<span data-ttu-id="9dcc7-134">Résolution d’affichage.</span><span class="sxs-lookup"><span data-stu-id="9dcc7-134">Display resolution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dcc7-135"><span id="PDC_ORIGIN"></span><span id="pdc_origin"></span>**PDC_ORIGIN**</span><span class="sxs-lookup"><span data-stu-id="9dcc7-135"><span id="PDC_ORIGIN"></span><span id="pdc_origin"></span>**PDC_ORIGIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dcc7-136">0x400</span><span class="sxs-lookup"><span data-stu-id="9dcc7-136">0x400</span></span>
</dt> <dt>



<span data-ttu-id="9dcc7-137">Origine de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="9dcc7-137">The display origin.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dcc7-138"><span id="PDC_MODE_ASPECTRATIOPRESERVED"></span><span id="pdc_mode_aspectratiopreserved"></span>**PDC_MODE_ASPECTRATIOPRESERVED**</span><span class="sxs-lookup"><span data-stu-id="9dcc7-138"><span id="PDC_MODE_ASPECTRATIOPRESERVED"></span><span id="pdc_mode_aspectratiopreserved"></span>**PDC_MODE_ASPECTRATIOPRESERVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dcc7-139">0x800</span><span class="sxs-lookup"><span data-stu-id="9dcc7-139">0x800</span></span>
</dt> <dt>



<span data-ttu-id="9dcc7-140">Proportions d’affichage.</span><span class="sxs-lookup"><span data-stu-id="9dcc7-140">The display aspect ratio.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9dcc7-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9dcc7-141">Requirements</span></span>



| <span data-ttu-id="9dcc7-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9dcc7-142">Requirement</span></span> | <span data-ttu-id="9dcc7-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="9dcc7-143">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9dcc7-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9dcc7-144">Minimum supported client</span></span><br/> | <span data-ttu-id="9dcc7-145">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9dcc7-145">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9dcc7-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9dcc7-146">Minimum supported server</span></span><br/> | <span data-ttu-id="9dcc7-147">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9dcc7-147">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9dcc7-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="9dcc7-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="9dcc7-149"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="9dcc7-149"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9dcc7-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9dcc7-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dcc7-151">Constantes</span><span class="sxs-lookup"><span data-stu-id="9dcc7-151">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="9dcc7-152">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="9dcc7-152">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





