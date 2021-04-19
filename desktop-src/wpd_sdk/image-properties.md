---
description: Appareils mobiles Windows prend en charge les propriétés d’image suivantes.
ms.assetid: fb1707a7-16b0-4073-b21d-2ba2f4fd76f7
title: Propriétés de l’image (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 959a008d9c30991058226e52db6e45ed417ee6e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541538"
---
# <a name="image-properties"></a><span data-ttu-id="81005-103">Propriétés de l’image</span><span class="sxs-lookup"><span data-stu-id="81005-103">Image Properties</span></span>

<span data-ttu-id="81005-104">Appareils mobiles Windows prend en charge les propriétés d’image suivantes.</span><span class="sxs-lookup"><span data-stu-id="81005-104">Windows Portable Devices supports the following image properties.</span></span>



| <span data-ttu-id="81005-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="81005-105">Property</span></span>                                                                                                                                       | <span data-ttu-id="81005-106">VarType</span><span class="sxs-lookup"><span data-stu-id="81005-106">VarType</span></span>     | <span data-ttu-id="81005-107">Description</span><span class="sxs-lookup"><span data-stu-id="81005-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81005-108">**\_image wpd \_ BITDEPTH**</span><span class="sxs-lookup"><span data-stu-id="81005-108">**WPD\_IMAGE\_BITDEPTH**</span></span>                                                                                                                       | <span data-ttu-id="81005-109">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="81005-109">**VT\_UI4**</span></span> | <span data-ttu-id="81005-110">Profondeur de bit de l’image.</span><span class="sxs-lookup"><span data-stu-id="81005-110">The bit depth of the image.</span></span>                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="81005-111"><span id="wpd_image_color_corrected_status"></span><span id="WPD_IMAGE_COLOR_CORRECTED_STATUS"></span>**État de couleur de l' \_ image wpd \_ \_ corrigé \_**</span><span class="sxs-lookup"><span data-stu-id="81005-111"><span id="wpd_image_color_corrected_status"></span><span id="WPD_IMAGE_COLOR_CORRECTED_STATUS"></span>**WPD\_IMAGE\_COLOR\_CORRECTED\_STATUS**</span></span> | <span data-ttu-id="81005-112">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="81005-112">**VT\_UI4**</span></span> | <span data-ttu-id="81005-113">Énumération de [**\_ \_ \_ \_ valeurs d’État corrigées pour la couleur wpd**](wpd-color-corrected-status-values.md) qui spécifie si le fichier a été corrigé par des couleurs. Cela empêche plusieurs appareils de corriger automatiquement les couleurs de l’image pendant le traitement.</span><span class="sxs-lookup"><span data-stu-id="81005-113">A [**WPD\_COLOR\_CORRECTED\_STATUS\_VALUES**](wpd-color-corrected-status-values.md) enumeration that specifies whether the file has been color-corrected.This prevents multiple devices from automatically color-correcting the image during post-processing.</span></span><br/>                                                                       |
| <span data-ttu-id="81005-114">**\_ \_ État rogné de l’image wpd \_**</span><span class="sxs-lookup"><span data-stu-id="81005-114">**WPD\_IMAGE\_CROPPED\_STATUS**</span></span>                                                                                                                | <span data-ttu-id="81005-115">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="81005-115">**VT\_UI4**</span></span> | <span data-ttu-id="81005-116">Énumération des valeurs d’état d’un fichier [**wpd \_ rogné \_ \_**](wpd-cropped-status-values.md) qui spécifie si le fichier a été rogné. Cela empêche plusieurs appareils de rogner automatiquement l’image pendant le traitement.</span><span class="sxs-lookup"><span data-stu-id="81005-116">A [**WPD\_CROPPED\_STATUS\_VALUES**](wpd-cropped-status-values.md) enumeration that specifies whether the file has been cropped.This prevents multiple devices from automatically cropping the image during post-processing.</span></span><br/>                                                                                                        |
| <span data-ttu-id="81005-117">**\_index d' \_ exposition d’image wpd \_**</span><span class="sxs-lookup"><span data-stu-id="81005-117">**WPD\_IMAGE\_EXPOSURE\_INDEX**</span></span>                                                                                                                | <span data-ttu-id="81005-118">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="81005-118">**VT\_UI4**</span></span> | <span data-ttu-id="81005-119">Valeur qui identifie les paramètres de vitesse du film lorsque cette image a été capturée. Les paramètres correspondent aux désignations ISO de ASA/DIN.</span><span class="sxs-lookup"><span data-stu-id="81005-119">A value that identifies the film speed settings when this image was captured.The settings correspond to the ISO designations of ASA/DIN.</span></span><br/> <span data-ttu-id="81005-120">En règle générale, un appareil prend en charge des valeurs énumérées discrètes, mais le contrôle continu sur une plage est possible.</span><span class="sxs-lookup"><span data-stu-id="81005-120">Typically, a device supports discrete enumerated values, but continuous control over a range is possible.</span></span><br/> <span data-ttu-id="81005-121">La valeur 0xFFFFFFFF correspond au paramètre ISO automatique.</span><span class="sxs-lookup"><span data-stu-id="81005-121">A value of 0xFFFFFFFF corresponds to automatic ISO setting.</span></span><br/> |
| <span data-ttu-id="81005-122">**temps d’exposition de l' \_ image wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="81005-122">**WPD\_IMAGE\_EXPOSURE\_TIME**</span></span>                                                                                                                 | <span data-ttu-id="81005-123">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="81005-123">**VT\_UI4**</span></span> | <span data-ttu-id="81005-124">Identifie la vitesse d’obturation de l’appareil lorsque cette image a été capturée. Les unités sont en secondes mises à l’échelle par 10000.</span><span class="sxs-lookup"><span data-stu-id="81005-124">Identifies the shutter speed of the device when this image was captured.Units are in seconds scaled by 10000.</span></span><br/>                                                                                                                                                                                                                        |
| <span data-ttu-id="81005-125">**\_image wpd \_ FNUMBER**</span><span class="sxs-lookup"><span data-stu-id="81005-125">**WPD\_IMAGE\_FNUMBER**</span></span>                                                                                                                        | <span data-ttu-id="81005-126">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="81005-126">**VT\_UI4**</span></span> | <span data-ttu-id="81005-127">Identifie le paramètre d’ouverture de la lentille lorsque cette image a été capturée. Les unités sont égales au nombre f mis à l’échelle par 100.</span><span class="sxs-lookup"><span data-stu-id="81005-127">Identifies the aperture setting of the lens when this image was captured.Units are equal to the f-number scaled by 100.</span></span><br/>                                                                                                                                                                                                              |
| <span data-ttu-id="81005-128">**\_ \_ résolution horizontale de l’image wpd \_**</span><span class="sxs-lookup"><span data-stu-id="81005-128">**WPD\_IMAGE\_HORIZONTAL\_RESOLUTION**</span></span>                                                                                                         | <span data-ttu-id="81005-129">**VT \_ R8**</span><span class="sxs-lookup"><span data-stu-id="81005-129">**VT\_R8**</span></span>  | <span data-ttu-id="81005-130">Indique la résolution horizontale d’une image, en points par pouce (DPI).</span><span class="sxs-lookup"><span data-stu-id="81005-130">Indicates the horizontal resolution of an image, in dots per inch (DPI) .</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="81005-131">**\_ \_ résolution verticale de l’image wpd \_**</span><span class="sxs-lookup"><span data-stu-id="81005-131">**WPD\_IMAGE\_VERTICAL\_RESOLUTION**</span></span>                                                                                                           | <span data-ttu-id="81005-132">**VT \_ R8**</span><span class="sxs-lookup"><span data-stu-id="81005-132">**VT\_R8**</span></span>  | <span data-ttu-id="81005-133">Indique la résolution verticale d’une image, en points par pouce (DPI).</span><span class="sxs-lookup"><span data-stu-id="81005-133">Indicates the vertical resolution of an image, in dots per inch (DPI) .</span></span>                                                                                                                                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="81005-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81005-134">Requirements</span></span>



| <span data-ttu-id="81005-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81005-135">Requirement</span></span> | <span data-ttu-id="81005-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="81005-136">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="81005-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="81005-137">Header</span></span><br/> | <dl> <span data-ttu-id="81005-138"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="81005-138"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81005-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81005-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81005-140">**Propriétés et attributs WPD**</span><span class="sxs-lookup"><span data-stu-id="81005-140">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




