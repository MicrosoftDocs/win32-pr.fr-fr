---
description: L’API d’emplacement définit les types d’énumération suivants.
ms.assetid: a1d9d274-2861-4818-8fa1-d8d66edf27b3
title: Structures et types énumération (API location)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a73c27cb2ad6dc0dcd0c2b92f4e9ba52e98fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526158"
---
# <a name="structures-and-enumeration-types-location-api"></a><span data-ttu-id="a809a-103">Structures et types énumération (API location)</span><span class="sxs-lookup"><span data-stu-id="a809a-103">Structures and Enumeration Types (Location API)</span></span>

<span data-ttu-id="a809a-104">\[L’API emplacement Win32 peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="a809a-104">\[The Win32 Location API is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a809a-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a809a-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a809a-106">Utilisez plutôt l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .</span><span class="sxs-lookup"><span data-stu-id="a809a-106">Instead, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.</span></span> <span data-ttu-id="a809a-107">\]</span><span class="sxs-lookup"><span data-stu-id="a809a-107">\]</span></span>

<span data-ttu-id="a809a-108">L’API d’emplacement définit les types d’énumération suivants.</span><span class="sxs-lookup"><span data-stu-id="a809a-108">The Location API defines the following enumeration types.</span></span>



| <span data-ttu-id="a809a-109">Énumération</span><span class="sxs-lookup"><span data-stu-id="a809a-109">Enumeration</span></span>                                                                       | <span data-ttu-id="a809a-110">Description</span><span class="sxs-lookup"><span data-stu-id="a809a-110">Description</span></span>                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="a809a-111">[**précision de l’emplacement \_ souhaitée \_**](/previous-versions/windows/desktop/legacy/dd756639(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a809a-111">[**LOCATION\_DESIRED\_ACCURACY**](/previous-versions/windows/desktop/legacy/dd756639(v=vs.85))</span></span>                  | <span data-ttu-id="a809a-112">Définit les types de précision souhaités possibles.</span><span class="sxs-lookup"><span data-stu-id="a809a-112">Defines the possible desired accuracy types.</span></span>                         |
| [<span data-ttu-id="a809a-113">**\_État du rapport d’emplacement \_**</span><span class="sxs-lookup"><span data-stu-id="a809a-113">**LOCATION\_REPORT\_STATUS**</span></span>](/windows/win32/api/locationapi/ne-locationapi-location_report_status) | <span data-ttu-id="a809a-114">Définit l’état possible des nouveaux rapports d’un type de rapport particulier.</span><span class="sxs-lookup"><span data-stu-id="a809a-114">Defines possible status for new reports of a particular report type.</span></span> |



 

## <a name="location-constants-from-the-sensor-api"></a><span data-ttu-id="a809a-115">Constantes d’emplacement à partir de l’API de capteur</span><span class="sxs-lookup"><span data-stu-id="a809a-115">Location Constants from the Sensor API</span></span>

<span data-ttu-id="a809a-116">L’API de capteur définit également des constantes et des clés de propriétés liées à l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="a809a-116">The Sensor API also defines location-related property keys and constants.</span></span> <span data-ttu-id="a809a-117">Les clés de propriété définies dans sensors. h peuvent être utilisées pour récupérer des données d’emplacement à partir d’un rapport en appelant [**ILocationReport :: GetValue**](/windows/win32/api/locationapi/nf-locationapi-ilocationreport-getvalue).</span><span class="sxs-lookup"><span data-stu-id="a809a-117">The property keys defined in sensors.h can be used to retrieve location data from a report by calling [**ILocationReport::GetValue**](/windows/win32/api/locationapi/nf-locationapi-ilocationreport-getvalue).</span></span>

 

 
