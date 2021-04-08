---
description: Le type \_ de données d’initialisation de la négociation est une valeur spéciale de type DWORD.
ms.assetid: ce978913-47a1-4387-bd1b-1795aaf82dd7
title: INITIALIZE_NEGOTIATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51a55879a0952d3f8b5e268ec6a01a666bdbf5ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753420"
---
# <a name="initialize_negotiation"></a><span data-ttu-id="87255-103">INITIALiser la \_ négociation</span><span class="sxs-lookup"><span data-stu-id="87255-103">INITIALIZE\_NEGOTIATION</span></span>

<span data-ttu-id="87255-104">Le type de données **d’initialisation de la \_ négociation** est une valeur spéciale de type **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="87255-104">The **INITIALIZE\_NEGOTIATION** datatype is a special value of type **DWORD**.</span></span> <span data-ttu-id="87255-105">Il peut être passé comme paramètre *dwDeviceID* dans les fonctions [**TSPI \_ lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) et [**TSPI \_ phoneNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) .</span><span class="sxs-lookup"><span data-stu-id="87255-105">It can be passed as the *dwDeviceID* parameter in the [**TSPI\_lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) and [**TSPI\_phoneNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) functions.</span></span> <span data-ttu-id="87255-106">Cela indique que l’interface TAPI peut négocier un numéro de version de l’interface TSPI indépendamment des appareils spécifiques.</span><span class="sxs-lookup"><span data-stu-id="87255-106">Doing so indicates that TAPI can negotiate a TSPI interface version number independent of any specific devices.</span></span>

 

 
