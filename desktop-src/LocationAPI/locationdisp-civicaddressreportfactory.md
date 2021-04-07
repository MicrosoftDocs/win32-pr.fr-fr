---
description: Gère les rapports d’adresse postale.
ms.assetid: 46c2d001-409a-4a0a-9006-1c2c9d327c13
title: LocationDisp. CivicAddressReportFactory, objet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 451bb21822d1b56e4c7a45f1587df04761b67690
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758278"
---
# <a name="locationdispcivicaddressreportfactory-object"></a><span data-ttu-id="7d274-103">LocationDisp. CivicAddressReportFactory, objet</span><span class="sxs-lookup"><span data-stu-id="7d274-103">LocationDisp.CivicAddressReportFactory object</span></span>

<span data-ttu-id="7d274-104">\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="7d274-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7d274-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="7d274-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="7d274-106">Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7d274-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="7d274-107">Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="7d274-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="7d274-108">Gère les rapports d’adresse postale.</span><span class="sxs-lookup"><span data-stu-id="7d274-108">Manages civic address reports.</span></span>

## <a name="members"></a><span data-ttu-id="7d274-109">Membres</span><span class="sxs-lookup"><span data-stu-id="7d274-109">Members</span></span>

<span data-ttu-id="7d274-110">L’objet **LocationDisp. CivicAddressReportFactory** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7d274-110">The **LocationDisp.CivicAddressReportFactory** object has these types of members:</span></span>

-   [<span data-ttu-id="7d274-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7d274-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="7d274-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7d274-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7d274-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7d274-113">Methods</span></span>

<span data-ttu-id="7d274-114">L’objet **LocationDisp. CivicAddressReportFactory** possède les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="7d274-114">The **LocationDisp.CivicAddressReportFactory** object has these methods.</span></span>



| <span data-ttu-id="7d274-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="7d274-115">Method</span></span>                                                                                            | <span data-ttu-id="7d274-116">Description</span><span class="sxs-lookup"><span data-stu-id="7d274-116">Description</span></span>                                                                                   |
|:--------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7d274-117">**ListenForReports**</span><span class="sxs-lookup"><span data-stu-id="7d274-117">**ListenForReports**</span></span>](locationdisp-civicaddressreportfactory-listenforreports.md)               | <span data-ttu-id="7d274-118">Demande les événements de rapport d’adresse postale.</span><span class="sxs-lookup"><span data-stu-id="7d274-118">Requests civic address report events.</span></span><br/>                                              |
| [<span data-ttu-id="7d274-119">**RequestPermissions**</span><span class="sxs-lookup"><span data-stu-id="7d274-119">**RequestPermissions**</span></span>](locationdisp-civicaddressreportfactory-requestpermissions.md)           | <span data-ttu-id="7d274-120">Ouvre une boîte de dialogue système pour demander l’autorisation de l’utilisateur pour les périphériques avec emplacement.</span><span class="sxs-lookup"><span data-stu-id="7d274-120">Opens a system dialog box to request user permission for location-enabled devices.</span></span><br/> |
| [<span data-ttu-id="7d274-121">**StopListeningForReports**</span><span class="sxs-lookup"><span data-stu-id="7d274-121">**StopListeningForReports**</span></span>](locationdisp-civicaddressreportfactory-stoplisteningforreports.md) | <span data-ttu-id="7d274-122">Annule les demandes d’événements de rapport d’adresse postale.</span><span class="sxs-lookup"><span data-stu-id="7d274-122">Cancels civic address report event requests.</span></span><br/>                                       |



 

### <a name="properties"></a><span data-ttu-id="7d274-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7d274-123">Properties</span></span>

<span data-ttu-id="7d274-124">L’objet **LocationDisp. CivicAddressReportFactory** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="7d274-124">The **LocationDisp.CivicAddressReportFactory** object has these properties.</span></span>



| <span data-ttu-id="7d274-125">Propriété</span><span class="sxs-lookup"><span data-stu-id="7d274-125">Property</span></span>                                                                                        | <span data-ttu-id="7d274-126">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="7d274-126">Access type</span></span>           | <span data-ttu-id="7d274-127">Description</span><span class="sxs-lookup"><span data-stu-id="7d274-127">Description</span></span>                                                                                                |
|:------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7d274-128">**CivicAddressReport**</span><span class="sxs-lookup"><span data-stu-id="7d274-128">**CivicAddressReport**</span></span>](locationdisp-dispcivicaddressreport-civicaddressreport.md)<br/> | <span data-ttu-id="7d274-129">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7d274-129">Read-only</span></span><br/>  | <span data-ttu-id="7d274-130">[**LocationDisp. DispCivicAddressReport**](locationdisp-dispcivicaddressreport.md)actuel.</span><span class="sxs-lookup"><span data-stu-id="7d274-130">The current [**LocationDisp.DispCivicAddressReport**](locationdisp-dispcivicaddressreport.md).</span></span><br/> |
| [<span data-ttu-id="7d274-131">**DesiredAccuracy**</span><span class="sxs-lookup"><span data-stu-id="7d274-131">**DesiredAccuracy**</span></span>](locationdisp-civicaddressreportfactory-desiredaccuracy.md)<br/>    | <span data-ttu-id="7d274-132">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7d274-132">Read/write</span></span><br/> | <span data-ttu-id="7d274-133">Paramètre de précision souhaité.</span><span class="sxs-lookup"><span data-stu-id="7d274-133">The current desired-accuracy setting.</span></span><br/>                                                           |
| [<span data-ttu-id="7d274-134">**ReportInterval**</span><span class="sxs-lookup"><span data-stu-id="7d274-134">**ReportInterval**</span></span>](locationdisp-civicaddressreportfactory-reportinterval.md)<br/>      | <span data-ttu-id="7d274-135">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7d274-135">Read/write</span></span><br/> | <span data-ttu-id="7d274-136">Intervalle d’événements de rapport d’adresse postale actuel, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="7d274-136">The current civic address report event interval in milliseconds.</span></span><br/>                                |
| [<span data-ttu-id="7d274-137">**Statu**</span><span class="sxs-lookup"><span data-stu-id="7d274-137">**Status**</span></span>](locationdisp-civicaddressreportfactory-status.md)<br/>                      | <span data-ttu-id="7d274-138">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7d274-138">Read-only</span></span><br/>  | <span data-ttu-id="7d274-139">État actuel du rapport.</span><span class="sxs-lookup"><span data-stu-id="7d274-139">The current report status.</span></span><br/>                                                                      |



 

## <a name="examples"></a><span data-ttu-id="7d274-140">Exemples</span><span class="sxs-lookup"><span data-stu-id="7d274-140">Examples</span></span>

<span data-ttu-id="7d274-141">L’exemple de code suivant montre comment créer cet objet dans du code HTML.</span><span class="sxs-lookup"><span data-stu-id="7d274-141">The following example code shows how to create this object in HTML code.</span></span>


```Text
<object id="civicfactory" 
    classid="clsid:2A11F42C-3E81-4ad4-9CBE-45579D89671A"
    type="application/x-oleobject">
</object>
```



<span data-ttu-id="7d274-142">L’exemple de code suivant montre comment créer cet objet dans JScript à l’aide de Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="7d274-142">The following example code shows how to create this object in JScript using Windows Script Host.</span></span>


```JScript
var civicfactory = WScript.CreateObject("LocationDisp.CivicAddressReportFactory");
```



<span data-ttu-id="7d274-143">L’exemple de code suivant montre comment créer cet objet dans VBScript à l’aide de Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="7d274-143">The following example code shows how to create this object in VBScript using Windows Script Host.</span></span>


```VB
Dim civicfactory
Set civicfactory = WScript.CreateObject("LocationDisp.CivicAddressReportFactory")
```



## <a name="requirements"></a><span data-ttu-id="7d274-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7d274-144">Requirements</span></span>



| <span data-ttu-id="7d274-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7d274-145">Requirement</span></span> | <span data-ttu-id="7d274-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d274-146">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="7d274-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d274-147">Minimum supported client</span></span><br/> | <span data-ttu-id="7d274-148">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7d274-148">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7d274-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d274-149">Minimum supported server</span></span><br/> | <span data-ttu-id="7d274-150">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d274-150">None supported</span></span><br/>                  |



## <a name="see-also"></a><span data-ttu-id="7d274-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d274-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d274-152">**LocationDisp.CivicAddressReport**</span><span class="sxs-lookup"><span data-stu-id="7d274-152">**LocationDisp.CivicAddressReport**</span></span>](locationdisp-dispcivicaddressreport.md)
</dt> </dl>

 

