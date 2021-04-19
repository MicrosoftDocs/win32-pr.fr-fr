---
description: Distance à partir de l’emplacement indiqué, en mètres. Combiné avec l’emplacement signalé comme origine, ce rayon décrit le cercle dans lequel l’emplacement réel est probablement situé.
ms.assetid: a9565bd5-d1e0-45f8-abeb-3191b16480fa
title: LocationDisp. DispLatLongReport. ErrorRadius, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.ErrorRadius
api_type:
- COM
api_location: ''
ms.openlocfilehash: f99ff9b03451738158a98541bfae0e67a8827717
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106517902"
---
# <a name="locationdispdisplatlongreporterrorradius-property"></a><span data-ttu-id="676f4-104">LocationDisp. DispLatLongReport. ErrorRadius, propriété</span><span class="sxs-lookup"><span data-stu-id="676f4-104">LocationDisp.DispLatLongReport.ErrorRadius property</span></span>

<span data-ttu-id="676f4-105">\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="676f4-105">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="676f4-106">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="676f4-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="676f4-107">Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="676f4-107">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="676f4-108">Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="676f4-108">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="676f4-109">Distance à partir de l’emplacement indiqué, en mètres.</span><span class="sxs-lookup"><span data-stu-id="676f4-109">A distance from the reported location, in meters.</span></span> <span data-ttu-id="676f4-110">Combiné avec l’emplacement signalé comme origine, ce rayon décrit le cercle dans lequel l’emplacement réel est probablement situé.</span><span class="sxs-lookup"><span data-stu-id="676f4-110">Combined with the reported location as the origin, this radius describes the circle in which the actual location is probably located.</span></span>

<span data-ttu-id="676f4-111">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="676f4-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="676f4-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="676f4-112">Syntax</span></span>


```JScript
ErrorRadius = LocationDisp.DispLatLongReport.ErrorRadius
```



## <a name="property-value"></a><span data-ttu-id="676f4-113">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="676f4-113">Property value</span></span>

<span data-ttu-id="676f4-114">Cette propriété est un **nombre** en lecture seule (virgule flottante double précision).</span><span class="sxs-lookup"><span data-stu-id="676f4-114">This property is a read-only **Number** (double precision floating point).</span></span>

## <a name="examples"></a><span data-ttu-id="676f4-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="676f4-115">Examples</span></span>

<span data-ttu-id="676f4-116">Pour obtenir un exemple d’utilisation de cette propriété, consultez [un exemple de rapport LatLong simple](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="676f4-116">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="676f4-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="676f4-117">Requirements</span></span>



| <span data-ttu-id="676f4-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="676f4-118">Requirement</span></span> | <span data-ttu-id="676f4-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="676f4-119">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="676f4-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="676f4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="676f4-121">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="676f4-121">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="676f4-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="676f4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="676f4-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="676f4-123">None supported</span></span><br/>                  |



 

