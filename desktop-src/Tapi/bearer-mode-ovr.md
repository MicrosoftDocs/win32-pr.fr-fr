---
description: Le mode porteur correspond à la qualité de transmission demandée à partir du réseau pour l’établissement d’un appel.
ms.assetid: 5276e1e7-7a91-4b74-b8c2-c0c7cebb203f
title: Mode porteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1780bee44254e6da754584f838785452ee728f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202195"
---
# <a name="bearer-mode"></a><span data-ttu-id="1c995-103">Mode porteur</span><span class="sxs-lookup"><span data-stu-id="1c995-103">Bearer Mode</span></span>

<span data-ttu-id="1c995-104">Le [**mode porteur**](./linebearermode--constants.md) correspond à la qualité de transmission demandée à partir du réseau pour l’établissement d’un appel.</span><span class="sxs-lookup"><span data-stu-id="1c995-104">The [**bearer mode**](./linebearermode--constants.md) corresponds to the quality of transmission requested from the network for establishing a call.</span></span> <span data-ttu-id="1c995-105">Il est important de conserver le concept de mode porteur distinct de celui du [**type de média**](tapimediatype--constants.md).</span><span class="sxs-lookup"><span data-stu-id="1c995-105">It is important to keep the concept of bearer mode separate from that of [**media type**](tapimediatype--constants.md).</span></span> <span data-ttu-id="1c995-106">Par exemple, le réseau téléphonique analogique (RTPC) fournit uniquement un mode de prise en charge de la voix de 3,1 kHz, mais les appels qui l’utilisent peuvent prendre en charge des types de médias tels que la voix, la télécopie ou le modem de données.</span><span class="sxs-lookup"><span data-stu-id="1c995-106">As an example, the analog telephone network (PSTN) provides only a 3.1 kHz voice-grade bearer mode but calls using it can support media types such as voice, fax, or data modem.</span></span>

<span data-ttu-id="1c995-107">Le mode de porteur d’un appel est spécifié lorsque l’appel est configuré ou est fourni lorsque l’appel est proposé.</span><span class="sxs-lookup"><span data-stu-id="1c995-107">The bearer mode of a call is specified when the call is set up, or is provided when the call is offered.</span></span> <span data-ttu-id="1c995-108">Avec les appareils de ligne capables de représenter des pools de canaux, il est possible qu’un fournisseur de services autorise l’établissement d’appels avec une plus grande bande passante.</span><span class="sxs-lookup"><span data-stu-id="1c995-108">With line devices able to represent channel pools, it is possible for a service provider to allow calls to be established with wider bandwidth.</span></span>

<span data-ttu-id="1c995-109">Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.</span><span class="sxs-lookup"><span data-stu-id="1c995-109">Not all service providers support use of this information.</span></span>

<span data-ttu-id="1c995-110">**TAPI 2. x :** Consultez [**lineSetCallParams**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwBearerMode** membre de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo).</span><span class="sxs-lookup"><span data-stu-id="1c995-110">**TAPI 2.x:** See [**lineSetCallParams**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwBearerMode** member of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo).</span></span>

<span data-ttu-id="1c995-111">**TAPI 3. x :** Consultez [**ITCallInfo :: obtenir \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo ::p ut \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **CIL \_ BEARERMODE** Member of [**CALLINFO \_ long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span><span class="sxs-lookup"><span data-stu-id="1c995-111">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::put\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **CIL\_BEARERMODE** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span></span>

<span data-ttu-id="1c995-112">**TSPI :** Consultez la [**ligne \_ CALLINFO**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) message, avec *dwParam1* défini sur LINECALLINFOSTATE \_ BEARERMODE.</span><span class="sxs-lookup"><span data-stu-id="1c995-112">**TSPI:** See [**LINE\_CALLINFO**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) message, with *dwParam1* set to LINECALLINFOSTATE\_BEARERMODE.</span></span>

 

 
