---
description: Se produit lors de la génération d’un rapport de latitude/longitude.
ms.assetid: 2b1a25a1-ccd6-43f8-979b-c2d414d666a2
title: Événement NewLatLongReport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewLatLongReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: ea305d17169b71d183a8d453e9885d8de878b026
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532333"
---
# <a name="newlatlongreport-event"></a><span data-ttu-id="7aea7-103">Événement NewLatLongReport</span><span class="sxs-lookup"><span data-stu-id="7aea7-103">NewLatLongReport event</span></span>

<span data-ttu-id="7aea7-104">\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="7aea7-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7aea7-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="7aea7-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="7aea7-106">Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7aea7-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="7aea7-107">Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="7aea7-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="7aea7-108">Se produit lors de la génération d’un rapport de latitude/longitude.</span><span class="sxs-lookup"><span data-stu-id="7aea7-108">Occurs when a new latitude/longitude report is generated.</span></span>

## <a name="syntax"></a><span data-ttu-id="7aea7-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7aea7-109">Syntax</span></span>


```JScript
.NewLatLongReport(
  newReport
)
```



## <a name="parameters"></a><span data-ttu-id="7aea7-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7aea7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7aea7-111">*newReport*</span><span class="sxs-lookup"><span data-stu-id="7aea7-111">*newReport*</span></span> 
</dt> <dd>

<span data-ttu-id="7aea7-112">Nouvel objet [**LocationDisp. DispLatLongReport**](locationdisp-displatlongreport.md) .</span><span class="sxs-lookup"><span data-stu-id="7aea7-112">The new [**LocationDisp.DispLatLongReport**](locationdisp-displatlongreport.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7aea7-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7aea7-113">Return value</span></span>

<span data-ttu-id="7aea7-114">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="7aea7-114">This event does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="7aea7-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="7aea7-115">Examples</span></span>

<span data-ttu-id="7aea7-116">Pour obtenir un exemple d’utilisation de cet événement, consultez [écoute des événements de rapport LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="7aea7-116">For an example of how to use this event, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="7aea7-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7aea7-117">Requirements</span></span>



| <span data-ttu-id="7aea7-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7aea7-118">Requirement</span></span> | <span data-ttu-id="7aea7-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="7aea7-119">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="7aea7-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7aea7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7aea7-121">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7aea7-121">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7aea7-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7aea7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7aea7-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7aea7-123">None supported</span></span><br/>                  |



 

