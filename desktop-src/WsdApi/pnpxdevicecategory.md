---
description: Spécifie la catégorie PnP-X à laquelle l’appareil appartient. Plusieurs catégories peuvent être spécifiées.
ms.assetid: 1ca46000-4700-4326-8f49-1b9a22d45bfa
title: Élément PnPXDeviceCategory
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 731dd78fbe366fc9c7923686d3d9ac90b772c23d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524248"
---
# <a name="pnpxdevicecategory-element"></a><span data-ttu-id="ec7c0-104">Élément PnPXDeviceCategory</span><span class="sxs-lookup"><span data-stu-id="ec7c0-104">PnPXDeviceCategory element</span></span>

<span data-ttu-id="ec7c0-105">Spécifie la catégorie PnP-X à laquelle l’appareil appartient.</span><span class="sxs-lookup"><span data-stu-id="ec7c0-105">Specifies the PnP-X category to which the device belongs.</span></span> <span data-ttu-id="ec7c0-106">Plusieurs catégories peuvent être spécifiées.</span><span class="sxs-lookup"><span data-stu-id="ec7c0-106">More than one category can be specified.</span></span>

## <a name="usage"></a><span data-ttu-id="ec7c0-107">Utilisation</span><span class="sxs-lookup"><span data-stu-id="ec7c0-107">Usage</span></span>

``` syntax
<PnPXDeviceCategory/>
```

## <a name="attributes"></a><span data-ttu-id="ec7c0-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="ec7c0-108">Attributes</span></span>

<span data-ttu-id="ec7c0-109">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="ec7c0-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ec7c0-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ec7c0-110">Child elements</span></span>

<span data-ttu-id="ec7c0-111">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="ec7c0-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="ec7c0-112">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ec7c0-112">Parent elements</span></span>



| <span data-ttu-id="ec7c0-113">Élément</span><span class="sxs-lookup"><span data-stu-id="ec7c0-113">Element</span></span>                                                   | <span data-ttu-id="ec7c0-114">Description</span><span class="sxs-lookup"><span data-stu-id="ec7c0-114">Description</span></span>                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ec7c0-115">**thisModelMetadata**</span><span class="sxs-lookup"><span data-stu-id="ec7c0-115">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/> | <span data-ttu-id="ec7c0-116">Définit les métadonnées du fabricant et du modèle pour l’appareil à implémenter.</span><span class="sxs-lookup"><span data-stu-id="ec7c0-116">Defines the manufacturer and model metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="ec7c0-117">Notes</span><span class="sxs-lookup"><span data-stu-id="ec7c0-117">Remarks</span></span>

<span data-ttu-id="ec7c0-118">Les appareils peuvent également spécifier une sous-catégorie d’appareil pour une catégorie d’appareil plus descriptive.</span><span class="sxs-lookup"><span data-stu-id="ec7c0-118">Devices can also specify a device subcategory for a more descriptive device category.</span></span> <span data-ttu-id="ec7c0-119">Par exemple, « phones. WindowsMobile cameras. DigitalStillCamera MediaDevices. MusicPlayer » identifie un appareil qui est un appareil Microsoft Windows Mobile avec un appareil photo et un lecteur de musique.</span><span class="sxs-lookup"><span data-stu-id="ec7c0-119">For example, "Phones.WindowsMobile Cameras.DigitalStillCamera MediaDevices.MusicPlayer" identifies a device that is a Microsoft Windows Mobile  device with a camera and music player.</span></span> <span data-ttu-id="ec7c0-120">La catégorie d’appareil principale de cet appareil est « téléphone ».</span><span class="sxs-lookup"><span data-stu-id="ec7c0-120">The primary device category for this device would be "Phones".</span></span>

<span data-ttu-id="ec7c0-121">Pour spécifier plusieurs catégories d’appareils, séparez-les par un espace.</span><span class="sxs-lookup"><span data-stu-id="ec7c0-121">To specify more than one device category, separate the categories with a space.</span></span> <span data-ttu-id="ec7c0-122">Par exemple, « imprimantes Storage » identifie un appareil avec la catégorie principale « Printers » et une catégorie secondaire de « Storage ».</span><span class="sxs-lookup"><span data-stu-id="ec7c0-122">For example, "Printers Storage" identifies a device with a primary category of "Printers" and a secondary category of "Storage".</span></span>

<span data-ttu-id="ec7c0-123">Si un élément **PnPXDeviceCategory** est présent, au moins un élément [**hébergé**](hosted.md) doit contenir à la fois des éléments [**PnPXHardwareId**](pnpxhardwareid.md) et [**PnPXCompatibleId**](pnpxcompatibleid.md) .</span><span class="sxs-lookup"><span data-stu-id="ec7c0-123">If a **PnPXDeviceCategory** element is present, then at least one [**hosted**](hosted.md) element should contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="ec7c0-124">De même, si des éléments **PnPXHardwareId** et **PnPXCompatibleId** sont présents dans un élément **hébergé** , au moins un élément **PnPXDeviceCategory** doit être présent dans l’élément [**thisModelMetadata**](thismodelmetadata.md) .</span><span class="sxs-lookup"><span data-stu-id="ec7c0-124">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, at least one **PnPXDeviceCategory** element should be present inside the [**thisModelMetadata**](thismodelmetadata.md) element.</span></span>

## <a name="element-information"></a><span data-ttu-id="ec7c0-125">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="ec7c0-125">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="ec7c0-126">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec7c0-126">Minimum supported system</span></span><br/> | <span data-ttu-id="ec7c0-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ec7c0-127">Windows Vista</span></span> |
| <span data-ttu-id="ec7c0-128">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="ec7c0-128">Can be empty</span></span>                        | <span data-ttu-id="ec7c0-129">Oui</span><span class="sxs-lookup"><span data-stu-id="ec7c0-129">Yes</span></span>           |



 

 




