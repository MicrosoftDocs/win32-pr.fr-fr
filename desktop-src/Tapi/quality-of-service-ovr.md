---
description: La mise en réseau ATM (Asynchronous Transfer Mode) est émergente dans le monde de l’informatique, et la prise en charge de la technologie ATM a été ajoutée à de nombreuses parties du système d’exploitation.
ms.assetid: 0ca0ecf3-2b67-4925-a6fc-3edfaad2c0e2
title: Qualité de service (API de téléphonie)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6525ced0b29d35482244c3c37f8382edbfcb9fd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867369"
---
# <a name="quality-of-service-telephony-api"></a>Qualité de service (API de téléphonie)

La mise en réseau ATM (Asynchronous Transfer Mode) est émergente dans le monde de l’informatique, et la prise en charge de la technologie ATM a été ajoutée à de nombreuses parties du système d’exploitation. L’interface TAPI prend également en charge des attributs clés pour établir des appels sur des installations ATM. Les plus importantes du point de vue d’une application sont la possibilité de demander, de négocier, de renégocier et de recevoir des indications de paramètres de qualité de service (QOS) sur les appels entrants et sortants.

Les informations de QOS dans TAPI sont échangées entre les applications et les fournisseurs de services dans les structures [**FLOWSPEC**](/windows/desktop/api/qos/ns-qos-flowspec) définies dans Windows sockets 2,0.

Les applications demandent la qualité de service (QOS) aux appels sortants en définissant les valeurs d’informations de session avant de démarrer une session de communication. Le fournisseur de services essaiera de fournir la qualité de service spécifiée et de faire échouer l’appel si ce n’est pas possible. L’application peut ensuite ajuster ses paramètres et retenter l’appel. Une fois qu’un appel est établi, une application peut demander une modification de la qualité de service (QOS).

L’interface TAPI fournit des notifications d’événements pour le propriétaire ou le contrôle des applications en cas de modification des niveaux de QOS.

La prise en charge de QOS n’est pas limitée aux transports ATM ; n’importe quel fournisseur de services peut implémenter des fonctionnalités QOS.

Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.

* * TAPI 2. x : * *[**lineSetCallQualityOfService**](/windows/win32/api/tapi/nf-tapi-linesetcallqualityofservice), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwSendingFlowspecSize**, **DwSendingFlowspecOffset**, **dwReceivingFlowspecSize** et **dwReceivingFlowspecOffset** membres de [**LINECALLPARAMS**](/windows/win32/api/tapi/ns-tapi-linecallparams)

* * TAPI 3. x : * *[**ITBasicCallControl :: SetQOS**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-setqos), [**ITQOSEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itqosevent)

 

 
