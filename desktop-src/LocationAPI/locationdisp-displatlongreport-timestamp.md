---
description: 'Propriété LocationDisp. DispLatLongReport. Timestamp : date et heure de génération du rapport.'
ms.assetid: 3b8036aa-499c-4baf-bcc4-5b6c3f54eb7b
title: LocationDisp. DispLatLongReport. Timestamp, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Timestamp
api_type:
- COM
api_location: ''
ms.openlocfilehash: fd505f967bad31afa908609a72d108b17552fce8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105687"
---
# <a name="locationdispdisplatlongreporttimestamp-property"></a><span data-ttu-id="896a0-103">LocationDisp. DispLatLongReport. Timestamp, propriété</span><span class="sxs-lookup"><span data-stu-id="896a0-103">LocationDisp.DispLatLongReport.Timestamp property</span></span>

<span data-ttu-id="896a0-104">\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="896a0-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="896a0-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="896a0-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="896a0-106">Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="896a0-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="896a0-107">Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="896a0-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="896a0-108">Date et heure de génération du rapport.</span><span class="sxs-lookup"><span data-stu-id="896a0-108">The date and time when the report was generated.</span></span>

<span data-ttu-id="896a0-109">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="896a0-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="896a0-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="896a0-110">Syntax</span></span>


```JScript
Timestamp = LocationDisp.DispLatLongReport.Timestamp
```



## <a name="property-value"></a><span data-ttu-id="896a0-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="896a0-111">Property value</span></span>

<span data-ttu-id="896a0-112">Cette propriété est une **Date** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="896a0-112">This property is a read-only **Date**.</span></span> <span data-ttu-id="896a0-113">Les horodatages sont fournis comme temps universel coordonné (UTC, Universal Time Coordinated).</span><span class="sxs-lookup"><span data-stu-id="896a0-113">Time stamps are provided as Coordinated Universal Time (UTC).</span></span>

## <a name="remarks"></a><span data-ttu-id="896a0-114">Notes </span><span class="sxs-lookup"><span data-stu-id="896a0-114">Remarks</span></span>

<span data-ttu-id="896a0-115">Notez que les langages de script, tels que Microsoft JScript, peuvent vous obliger à effectuer des conversions dans d’autres formats d’heure lorsque vous affichez des horodatages sous forme de chaînes.</span><span class="sxs-lookup"><span data-stu-id="896a0-115">Note that scripting languages, such as Microsoft JScript, might require you to perform conversions to other time formats when you display time stamps as strings.</span></span>

## <a name="examples"></a><span data-ttu-id="896a0-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="896a0-116">Examples</span></span>

<span data-ttu-id="896a0-117">Pour obtenir un exemple d’utilisation de cette propriété, consultez [un exemple de rapport LatLong simple](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="896a0-117">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="896a0-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="896a0-118">Requirements</span></span>



| <span data-ttu-id="896a0-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="896a0-119">Requirement</span></span> | <span data-ttu-id="896a0-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="896a0-120">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="896a0-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="896a0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="896a0-122">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="896a0-122">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="896a0-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="896a0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="896a0-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="896a0-124">None supported</span></span><br/>                  |



 

