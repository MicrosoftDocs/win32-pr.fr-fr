---
description: Retourne les informations de résumé de la machine virtuelle.
ms.assetid: CDDC2B5A-8172-4E6D-A206-CEAB9E54C69A
title: Méthode GetSummaryInformation de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetSummaryInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1399acd40f768fdb857d6a4a26e80a52d29111b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318097"
---
# <a name="getsummaryinformation-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="579c4-103">Méthode GetSummaryInformation de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="579c4-103">GetSummaryInformation method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="579c4-104">Retourne les informations de résumé de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="579c4-104">Returns virtual machine summary information.</span></span>

## <a name="syntax"></a><span data-ttu-id="579c4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="579c4-105">Syntax</span></span>


```mof
uint32 GetSummaryInformation(
  [in]  CIM_VirtualSystemSettingData REF SettingData[],
  [in]  uint32                           RequestedInformation[],
  [out] Msvm_SummaryInformationBase      SummaryInformation[]
);
```



## <a name="parameters"></a><span data-ttu-id="579c4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="579c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="579c4-107">*SettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="579c4-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="579c4-108">Type : **CIM \_ VirtualSystemSettingData \[ \]**</span><span class="sxs-lookup"><span data-stu-id="579c4-108">Type: **CIM\_VirtualSystemSettingData\[\]**</span></span>

<span data-ttu-id="579c4-109">Tableau d’instances [**de \_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)) qui spécifient les ordinateurs virtuels ou les captures instantanées dont les informations doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="579c4-109">An array of [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instances that specify the virtual machines or snapshots for which information is to be retrieved.</span></span> <span data-ttu-id="579c4-110">Si ce paramètre a la **valeur null**, les informations de toutes les machines virtuelles sont récupérées.</span><span class="sxs-lookup"><span data-stu-id="579c4-110">If this parameter is **Null**, information for all virtual machines is retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="579c4-111">*RequestedInformation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="579c4-111">*RequestedInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="579c4-112">Type : **UInt32 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="579c4-112">Type: **uint32\[\]**</span></span>

<span data-ttu-id="579c4-113">Tableau de valeurs d’énumération, qui correspondent aux propriétés de la classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) , qui spécifient les données à récupérer pour les machines virtuelles et les instantanés spécifiés dans le tableau *SettingData* .</span><span class="sxs-lookup"><span data-stu-id="579c4-113">An array of enumeration values, which correspond to the properties in the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class, that specify the data to retrieve for the virtual machines and snapshots specified in the *SettingData* array.</span></span>

<dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>

<span data-ttu-id="579c4-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nom** (0)</span><span class="sxs-lookup"><span data-stu-id="579c4-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name** (0)</span></span>


</dt> <dd>

<span data-ttu-id="579c4-115">Cela correspond à la propriété **Name** de la classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="579c4-115">This corresponds to the **Name** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>

<span data-ttu-id="579c4-116"><span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>**Nom** de l’élément (1)</span><span class="sxs-lookup"><span data-stu-id="579c4-116"><span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>**Element Name** (1)</span></span>


</dt> <dd>

<span data-ttu-id="579c4-117">Cela correspond à la propriété **ElementName** de la classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="579c4-117">This corresponds to the **ElementName** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>

<span data-ttu-id="579c4-118"><span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>**Heure de création** (2)</span><span class="sxs-lookup"><span data-stu-id="579c4-118"><span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>**Creation Time** (2)</span></span>


</dt> <dd>

<span data-ttu-id="579c4-119">Cela correspond à la propriété **CreationTime** de la classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="579c4-119">This corresponds to the **CreationTime** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>

<span data-ttu-id="579c4-120"><span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>**Remarques** (3)</span><span class="sxs-lookup"><span data-stu-id="579c4-120"><span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>**Notes** (3)</span></span>


</dt> <dd>

<span data-ttu-id="579c4-121">Cela correspond à la propriété **Notes** de la classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="579c4-121">This corresponds to the **Notes** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>

<span data-ttu-id="579c4-122"><span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>**Nombre de processeurs** (4)</span><span class="sxs-lookup"><span data-stu-id="579c4-122"><span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>**Number of Processors** (4)</span></span>


</dt> <dd>

<span data-ttu-id="579c4-123">Cela correspond à la propriété **NumberOfProcessors** de la classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="579c4-123">This corresponds to the **NumberOfProcessors** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>

<span data-ttu-id="579c4-124"><span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>**Petite image miniature (80x60)** (5)</span><span class="sxs-lookup"><span data-stu-id="579c4-124"><span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>**Small Thumbnail Image (80x60)** (5)</span></span>


</dt> <dd>

<span data-ttu-id="579c4-125">Cela correspond à la propriété **ThumbnailImage** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="579c4-125">This corresponds to the **ThumbnailImage** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span> <span data-ttu-id="579c4-126">Une image miniature avec les dimensions 80 60 sera récupérée.</span><span class="sxs-lookup"><span data-stu-id="579c4-126">A thumbnail image with the dimensions of 80 60 will be retrieved.</span></span>

</dd> <dt>

<span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>

<span data-ttu-id="579c4-127"><span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>**Image miniature moyenne (160x120)** (6)</span><span class="sxs-lookup"><span data-stu-id="579c4-127"><span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>**Medium Thumbnail Image (160x120)** (6)</span></span>


</dt> <dd>

<span data-ttu-id="579c4-128">Cela correspond à la propriété **ThumbnailImage** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="579c4-128">This corresponds to the **ThumbnailImage** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span> <span data-ttu-id="579c4-129">Une image miniature avec les dimensions 160 120 sera récupérée.</span><span class="sxs-lookup"><span data-stu-id="579c4-129">A thumbnail image with the dimensions of 160 120 will be retrieved.</span></span>

</dd> <dt>

<span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>

<span data-ttu-id="579c4-130"><span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>**Grande image miniature (320x240)** (7)</span><span class="sxs-lookup"><span data-stu-id="579c4-130"><span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>**Large Thumbnail Image (320x240)** (7)</span></span>


</dt> <dd>

<span data-ttu-id="579c4-131">Cela correspond à la propriété **ThumbnailImage** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="579c4-131">This corresponds to the **ThumbnailImage** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span> <span data-ttu-id="579c4-132">Une image miniature avec les dimensions 320 240 sera récupérée.</span><span class="sxs-lookup"><span data-stu-id="579c4-132">A thumbnail image with the dimensions of 320 240 will be retrieved.</span></span>

</dd> <dt>

<span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>

<span data-ttu-id="579c4-133"><span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>**AllocatedGPU** (8)</span><span class="sxs-lookup"><span data-stu-id="579c4-133"><span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>**AllocatedGPU** (8)</span></span>


</dt> <dd>

<span data-ttu-id="579c4-134">Cela correspond à la propriété **AllocatedGPU** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="579c4-134">This corresponds to the **AllocatedGPU** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>

<span data-ttu-id="579c4-135"><span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>**VirtualSwitchNames** (9)</span><span class="sxs-lookup"><span data-stu-id="579c4-135"><span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>**VirtualSwitchNames** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>

<span data-ttu-id="579c4-136"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version** (10)</span><span class="sxs-lookup"><span data-stu-id="579c4-136"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version** (10)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="579c4-137">Ajouté dans Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="579c4-137">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span data-ttu-id="579c4-138"><span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Protégé** (11)</span><span class="sxs-lookup"><span data-stu-id="579c4-138"><span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Shielded** (11)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="579c4-139">Ajouté dans Windows 10, version 1703 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="579c4-139">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>

<span data-ttu-id="579c4-140"><span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>**EnabledState** (100)</span><span class="sxs-lookup"><span data-stu-id="579c4-140"><span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>**EnabledState** (100)</span></span>


</dt> <dd>

<span data-ttu-id="579c4-141">Cela correspond à la propriété **EnabledState** de la classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="579c4-141">This corresponds to the **EnabledState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>

<span data-ttu-id="579c4-142"><span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>**ProcessorLoad** (101)</span><span class="sxs-lookup"><span data-stu-id="579c4-142"><span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>**ProcessorLoad** (101)</span></span>


</dt> <dd>

<span data-ttu-id="579c4-143">Cela correspond à la propriété **ProcessorLoad** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="579c4-143">This corresponds to the **ProcessorLoad** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>

<span data-ttu-id="579c4-144"><span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>**ProcessorLoadHistory** (102)</span><span class="sxs-lookup"><span data-stu-id="579c4-144"><span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>**ProcessorLoadHistory** (102)</span></span>


</dt> <dd>

<span data-ttu-id="579c4-145">Cela correspond à la propriété **ProcessorLoadHistory** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="579c4-145">This corresponds to the **ProcessorLoadHistory** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>

<span data-ttu-id="579c4-146"><span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>**MemoryUsage** (103)</span><span class="sxs-lookup"><span data-stu-id="579c4-146"><span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>**MemoryUsage** (103)</span></span>


</dt> <dd>

<span data-ttu-id="579c4-147">Cela correspond à la propriété **MemoryUsage** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="579c4-147">This corresponds to the **MemoryUsage** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>

<span data-ttu-id="579c4-148"><span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>**Pulsation** (104)</span><span class="sxs-lookup"><span data-stu-id="579c4-148"><span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>**Heartbeat** (104)</span></span>


</dt> <dd>

<span data-ttu-id="579c4-149">Cela correspond à la propriété **Heartbeat** de la classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="579c4-149">This corresponds to the **Heartbeat** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>

<span data-ttu-id="579c4-150"><span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>**Temps d’activité** (105)</span><span class="sxs-lookup"><span data-stu-id="579c4-150"><span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>**Uptime** (105)</span></span>


</dt> <dd>

<span data-ttu-id="579c4-151">Cela correspond à la propriété **Uptime** de la classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="579c4-151">This corresponds to the **UpTime** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>

<span data-ttu-id="579c4-152"><span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>**GuestOperatingSystem** (106)</span><span class="sxs-lookup"><span data-stu-id="579c4-152"><span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>**GuestOperatingSystem** (106)</span></span>


</dt> <dd>

<span data-ttu-id="579c4-153">Cela correspond à la propriété **GuestOperatingSystem** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="579c4-153">This corresponds to the **GuestOperatingSystem** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>

<span data-ttu-id="579c4-154"><span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>**Instantanés** (107)</span><span class="sxs-lookup"><span data-stu-id="579c4-154"><span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>**Snapshots** (107)</span></span>


</dt> <dd>

<span data-ttu-id="579c4-155">Cela correspond à la propriété d' **instantanés** de la classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="579c4-155">This corresponds to the **Snapshots** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>

<span data-ttu-id="579c4-156"><span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>**AsynchronousTasks** (108)</span><span class="sxs-lookup"><span data-stu-id="579c4-156"><span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>**AsynchronousTasks** (108)</span></span>


</dt> <dd>

<span data-ttu-id="579c4-157">Cela correspond à la propriété **AsynchronousTasks** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="579c4-157">This corresponds to the **AsynchronousTasks** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>

<span data-ttu-id="579c4-158"><span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>**HealthState** (109)</span><span class="sxs-lookup"><span data-stu-id="579c4-158"><span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>**HealthState** (109)</span></span>


</dt> <dd>

<span data-ttu-id="579c4-159">Cela correspond à la propriété **HealthState** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="579c4-159">This corresponds to the **HealthState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>

<span data-ttu-id="579c4-160"><span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>**OperationalStatus** (110)</span><span class="sxs-lookup"><span data-stu-id="579c4-160"><span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>**OperationalStatus** (110)</span></span>


</dt> <dd>

<span data-ttu-id="579c4-161">Cela correspond à la propriété **OperationalStatus** de la classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="579c4-161">This corresponds to the **OperationalStatus** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>

<span data-ttu-id="579c4-162"><span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>**StatusDescriptions** (111)</span><span class="sxs-lookup"><span data-stu-id="579c4-162"><span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>**StatusDescriptions** (111)</span></span>


</dt> <dd>

<span data-ttu-id="579c4-163">Cela correspond à la propriété **StatusDescriptions** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="579c4-163">This corresponds to the **StatusDescriptions** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>

<span data-ttu-id="579c4-164"><span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>**MemoryAvailable** (112)</span><span class="sxs-lookup"><span data-stu-id="579c4-164"><span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>**MemoryAvailable** (112)</span></span>


</dt> <dd>

<span data-ttu-id="579c4-165">Cela correspond à la propriété **MemoryAvailable** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="579c4-165">This corresponds to the **MemoryAvailable** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>

<span data-ttu-id="579c4-166"><span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>**AvailableMemoryBuffer** (113)</span><span class="sxs-lookup"><span data-stu-id="579c4-166"><span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>**AvailableMemoryBuffer** (113)</span></span>


</dt> <dd>

<span data-ttu-id="579c4-167">Cela correspond à la propriété **AvailableMemoryBuffer** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="579c4-167">This corresponds to the **AvailableMemoryBuffer** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>

<span data-ttu-id="579c4-168"><span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>**Mode de réplication** (114)</span><span class="sxs-lookup"><span data-stu-id="579c4-168"><span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>**Replication Mode** (114)</span></span>


</dt> <dd>

<span data-ttu-id="579c4-169">Cela correspond à la propriété **ReplicationMode** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="579c4-169">This corresponds to the **ReplicationMode** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>

<span data-ttu-id="579c4-170"><span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>**État de réplication** (115)</span><span class="sxs-lookup"><span data-stu-id="579c4-170"><span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>**Replication State** (115)</span></span>


</dt> <dd>

<span data-ttu-id="579c4-171">Cela correspond à la propriété **ReplicationState** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="579c4-171">This corresponds to the **ReplicationState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>

<span data-ttu-id="579c4-172"><span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>**Système de réplication HealthTest réplica** (116)</span><span class="sxs-lookup"><span data-stu-id="579c4-172"><span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>**Replication HealthTest Replica System** (116)</span></span>


</dt> <dd>

<span data-ttu-id="579c4-173">Cela correspond à la propriété **ReplicationHealth** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="579c4-173">This corresponds to the **ReplicationHealth** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>

<span data-ttu-id="579c4-174"><span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>**Intégrité** de l’Application (117)</span><span class="sxs-lookup"><span data-stu-id="579c4-174"><span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>**Application Health** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>

<span data-ttu-id="579c4-175"><span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>**ReplicationStateEx** (118)</span><span class="sxs-lookup"><span data-stu-id="579c4-175"><span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>**ReplicationStateEx** (118)</span></span>


</dt> <dd>

<span data-ttu-id="579c4-176">Cela correspond à la propriété **ReplicationState** de la [**classe \_ ReplicationRelationship MSVM**](msvm-replicationrelationship.md) .</span><span class="sxs-lookup"><span data-stu-id="579c4-176">This corresponds to the **ReplicationState** property of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class.</span></span> <span data-ttu-id="579c4-177">Il s’agit d’un tableau pour toutes les valeurs d’état de réplication sur les relations principales et étendues.</span><span class="sxs-lookup"><span data-stu-id="579c4-177">This is array for all replication state values across primary and extended relationship.</span></span> <span data-ttu-id="579c4-178">0 la valeur d’index est toujours pour la relation principale, et si la réplication étendue est activée, elle est retournée dans l’index 1.</span><span class="sxs-lookup"><span data-stu-id="579c4-178">0 index value is always for primary relationship, and if extended replication is enabled, it is returned in index 1.</span></span>

</dd> <dt>

<span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>

<span data-ttu-id="579c4-179"><span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>**ReplicationHealthEx** (119)</span><span class="sxs-lookup"><span data-stu-id="579c4-179"><span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>**ReplicationHealthEx** (119)</span></span>


</dt> <dd>

<span data-ttu-id="579c4-180">Cela correspond à la propriété **ReplicationHealth** de la [**classe \_ ReplicationRelationship MSVM**](msvm-replicationrelationship.md) .</span><span class="sxs-lookup"><span data-stu-id="579c4-180">This corresponds to the **ReplicationHealth** property of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class.</span></span> <span data-ttu-id="579c4-181">Il s’agit d’un tableau pour toutes les valeurs d’intégrité de réplication entre les relations principale et étendue.</span><span class="sxs-lookup"><span data-stu-id="579c4-181">This is array for all replication health values across primary and extended relationship.</span></span> <span data-ttu-id="579c4-182">0 la valeur d’index est toujours pour la relation principale, et si la réplication étendue est activée, elle est retournée dans l’index 1.</span><span class="sxs-lookup"><span data-stu-id="579c4-182">0 index value is always for primary relationship, and if extended replication is enabled, it is returned in index 1.</span></span>

</dd> <dt>

<span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>

<span data-ttu-id="579c4-183"><span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>**SwapFilesInUse** (120)</span><span class="sxs-lookup"><span data-stu-id="579c4-183"><span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>**SwapFilesInUse** (120)</span></span>


</dt> <dd>

<span data-ttu-id="579c4-184">Cela correspond à la propriété **SwapFilesInUse** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="579c4-184">This corresponds to the **SwapFilesInUse** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>

<span data-ttu-id="579c4-185"><span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (121)</span><span class="sxs-lookup"><span data-stu-id="579c4-185"><span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>

<span data-ttu-id="579c4-186"><span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>**ReplicationProviderId** (122)</span><span class="sxs-lookup"><span data-stu-id="579c4-186"><span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>**ReplicationProviderId** (122)</span></span>


</dt> <dd>

<span data-ttu-id="579c4-187">Cela correspond à la propriété **Name** de la classe [**MSVM \_ ReplicationProvider**](msvm-replicationprovider.md) .</span><span class="sxs-lookup"><span data-stu-id="579c4-187">This corresponds to the **Name** property of the [**Msvm\_ReplicationProvider**](msvm-replicationprovider.md) class.</span></span>

</dd> <dt>

<span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>

<span data-ttu-id="579c4-188"><span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>**MemorySpansPhysicalNumaNodes** (123)</span><span class="sxs-lookup"><span data-stu-id="579c4-188"><span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>**MemorySpansPhysicalNumaNodes** (123)</span></span>


</dt> <dd></dd> <dt>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>

<span data-ttu-id="579c4-189"><span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (132)</span><span class="sxs-lookup"><span data-stu-id="579c4-189"><span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (132)</span></span>


</dt> <dd>

<span data-ttu-id="579c4-190">Cela correspond à la propriété **IntegrationServicesVersionState** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="579c4-190">This corresponds to the **IntegrationServicesVersionState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>

<span data-ttu-id="579c4-191"><span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>**OtherEnabledState** (132)</span><span class="sxs-lookup"><span data-stu-id="579c4-191"><span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>**OtherEnabledState** (132)</span></span>


</dt> <dd>

<span data-ttu-id="579c4-192">Cela correspond à la propriété **OtherEnabledState** de la [**classe \_ SummaryInformation MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="579c4-192">This corresponds to the **OtherEnabledState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>



 <span data-ttu-id="579c4-193">(133)</span><span class="sxs-lookup"><span data-stu-id="579c4-193">(133)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="579c4-194">*SummaryInformation* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="579c4-194">*SummaryInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="579c4-195">Type : **[ **MSVM \_ SummaryInformationBase**](msvm-summaryinformationbase.md)\[\]**</span><span class="sxs-lookup"><span data-stu-id="579c4-195">Type: **[**Msvm\_SummaryInformationBase**](msvm-summaryinformationbase.md)\[\]**</span></span>

<span data-ttu-id="579c4-196">Tableau d’instances [**de \_ SummaryInformationBase MSVM**](msvm-summaryinformationbase.md) contenant les informations demandées pour les ordinateurs virtuels et/ou les instantanés spécifiés dans le tableau *SettingData* .</span><span class="sxs-lookup"><span data-stu-id="579c4-196">An array of [**Msvm\_SummaryInformationBase**](msvm-summaryinformationbase.md) instances containing the requested information for the virtual machines and/or snapshots specified in the *SettingData* array.</span></span> <span data-ttu-id="579c4-197">Ce tableau aura le même nombre d’éléments que le tableau *SettingData* .</span><span class="sxs-lookup"><span data-stu-id="579c4-197">This array will have the same number of elements as the *SettingData* array.</span></span> <span data-ttu-id="579c4-198">Chacune de ces entrées contient la propriété **Name** , même si cette propriété n’a pas été demandée.</span><span class="sxs-lookup"><span data-stu-id="579c4-198">Each of these entries will contain the **Name** property, even if this property was not requested.</span></span> <span data-ttu-id="579c4-199">Si la machine virtuelle ou la capture instantanée est introuvable ou n’est pas disponible, la propriété **nom** de l’entrée de résumé correspondante est vide.</span><span class="sxs-lookup"><span data-stu-id="579c4-199">If the virtual machine or snapshot cannot be found or is unavailable, the **Name** property of the corresponding summary information entry will be empty.</span></span>

<span data-ttu-id="579c4-200">Les propriétés non spécifiées dans le paramètre *RequestedInformation* auront une valeur **null** .</span><span class="sxs-lookup"><span data-stu-id="579c4-200">Properties not specified in the *RequestedInformation* parameter will have a **Null** value.</span></span>

> [!Note]  
> <span data-ttu-id="579c4-201">Type de données mis à jour à partir de dans Windows 10, version 1703 à partir de [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md).</span><span class="sxs-lookup"><span data-stu-id="579c4-201">Datatype updated from in Windows 10, version 1703 from [**Msvm\_SummaryInformation**](msvm-summaryinformation.md).</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="579c4-202">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="579c4-202">Return value</span></span>

<span data-ttu-id="579c4-203">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="579c4-203">Type: **uint32**</span></span>

<span data-ttu-id="579c4-204">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="579c4-204">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="579c4-205">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="579c4-205">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="579c4-206">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="579c4-206">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="579c4-207">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="579c4-207">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="579c4-208">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="579c4-208">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="579c4-209">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="579c4-209">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="579c4-210">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="579c4-210">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="579c4-211">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="579c4-211">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="579c4-212">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="579c4-212">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="579c4-213">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="579c4-213">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="579c4-214">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="579c4-214">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="579c4-215">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="579c4-215">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="579c4-216">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="579c4-216">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="579c4-217">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="579c4-217">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="579c4-218">Notes</span><span class="sxs-lookup"><span data-stu-id="579c4-218">Remarks</span></span>

<span data-ttu-id="579c4-219">L’accès à la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="579c4-219">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="579c4-220">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="579c4-220">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="579c4-221">Exemples</span><span class="sxs-lookup"><span data-stu-id="579c4-221">Examples</span></span>

<span data-ttu-id="579c4-222">L’exemple C# suivant affiche des informations de synthèse.</span><span class="sxs-lookup"><span data-stu-id="579c4-222">The following C# sample displays summary information.</span></span> <span data-ttu-id="579c4-223">Les utilitaires référencés se trouvent dans [les utilitaires courants pour les exemples de virtualisation (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="579c4-223">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="579c4-224">Pour fonctionner correctement, le code suivant doit être exécuté sur le serveur hôte de l’ordinateur virtuel et doit être exécuté avec des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="579c4-224">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
public class GetSummaryInformationClassV2
{
    public static void GetSummaryInformation(string[] vmNames)
    {
        ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
        ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");
        ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("GetSummaryInformation");

        ManagementObject[] virtualSystemSettings = new ManagementObject[vmNames.Length];

        for (int i = 0; i < vmNames.Length; i++)
        {
            virtualSystemSettings[i] = GetVirtualSystemSetting(vmNames[i], scope);
        }

        UInt32[] requestedInformation = new UInt32[4];
        requestedInformation[0] = 1;    // ElementName
        requestedInformation[2] = 103;  // MemoryUsage
        requestedInformation[3] = 112;  // MemoryAvailable

        inParams["SettingData"] = virtualSystemSettings;
        inParams["RequestedInformation"] = requestedInformation;

        ManagementBaseObject outParams = virtualSystemService.InvokeMethod("GetSummaryInformation", inParams, null);

        if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
        {
            Console.WriteLine("Summary information was retrieved successfully.");

            ManagementBaseObject[] summaryInformationArray = 
                (ManagementBaseObject[])outParams["SummaryInformation"];

            foreach (ManagementBaseObject summaryInformation in summaryInformationArray)
            {
                Console.WriteLine("\nVirtual System Summary Information:");
                if ((null == summaryInformation["Name"]) || 
                    (summaryInformation["Name"].ToString().Length == 0))
                {
                    Console.WriteLine("\tThe VM or snapshot could not be found.");
                }
                else
                {
                    Console.WriteLine("\tName: {0}", summaryInformation["Name"].ToString());
                    foreach (UInt32 requested in requestedInformation)
                    {
                        switch (requested)
                        {
                            case 1:
                                Console.WriteLine("\tElementName: {0}", summaryInformation["ElementName"].ToString());
                                break;

                            case 103:
                                Console.WriteLine("\tMemoryUsage: {0}", summaryInformation["MemoryUsage"].ToString());
                                break;

                            case 112:
                                Console.WriteLine("\tMemoryAvailable: {0}", summaryInformation["MemoryAvailable"].ToString());
                                break;
                        }
                    }
                }
            }
        }
        else
        {
            Console.WriteLine("Failed to retrieve virtual system summary information");
        }

        inParams.Dispose();
        outParams.Dispose();
        virtualSystemService.Dispose();
    }

    public static ManagementObject GetVirtualSystemSetting(string vmName, ManagementScope scope)
    {
        ManagementObject virtualSystem = Utility.GetTargetComputer(vmName, scope);

        ManagementObjectCollection virtualSystemSettings = virtualSystem.GetRelated
         (
             "Msvm_VirtualSystemSettingData",
             "Msvm_SettingsDefineState",
             null,
             null,
             "SettingData",
             "ManagedElement",
             false,
             null
         );

        ManagementObject virtualSystemSetting = null;

        foreach (ManagementObject instance in virtualSystemSettings)
        {
            virtualSystemSetting = instance;
            break;
        }

        return virtualSystemSetting;

    }
}
```



## <a name="requirements"></a><span data-ttu-id="579c4-225">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="579c4-225">Requirements</span></span>



| <span data-ttu-id="579c4-226">Condition requise</span><span class="sxs-lookup"><span data-stu-id="579c4-226">Requirement</span></span> | <span data-ttu-id="579c4-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="579c4-227">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="579c4-228">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="579c4-228">Minimum supported client</span></span><br/> | <span data-ttu-id="579c4-229">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="579c4-229">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="579c4-230">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="579c4-230">Minimum supported server</span></span><br/> | <span data-ttu-id="579c4-231">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="579c4-231">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="579c4-232">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="579c4-232">Namespace</span></span><br/>                | <span data-ttu-id="579c4-233">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="579c4-233">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="579c4-234">MOF</span><span class="sxs-lookup"><span data-stu-id="579c4-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="579c4-235"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="579c4-235"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="579c4-236">DLL</span><span class="sxs-lookup"><span data-stu-id="579c4-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="579c4-237"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="579c4-237"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="579c4-238">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="579c4-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="579c4-239">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="579c4-239">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> <dt>

<span data-ttu-id="579c4-240">[**\_VIRTUALSYSTEMSETTINGDATA CIM**](/previous-versions//cc136954(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="579c4-240">[**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="579c4-241">**MSVM \_ SummaryInformation**</span><span class="sxs-lookup"><span data-stu-id="579c4-241">**Msvm\_SummaryInformation**</span></span>](msvm-summaryinformation.md)
</dt> </dl>

 

