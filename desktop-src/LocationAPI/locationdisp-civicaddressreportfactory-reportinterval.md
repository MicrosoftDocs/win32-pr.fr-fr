---
description: Intervalle d’événements de rapport d’adresse postale actuel, en millisecondes.
ms.assetid: 495dd8a1-4244-468f-b295-337b393aea8a
title: LocationDisp. CivicAddressReportFactory. ReportInterval, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.ReportInterval
api_type:
- COM
api_location: ''
ms.openlocfilehash: 47f7840be20ac640b5a8e7014f8401bc2350d328
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532297"
---
# <a name="locationdispcivicaddressreportfactoryreportinterval-property"></a><span data-ttu-id="3d14f-103">LocationDisp. CivicAddressReportFactory. ReportInterval, propriété</span><span class="sxs-lookup"><span data-stu-id="3d14f-103">LocationDisp.CivicAddressReportFactory.ReportInterval property</span></span>

<span data-ttu-id="3d14f-104">\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="3d14f-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3d14f-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d14f-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="3d14f-106">Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3d14f-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="3d14f-107">Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="3d14f-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="3d14f-108">Intervalle d’événements de rapport d’adresse postale actuel, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="3d14f-108">The current civic address report event interval in milliseconds.</span></span>

<span data-ttu-id="3d14f-109">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d14f-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d14f-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d14f-110">Syntax</span></span>


```JScript
ReportInterval = LocationDisp.CivicAddressReportFactory.ReportInterval
LocationDisp.CivicAddressReportFactory.ReportInterval = ReportInterval
```



## <a name="property-value"></a><span data-ttu-id="3d14f-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3d14f-111">Property value</span></span>

<span data-ttu-id="3d14f-112">Cette propriété est en lecture/écriture **ULong**.</span><span class="sxs-lookup"><span data-stu-id="3d14f-112">This property is a read/write **ULONG**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d14f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="3d14f-113">Remarks</span></span>

<span data-ttu-id="3d14f-114">Cette valeur est une demande pour le fournisseur de localisation.</span><span class="sxs-lookup"><span data-stu-id="3d14f-114">This value is a request for the location provider.</span></span> <span data-ttu-id="3d14f-115">Le fournisseur d’emplacement n’est pas obligé de fournir des rapports à l’intervalle que vous avez demandé.</span><span class="sxs-lookup"><span data-stu-id="3d14f-115">The location provider is not required to provide reports at the interval that you requested.</span></span> <span data-ttu-id="3d14f-116">Lisez la valeur de cette propriété pour découvrir le paramètre d’intervalle de rapport réel.</span><span class="sxs-lookup"><span data-stu-id="3d14f-116">Read the value of this property to discover the true report interval setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d14f-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d14f-117">Requirements</span></span>



| <span data-ttu-id="3d14f-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d14f-118">Requirement</span></span> | <span data-ttu-id="3d14f-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d14f-119">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="3d14f-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d14f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3d14f-121">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3d14f-121">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3d14f-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d14f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3d14f-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d14f-123">None supported</span></span><br/>                  |



 

