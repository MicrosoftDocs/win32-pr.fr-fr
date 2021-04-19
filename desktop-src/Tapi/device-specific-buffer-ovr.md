---
description: Les mémoires tampons spécifiques à l’appareil peuvent faire partie d’une implémentation de fournisseurs de services d’opérations étendues. Le fournisseur de services définit la signification de ces mémoires tampons.
ms.assetid: 5783f892-ec11-4340-afad-44f2ef55fd18
title: Mémoire tampon spécifique à l’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 628ee93e4f88fc733e744b3c52af3c0a1c31ecf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518469"
---
# <a name="device-specific-buffer"></a><span data-ttu-id="87f3c-104">Mémoire tampon spécifique à l’appareil</span><span class="sxs-lookup"><span data-stu-id="87f3c-104">Device-specific Buffer</span></span>

<span data-ttu-id="87f3c-105">Les mémoires tampons spécifiques à l’appareil peuvent faire partie de l’implémentation d’opérations étendues d’un fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="87f3c-105">Device-specific buffers may be part of a service provider's implementation of extended operations.</span></span> <span data-ttu-id="87f3c-106">Le fournisseur de services définit la signification de ces mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="87f3c-106">The service provider defines the meaning of these buffers.</span></span>

<span data-ttu-id="87f3c-107">Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.</span><span class="sxs-lookup"><span data-stu-id="87f3c-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="87f3c-108">**TAPI 2. x :** Consultez [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (membres **dwDevSpecificSize** et **dwDevSpecificOffset** de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).</span><span class="sxs-lookup"><span data-stu-id="87f3c-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwDevSpecificSize** and **dwDevSpecificOffset** members of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).</span></span>

<span data-ttu-id="87f3c-109">**TAPI 3. x :** Consultez [**ITCallInfo :: GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer) (**CIM \_ DEVSPECIFICBUFFER** membre de [**CALLINFO \_ buffer**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).</span><span class="sxs-lookup"><span data-stu-id="87f3c-109">**TAPI 3.x:** See [**ITCallInfo::GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer) (**CIB\_DEVSPECIFICBUFFER** member of [**CALLINFO\_BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).</span></span>

 

 
