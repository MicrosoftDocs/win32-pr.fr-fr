---
title: Fonctionnement de SNMP
description: Comment une application de console de gestion SNMP tierce retourne des informations du service SNMP.
ms.assetid: 2edbf9ff-b9e3-4103-affc-a5c0f22b80a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1feb82b50a954ef96310b887b9fc6e73694242b639a354cd29a5c328c43daf5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009467"
---
# <a name="how-snmp-works"></a>Fonctionnement de SNMP

Les étapes suivantes décrivent comment une application de console de gestion SNMP tierce retourne des informations à partir du service SNMP :

1.  L’application de la console de gestion SNMP formule un message SNMP basé sur l’entrée de l’utilisateur. Le message comprend une unité de données de protocole (PDU) et des informations d’authentification. L’application console de gestion peut utiliser la bibliothèque de l’API de gestion SNMP Microsoft (MGMTAPI.DLL) ou la bibliothèque de l' [API WinSNMP](winsnmp-api.md) microsoft (WSNMP32.DLL) pour effectuer cette étape.
2.  L’application de la console de gestion SNMP envoie le message SNMP au service SNMP, à l’aide des bibliothèques de service SNMP.
3.  Le service SNMP reçoit la demande. Il vérifie les informations d’authentification et l’adresse IP source.
4.  Le service SNMP sélectionne l’agent d’extension approprié et demande que l’agent récupère les informations demandées.
5.  Le service SNMP envoie la réponse à l’application de la console de gestion SNMP.

 

 




