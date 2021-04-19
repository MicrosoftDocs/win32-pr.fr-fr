---
description: Valeur actuelle de précision souhaitée.
ms.assetid: dfad833b-bb0c-4c66-9942-da10abee5381
title: LocationDisp. LatLongReportFactory. DesiredAccuracy, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.DesiredAccuracy
api_type:
- COM
api_location: ''
ms.openlocfilehash: e17e415d9503660d873ae4df67d2469c646dd80e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527707"
---
# <a name="locationdisplatlongreportfactorydesiredaccuracy-property"></a><span data-ttu-id="f764c-103">LocationDisp. LatLongReportFactory. DesiredAccuracy, propriété</span><span class="sxs-lookup"><span data-stu-id="f764c-103">LocationDisp.LatLongReportFactory.DesiredAccuracy property</span></span>

<span data-ttu-id="f764c-104">\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="f764c-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f764c-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="f764c-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="f764c-106">Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f764c-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="f764c-107">Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="f764c-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="f764c-108">Valeur actuelle de précision souhaitée.</span><span class="sxs-lookup"><span data-stu-id="f764c-108">The current desired-accuracy value.</span></span>

<span data-ttu-id="f764c-109">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="f764c-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f764c-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f764c-110">Syntax</span></span>


```JScript
DesiredAccuracy = LocationDisp.LatLongReportFactory.DesiredAccuracy
LocationDisp.LatLongReportFactory.DesiredAccuracy = DesiredAccuracy
```



## <a name="property-value"></a><span data-ttu-id="f764c-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f764c-111">Property value</span></span>

<span data-ttu-id="f764c-112">Cette propriété est en lecture/écriture **ULong**.</span><span class="sxs-lookup"><span data-stu-id="f764c-112">This property is a read/write **ULONG**.</span></span>



| <span data-ttu-id="f764c-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="f764c-113">Value</span></span>                                                                        | <span data-ttu-id="f764c-114">Signification</span><span class="sxs-lookup"><span data-stu-id="f764c-114">Meaning</span></span>                                                                                                                                                                                            |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f764c-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f764c-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="f764c-116">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="f764c-116">Default.</span></span> <span data-ttu-id="f764c-117">Le capteur doit utiliser la précision pour laquelle il peut optimiser l’utilisation de l’alimentation et d’autres considérations relatives aux coûts.</span><span class="sxs-lookup"><span data-stu-id="f764c-117">The sensor should use the accuracy for which it can optimize power use and other cost considerations.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="f764c-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f764c-118"><dt>1</dt></span></span> </dl> | <span data-ttu-id="f764c-119">Le capteur doit fournir le rapport le plus précis possible.</span><span class="sxs-lookup"><span data-stu-id="f764c-119">The sensor should deliver the most accurate report possible.</span></span> <span data-ttu-id="f764c-120">Cela inclut l'utilisation des services qui peuvent facturer des sommes d'argent ou la consommation de niveaux supérieurs d'alimentation de batterie ou de bande passante de connexion.</span><span class="sxs-lookup"><span data-stu-id="f764c-120">This includes using services that might charge money, or consuming higher levels of battery power or connection bandwidth.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f764c-121">Notes</span><span class="sxs-lookup"><span data-stu-id="f764c-121">Remarks</span></span>

<span data-ttu-id="f764c-122">Cette valeur est une demande au fournisseur de localisation.</span><span class="sxs-lookup"><span data-stu-id="f764c-122">This value is a request to the location provider.</span></span> <span data-ttu-id="f764c-123">Le fournisseur d’emplacement n’est pas obligé de fournir des rapports à l’intervalle que vous avez demandé.</span><span class="sxs-lookup"><span data-stu-id="f764c-123">The location provider is not required to provide reports at the interval you requested.</span></span> <span data-ttu-id="f764c-124">Lisez la valeur de cette propriété pour découvrir le paramètre d’intervalle de rapport réel.</span><span class="sxs-lookup"><span data-stu-id="f764c-124">Read the value of this property to discover the true report interval setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="f764c-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f764c-125">Requirements</span></span>



| <span data-ttu-id="f764c-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f764c-126">Requirement</span></span> | <span data-ttu-id="f764c-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="f764c-127">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="f764c-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f764c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f764c-129">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f764c-129">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f764c-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f764c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f764c-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f764c-131">None supported</span></span><br/>                  |



 

