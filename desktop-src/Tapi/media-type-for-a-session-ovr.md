---
description: Le type de média (ou mode) décrit le type d’informations échangées, par exemple la voix interactive. Une session de communication donnée peut impliquer plusieurs types de médias.
ms.assetid: 2eb140f0-ca07-4e60-b9f3-be2f466f4fca
title: Type de média pour une session
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc8f5c7743a5d5a85003c99b2ac1abbf13f54168
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530513"
---
# <a name="media-type-for-a-session"></a><span data-ttu-id="54543-104">Type de média pour une session</span><span class="sxs-lookup"><span data-stu-id="54543-104">Media Type for a Session</span></span>

<span data-ttu-id="54543-105">Le type de média (ou mode) décrit le type d’informations échangées, par exemple la voix interactive.</span><span class="sxs-lookup"><span data-stu-id="54543-105">The media type (or mode) describes the type of information being exchanged, such as interactive voice.</span></span> <span data-ttu-id="54543-106">Une session de communication donnée peut impliquer plusieurs types de médias.</span><span class="sxs-lookup"><span data-stu-id="54543-106">A given communications session may involve several media types.</span></span>

<span data-ttu-id="54543-107">Les fournisseurs de services exposent à TAPI et aux applications le type de média ou les types qu’ils prennent en charge.</span><span class="sxs-lookup"><span data-stu-id="54543-107">Service providers expose to TAPI and to applications the media type or types they support.</span></span> <span data-ttu-id="54543-108">Pour plus d’informations sur l’acquisition de ces données, consultez vue d’ensemble du [type de média](media-type-ovr.md) de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="54543-108">See the device [media type](media-type-ovr.md) overview for information on acquiring this data.</span></span>

<span data-ttu-id="54543-109">**TAPI 2. x :** Consultez [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**lineSetMediaMode**](/windows/win32/api/tapi/nf-tapi-linesetmediamode), [**lineMonitorMedia**](/windows/win32/api/tapi/nf-tapi-linemonitormedia), [**ligne \_ MONITORMEDIA**](./line-monitormedia.md) message, [LINEMEDIAMODE \_ constants](./linemediamode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="54543-109">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**lineSetMediaMode**](/windows/win32/api/tapi/nf-tapi-linesetmediamode), [**lineMonitorMedia**](/windows/win32/api/tapi/nf-tapi-linemonitormedia), [**LINE\_MONITORMEDIA**](./line-monitormedia.md) message, [LINEMEDIAMODE\_ Constants](./linemediamode--constants.md).</span></span>

<span data-ttu-id="54543-110">**TAPI 3. x :** Consultez [**ITCallInfo :: obtenir \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) avec **CIL \_ MEDIATYPESAVAILABLE**, [**ITCallInfo ::p ut \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) avec **CIL \_ MEDIATYPESAVAILABLE**, [**ITCallInfoChangeEvent :: obtenir la \_ cause**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) (retourne la [**\_ cause CALLINFOCHANGE**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause) du **\_ MediaType CIC**), [TAPIMEDIATYPE \_ constantes](tapimediatype--constants.md).</span><span class="sxs-lookup"><span data-stu-id="54543-110">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) with **CIL\_MEDIATYPESAVAILABLE**, [**ITCallInfo::put\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) with **CIL\_MEDIATYPESAVAILABLE**, [**ITCallInfoChangeEvent::get\_Cause**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) (returns [**CALLINFOCHANGE\_CAUSE**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause) of **CIC\_MEDIATYPE**), [TAPIMEDIATYPE\_ Constants](tapimediatype--constants.md).</span></span>

 

 
