---
description: Numéro du Trunk sur lequel l’appel est routé. Ce membre est utilisé pour les appels entrants et sortants.
ms.assetid: e57e1aac-a2f1-42b7-9a0c-c74009a75305
title: Trunk
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb4afea1387c6d43dc4d9a2f5a6a12f260a8daeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204127"
---
# <a name="trunk"></a><span data-ttu-id="88fa7-104">Trunk</span><span class="sxs-lookup"><span data-stu-id="88fa7-104">Trunk</span></span>

<span data-ttu-id="88fa7-105">Numéro du Trunk sur lequel l’appel est routé.</span><span class="sxs-lookup"><span data-stu-id="88fa7-105">The number of the trunk over which the call is routed.</span></span> <span data-ttu-id="88fa7-106">Ce membre est utilisé pour les appels entrants et sortants.</span><span class="sxs-lookup"><span data-stu-id="88fa7-106">This member is used for both incoming and outgoing calls.</span></span>

<span data-ttu-id="88fa7-107">Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.</span><span class="sxs-lookup"><span data-stu-id="88fa7-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="88fa7-108">\* \* TAPI 2. x : \* \*[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwTrunk** of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)</span><span class="sxs-lookup"><span data-stu-id="88fa7-108">\*\*TAPI 2.x:  \*\*[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwTrunk** of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)</span></span>

<span data-ttu-id="88fa7-109">\* \* TAPI 3. x : \* \*[**ITCallInfo :: obten \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), appelé avec le membre de **\_ Trunk CIL** de [**CALLINFO \_ long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)</span><span class="sxs-lookup"><span data-stu-id="88fa7-109">\*\*TAPI 3.x:  \*\*[**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), called with **CIL\_TRUNK** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)</span></span>

 

 
