---
description: Valeur actuelle de précision souhaitée.
ms.assetid: 296164cf-a8ed-4277-bb4c-83ac09e63291
title: LocationDisp. CivicAddressReportFactory. DesiredAccuracy, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.DesiredAccuracy
api_type:
- COM
api_location: ''
ms.openlocfilehash: eb05aeb6a69bfe978682d418cf1e71aed2184bc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538188"
---
# <a name="locationdispcivicaddressreportfactorydesiredaccuracy-property"></a><span data-ttu-id="88780-103">LocationDisp. CivicAddressReportFactory. DesiredAccuracy, propriété</span><span class="sxs-lookup"><span data-stu-id="88780-103">LocationDisp.CivicAddressReportFactory.DesiredAccuracy property</span></span>

<span data-ttu-id="88780-104">\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="88780-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="88780-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="88780-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="88780-106">Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="88780-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="88780-107">Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="88780-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="88780-108">Valeur actuelle de précision souhaitée.</span><span class="sxs-lookup"><span data-stu-id="88780-108">The current desired-accuracy value.</span></span>

<span data-ttu-id="88780-109">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="88780-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="88780-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88780-110">Syntax</span></span>


```JScript
DesiredAccuracy = LocationDisp.CivicAddressReportFactory.DesiredAccuracy
LocationDisp.CivicAddressReportFactory.DesiredAccuracy = DesiredAccuracy
```



## <a name="property-value"></a><span data-ttu-id="88780-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="88780-111">Property value</span></span>

<span data-ttu-id="88780-112">Cette propriété est en lecture/écriture **ULong**.</span><span class="sxs-lookup"><span data-stu-id="88780-112">This property is a read/write **ULONG**.</span></span>



| <span data-ttu-id="88780-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="88780-113">Value</span></span>                                                                        | <span data-ttu-id="88780-114">Signification</span><span class="sxs-lookup"><span data-stu-id="88780-114">Meaning</span></span>                                                                                                                                                                                            |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="88780-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="88780-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="88780-116">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="88780-116">Default.</span></span> <span data-ttu-id="88780-117">Le capteur doit utiliser la précision pour laquelle il peut optimiser l’utilisation de l’alimentation et d’autres considérations relatives aux coûts.</span><span class="sxs-lookup"><span data-stu-id="88780-117">The sensor should use the accuracy for which it can optimize power use and other cost considerations.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="88780-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="88780-118"><dt>1</dt></span></span> </dl> | <span data-ttu-id="88780-119">Le capteur doit fournir le rapport le plus précis possible.</span><span class="sxs-lookup"><span data-stu-id="88780-119">The sensor should deliver the most accurate report possible.</span></span> <span data-ttu-id="88780-120">Cela inclut l'utilisation des services qui peuvent facturer des sommes d'argent ou la consommation de niveaux supérieurs d'alimentation de batterie ou de bande passante de connexion.</span><span class="sxs-lookup"><span data-stu-id="88780-120">This includes using services that might charge money, or consuming higher levels of battery power or connection bandwidth.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="88780-121">Notes</span><span class="sxs-lookup"><span data-stu-id="88780-121">Remarks</span></span>

<span data-ttu-id="88780-122">Cette valeur est une demande au fournisseur de localisation.</span><span class="sxs-lookup"><span data-stu-id="88780-122">This value is a request to the location provider.</span></span> <span data-ttu-id="88780-123">Le fournisseur de localisation n’est pas requis pour fournir la précision que vous demandez.</span><span class="sxs-lookup"><span data-stu-id="88780-123">The location provider is not required to provide the accuracy that you request.</span></span> <span data-ttu-id="88780-124">Lisez la valeur de cette propriété pour découvrir le véritable paramètre de précision.</span><span class="sxs-lookup"><span data-stu-id="88780-124">Read the value of this property to discover the true accuracy setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="88780-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88780-125">Requirements</span></span>



| <span data-ttu-id="88780-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88780-126">Requirement</span></span> | <span data-ttu-id="88780-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="88780-127">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="88780-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88780-128">Minimum supported client</span></span><br/> | <span data-ttu-id="88780-129">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88780-129">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="88780-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88780-130">Minimum supported server</span></span><br/> | <span data-ttu-id="88780-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="88780-131">None supported</span></span><br/>                  |



 

