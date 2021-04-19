---
description: Les qualificateurs suivants sont utilisés par le fournisseur WDM dans les fichiers MOF de pilote de périphérique lors de l’extraction de données à partir de WNODEs pour générer des instances de classes de pilote WDM.
ms.assetid: 11b0af59-979f-4908-baef-c9ec564b3cfd
ms.tgt_platform: multiple
title: Qualificateurs spécifiques du fournisseur WDM
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: be2bc4593c19555dd5a851de89a1dc2e5db00596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517730"
---
# <a name="qualifiers-specific-to-the-wdm-provider"></a><span data-ttu-id="9f458-103">Qualificateurs spécifiques du fournisseur WDM</span><span class="sxs-lookup"><span data-stu-id="9f458-103">Qualifiers Specific to the WDM Provider</span></span>

<span data-ttu-id="9f458-104">Les qualificateurs suivants sont utilisés par le [fournisseur WDM](/windows/desktop/WmiCoreProv/wdm-provider) dans les fichiers MOF de pilote de périphérique lors de l’extraction de données à partir de WNODEs pour générer des instances de classes de pilote WDM.</span><span class="sxs-lookup"><span data-stu-id="9f458-104">The following qualifiers are used by the [WDM Provider](/windows/desktop/WmiCoreProv/wdm-provider) in device driver MOF files when they are extracting data from WNODEs to generate instances of WDM driver classes.</span></span>

<dt>

<span data-ttu-id="9f458-105"><span id="MissingValue"></span><span id="missingvalue"></span><span id="MISSINGVALUE"></span>**MissingValue**</span><span class="sxs-lookup"><span data-stu-id="9f458-105"><span id="MissingValue"></span><span id="missingvalue"></span><span id="MISSINGVALUE"></span>**MissingValue**</span></span>
</dt> <dd>

<span data-ttu-id="9f458-106">Type de données : **DWORD, Array, UInt8, UInt16, UInt32, sint8, sint16 ou sint32.**</span><span class="sxs-lookup"><span data-stu-id="9f458-106">Data type: **DWORD, array, uint8, uint16, uint32, sint8, sint16, or sint32.**</span></span>

<span data-ttu-id="9f458-107">S’applique à : Properties</span><span class="sxs-lookup"><span data-stu-id="9f458-107">Applies to: properties</span></span>

<span data-ttu-id="9f458-108">Une valeur manquante pour cette propriété doit être représentée par **null** au lieu de 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="9f458-108">A missing value for this property should be represented by **NULL** rather than 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="9f458-109"><span id="WMIDataId"></span><span id="wmidataid"></span><span id="WMIDATAID"></span>**WMIDataId**</span><span class="sxs-lookup"><span data-stu-id="9f458-109"><span id="WMIDataId"></span><span id="wmidataid"></span><span id="WMIDATAID"></span>**WMIDataId**</span></span>
</dt> <dd>

<span data-ttu-id="9f458-110">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f458-110">Data type: **uint32**</span></span>

<span data-ttu-id="9f458-111">S’applique à : Properties</span><span class="sxs-lookup"><span data-stu-id="9f458-111">Applies to: properties</span></span>

<span data-ttu-id="9f458-112">Index dans le WNODE des données pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="9f458-112">Index in the WNODE of the data for the property.</span></span> <span data-ttu-id="9f458-113">Le fournisseur WDM utilise ce qualificateur pour déterminer comment les données sont formatées lors de l’extraction des données à partir de WNODE et de la génération de classes WMI.</span><span class="sxs-lookup"><span data-stu-id="9f458-113">The WDM provider uses this qualifier to determine how the data is formatted while extracting data from the WNODE and generating WMI classes.</span></span> <span data-ttu-id="9f458-114">La valeur de départ est 1.</span><span class="sxs-lookup"><span data-stu-id="9f458-114">The starting value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="9f458-115"><span id="WMIExpense"></span><span id="wmiexpense"></span><span id="WMIEXPENSE"></span>**WMIExpense**</span><span class="sxs-lookup"><span data-stu-id="9f458-115"><span id="WMIExpense"></span><span id="wmiexpense"></span><span id="WMIEXPENSE"></span>**WMIExpense**</span></span>
</dt> <dd>

<span data-ttu-id="9f458-116">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f458-116">Data type: **uint32**</span></span>

<span data-ttu-id="9f458-117">S’applique à : classes</span><span class="sxs-lookup"><span data-stu-id="9f458-117">Applies to: classes</span></span>

<span data-ttu-id="9f458-118">Indication du coût des ressources pour accéder au bloc de données.</span><span class="sxs-lookup"><span data-stu-id="9f458-118">Indication of the resource cost to access the data block.</span></span> <span data-ttu-id="9f458-119">Par exemple, les informations sur la géométrie du disque ne nécessitent pas beaucoup de ressources à obtenir, car elles sont disponibles dans l’extension de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9f458-119">For example, disk geometry information does not require a lot of resources to obtain because it is available in the device extension.</span></span> <span data-ttu-id="9f458-120">Les performances de lecture/écriture sur le disque sont plus gourmandes en ressources, car elles nécessitent un travail supplémentaire pour chaque opération de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="9f458-120">Disk read/write performance is more resource-intensive because it requires extra work on each read/write operation.</span></span> <span data-ttu-id="9f458-121">Par conséquent, la valeur du qualificateur **WMIExpense** est supérieure pour les performances de lecture/écriture sur le disque.</span><span class="sxs-lookup"><span data-stu-id="9f458-121">Therefore, the **WMIExpense** qualifier value is larger for disk read/write performance.</span></span>

</dd> <dt>

<span data-ttu-id="9f458-122"><span id="WMIMethodId"></span><span id="wmimethodid"></span><span id="WMIMETHODID"></span>**WMIMethodId**</span><span class="sxs-lookup"><span data-stu-id="9f458-122"><span id="WMIMethodId"></span><span id="wmimethodid"></span><span id="WMIMETHODID"></span>**WMIMethodId**</span></span>
</dt> <dd>

<span data-ttu-id="9f458-123">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f458-123">Data type: **uint32**</span></span>

<span data-ttu-id="9f458-124">S’applique à : méthodes</span><span class="sxs-lookup"><span data-stu-id="9f458-124">Applies to: methods</span></span>

<span data-ttu-id="9f458-125">Index dans le WNODE des données pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="9f458-125">Index in the WNODE of the data for the property.</span></span> <span data-ttu-id="9f458-126">Le fournisseur WDM utilise ce qualificateur pour déterminer comment les données sont formatées lors de l’extraction des données à partir de WNODE et de la génération de classes WMI.</span><span class="sxs-lookup"><span data-stu-id="9f458-126">The WDM provider uses this qualifier to determine how the data is formatted while extracting data from the WNODE and generating WMI classes.</span></span> <span data-ttu-id="9f458-127">La valeur de départ est 1.</span><span class="sxs-lookup"><span data-stu-id="9f458-127">The starting value is 1.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9f458-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9f458-128">Requirements</span></span>



| <span data-ttu-id="9f458-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f458-129">Requirement</span></span> | <span data-ttu-id="9f458-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f458-130">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="9f458-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f458-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9f458-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f458-132">Windows Vista</span></span><br/>       |
| <span data-ttu-id="9f458-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f458-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9f458-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f458-134">Windows Server 2008</span></span><br/> |



 

