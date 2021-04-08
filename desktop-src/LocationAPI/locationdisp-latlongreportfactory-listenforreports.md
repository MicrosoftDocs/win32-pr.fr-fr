---
description: Demande des événements de rapport Latitude/Longitude.
ms.assetid: c26a388b-e042-43da-a220-e3ecfcbd03a8
title: Méthode LocationDisp. LatLongReportFactory. ListenForReports (Locationapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.ListenForReports
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: 7e822595339fa499aaf469336ca3580acb2815bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757336"
---
# <a name="locationdisplatlongreportfactorylistenforreports-method"></a><span data-ttu-id="670bf-103">Méthode LocationDisp. LatLongReportFactory. ListenForReports</span><span class="sxs-lookup"><span data-stu-id="670bf-103">LocationDisp.LatLongReportFactory.ListenForReports method</span></span>

<span data-ttu-id="670bf-104">\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="670bf-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="670bf-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="670bf-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="670bf-106">Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="670bf-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="670bf-107">Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="670bf-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="670bf-108">Demande des événements de rapport Latitude/Longitude.</span><span class="sxs-lookup"><span data-stu-id="670bf-108">Requests latitude/longitude report events.</span></span>

## <a name="syntax"></a><span data-ttu-id="670bf-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="670bf-109">Syntax</span></span>


```JScript
LocationDisp.LatLongReportFactory.ListenForReports(
  requestedReportInterval
)
```



## <a name="parameters"></a><span data-ttu-id="670bf-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="670bf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="670bf-111">*requestedReportInterval*</span><span class="sxs-lookup"><span data-stu-id="670bf-111">*requestedReportInterval*</span></span> 
</dt> <dd> <span data-ttu-id="670bf-112">Nombre (**double mot**) représentant le délai demandé entre les événements de rapport Latitude/Longitude, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="670bf-112">Number (**double word**) representing the requested time between latitude/longitude report events, in milliseconds.</span></span> <span data-ttu-id="670bf-113">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="670bf-113">See Remarks.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="670bf-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="670bf-114">Return value</span></span>

<span data-ttu-id="670bf-115">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="670bf-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="670bf-116">Notes</span><span class="sxs-lookup"><span data-stu-id="670bf-116">Remarks</span></span>

<span data-ttu-id="670bf-117">Le fournisseur d’emplacement n’est pas obligé de fournir des rapports à l’intervalle que vous demandez.</span><span class="sxs-lookup"><span data-stu-id="670bf-117">The location provider is not required to provide reports at the interval that you request.</span></span> <span data-ttu-id="670bf-118">Lisez la valeur de la propriété [**ReportInterval**](locationdisp-latlongreportfactory-reportinterval.md) pour découvrir le paramètre d’intervalle de rapport réel.</span><span class="sxs-lookup"><span data-stu-id="670bf-118">Read the value of the [**ReportInterval**](locationdisp-latlongreportfactory-reportinterval.md) property to discover the true report interval setting.</span></span>

## <a name="examples"></a><span data-ttu-id="670bf-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="670bf-119">Examples</span></span>

<span data-ttu-id="670bf-120">Pour obtenir un exemple d’utilisation de cette méthode, consultez [écoute des événements de rapport LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="670bf-120">For an example of how to use this method, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="670bf-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="670bf-121">Requirements</span></span>



| <span data-ttu-id="670bf-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="670bf-122">Requirement</span></span> | <span data-ttu-id="670bf-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="670bf-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="670bf-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="670bf-124">Minimum supported client</span></span><br/> | <span data-ttu-id="670bf-125">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="670bf-125">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="670bf-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="670bf-126">Minimum supported server</span></span><br/> | <span data-ttu-id="670bf-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="670bf-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="670bf-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="670bf-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="670bf-129"><dt>Locationapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="670bf-129"><dt>Locationapi.h</dt></span></span> </dl> |



 

