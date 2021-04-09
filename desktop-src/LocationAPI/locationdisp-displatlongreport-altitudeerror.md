---
description: Erreur d’altitude, en mètres.
ms.assetid: 36ebb079-26e6-4b3f-ad73-547a47bd23d7
title: LocationDisp. DispLatLongReport. AltitudeError, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.AltitudeError
api_type:
- COM
api_location: ''
ms.openlocfilehash: 92fd71b133912a57e6ed4ef034dda6fe92ef9b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866373"
---
# <a name="locationdispdisplatlongreportaltitudeerror-property"></a><span data-ttu-id="600a5-103">LocationDisp. DispLatLongReport. AltitudeError, propriété</span><span class="sxs-lookup"><span data-stu-id="600a5-103">LocationDisp.DispLatLongReport.AltitudeError property</span></span>

<span data-ttu-id="600a5-104">\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="600a5-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="600a5-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="600a5-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="600a5-106">Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="600a5-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="600a5-107">Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="600a5-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="600a5-108">Erreur d’altitude, en mètres.</span><span class="sxs-lookup"><span data-stu-id="600a5-108">Altitude error, in meters.</span></span>

<span data-ttu-id="600a5-109">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="600a5-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="600a5-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="600a5-110">Syntax</span></span>


```JScript
AltitudeError = LocationDisp.DispLatLongReport.AltitudeError
```



## <a name="property-value"></a><span data-ttu-id="600a5-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="600a5-111">Property value</span></span>

<span data-ttu-id="600a5-112">Cette propriété est un **nombre** en lecture seule (virgule flottante double précision).</span><span class="sxs-lookup"><span data-stu-id="600a5-112">This property is a read-only **Number** (double precision floating point).</span></span>

## <a name="remarks"></a><span data-ttu-id="600a5-113">Notes</span><span class="sxs-lookup"><span data-stu-id="600a5-113">Remarks</span></span>

<span data-ttu-id="600a5-114">Les capteurs d’emplacement ne sont pas requis pour fournir cette propriété.</span><span class="sxs-lookup"><span data-stu-id="600a5-114">Location sensors are not required to provide this property.</span></span> <span data-ttu-id="600a5-115">Vous devez gérer les exceptions lorsque vous tentez d’accéder à cette propriété.</span><span class="sxs-lookup"><span data-stu-id="600a5-115">You should handle exceptions when attempting to access this property.</span></span>

## <a name="examples"></a><span data-ttu-id="600a5-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="600a5-116">Examples</span></span>

<span data-ttu-id="600a5-117">Pour obtenir un exemple d’utilisation de cette propriété, consultez [un exemple de rapport LatLong simple](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="600a5-117">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="600a5-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="600a5-118">Requirements</span></span>



| <span data-ttu-id="600a5-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="600a5-119">Requirement</span></span> | <span data-ttu-id="600a5-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="600a5-120">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="600a5-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="600a5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="600a5-122">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="600a5-122">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="600a5-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="600a5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="600a5-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="600a5-124">None supported</span></span><br/>                  |



 

