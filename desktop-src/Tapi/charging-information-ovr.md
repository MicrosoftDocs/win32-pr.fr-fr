---
description: Les informations de facturation sont spécifiques à la norme Q. 931 RNIS. Reportez-vous à la documentation de votre fournisseur de services sur la signification et l’utilisation de ces données.
ms.assetid: 5032e2cb-486a-4667-9873-bf88365f12cf
title: Informations de facturation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14d988ec34e901a94e27156f321436b59714cffb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519353"
---
# <a name="charging-information"></a><span data-ttu-id="a4f14-104">Informations de facturation</span><span class="sxs-lookup"><span data-stu-id="a4f14-104">Charging Information</span></span>

<span data-ttu-id="a4f14-105">Les informations de facturation sont spécifiques à la norme Q. 931 RNIS.</span><span class="sxs-lookup"><span data-stu-id="a4f14-105">Charging information is specific to the ISDN Q.931 standard.</span></span> <span data-ttu-id="a4f14-106">Reportez-vous à la documentation de votre fournisseur de services sur la signification et l’utilisation de ces données.</span><span class="sxs-lookup"><span data-stu-id="a4f14-106">Please refer to your service provider's documentation on the meaning and use of this data.</span></span>

<span data-ttu-id="a4f14-107">Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.</span><span class="sxs-lookup"><span data-stu-id="a4f14-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="a4f14-108">**TAPI 2. x :** Consultez [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (membres **dwChargingInfoSize** et **dwChargingInfoOffset** de *lpCallInfo*).</span><span class="sxs-lookup"><span data-stu-id="a4f14-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwChargingInfoSize** and **dwChargingInfoOffset** members of *lpCallInfo*).</span></span>

<span data-ttu-id="a4f14-109">**TAPI 3. x :** Consultez [**ITCallInfo :: obtenir \_ CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer) (**CIM \_ CHARGINGINFOBUFFER** membre de [**CALLINFO \_ buffer**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).</span><span class="sxs-lookup"><span data-stu-id="a4f14-109">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer) (**CIB\_CHARGINGINFOBUFFER** member of [**CALLINFO\_BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).</span></span>

 

 
