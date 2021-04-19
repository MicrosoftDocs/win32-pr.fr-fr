---
description: Le modèle d’objet d’API emplacement fournit les événements suivants.
ms.assetid: c7ac0d81-ce36-4991-a0fb-6d3c6cc8efe8
title: Événements LocationDisp
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 55dae79305547bf4e41ee27c727ab9204eb561cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523688"
---
# <a name="locationdisp-events"></a><span data-ttu-id="6a130-103">Événements LocationDisp</span><span class="sxs-lookup"><span data-stu-id="6a130-103">LocationDisp Events</span></span>

<span data-ttu-id="6a130-104">\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="6a130-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6a130-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="6a130-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="6a130-106">Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6a130-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="6a130-107">Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="6a130-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="6a130-108">Le modèle d’objet d’API emplacement fournit les événements suivants.</span><span class="sxs-lookup"><span data-stu-id="6a130-108">The Location API object model provides the following events.</span></span>



| <span data-ttu-id="6a130-109">Événement</span><span class="sxs-lookup"><span data-stu-id="6a130-109">Event</span></span>                                                  | <span data-ttu-id="6a130-110">Description</span><span class="sxs-lookup"><span data-stu-id="6a130-110">Description</span></span>                                               |
|--------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="6a130-111">**NewCivicAddressReport**</span><span class="sxs-lookup"><span data-stu-id="6a130-111">**NewCivicAddressReport**</span></span>](newcivicaddressreport.md) | <span data-ttu-id="6a130-112">Se produit lors de la génération d’un nouveau rapport d’adresse postale.</span><span class="sxs-lookup"><span data-stu-id="6a130-112">Occurs when a new civic address report is generated.</span></span>      |
| [<span data-ttu-id="6a130-113">**NewLatLongReport**</span><span class="sxs-lookup"><span data-stu-id="6a130-113">**NewLatLongReport**</span></span>](newlatlongreport.md)           | <span data-ttu-id="6a130-114">Se produit lors de la génération d’un rapport de latitude/longitude.</span><span class="sxs-lookup"><span data-stu-id="6a130-114">Occurs when a new latitude/longitude report is generated.</span></span> |
| [<span data-ttu-id="6a130-115">**StatusChanged**</span><span class="sxs-lookup"><span data-stu-id="6a130-115">**StatusChanged**</span></span>](statuschanged.md)                 | <span data-ttu-id="6a130-116">Se produit lorsque l’état opérationnel d’un rapport change.</span><span class="sxs-lookup"><span data-stu-id="6a130-116">Occurs when the operational status of a report changes.</span></span>   |



 

 

 
