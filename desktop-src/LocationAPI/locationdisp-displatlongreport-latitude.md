---
description: Latitude actuelle, en degrés.
ms.assetid: 24a4e75c-5162-406a-bf34-471387bff5d9
title: Propriété LocationDisp. DispLatLongReport. Latitude
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Latitude
api_type:
- COM
api_location: ''
ms.openlocfilehash: ef7f1bb6e7441b4e007c972f43bb45f59236ebe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520128"
---
# <a name="locationdispdisplatlongreportlatitude-property"></a><span data-ttu-id="ef07a-103">Propriété LocationDisp. DispLatLongReport. Latitude</span><span class="sxs-lookup"><span data-stu-id="ef07a-103">LocationDisp.DispLatLongReport.Latitude property</span></span>

<span data-ttu-id="ef07a-104">\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="ef07a-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ef07a-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ef07a-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="ef07a-106">Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ef07a-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="ef07a-107">Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="ef07a-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="ef07a-108">Latitude actuelle, en degrés.</span><span class="sxs-lookup"><span data-stu-id="ef07a-108">Current latitude, in degrees.</span></span> <span data-ttu-id="ef07a-109">La latitude est comprise entre-90 et 90, où nord est positif.</span><span class="sxs-lookup"><span data-stu-id="ef07a-109">The latitude is between -90 and 90, where north is positive.</span></span>

<span data-ttu-id="ef07a-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ef07a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef07a-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef07a-111">Syntax</span></span>


```JScript
Latitude = LocationDisp.DispLatLongReport.Latitude
```



## <a name="property-value"></a><span data-ttu-id="ef07a-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ef07a-112">Property value</span></span>

<span data-ttu-id="ef07a-113">Cette propriété est un **nombre** en lecture seule (virgule flottante double précision).</span><span class="sxs-lookup"><span data-stu-id="ef07a-113">This property is a read-only **Number** (double precision floating point).</span></span>

## <a name="examples"></a><span data-ttu-id="ef07a-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="ef07a-114">Examples</span></span>

<span data-ttu-id="ef07a-115">Pour obtenir un exemple d’utilisation de cette propriété, consultez [un exemple de rapport LatLong simple](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="ef07a-115">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef07a-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef07a-116">Requirements</span></span>



| <span data-ttu-id="ef07a-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef07a-117">Requirement</span></span> | <span data-ttu-id="ef07a-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef07a-118">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="ef07a-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef07a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ef07a-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef07a-120">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ef07a-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef07a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ef07a-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef07a-122">None supported</span></span><br/>                  |



 

