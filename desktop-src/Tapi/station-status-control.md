---
description: Trois fonctions principales d’état de station requièrent le contrôle des éclairages de message en attente, le transfert et la non-perturbation.
ms.assetid: 4a6dc47f-caff-4f2b-8858-0e9bec32b137
title: Contrôle de l’état de la station
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e136450dbda8cec260a460f49ce8d45b65d1b58ec588ccbcc435c5e3a2b1cd7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118861932"
---
# <a name="station-status-control"></a>Contrôle de l’état de la station

Trois fonctions principales d’état de station nécessitent un contrôle : les lumières de message en attente, le transfert et la non-perturbation. Le transfert et le fait de ne pas déranger sont contrôlable via la fonction [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) existante (qui est spécifique à l’adresse) et interrogées à l’aide de [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus). Le \_ bit LINEDEVSTATUSFLAGS MSGWAIT du membre **DwDevStatusFlags** de [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) indique l’état du message en attente sur l’appareil, et un message LINEDEVSTATE MSGWAITON ou LINEDEVSTATE MSGWAITOFF \_ \_ est envoyé pour indiquer le moment où l’état change. La fonction [**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) permet de contrôler le signal d’attente du message sans avoir à implémenter un périphérique téléphonique TAPI uniquement à cet effet. Le \_ bit LINEFEATURE SETDEVSTATUS (dans le membre **DwLineFeatures** de [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) et **LINEDEVSTATUS**) indique quand il peut être appelé, et le membre **dwSettableDevStatus** de **LINEDEVCAPS** permet à l’application de détecter les paramètres d’état des appareils qui peuvent être contrôlés à partir de l’application. En plus de permettre le contrôle de la fonctionnalité d’attente du message, cela permet également de définir l’état connecté, InService et verrouillé de l’appareil, dans la mesure où ils sont pris en charge par le commutateur ou un autre matériel. Les appels à cette fonction entraînent l’envoi des messages [**\_ LINEDEVSTATE de ligne**](line-linedevstate.md) appropriés pour refléter le nouvel État.

 

 



