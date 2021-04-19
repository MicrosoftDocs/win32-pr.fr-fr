---
description: Représente un rapport d’adresse postale.
ms.assetid: 7c6e790f-0150-4ea8-9583-df633ebf035d
title: LocationDisp. DispCivicAddressReport, objet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispCivicAddressReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2a2a96f3d0c2a1fe8e3ac78e5db67ded031a4aa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529261"
---
# <a name="locationdispdispcivicaddressreport-object"></a><span data-ttu-id="3662d-103">LocationDisp. DispCivicAddressReport, objet</span><span class="sxs-lookup"><span data-stu-id="3662d-103">LocationDisp.DispCivicAddressReport object</span></span>

<span data-ttu-id="3662d-104">\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="3662d-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3662d-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3662d-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="3662d-106">Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3662d-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="3662d-107">Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="3662d-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="3662d-108">Représente un rapport d’adresse postale.</span><span class="sxs-lookup"><span data-stu-id="3662d-108">Represents a civic address report.</span></span>

## <a name="members"></a><span data-ttu-id="3662d-109">Membres</span><span class="sxs-lookup"><span data-stu-id="3662d-109">Members</span></span>

<span data-ttu-id="3662d-110">L’objet **LocationDisp. DispCivicAddressReport** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3662d-110">The **LocationDisp.DispCivicAddressReport** object has these types of members:</span></span>

-   [<span data-ttu-id="3662d-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3662d-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3662d-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3662d-112">Properties</span></span>

<span data-ttu-id="3662d-113">L’objet **LocationDisp. DispCivicAddressReport** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="3662d-113">The **LocationDisp.DispCivicAddressReport** object has these properties.</span></span>



| <span data-ttu-id="3662d-114">Propriété</span><span class="sxs-lookup"><span data-stu-id="3662d-114">Property</span></span>                                                                              | <span data-ttu-id="3662d-115">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="3662d-115">Access type</span></span>          | <span data-ttu-id="3662d-116">Description</span><span class="sxs-lookup"><span data-stu-id="3662d-116">Description</span></span>                                                 |
|:--------------------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------|
| [<span data-ttu-id="3662d-117">**AddressLine1**</span><span class="sxs-lookup"><span data-stu-id="3662d-117">**AddressLine1**</span></span>](locationdisp-dispcivicaddressreport-addressline1.md)<br/>   | <span data-ttu-id="3662d-118">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3662d-118">Read-only</span></span><br/> | <span data-ttu-id="3662d-119">Première ligne d’une adresse postale.</span><span class="sxs-lookup"><span data-stu-id="3662d-119">The first line of a street address.</span></span><br/>              |
| [<span data-ttu-id="3662d-120">**AddressLine2**</span><span class="sxs-lookup"><span data-stu-id="3662d-120">**AddressLine2**</span></span>](locationdisp-dispcivicaddressreport-addressline2.md)<br/>   | <span data-ttu-id="3662d-121">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3662d-121">Read-only</span></span><br/> | <span data-ttu-id="3662d-122">Deuxième ligne d’une adresse postale.</span><span class="sxs-lookup"><span data-stu-id="3662d-122">The second line of a street address.</span></span><br/>             |
| [<span data-ttu-id="3662d-123">**Urbain**</span><span class="sxs-lookup"><span data-stu-id="3662d-123">**City**</span></span>](locationdisp-dispcivicaddressreport-city.md)<br/>                   | <span data-ttu-id="3662d-124">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3662d-124">Read-only</span></span><br/> | <span data-ttu-id="3662d-125">Nom de la ville.</span><span class="sxs-lookup"><span data-stu-id="3662d-125">The city name.</span></span><br/>                                   |
| [<span data-ttu-id="3662d-126">**Pays**</span><span class="sxs-lookup"><span data-stu-id="3662d-126">**CountryRegion**</span></span>](locationdisp-civicaddressreport-countryregion.md)<br/>     | <span data-ttu-id="3662d-127">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3662d-127">Read-only</span></span><br/> | <span data-ttu-id="3662d-128">Nom du pays ou de la région.</span><span class="sxs-lookup"><span data-stu-id="3662d-128">The country or region name.</span></span><br/>                      |
| [<span data-ttu-id="3662d-129">**DetailLevel**</span><span class="sxs-lookup"><span data-stu-id="3662d-129">**DetailLevel**</span></span>](locationdisp-dispcivicaddressreport-detaillevel.md)<br/>     | <span data-ttu-id="3662d-130">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3662d-130">Read-only</span></span><br/> | <span data-ttu-id="3662d-131">Niveau de détail du rapport.</span><span class="sxs-lookup"><span data-stu-id="3662d-131">The detail level for the report.</span></span><br/>                 |
| [<span data-ttu-id="3662d-132">**Postal**</span><span class="sxs-lookup"><span data-stu-id="3662d-132">**PostalCode**</span></span>](locationdisp-dispcivicaddressreport-postalcode.md)<br/>       | <span data-ttu-id="3662d-133">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3662d-133">Read-only</span></span><br/> | <span data-ttu-id="3662d-134">Le code postal.</span><span class="sxs-lookup"><span data-stu-id="3662d-134">The postal code.</span></span><br/>                                 |
| [<span data-ttu-id="3662d-135">**StateProvince**</span><span class="sxs-lookup"><span data-stu-id="3662d-135">**StateProvince**</span></span>](locationdisp-dispcivicaddressreport-stateprovince.md)<br/> | <span data-ttu-id="3662d-136">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3662d-136">Read-only</span></span><br/> | <span data-ttu-id="3662d-137">Nom de l’État ou de la province.</span><span class="sxs-lookup"><span data-stu-id="3662d-137">The state or province name.</span></span><br/>                      |
| [<span data-ttu-id="3662d-138">**Timestamp**</span><span class="sxs-lookup"><span data-stu-id="3662d-138">**Timestamp**</span></span>](locationdisp-dispcivicaddressreport-timestamp.md)<br/>         | <span data-ttu-id="3662d-139">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3662d-139">Read-only</span></span><br/> | <span data-ttu-id="3662d-140">Date et heure de génération du rapport.</span><span class="sxs-lookup"><span data-stu-id="3662d-140">The date and time when the report was generated.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3662d-141">Notes</span><span class="sxs-lookup"><span data-stu-id="3662d-141">Remarks</span></span>

<span data-ttu-id="3662d-142">Vous pouvez récupérer cet objet via la propriété [**CivicAddressReport**](locationdisp-dispcivicaddressreport-civicaddressreport.md) d’un objet [**CivicAddressReportFactory**](locationdisp-civicaddressreportfactory.md) .</span><span class="sxs-lookup"><span data-stu-id="3662d-142">You can retrieve this object through the [**CivicAddressReport**](locationdisp-dispcivicaddressreport-civicaddressreport.md) property of a [**CivicAddressReportFactory**](locationdisp-civicaddressreportfactory.md) object.</span></span> <span data-ttu-id="3662d-143">Vous pouvez recevoir cet objet via l’événement [**NewCivicAddressReport**](newcivicaddressreport.md) .</span><span class="sxs-lookup"><span data-stu-id="3662d-143">You can receive this object through the [**NewCivicAddressReport**](newcivicaddressreport.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="3662d-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3662d-144">Requirements</span></span>



| <span data-ttu-id="3662d-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3662d-145">Requirement</span></span> | <span data-ttu-id="3662d-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="3662d-146">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="3662d-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3662d-147">Minimum supported client</span></span><br/> | <span data-ttu-id="3662d-148">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3662d-148">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3662d-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3662d-149">Minimum supported server</span></span><br/> | <span data-ttu-id="3662d-150">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3662d-150">None supported</span></span><br/>                  |



 

