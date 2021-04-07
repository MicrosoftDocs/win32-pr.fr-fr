---
title: Fonctionnement de SNMP
description: Comment une application de console de gestion SNMP tierce retourne des informations du service SNMP.
ms.assetid: 2edbf9ff-b9e3-4103-affc-a5c0f22b80a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d58943f0765b60f9c235094642d3fa759402db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939823"
---
# <a name="how-snmp-works"></a>Fonctionnement de SNMP

Les étapes suivantes décrivent comment une application de console de gestion SNMP tierce retourne des informations à partir du service SNMP :

1.  L’application de la console de gestion SNMP formule un message SNMP basé sur l’entrée de l’utilisateur. Le message comprend une unité de données de protocole (PDU) et des informations d’authentification. L’application console de gestion peut utiliser la bibliothèque de l’API de gestion SNMP Microsoft (MGMTAPI.DLL) ou la bibliothèque de l' [API WinSNMP](winsnmp-api.md) microsoft (WSNMP32.DLL) pour effectuer cette étape.
2.  L’application de la console de gestion SNMP envoie le message SNMP au service SNMP, à l’aide des bibliothèques de service SNMP.
3.  Le service SNMP reçoit la demande. Il vérifie les informations d’authentification et l’adresse IP source.
4.  Le service SNMP sélectionne l’agent d’extension approprié et demande que l’agent récupère les informations demandées.
5.  Le service SNMP envoie la réponse à l’application de la console de gestion SNMP.

 

 




