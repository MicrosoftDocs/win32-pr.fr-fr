---
description: Origin est une description générale de l’endroit où la session a démarré, par exemple si elle est externe ou interne à un réseau d’entreprise. Pour obtenir \_ la liste des origines prises en charge par TAPI, consultez constantes LINECALLORIGIN.
ms.assetid: d9779438-fd08-495a-ae3d-ffad9b543090
title: Origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71105caff17850c76c1e2c388911086a4cf9ea8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115526"
---
# <a name="origin"></a><span data-ttu-id="37e79-104">Origine</span><span class="sxs-lookup"><span data-stu-id="37e79-104">Origin</span></span>

<span data-ttu-id="37e79-105">Origin est une description générale de l’endroit où la session a démarré, par exemple si elle est externe ou interne à un réseau d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="37e79-105">Origin is a general description of where the session started, such as whether it is external or internal to a corporate network.</span></span> <span data-ttu-id="37e79-106">Pour obtenir la liste des origines prises en charge par TAPI, consultez [ \_ constantes LINECALLORIGIN](./linecallorigin--constants.md) .</span><span class="sxs-lookup"><span data-stu-id="37e79-106">See [LINECALLORIGIN\_ Constants](./linecallorigin--constants.md) for a listing of origins that TAPI supports.</span></span>

<span data-ttu-id="37e79-107">Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.</span><span class="sxs-lookup"><span data-stu-id="37e79-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="37e79-108">**TAPI 2. x :** Consultez [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (membre **dwOrigin** de *lpCallInfo*).</span><span class="sxs-lookup"><span data-stu-id="37e79-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwOrigin** member of *lpCallInfo*).</span></span>

<span data-ttu-id="37e79-109">**TAPI 3. x :** Consultez [**ITCallInfo :: obtenir \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (membre d'**\_ origine CIL** de [**CALLINFO \_ long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span><span class="sxs-lookup"><span data-stu-id="37e79-109">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL\_ORIGIN** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span></span>

 

 
