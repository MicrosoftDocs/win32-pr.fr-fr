---
description: L’identification connectée identifie le tiers qui a été réellement connecté à. Cela peut être différent de l’identification appelée si l’appel a été détourné.
ms.assetid: 3f9ba728-8e78-4f1f-a0c1-76799fd62c9d
title: Identification connectée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59fdb2f11b27bf9281b381170aa0d5b5ab027088
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321202"
---
# <a name="connected-identification"></a><span data-ttu-id="a0f24-104">Identification connectée</span><span class="sxs-lookup"><span data-stu-id="a0f24-104">Connected Identification</span></span>

<span data-ttu-id="a0f24-105">L’identification connectée identifie le tiers qui a été réellement connecté à.</span><span class="sxs-lookup"><span data-stu-id="a0f24-105">The connected identification identifies the party that was actually connected to.</span></span> <span data-ttu-id="a0f24-106">Cela peut être différent de l’identification appelée si l’appel a été détourné.</span><span class="sxs-lookup"><span data-stu-id="a0f24-106">This may be different from the called identification if the call was diverted.</span></span>

<span data-ttu-id="a0f24-107">Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.</span><span class="sxs-lookup"><span data-stu-id="a0f24-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="a0f24-108">**TAPI 2. x :** Consultez [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwConnectedIDFlags**, **dwConnectedIDSize**, **dwConnectedIDOffset**, **dwConnectedIDNameSize** et **dwConnectedIDNameOffset** *).*</span><span class="sxs-lookup"><span data-stu-id="a0f24-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwConnectedIDFlags**, **dwConnectedIDSize**, **dwConnectedIDOffset**, **dwConnectedIDNameSize**, and **dwConnectedIDNameOffset** members of *lpCallInfo*).</span></span>

<span data-ttu-id="a0f24-109">**TAPI 3. x :** Consultez [**ITCallInfo :: obtenir \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIL \_ CONNECTEDIDNAME** membre de [**CALLINFO \_ String**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).</span><span class="sxs-lookup"><span data-stu-id="a0f24-109">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIL\_CONNECTEDIDNAME** member of [**CALLINFO\_STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).</span></span>

 

 
