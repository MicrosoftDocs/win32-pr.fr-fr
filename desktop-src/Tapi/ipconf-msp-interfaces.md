---
description: Le MSP de conférence IP implémente plusieurs interfaces spécifiques au fournisseur pour le contrôle de participant. Ces interfaces sont exposées sur l’objet d’appel, si ce MSP est associé à l’appel.
ms.assetid: 01af2452-de2d-42ce-970d-82a83ae0b428
title: Interfaces MSP IPConf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edb3c04a93909d237ae25e06c3ed2e0fcc5db9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114927"
---
# <a name="ipconf-msp-interfaces"></a><span data-ttu-id="be98f-104">Interfaces MSP IPConf</span><span class="sxs-lookup"><span data-stu-id="be98f-104">IPConf MSP Interfaces</span></span>

<span data-ttu-id="be98f-105">\[ Les interfaces MSP IPConf ne sont pas utilisables dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="be98f-105">\[ The IPConf MSP Interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="be98f-106">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="be98f-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="be98f-107">Le MSP de conférence IP implémente plusieurs interfaces spécifiques au fournisseur pour le contrôle de participant.</span><span class="sxs-lookup"><span data-stu-id="be98f-107">The IP conferencing MSP implements several provider-specific interfaces for participant control.</span></span> <span data-ttu-id="be98f-108">Ces interfaces sont exposées sur l’objet d’appel, si ce MSP est associé à l’appel.</span><span class="sxs-lookup"><span data-stu-id="be98f-108">These interfaces are exposed on the call object, if this MSP is associated with the call.</span></span>

<span data-ttu-id="be98f-109">Les interfaces [**ITParticipantEvent**](itparticipantevent.md) et [**IEnumParticipant**](ienumparticipant.md) sont des objets autonomes et sont répertoriées ici pour des raisons de commodité de référence.</span><span class="sxs-lookup"><span data-stu-id="be98f-109">The [**ITParticipantEvent**](itparticipantevent.md) and [**IEnumParticipant**](ienumparticipant.md) interfaces are stand-alone objects, and are listed here for reference convenience.</span></span>



| <span data-ttu-id="be98f-110">Interface</span><span class="sxs-lookup"><span data-stu-id="be98f-110">Interface</span></span>                                            | <span data-ttu-id="be98f-111">Description</span><span class="sxs-lookup"><span data-stu-id="be98f-111">Description</span></span>                                                                                                                                               |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="be98f-112">**IMulticastControl**</span><span class="sxs-lookup"><span data-stu-id="be98f-112">**IMulticastControl**</span></span>](imulticastcontrol.md)       | <span data-ttu-id="be98f-113">Permet à une application de définir et d’obtenir le mode de bouclage ( [**\_ \_ mode de bouclage de multidiffusion**](multicast-loopback-mode.md)) pour un objet Conférence de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="be98f-113">Allows an application to set and get the loopback mode ( [**MULTICAST\_LOOPBACK\_MODE**](multicast-loopback-mode.md)) for a multicast conference object.</span></span> |
| [<span data-ttu-id="be98f-114">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="be98f-114">**ITParticipant**</span></span>](itparticipant.md)               | <span data-ttu-id="be98f-115">Permet à une application de récupérer des informations sur les participants aux conférences et d’obtenir des pointeurs vers les flux associés à ces participants.</span><span class="sxs-lookup"><span data-stu-id="be98f-115">Allows an application to retrieve information on conference participants, and get pointers to the streams associated with those participants.</span></span>             |
| [<span data-ttu-id="be98f-116">**ITParticipantControl**</span><span class="sxs-lookup"><span data-stu-id="be98f-116">**ITParticipantControl**</span></span>](itparticipantcontrol.md) | <span data-ttu-id="be98f-117">Permet à une application de récupérer des pointeurs vers les participants d’une conférence.</span><span class="sxs-lookup"><span data-stu-id="be98f-117">Allows an application to retrieve pointers to the participants in a conference.</span></span>                                                                           |
| [<span data-ttu-id="be98f-118">**ITParticipantEvent**</span><span class="sxs-lookup"><span data-stu-id="be98f-118">**ITParticipantEvent**</span></span>](itparticipantevent.md)     | <span data-ttu-id="be98f-119">Permet à une application de récupérer des informations sur les événements concernant un participant à la Conférence.</span><span class="sxs-lookup"><span data-stu-id="be98f-119">Allows an application to retrieve event information concerning a conference participant.</span></span>                                                                  |
| [<span data-ttu-id="be98f-120">**IEnumParticipant**</span><span class="sxs-lookup"><span data-stu-id="be98f-120">**IEnumParticipant**</span></span>](ienumparticipant.md)         | <span data-ttu-id="be98f-121">Énumère [**ITParticipant**](itparticipant.md).</span><span class="sxs-lookup"><span data-stu-id="be98f-121">Enumerates [**ITParticipant**](itparticipant.md).</span></span>                                                                                                        |



 

 

 



