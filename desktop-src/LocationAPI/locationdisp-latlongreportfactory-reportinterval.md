---
description: Intervalle d’événements de rapport Latitude/Longitude actuel en millisecondes.
ms.assetid: bb33c4c1-805d-4519-8363-b0221d420b36
title: LocationDisp. LatLongReportFactory. ReportInterval, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.ReportInterval
api_type:
- COM
api_location: ''
ms.openlocfilehash: b456f69a70655b22b1eca30e02d9d5369d19f38c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203410"
---
# <a name="locationdisplatlongreportfactoryreportinterval-property"></a><span data-ttu-id="f17f6-103">LocationDisp. LatLongReportFactory. ReportInterval, propriété</span><span class="sxs-lookup"><span data-stu-id="f17f6-103">LocationDisp.LatLongReportFactory.ReportInterval property</span></span>

<span data-ttu-id="f17f6-104">\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="f17f6-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f17f6-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="f17f6-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="f17f6-106">Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f17f6-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="f17f6-107">Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="f17f6-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="f17f6-108">Intervalle d’événements de rapport Latitude/Longitude actuel en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="f17f6-108">The current latitude/longitude report event interval in milliseconds.</span></span>

<span data-ttu-id="f17f6-109">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="f17f6-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f17f6-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f17f6-110">Syntax</span></span>


```JScript
ReportInterval = LocationDisp.LatLongReportFactory.ReportInterval
LocationDisp.LatLongReportFactory.ReportInterval = ReportInterval
```



## <a name="property-value"></a><span data-ttu-id="f17f6-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f17f6-111">Property value</span></span>

<span data-ttu-id="f17f6-112">Cette propriété est en lecture/écriture **ULong**.</span><span class="sxs-lookup"><span data-stu-id="f17f6-112">This property is a read/write **ULONG**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f17f6-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f17f6-113">Remarks</span></span>

<span data-ttu-id="f17f6-114">Cette valeur est une demande au fournisseur de localisation.</span><span class="sxs-lookup"><span data-stu-id="f17f6-114">This value is a request to the location provider.</span></span> <span data-ttu-id="f17f6-115">Le fournisseur d’emplacement n’est pas obligé de fournir des rapports à l’intervalle que vous demandez.</span><span class="sxs-lookup"><span data-stu-id="f17f6-115">The location provider is not required to provide reports at the interval that you request.</span></span> <span data-ttu-id="f17f6-116">Lisez la valeur de cette propriété pour découvrir le paramètre d’intervalle de rapport réel.</span><span class="sxs-lookup"><span data-stu-id="f17f6-116">Read the value of this property to discover the true report interval setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="f17f6-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f17f6-117">Requirements</span></span>



| <span data-ttu-id="f17f6-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f17f6-118">Requirement</span></span> | <span data-ttu-id="f17f6-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="f17f6-119">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="f17f6-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f17f6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f17f6-121">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f17f6-121">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f17f6-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f17f6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f17f6-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f17f6-123">None supported</span></span><br/>                  |



 

