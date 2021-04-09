---
description: Gère les rapports de latitude/longitude.
ms.assetid: 66025874-32dd-4494-a9ad-12fe3afa60f9
title: LocationDisp. LatLongReportFactory, objet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9fad1ca0f4605f1167f9b86b0df5bc8f20e46285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868893"
---
# <a name="locationdisplatlongreportfactory-object"></a><span data-ttu-id="a8fe1-103">LocationDisp. LatLongReportFactory, objet</span><span class="sxs-lookup"><span data-stu-id="a8fe1-103">LocationDisp.LatLongReportFactory object</span></span>

<span data-ttu-id="a8fe1-104">\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="a8fe1-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a8fe1-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a8fe1-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a8fe1-106">Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a8fe1-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="a8fe1-107">Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="a8fe1-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="a8fe1-108">Gère les rapports de latitude/longitude.</span><span class="sxs-lookup"><span data-stu-id="a8fe1-108">Manages latitude/longitude reports.</span></span>

## <a name="members"></a><span data-ttu-id="a8fe1-109">Membres</span><span class="sxs-lookup"><span data-stu-id="a8fe1-109">Members</span></span>

<span data-ttu-id="a8fe1-110">L’objet **LocationDisp. LatLongReportFactory** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a8fe1-110">The **LocationDisp.LatLongReportFactory** object has these types of members:</span></span>

-   [<span data-ttu-id="a8fe1-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a8fe1-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="a8fe1-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a8fe1-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a8fe1-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a8fe1-113">Methods</span></span>

<span data-ttu-id="a8fe1-114">L’objet **LocationDisp. LatLongReportFactory** possède les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="a8fe1-114">The **LocationDisp.LatLongReportFactory** object has these methods.</span></span>



| <span data-ttu-id="a8fe1-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="a8fe1-115">Method</span></span>                                                                                       | <span data-ttu-id="a8fe1-116">Description</span><span class="sxs-lookup"><span data-stu-id="a8fe1-116">Description</span></span>                                                                                   |
|:---------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8fe1-117">**ListenForReports**</span><span class="sxs-lookup"><span data-stu-id="a8fe1-117">**ListenForReports**</span></span>](locationdisp-latlongreportfactory-listenforreports.md)               | <span data-ttu-id="a8fe1-118">Demande des événements de rapport Latitude/Longitude.</span><span class="sxs-lookup"><span data-stu-id="a8fe1-118">Requests latitude/longitude report events.</span></span><br/>                                         |
| [<span data-ttu-id="a8fe1-119">**RequestPermissions**</span><span class="sxs-lookup"><span data-stu-id="a8fe1-119">**RequestPermissions**</span></span>](locationdisp-latlongreportfactory-requestpermissions.md)           | <span data-ttu-id="a8fe1-120">Ouvre une boîte de dialogue système pour demander l’autorisation de l’utilisateur pour les périphériques avec emplacement.</span><span class="sxs-lookup"><span data-stu-id="a8fe1-120">Opens a system dialog box to request user permission for location-enabled devices.</span></span><br/> |
| <span data-ttu-id="a8fe1-121">[**StopListeningForReports**](/previous-versions/windows/desktop/legacy/dd317718(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a8fe1-121">[**StopListeningForReports**](/previous-versions/windows/desktop/legacy/dd317718(v=vs.85))</span></span> | <span data-ttu-id="a8fe1-122">Annule les demandes d’événements de rapport Latitude/Longitude.</span><span class="sxs-lookup"><span data-stu-id="a8fe1-122">Cancels requests for latitude/longitude report events.</span></span><br/>                             |



 

### <a name="properties"></a><span data-ttu-id="a8fe1-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a8fe1-123">Properties</span></span>

<span data-ttu-id="a8fe1-124">L’objet **LocationDisp. LatLongReportFactory** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="a8fe1-124">The **LocationDisp.LatLongReportFactory** object has these properties.</span></span>



| <span data-ttu-id="a8fe1-125">Propriété</span><span class="sxs-lookup"><span data-stu-id="a8fe1-125">Property</span></span>                                                                                | <span data-ttu-id="a8fe1-126">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="a8fe1-126">Access type</span></span>           | <span data-ttu-id="a8fe1-127">Description</span><span class="sxs-lookup"><span data-stu-id="a8fe1-127">Description</span></span>                                                                                      |
|:----------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8fe1-128">**DesiredAccuracy**</span><span class="sxs-lookup"><span data-stu-id="a8fe1-128">**DesiredAccuracy**</span></span>](locationdisp-latlongreportfactory-desiredaccuracy.md)<br/> | <span data-ttu-id="a8fe1-129">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a8fe1-129">Read/write</span></span><br/> | <span data-ttu-id="a8fe1-130">Valeur actuelle de précision souhaitée.</span><span class="sxs-lookup"><span data-stu-id="a8fe1-130">The current desired-accuracy value.</span></span><br/>                                                   |
| [<span data-ttu-id="a8fe1-131">**LatLongReport**</span><span class="sxs-lookup"><span data-stu-id="a8fe1-131">**LatLongReport**</span></span>](locationdisp-latlongreportfactory-latlongreport.md)<br/>     | <span data-ttu-id="a8fe1-132">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a8fe1-132">Read-only</span></span><br/>  | <span data-ttu-id="a8fe1-133">[**LocationDisp. DispLatLongReport**](locationdisp-displatlongreport.md)actuel.</span><span class="sxs-lookup"><span data-stu-id="a8fe1-133">The current [**LocationDisp.DispLatLongReport**](locationdisp-displatlongreport.md).</span></span><br/> |
| [<span data-ttu-id="a8fe1-134">**ReportInterval**</span><span class="sxs-lookup"><span data-stu-id="a8fe1-134">**ReportInterval**</span></span>](locationdisp-latlongreportfactory-reportinterval.md)<br/>   | <span data-ttu-id="a8fe1-135">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a8fe1-135">Read/write</span></span><br/> | <span data-ttu-id="a8fe1-136">Intervalle d’événements de rapport Latitude/Longitude actuel en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="a8fe1-136">The current latitude/longitude report event interval in milliseconds.</span></span><br/>                 |
| [<span data-ttu-id="a8fe1-137">**Statu**</span><span class="sxs-lookup"><span data-stu-id="a8fe1-137">**Status**</span></span>](locationdisp-latlongreportfactory-status.md)<br/>                   | <span data-ttu-id="a8fe1-138">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a8fe1-138">Read-only</span></span><br/>  | <span data-ttu-id="a8fe1-139">État actuel du rapport.</span><span class="sxs-lookup"><span data-stu-id="a8fe1-139">The current report status.</span></span><br/>                                                            |



 

## <a name="examples"></a><span data-ttu-id="a8fe1-140">Exemples</span><span class="sxs-lookup"><span data-stu-id="a8fe1-140">Examples</span></span>

<span data-ttu-id="a8fe1-141">L’exemple de code suivant montre comment créer cet objet dans du code HTML.</span><span class="sxs-lookup"><span data-stu-id="a8fe1-141">The following example code shows how to create this object in HTML code.</span></span>


```
<object id="latlongfactory" 
    classid="clsid:9DCC3CC8-8609-4863-BAD4-03601F4C65E8"
    type="application/x-oleobject">
</object>
```



<span data-ttu-id="a8fe1-142">L’exemple de code suivant montre comment créer cet objet dans JScript à l’aide de Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="a8fe1-142">The following example code shows how to create this object in JScript using Windows Script Host.</span></span>


```JScript
var latlongfactory = WScript.CreateObject("LocationDisp.LatLongReportFactory");
```



<span data-ttu-id="a8fe1-143">L’exemple de code suivant montre comment créer cet objet dans VBScript à l’aide de Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="a8fe1-143">The following example code shows how to create this object in VBScript using Windows Script Host.</span></span>


```VB
Dim latlongfactory
Set latlongfactory = WScript.CreateObject("LocationDisp.LatLongReportFactory")
```



## <a name="requirements"></a><span data-ttu-id="a8fe1-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8fe1-144">Requirements</span></span>



| <span data-ttu-id="a8fe1-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8fe1-145">Requirement</span></span> | <span data-ttu-id="a8fe1-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8fe1-146">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="a8fe1-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8fe1-147">Minimum supported client</span></span><br/> | <span data-ttu-id="a8fe1-148">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8fe1-148">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a8fe1-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8fe1-149">Minimum supported server</span></span><br/> | <span data-ttu-id="a8fe1-150">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8fe1-150">None supported</span></span><br/>                  |



## <a name="see-also"></a><span data-ttu-id="a8fe1-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8fe1-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8fe1-152">**LocationDisp.DispLatLongReport**</span><span class="sxs-lookup"><span data-stu-id="a8fe1-152">**LocationDisp.DispLatLongReport**</span></span>](locationdisp-displatlongreport.md)
</dt> </dl>

 

