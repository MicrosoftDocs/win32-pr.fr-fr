---
description: Arrête les événements de rapport d’adresse postale.
ms.assetid: 6efe26bc-842d-49fc-aec2-e0dfa7f1eb0a
title: Méthode LocationDisp. CivicAddressReportFactory. StopListeningForReports (Locationapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.StopListeningForReports
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: 36c58e9db0edb66735dcbd58c8e1968cfa8b1fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539748"
---
# <a name="locationdispcivicaddressreportfactorystoplisteningforreports-method"></a><span data-ttu-id="d0e62-103">Méthode LocationDisp. CivicAddressReportFactory. StopListeningForReports</span><span class="sxs-lookup"><span data-stu-id="d0e62-103">LocationDisp.CivicAddressReportFactory.StopListeningForReports method</span></span>

<span data-ttu-id="d0e62-104">\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="d0e62-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d0e62-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d0e62-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="d0e62-106">Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d0e62-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="d0e62-107">Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="d0e62-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="d0e62-108">Arrête les événements de rapport d’adresse postale.</span><span class="sxs-lookup"><span data-stu-id="d0e62-108">Stops civic address report events.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0e62-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0e62-109">Syntax</span></span>


```JScript
LocationDisp.CivicAddressReportFactory.StopListeningForReports()
```



## <a name="parameters"></a><span data-ttu-id="d0e62-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0e62-110">Parameters</span></span>

<span data-ttu-id="d0e62-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d0e62-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d0e62-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d0e62-112">Return value</span></span>

<span data-ttu-id="d0e62-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d0e62-113">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="d0e62-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="d0e62-114">Examples</span></span>

<span data-ttu-id="d0e62-115">Pour obtenir un exemple d’utilisation de cette méthode, consultez [écoute des événements de rapport d’adresse postale](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="d0e62-115">For an example of how to use this method, see [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0e62-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0e62-116">Requirements</span></span>



| <span data-ttu-id="d0e62-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0e62-117">Requirement</span></span> | <span data-ttu-id="d0e62-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0e62-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0e62-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0e62-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d0e62-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d0e62-120">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d0e62-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0e62-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d0e62-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0e62-122">None supported</span></span><br/>                                                                |
| <span data-ttu-id="d0e62-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="d0e62-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0e62-124"><dt>Locationapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0e62-124"><dt>Locationapi.h</dt></span></span> </dl> |



 

