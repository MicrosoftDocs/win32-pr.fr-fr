---
description: Rapport de latitude/longitude actuel.
ms.assetid: d2bb305f-911e-46f7-abde-56e9fba9182b
title: LocationDisp. LatLongReportFactory. LatLongReport, propriété (Locationapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.LatLongReport
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: c44582c01685431e9b5dfa4820735728dd2a9cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203220"
---
# <a name="locationdisplatlongreportfactorylatlongreport-property"></a><span data-ttu-id="b42cb-103">LocationDisp. LatLongReportFactory. LatLongReport, propriété</span><span class="sxs-lookup"><span data-stu-id="b42cb-103">LocationDisp.LatLongReportFactory.LatLongReport property</span></span>

<span data-ttu-id="b42cb-104">\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="b42cb-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b42cb-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b42cb-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b42cb-106">Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b42cb-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="b42cb-107">Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="b42cb-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="b42cb-108">Rapport de latitude/longitude actuel.</span><span class="sxs-lookup"><span data-stu-id="b42cb-108">The current latitude/longitude report.</span></span>

<span data-ttu-id="b42cb-109">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b42cb-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b42cb-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b42cb-110">Syntax</span></span>


```JScript
objLatLongReport = LocationDisp.LatLongReportFactory.LatLongReport
```



## <a name="property-value"></a><span data-ttu-id="b42cb-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b42cb-111">Property value</span></span>

<span data-ttu-id="b42cb-112">Cette propriété est un [**LocationDisp. DispLatLongReport**](locationdisp-displatlongreport.md)en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b42cb-112">This property is a read-only [**LocationDisp.DispLatLongReport**](locationdisp-displatlongreport.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b42cb-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="b42cb-113">Examples</span></span>

<span data-ttu-id="b42cb-114">Pour obtenir un exemple d’utilisation de cette propriété, consultez [un exemple de rapport LatLong simple](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="b42cb-114">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="b42cb-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b42cb-115">Requirements</span></span>



| <span data-ttu-id="b42cb-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b42cb-116">Requirement</span></span> | <span data-ttu-id="b42cb-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b42cb-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b42cb-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b42cb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b42cb-119">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b42cb-119">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b42cb-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b42cb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b42cb-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b42cb-121">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b42cb-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="b42cb-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b42cb-123"><dt>Locationapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b42cb-123"><dt>Locationapi.h</dt></span></span> </dl> |



 

