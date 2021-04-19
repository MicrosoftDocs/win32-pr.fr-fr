---
description: Représente un rapport de latitude/longitude.
ms.assetid: efa8d805-8546-4bab-95a0-69e1edc28753
title: LocationDisp. DispLatLongReport, objet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1b9629f22aee33670463b2a0832c12d520a9b8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535618"
---
# <a name="locationdispdisplatlongreport-object"></a><span data-ttu-id="7fe80-103">LocationDisp. DispLatLongReport, objet</span><span class="sxs-lookup"><span data-stu-id="7fe80-103">LocationDisp.DispLatLongReport object</span></span>

<span data-ttu-id="7fe80-104">\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="7fe80-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7fe80-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="7fe80-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="7fe80-106">Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7fe80-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="7fe80-107">Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="7fe80-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="7fe80-108">Représente un rapport de latitude/longitude.</span><span class="sxs-lookup"><span data-stu-id="7fe80-108">Represents a latitude/longitude report.</span></span>

## <a name="members"></a><span data-ttu-id="7fe80-109">Membres</span><span class="sxs-lookup"><span data-stu-id="7fe80-109">Members</span></span>

<span data-ttu-id="7fe80-110">L’objet **LocationDisp. DispLatLongReport** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7fe80-110">The **LocationDisp.DispLatLongReport** object has these types of members:</span></span>

-   [<span data-ttu-id="7fe80-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7fe80-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7fe80-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7fe80-112">Properties</span></span>

<span data-ttu-id="7fe80-113">L’objet **LocationDisp. DispLatLongReport** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="7fe80-113">The **LocationDisp.DispLatLongReport** object has these properties.</span></span>



| <span data-ttu-id="7fe80-114">Propriété</span><span class="sxs-lookup"><span data-stu-id="7fe80-114">Property</span></span>                                                                         | <span data-ttu-id="7fe80-115">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="7fe80-115">Access type</span></span>          | <span data-ttu-id="7fe80-116">Description</span><span class="sxs-lookup"><span data-stu-id="7fe80-116">Description</span></span>                                                                                                                                                                                       |
|:---------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7fe80-117">**Altitude**</span><span class="sxs-lookup"><span data-stu-id="7fe80-117">**Altitude**</span></span>](locationdisp-displatlongreport-altitude.md)<br/>           | <span data-ttu-id="7fe80-118">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fe80-118">Read-only</span></span><br/> | <span data-ttu-id="7fe80-119">Altitude actuelle, en mètres.</span><span class="sxs-lookup"><span data-stu-id="7fe80-119">Current altitude, in meters.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="7fe80-120">**AltitudeError**</span><span class="sxs-lookup"><span data-stu-id="7fe80-120">**AltitudeError**</span></span>](locationdisp-displatlongreport-altitudeerror.md)<br/> | <span data-ttu-id="7fe80-121">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fe80-121">Read-only</span></span><br/> | <span data-ttu-id="7fe80-122">Erreur d’altitude, en mètres.</span><span class="sxs-lookup"><span data-stu-id="7fe80-122">Altitude error, in meters.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="7fe80-123">**ErrorRadius**</span><span class="sxs-lookup"><span data-stu-id="7fe80-123">**ErrorRadius**</span></span>](locationdisp-displatlongreport-errorradius.md)<br/>     | <span data-ttu-id="7fe80-124">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fe80-124">Read-only</span></span><br/> | <span data-ttu-id="7fe80-125">Distance à partir de l’emplacement indiqué, en mètres.</span><span class="sxs-lookup"><span data-stu-id="7fe80-125">A distance from the reported location, in meters.</span></span> <span data-ttu-id="7fe80-126">Combiné avec l’emplacement signalé comme origine, ce rayon décrit le cercle dans lequel l’emplacement réel est proably.</span><span class="sxs-lookup"><span data-stu-id="7fe80-126">Combined with the reported location as the origin, this radius describes the circle in which the actual location is proably located.</span></span><br/> |
| [<span data-ttu-id="7fe80-127">**Latitude**</span><span class="sxs-lookup"><span data-stu-id="7fe80-127">**Latitude**</span></span>](locationdisp-displatlongreport-latitude.md)<br/>           | <span data-ttu-id="7fe80-128">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fe80-128">Read-only</span></span><br/> | <span data-ttu-id="7fe80-129">Latitude actuelle, en degrés.</span><span class="sxs-lookup"><span data-stu-id="7fe80-129">Current latitude, in degrees.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="7fe80-130">**Longitude**</span><span class="sxs-lookup"><span data-stu-id="7fe80-130">**Longitude**</span></span>](locationdisp-displatlongreport-longitude.md)<br/>         | <span data-ttu-id="7fe80-131">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fe80-131">Read-only</span></span><br/> | <span data-ttu-id="7fe80-132">Longitude actuelle, en degrés.</span><span class="sxs-lookup"><span data-stu-id="7fe80-132">Current longitude, in degrees.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="7fe80-133">**Timestamp**</span><span class="sxs-lookup"><span data-stu-id="7fe80-133">**Timestamp**</span></span>](locationdisp-displatlongreport-timestamp.md)<br/>         | <span data-ttu-id="7fe80-134">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fe80-134">Read-only</span></span><br/> | <span data-ttu-id="7fe80-135">Date et heure de génération du rapport.</span><span class="sxs-lookup"><span data-stu-id="7fe80-135">The date and time when the report was generated.</span></span><br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="7fe80-136">Notes</span><span class="sxs-lookup"><span data-stu-id="7fe80-136">Remarks</span></span>

<span data-ttu-id="7fe80-137">Vous pouvez récupérer cet objet via la propriété [**LatLongReport**](locationdisp-latlongreportfactory-latlongreport.md) de l’objet [**LatLongReportFactory**](locationdisp-latlongreportfactory.md) .</span><span class="sxs-lookup"><span data-stu-id="7fe80-137">You can retrieve this object through the [**LatLongReport**](locationdisp-latlongreportfactory-latlongreport.md) property of the [**LatLongReportFactory**](locationdisp-latlongreportfactory.md) object.</span></span> <span data-ttu-id="7fe80-138">Vous pouvez recevoir cet objet via l’événement [**NewLatLongReport**](newlatlongreport.md) .</span><span class="sxs-lookup"><span data-stu-id="7fe80-138">You can receive this object through the [**NewLatLongReport**](newlatlongreport.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fe80-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7fe80-139">Requirements</span></span>



| <span data-ttu-id="7fe80-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7fe80-140">Requirement</span></span> | <span data-ttu-id="7fe80-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="7fe80-141">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="7fe80-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7fe80-142">Minimum supported client</span></span><br/> | <span data-ttu-id="7fe80-143">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7fe80-143">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7fe80-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7fe80-144">Minimum supported server</span></span><br/> | <span data-ttu-id="7fe80-145">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7fe80-145">None supported</span></span><br/>                  |



 

