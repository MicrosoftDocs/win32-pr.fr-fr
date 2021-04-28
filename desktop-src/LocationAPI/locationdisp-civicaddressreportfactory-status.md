---
description: 'Propriété LocationDisp. CivicAddressReportFactory. Status : état actuel du rapport.'
ms.assetid: 3aae0b61-cdaa-4131-b6e1-406813bb1848
title: LocationDisp. CivicAddressReportFactory. Status, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.Status
api_type:
- COM
api_location: ''
ms.openlocfilehash: acb5bcfa589139e2c69e75124253f9d9a7b53a87
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118497"
---
# <a name="locationdispcivicaddressreportfactorystatus-property"></a><span data-ttu-id="b27df-103">LocationDisp. CivicAddressReportFactory. Status, propriété</span><span class="sxs-lookup"><span data-stu-id="b27df-103">LocationDisp.CivicAddressReportFactory.Status property</span></span>

<span data-ttu-id="b27df-104">\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="b27df-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b27df-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b27df-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b27df-106">Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b27df-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="b27df-107">Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="b27df-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="b27df-108">État actuel du rapport.</span><span class="sxs-lookup"><span data-stu-id="b27df-108">The current report status.</span></span>

<span data-ttu-id="b27df-109">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b27df-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b27df-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b27df-110">Syntax</span></span>


```JScript
Status = LocationDisp.CivicAddressReportFactory.Status
```



## <a name="property-value"></a><span data-ttu-id="b27df-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b27df-111">Property value</span></span>

<span data-ttu-id="b27df-112">Cette propriété est un **nombre** en lecture seule (unsigned long).</span><span class="sxs-lookup"><span data-stu-id="b27df-112">This property is a read-only **Number** (unsigned long).</span></span>



| <span data-ttu-id="b27df-113">Statut</span><span class="sxs-lookup"><span data-stu-id="b27df-113">Status</span></span>                                                                                               | <span data-ttu-id="b27df-114">Signification</span><span class="sxs-lookup"><span data-stu-id="b27df-114">Meaning</span></span>                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="b27df-115"><dt>**entre**</dt></span><span class="sxs-lookup"><span data-stu-id="b27df-115"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="b27df-116">Rapport non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b27df-116">Report not supported.</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="b27df-117"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="b27df-117"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="b27df-118">Erreur.</span><span class="sxs-lookup"><span data-stu-id="b27df-118">Error.</span></span><br/>                |
| <span id="2"></span><dl> <span data-ttu-id="b27df-119"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="b27df-119"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="b27df-120">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="b27df-120">Access denied.</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="b27df-121"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="b27df-121"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="b27df-122">Initialisation en cours.</span><span class="sxs-lookup"><span data-stu-id="b27df-122">Initializing.</span></span><br/>         |
| <span id="4"></span><dl> <span data-ttu-id="b27df-123"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="b27df-123"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="b27df-124">En cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="b27df-124">Running.</span></span><br/>              |



 

## <a name="examples"></a><span data-ttu-id="b27df-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="b27df-125">Examples</span></span>

<span data-ttu-id="b27df-126">Pour obtenir un exemple d’utilisation de cette propriété, consultez [écoute des événements de rapport d’adresse postale](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="b27df-126">For an example of how to use this property, see [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="b27df-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b27df-127">Requirements</span></span>



| <span data-ttu-id="b27df-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b27df-128">Requirement</span></span> | <span data-ttu-id="b27df-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="b27df-129">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="b27df-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b27df-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b27df-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b27df-131">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b27df-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b27df-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b27df-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b27df-133">None supported</span></span><br/>                  |



 

