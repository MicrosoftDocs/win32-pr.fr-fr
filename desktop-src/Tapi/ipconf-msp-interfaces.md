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
# <a name="ipconf-msp-interfaces"></a>Interfaces MSP IPConf

\[ Les interfaces MSP IPConf ne sont pas utilisables dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

Le MSP de conférence IP implémente plusieurs interfaces spécifiques au fournisseur pour le contrôle de participant. Ces interfaces sont exposées sur l’objet d’appel, si ce MSP est associé à l’appel.

Les interfaces [**ITParticipantEvent**](itparticipantevent.md) et [**IEnumParticipant**](ienumparticipant.md) sont des objets autonomes et sont répertoriées ici pour des raisons de commodité de référence.



| Interface                                            | Description                                                                                                                                               |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMulticastControl**](imulticastcontrol.md)       | Permet à une application de définir et d’obtenir le mode de bouclage ( [**\_ \_ mode de bouclage de multidiffusion**](multicast-loopback-mode.md)) pour un objet Conférence de multidiffusion. |
| [**ITParticipant**](itparticipant.md)               | Permet à une application de récupérer des informations sur les participants aux conférences et d’obtenir des pointeurs vers les flux associés à ces participants.             |
| [**ITParticipantControl**](itparticipantcontrol.md) | Permet à une application de récupérer des pointeurs vers les participants d’une conférence.                                                                           |
| [**ITParticipantEvent**](itparticipantevent.md)     | Permet à une application de récupérer des informations sur les événements concernant un participant à la Conférence.                                                                  |
| [**IEnumParticipant**](ienumparticipant.md)         | Énumère [**ITParticipant**](itparticipant.md).                                                                                                        |



 

 

 



