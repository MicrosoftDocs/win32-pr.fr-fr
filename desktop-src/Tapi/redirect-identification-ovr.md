---
description: Quand une application redirige une session, TAPI conserve les informations d’identification relatives à l’emplacement qui a redirigé la session et à l’emplacement vers lequel elle a été redirigée.
ms.assetid: 08484b38-7c97-4acc-921e-0f566b2d3415
title: Identification de la redirection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8316b7d1566a24ead21f7b1fdf2d16b1c48a2b15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522746"
---
# <a name="redirect-identification"></a><span data-ttu-id="26dbc-103">Identification de la redirection</span><span class="sxs-lookup"><span data-stu-id="26dbc-103">Redirect Identification</span></span>

<span data-ttu-id="26dbc-104">Quand une application [redirige](redirect-ovr.md) une session, TAPI conserve les informations d’identification relatives à l’emplacement qui a redirigé la session et à l’emplacement vers lequel elle a été redirigée.</span><span class="sxs-lookup"><span data-stu-id="26dbc-104">When an application [redirects](redirect-ovr.md) a session, TAPI retains identification information about the location that redirected the session and the location to which it was redirected.</span></span>

<span data-ttu-id="26dbc-105">La « redirection » fait référence à l’emplacement qui a appelé l’opération de redirection.</span><span class="sxs-lookup"><span data-stu-id="26dbc-105">"Redirecting" refers to the location that invoked the redirect operation.</span></span> <span data-ttu-id="26dbc-106">« Redirection » identifie la nouvelle destination pour la session.</span><span class="sxs-lookup"><span data-stu-id="26dbc-106">"Redirection" identifies the new destination for the session.</span></span>

<span data-ttu-id="26dbc-107">Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.</span><span class="sxs-lookup"><span data-stu-id="26dbc-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="26dbc-108">\* \* TAPI 2. x : \* \*[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwRedirectionIDSize**, **dwRedirectionIDOffset**, **dwRedirectionIDNameSize**, **dwRedirectionIDNameOffset**, **dwRedirectingIDSize**, **dwRedirectingIDOffset**, **dwRedirectingIDNameSize** et **dwRedirectingIDNameOffset** membres de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)</span><span class="sxs-lookup"><span data-stu-id="26dbc-108">\*\*TAPI 2.x:  \*\*[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwRedirectionIDSize**, **dwRedirectionIDOffset**, **dwRedirectionIDNameSize**, **dwRedirectionIDNameOffset**, **dwRedirectingIDSize**, **dwRedirectingIDOffset**, **dwRedirectingIDNameSize**, and **dwRedirectingIDNameOffset** members of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)</span></span>

<span data-ttu-id="26dbc-109">\* \* TAPI 3. x : \* \*[**ITCallInfo :: obten \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring)appelé avec les **membres CIS \_ REDIRECTIONIDNAME**, **CIS \_ REDIRECTIONIDNUMBER**, **CIS \_ REDIRECTINGIDNAME** ou **CIS \_ REDIRECTINGIDNUMBER** de la [**\_ chaîne CALLINFO**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)</span><span class="sxs-lookup"><span data-stu-id="26dbc-109">\*\*TAPI 3.x:  \*\*[**ITCallInfo::get\_CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring)called with the **CIS\_REDIRECTIONIDNAME**, **CIS\_REDIRECTIONIDNUMBER**, **CIS\_REDIRECTINGIDNAME**, or **CIS\_REDIRECTINGIDNUMBER** member of [**CALLINFO\_STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)</span></span>

 

 
