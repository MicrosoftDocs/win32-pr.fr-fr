---
description: Spécifie la catégorie PnP-X à laquelle l’appareil appartient. Plusieurs catégories peuvent être spécifiées.
ms.assetid: 1ca46000-4700-4326-8f49-1b9a22d45bfa
title: Élément PnPXDeviceCategory
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a08084d780c26d2f7fab902156939fd14a3e60c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996586"
---
# <a name="pnpxdevicecategory-element"></a><span data-ttu-id="8ad69-104">Élément PnPXDeviceCategory</span><span class="sxs-lookup"><span data-stu-id="8ad69-104">PnPXDeviceCategory element</span></span>

<span data-ttu-id="8ad69-105">Spécifie la catégorie PnP-X à laquelle l’appareil appartient.</span><span class="sxs-lookup"><span data-stu-id="8ad69-105">Specifies the PnP-X category to which the device belongs.</span></span> <span data-ttu-id="8ad69-106">Plusieurs catégories peuvent être spécifiées.</span><span class="sxs-lookup"><span data-stu-id="8ad69-106">More than one category can be specified.</span></span>

## <a name="usage"></a><span data-ttu-id="8ad69-107">Usage</span><span class="sxs-lookup"><span data-stu-id="8ad69-107">Usage</span></span>

``` syntax
<PnPXDeviceCategory/>
```

## <a name="attributes"></a><span data-ttu-id="8ad69-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="8ad69-108">Attributes</span></span>

<span data-ttu-id="8ad69-109">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="8ad69-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="8ad69-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="8ad69-110">Child elements</span></span>

<span data-ttu-id="8ad69-111">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="8ad69-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="8ad69-112">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="8ad69-112">Parent elements</span></span>



| <span data-ttu-id="8ad69-113">Élément</span><span class="sxs-lookup"><span data-stu-id="8ad69-113">Element</span></span>                                                   | <span data-ttu-id="8ad69-114">Description</span><span class="sxs-lookup"><span data-stu-id="8ad69-114">Description</span></span>                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8ad69-115">**thisModelMetadata**</span><span class="sxs-lookup"><span data-stu-id="8ad69-115">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/> | <span data-ttu-id="8ad69-116">Définit les métadonnées du fabricant et du modèle pour l’appareil à implémenter.</span><span class="sxs-lookup"><span data-stu-id="8ad69-116">Defines the manufacturer and model metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="8ad69-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="8ad69-117">Remarks</span></span>

<span data-ttu-id="8ad69-118">Les appareils peuvent également spécifier une sous-catégorie d’appareil pour une catégorie d’appareil plus descriptive.</span><span class="sxs-lookup"><span data-stu-id="8ad69-118">Devices can also specify a device subcategory for a more descriptive device category.</span></span> <span data-ttu-id="8ad69-119">Par exemple, « phones. WindowsMobile cameras. DigitalStillCamera MediaDevices. MusicPlayer » identifie un appareil qui est un appareil Microsoft Windows Mobile avec un appareil photo et un lecteur de musique.</span><span class="sxs-lookup"><span data-stu-id="8ad69-119">For example, "Phones.WindowsMobile Cameras.DigitalStillCamera MediaDevices.MusicPlayer" identifies a device that is a Microsoft Windows Mobile  device with a camera and music player.</span></span> <span data-ttu-id="8ad69-120">La catégorie d’appareil principale de cet appareil est « téléphone ».</span><span class="sxs-lookup"><span data-stu-id="8ad69-120">The primary device category for this device would be "Phones".</span></span>

<span data-ttu-id="8ad69-121">Pour spécifier plusieurs catégories d’appareils, séparez-les par un espace.</span><span class="sxs-lookup"><span data-stu-id="8ad69-121">To specify more than one device category, separate the categories with a space.</span></span> <span data-ttu-id="8ad69-122">Par exemple, « imprimantes Storage » identifie un appareil avec la catégorie principale « Printers » et une catégorie secondaire de « Storage ».</span><span class="sxs-lookup"><span data-stu-id="8ad69-122">For example, "Printers Storage" identifies a device with a primary category of "Printers" and a secondary category of "Storage".</span></span>

<span data-ttu-id="8ad69-123">Si un élément **PnPXDeviceCategory** est présent, au moins un élément [**hébergé**](hosted.md) doit contenir à la fois des éléments [**PnPXHardwareId**](pnpxhardwareid.md) et [**PnPXCompatibleId**](pnpxcompatibleid.md) .</span><span class="sxs-lookup"><span data-stu-id="8ad69-123">If a **PnPXDeviceCategory** element is present, then at least one [**hosted**](hosted.md) element should contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="8ad69-124">De même, si des éléments **PnPXHardwareId** et **PnPXCompatibleId** sont présents dans un élément **hébergé** , au moins un élément **PnPXDeviceCategory** doit être présent dans l’élément [**thisModelMetadata**](thismodelmetadata.md) .</span><span class="sxs-lookup"><span data-stu-id="8ad69-124">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, at least one **PnPXDeviceCategory** element should be present inside the [**thisModelMetadata**](thismodelmetadata.md) element.</span></span>

## <a name="element-information"></a><span data-ttu-id="8ad69-125">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="8ad69-125">Element information</span></span>



| <span data-ttu-id="8ad69-126">Étiquette</span><span class="sxs-lookup"><span data-stu-id="8ad69-126">Label</span></span> | <span data-ttu-id="8ad69-127">Value</span><span class="sxs-lookup"><span data-stu-id="8ad69-127">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="8ad69-128">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ad69-128">Minimum supported system</span></span><br/> | <span data-ttu-id="8ad69-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8ad69-129">Windows Vista</span></span> |
| <span data-ttu-id="8ad69-130">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="8ad69-130">Can be empty</span></span>                        | <span data-ttu-id="8ad69-131">Oui</span><span class="sxs-lookup"><span data-stu-id="8ad69-131">Yes</span></span>           |



 

 




