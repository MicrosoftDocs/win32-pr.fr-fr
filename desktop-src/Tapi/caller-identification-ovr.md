---
description: L’identification de l’appelant fournit des informations sur le tiers appelant lors de la réception d’une session entrante. Une application utilise généralement ces données dans le cadre d’un message d’État à un utilisateur.
ms.assetid: aaaa5eae-e917-44a7-b9c5-97ca2d9a4eec
title: Identification de l’appelant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93513e3d94fac9c550b23651b3987bc794905beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866593"
---
# <a name="caller-identification"></a><span data-ttu-id="dfd43-104">Identification de l’appelant</span><span class="sxs-lookup"><span data-stu-id="dfd43-104">Caller Identification</span></span>

<span data-ttu-id="dfd43-105">L’identification de l’appelant fournit des informations sur le tiers appelant lors de la réception d’une session entrante.</span><span class="sxs-lookup"><span data-stu-id="dfd43-105">Caller identification provides information on the calling party when receiving an incoming session.</span></span> <span data-ttu-id="dfd43-106">Une application utilise généralement ces données dans le cadre d’un message d’État à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dfd43-106">An application typically uses this data as part of a status message to a user.</span></span>

<span data-ttu-id="dfd43-107">Ces informations ne sont pas toujours disponibles immédiatement.</span><span class="sxs-lookup"><span data-stu-id="dfd43-107">This information is not always available immediately.</span></span> <span data-ttu-id="dfd43-108">Une application qui souhaite utiliser ces informations et qui a vérifié que le fournisseur de services est pris en charge doit vérifier plusieurs fois avant de supposer que les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="dfd43-108">An application that wants to use this information and has verified that the service provider supports it should check several times before assuming that the information is not available.</span></span>

<span data-ttu-id="dfd43-109">Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.</span><span class="sxs-lookup"><span data-stu-id="dfd43-109">Not all service providers support use of this information.</span></span>

<span data-ttu-id="dfd43-110">**TAPI 2. x :** Consultez [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCallerIDFlags**, **dwCallerIDSize**, **dwCallerIDOffset**, **dwCallerIDNameSize**, **dwCallerIDNameOffset** et **dwCallerIDAddressType** , membres de *lpCallInfo*).</span><span class="sxs-lookup"><span data-stu-id="dfd43-110">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCallerIDFlags**, **dwCallerIDSize**, **dwCallerIDOffset**, **dwCallerIDNameSize**, **dwCallerIDNameOffset**, and **dwCallerIDAddressType** members of *lpCallInfo*).</span></span>

<span data-ttu-id="dfd43-111">**TAPI 3. x :** Consultez [**ITCallInfo :: obtenir \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL \_ CALLERIDADDRESSTYPE** membre de [**CALLINFO \_ long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**ITCallInfo :: obtenir \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS \_ CALLERIDNAME** et **CIS \_ CALLERIDNAME** members de [**CALLINFO \_ String**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).</span><span class="sxs-lookup"><span data-stu-id="dfd43-111">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL\_CALLERIDADDRESSTYPE** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**ITCallInfo::get\_CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS\_CALLERIDNAME** and **CIS\_CALLERIDNAME** members of [**CALLINFO\_STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).</span></span>

 

 
