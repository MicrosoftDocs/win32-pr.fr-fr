---
description: Altitude actuelle, en mètres. L’altitude est relative à la référence ellipsoïde.
ms.assetid: fbe9984c-aa9d-4ce0-9f8b-d79ca06764d4
title: LocationDisp. DispLatLongReport. altitude, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Altitude
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2004c8df6c61fb890bf8f71fb3c2b5446d71d79a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865478"
---
# <a name="locationdispdisplatlongreportaltitude-property"></a><span data-ttu-id="06bd2-104">LocationDisp. DispLatLongReport. altitude, propriété</span><span class="sxs-lookup"><span data-stu-id="06bd2-104">LocationDisp.DispLatLongReport.Altitude property</span></span>

<span data-ttu-id="06bd2-105">\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="06bd2-105">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="06bd2-106">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="06bd2-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="06bd2-107">Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="06bd2-107">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="06bd2-108">Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="06bd2-108">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="06bd2-109">Altitude actuelle, en mètres.</span><span class="sxs-lookup"><span data-stu-id="06bd2-109">Current altitude, in meters.</span></span> <span data-ttu-id="06bd2-110">L’altitude est relative à la référence ellipsoïde.</span><span class="sxs-lookup"><span data-stu-id="06bd2-110">Altitude is relative to the reference ellipsoid.</span></span>

<span data-ttu-id="06bd2-111">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="06bd2-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="06bd2-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06bd2-112">Syntax</span></span>


```JScript
Altitude = LocationDisp.DispLatLongReport.Altitude
```



## <a name="property-value"></a><span data-ttu-id="06bd2-113">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="06bd2-113">Property value</span></span>

<span data-ttu-id="06bd2-114">Cette propriété est un **nombre** en lecture seule (virgule flottante double précision).</span><span class="sxs-lookup"><span data-stu-id="06bd2-114">This property is a read-only **Number** (double precision floating point).</span></span>

## <a name="remarks"></a><span data-ttu-id="06bd2-115">Notes</span><span class="sxs-lookup"><span data-stu-id="06bd2-115">Remarks</span></span>

<span data-ttu-id="06bd2-116">Les capteurs d’emplacement ne sont pas requis pour fournir cette propriété.</span><span class="sxs-lookup"><span data-stu-id="06bd2-116">Location sensors are not required to provide this property.</span></span> <span data-ttu-id="06bd2-117">Vous devez gérer les exceptions lorsque vous tentez d’accéder à cette propriété.</span><span class="sxs-lookup"><span data-stu-id="06bd2-117">You should handle exceptions when attempting to access this property.</span></span>

<span data-ttu-id="06bd2-118">La méthode **altitude** récupère l’altitude relative à la ellipsoïde de référence qui est définie par la dernière révision du système géodésique universel (WGS 84), plutôt que l’altitude par rapport au niveau de la mer.</span><span class="sxs-lookup"><span data-stu-id="06bd2-118">The **Altitude** method retrieves the altitude relative to the reference ellipsoid that is defined by the latest revision of the World Geodetic System (WGS 84), rather than the altitude relative to sea level.</span></span>

## <a name="examples"></a><span data-ttu-id="06bd2-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="06bd2-119">Examples</span></span>

<span data-ttu-id="06bd2-120">Pour obtenir un exemple d’utilisation de cette propriété, consultez [un exemple de rapport LatLong simple](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="06bd2-120">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="06bd2-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06bd2-121">Requirements</span></span>



| <span data-ttu-id="06bd2-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06bd2-122">Requirement</span></span> | <span data-ttu-id="06bd2-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="06bd2-123">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="06bd2-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06bd2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="06bd2-125">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06bd2-125">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="06bd2-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06bd2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="06bd2-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="06bd2-127">None supported</span></span><br/>                  |



 

