---
description: État actuel du rapport.
ms.assetid: bcdf76b5-88c4-481a-89ac-2b9558cecfc0
title: LocationDisp. LatLongReportFactory. Status, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.Status
api_type:
- COM
api_location: ''
ms.openlocfilehash: c32f1e58c5c519bdbdf797f81f11a449bfb3dc1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319389"
---
# <a name="locationdisplatlongreportfactorystatus-property"></a><span data-ttu-id="88f13-103">LocationDisp. LatLongReportFactory. Status, propriété</span><span class="sxs-lookup"><span data-stu-id="88f13-103">LocationDisp.LatLongReportFactory.Status property</span></span>

<span data-ttu-id="88f13-104">\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="88f13-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="88f13-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="88f13-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="88f13-106">Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="88f13-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="88f13-107">Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="88f13-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="88f13-108">État actuel du rapport.</span><span class="sxs-lookup"><span data-stu-id="88f13-108">The current report status.</span></span>

<span data-ttu-id="88f13-109">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="88f13-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="88f13-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88f13-110">Syntax</span></span>


```JScript
Status = LocationDisp.LatLongReportFactory.Status
```



## <a name="property-value"></a><span data-ttu-id="88f13-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="88f13-111">Property value</span></span>

<span data-ttu-id="88f13-112">Cette propriété est un **nombre** en lecture seule (unsigned long).</span><span class="sxs-lookup"><span data-stu-id="88f13-112">This property is a read-only **Number** (unsigned long).</span></span>



| <span data-ttu-id="88f13-113">Statut</span><span class="sxs-lookup"><span data-stu-id="88f13-113">Status</span></span>                                                                                               | <span data-ttu-id="88f13-114">Signification</span><span class="sxs-lookup"><span data-stu-id="88f13-114">Meaning</span></span>                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="88f13-115"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="88f13-115"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="88f13-116">Rapport non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="88f13-116">Report not supported.</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="88f13-117"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="88f13-117"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="88f13-118">Erreur.</span><span class="sxs-lookup"><span data-stu-id="88f13-118">Error.</span></span><br/>                |
| <span id="2"></span><dl> <span data-ttu-id="88f13-119"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="88f13-119"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="88f13-120">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="88f13-120">Access denied.</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="88f13-121"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="88f13-121"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="88f13-122">Initialisation en cours.</span><span class="sxs-lookup"><span data-stu-id="88f13-122">Initializing.</span></span><br/>         |
| <span id="4"></span><dl> <span data-ttu-id="88f13-123"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="88f13-123"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="88f13-124">En cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="88f13-124">Running.</span></span><br/>              |



 

## <a name="examples"></a><span data-ttu-id="88f13-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="88f13-125">Examples</span></span>

<span data-ttu-id="88f13-126">Pour obtenir un exemple d’utilisation de cette propriété, consultez [écoute des événements de rapport LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="88f13-126">For an example of how to use this property, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="88f13-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88f13-127">Requirements</span></span>



| <span data-ttu-id="88f13-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88f13-128">Requirement</span></span> | <span data-ttu-id="88f13-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="88f13-129">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="88f13-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88f13-130">Minimum supported client</span></span><br/> | <span data-ttu-id="88f13-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88f13-131">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="88f13-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88f13-132">Minimum supported server</span></span><br/> | <span data-ttu-id="88f13-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="88f13-133">None supported</span></span><br/>                  |



 

