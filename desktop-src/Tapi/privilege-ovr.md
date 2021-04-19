---
description: Le privilège fait référence au fait qu’une application possède ou surveille la session.
ms.assetid: 0c02a88a-370f-4eb9-ba64-07a382bd2e87
title: Privilège
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2f773edb05afc029a8f9fb6b014cd8a737eef0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536800"
---
# <a name="privilege"></a><span data-ttu-id="2365b-103">Privilège</span><span class="sxs-lookup"><span data-stu-id="2365b-103">Privilege</span></span>

<span data-ttu-id="2365b-104">Le privilège fait référence au fait qu’une application possède ou surveille la session.</span><span class="sxs-lookup"><span data-stu-id="2365b-104">Privilege refers to whether an application owns or is monitoring the session.</span></span> <span data-ttu-id="2365b-105">Si l’application possède la session, elle est autorisée à effectuer diverses opérations de session.</span><span class="sxs-lookup"><span data-stu-id="2365b-105">If the application owns the session, it is allowed to perform a variety of session operations.</span></span> <span data-ttu-id="2365b-106">Si l’application est uniquement surveillée, elle reçoit des messages d’État et peut accéder aux informations de session, mais toute tentative d’exécution de la plupart des opérations génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="2365b-106">If the application is only monitoring, it will receive state messages and it can access session information, but any attempt to perform most operations will result in an error.</span></span>

<span data-ttu-id="2365b-107">Pendant l’initialisation, une application indique à TAPI le niveau de privilège requis pour les adresses.</span><span class="sxs-lookup"><span data-stu-id="2365b-107">During initialization, an application tells TAPI which privilege level it requires on which addresses.</span></span> <span data-ttu-id="2365b-108">L’interface TAPI offre des sessions entrantes uniquement aux applications qui ont été inscrites pour le propriétaire ou le propriétaire et le privilège de surveillance.</span><span class="sxs-lookup"><span data-stu-id="2365b-108">TAPI offers incoming sessions only to applications that have registered for either owner or owner and monitor privilege.</span></span>

<span data-ttu-id="2365b-109">Le privilège d’une application sur une session qu’il crée est toujours propriétaire.</span><span class="sxs-lookup"><span data-stu-id="2365b-109">An application's privilege on a session it creates is always owner.</span></span>

<span data-ttu-id="2365b-110">**TAPI 2. x :** Consultez [**lineGetCallStatus**](/windows/win32/api/tapi/nf-tapi-linegetcallstatus), **dwCallPrivilege** , membre de [**LINECALLSTATUS**](/windows/win32/api/tapi/ns-tapi-linecallstatus), [**lineSetCallPrivilege**](/windows/win32/api/tapi/nf-tapi-linesetcallprivilege).</span><span class="sxs-lookup"><span data-stu-id="2365b-110">**TAPI 2.x:** See [**lineGetCallStatus**](/windows/win32/api/tapi/nf-tapi-linegetcallstatus), **dwCallPrivilege** member of [**LINECALLSTATUS**](/windows/win32/api/tapi/ns-tapi-linecallstatus), [**lineSetCallPrivilege**](/windows/win32/api/tapi/nf-tapi-linesetcallprivilege).</span></span>

<span data-ttu-id="2365b-111">**TAPI 3. x :** Consultez [**ITCallInfo :: obtenir le \_ privilège**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_privilege), [**ITCallInfo :: \_ obtenir CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), appelé avec le membre **CIL \_ NUMBEROFOWNERS** ou **CIL \_ NUMBEROFMONITORS** de [**CALLINFO \_ long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span><span class="sxs-lookup"><span data-stu-id="2365b-111">**TAPI 3.x:** See [**ITCallInfo::get\_Privilege**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_privilege), [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), called with the **CIL\_NUMBEROFOWNERS** or **CIL\_NUMBEROFMONITORS** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span></span>

 

 
