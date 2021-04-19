---
description: L’ID d’appel est différent de l’identificateur de session de deux façons principales, le fournisseur de services l’attribue, et il est identique pour chaque application qui gère la session.
ms.assetid: c9d0d43b-3053-4e3e-b442-57942f3448df
title: ID d’appel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef571b55f653cb9c7bc1d61cdc8a3f71e91ba8f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527499"
---
# <a name="call-id"></a><span data-ttu-id="99012-103">ID d’appel</span><span class="sxs-lookup"><span data-stu-id="99012-103">Call ID</span></span>

<span data-ttu-id="99012-104">L’ID d’appel est différent de l' [identificateur de session](session-identifier-ovr.md) de deux manières principales : le fournisseur de services l’assigne et il est identique pour chaque application qui gère la session.</span><span class="sxs-lookup"><span data-stu-id="99012-104">The Call ID differs from the [Session Identifier](session-identifier-ovr.md) in two primary ways: the service provider assigns it, and it is the same for every application that handles the session.</span></span> <span data-ttu-id="99012-105">Il ne peut pas être utilisé pour la communication ordinaire avec TAPI concernant les opérations de session, car il ne correspond pas à une application particulière.</span><span class="sxs-lookup"><span data-stu-id="99012-105">It cannot be used for ordinary communication with TAPI concerning session operations because it does not match to a particular application.</span></span>

<span data-ttu-id="99012-106">L’ID d’appel est utilisé dans les opérations telles que la détermination de si un groupe d’ID de session fait réellement référence à un appel, comme c’est le cas pour une conférence ou pour la communication avec une autre application.</span><span class="sxs-lookup"><span data-stu-id="99012-106">The Call ID is used in operations such as determining whether a group of session IDs actually refer to one call, as is the case for a conference, or for communications with another application.</span></span>

<span data-ttu-id="99012-107">Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.</span><span class="sxs-lookup"><span data-stu-id="99012-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="99012-108">**TAPI 2. x :** Consultez [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (membre **dwCallID** de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).</span><span class="sxs-lookup"><span data-stu-id="99012-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCallID** member of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).</span></span>

<span data-ttu-id="99012-109">**TAPI 3. x :** Consultez [**ITCallInfo :: obtenir \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL \_ CALLID** membre de [**CALLINFO \_ long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span><span class="sxs-lookup"><span data-stu-id="99012-109">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL\_CALLID** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span></span>

 

 
