---
description: Se produit lorsque l’état opérationnel d’un rapport change.
ms.assetid: f0c4e678-1666-4f99-89de-85879eacd0ac
title: Événement StatusChanged
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StatusChanged
api_type:
- COM
api_location: ''
ms.openlocfilehash: d1bda6645002f586eda0e2dad99a134450329d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104211101"
---
# <a name="statuschanged-event"></a><span data-ttu-id="9d6f1-103">Événement StatusChanged</span><span class="sxs-lookup"><span data-stu-id="9d6f1-103">StatusChanged event</span></span>

<span data-ttu-id="9d6f1-104">\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="9d6f1-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9d6f1-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="9d6f1-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="9d6f1-106">Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9d6f1-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="9d6f1-107">Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="9d6f1-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="9d6f1-108">Se produit lorsque l’état opérationnel d’un rapport change.</span><span class="sxs-lookup"><span data-stu-id="9d6f1-108">Occurs when the operational status of a report changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d6f1-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d6f1-109">Syntax</span></span>


```JScript
.StatusChanged(
  status
)
```



## <a name="parameters"></a><span data-ttu-id="9d6f1-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d6f1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d6f1-111">*statut*</span><span class="sxs-lookup"><span data-stu-id="9d6f1-111">*status*</span></span> 
</dt> <dd>

<span data-ttu-id="9d6f1-112">Nouvel état.</span><span class="sxs-lookup"><span data-stu-id="9d6f1-112">The new status.</span></span>



| <span data-ttu-id="9d6f1-113">Statut</span><span class="sxs-lookup"><span data-stu-id="9d6f1-113">Status</span></span>                                                                                               | <span data-ttu-id="9d6f1-114">Signification</span><span class="sxs-lookup"><span data-stu-id="9d6f1-114">Meaning</span></span>                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="9d6f1-115"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="9d6f1-115"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="9d6f1-116">Rapport non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9d6f1-116">Report not supported.</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="9d6f1-117"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="9d6f1-117"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="9d6f1-118">Erreur.</span><span class="sxs-lookup"><span data-stu-id="9d6f1-118">Error.</span></span><br/>                |
| <span id="2"></span><dl> <span data-ttu-id="9d6f1-119"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="9d6f1-119"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="9d6f1-120">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="9d6f1-120">Access denied.</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="9d6f1-121"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="9d6f1-121"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="9d6f1-122">Initialisation en cours.</span><span class="sxs-lookup"><span data-stu-id="9d6f1-122">Initializing.</span></span><br/>         |
| <span id="4"></span><dl> <span data-ttu-id="9d6f1-123"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="9d6f1-123"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="9d6f1-124">En cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="9d6f1-124">Running.</span></span><br/>              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d6f1-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9d6f1-125">Return value</span></span>

<span data-ttu-id="9d6f1-126">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9d6f1-126">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d6f1-127">Notes</span><span class="sxs-lookup"><span data-stu-id="9d6f1-127">Remarks</span></span>

<span data-ttu-id="9d6f1-128">Vous devez implémenter des gestionnaires de rapports de modification d’État distincts pour les rapports d’adresse civique et les rapports de latitude/longitude.</span><span class="sxs-lookup"><span data-stu-id="9d6f1-128">You should implement separate status change report handlers for civic address reports and latitude/longitude reports.</span></span>

## <a name="examples"></a><span data-ttu-id="9d6f1-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="9d6f1-129">Examples</span></span>

<span data-ttu-id="9d6f1-130">Pour obtenir un exemple d’utilisation de cet événement, consultez [écoute des événements de rapport LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="9d6f1-130">For an example of how to use this event, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="9d6f1-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d6f1-131">Requirements</span></span>



| <span data-ttu-id="9d6f1-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d6f1-132">Requirement</span></span> | <span data-ttu-id="9d6f1-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d6f1-133">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="9d6f1-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d6f1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9d6f1-135">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d6f1-135">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9d6f1-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d6f1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9d6f1-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d6f1-137">None supported</span></span><br/>                  |



 

