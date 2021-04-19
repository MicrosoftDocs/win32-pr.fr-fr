---
description: Longitude actuelle, en degrés.
ms.assetid: f4fa1cbb-d682-42ab-9dd8-dff636ea4c8a
title: LocationDisp. DispLatLongReport. longitude, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Longitude
api_type:
- COM
api_location: ''
ms.openlocfilehash: c705ebd9476582f05b6dc87233dcc8e8990c5202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539747"
---
# <a name="locationdispdisplatlongreportlongitude-property"></a><span data-ttu-id="792d5-103">LocationDisp. DispLatLongReport. longitude, propriété</span><span class="sxs-lookup"><span data-stu-id="792d5-103">LocationDisp.DispLatLongReport.Longitude property</span></span>

<span data-ttu-id="792d5-104">\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="792d5-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="792d5-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="792d5-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="792d5-106">Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="792d5-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="792d5-107">Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="792d5-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="792d5-108">Longitude actuelle, en degrés.</span><span class="sxs-lookup"><span data-stu-id="792d5-108">Current longitude, in degrees.</span></span> <span data-ttu-id="792d5-109">La longitude est comprise entre-180 et 180, où est est positif.</span><span class="sxs-lookup"><span data-stu-id="792d5-109">The longitude is between -180 and 180, where east is positive.</span></span>

<span data-ttu-id="792d5-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="792d5-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="792d5-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="792d5-111">Syntax</span></span>


```JScript
Longitude = LocationDisp.DispLatLongReport.Longitude
```



## <a name="property-value"></a><span data-ttu-id="792d5-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="792d5-112">Property value</span></span>

<span data-ttu-id="792d5-113">Cette propriété est un **nombre** en lecture seule (virgule flottante double précision).</span><span class="sxs-lookup"><span data-stu-id="792d5-113">This property is a read-only **Number** (double precision floating point).</span></span>

## <a name="examples"></a><span data-ttu-id="792d5-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="792d5-114">Examples</span></span>

<span data-ttu-id="792d5-115">Pour obtenir un exemple d’utilisation de cette propriété, consultez [un exemple de rapport LatLong simple](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="792d5-115">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="792d5-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="792d5-116">Requirements</span></span>



| <span data-ttu-id="792d5-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="792d5-117">Requirement</span></span> | <span data-ttu-id="792d5-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="792d5-118">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="792d5-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="792d5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="792d5-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="792d5-120">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="792d5-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="792d5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="792d5-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="792d5-122">None supported</span></span><br/>                  |



 

