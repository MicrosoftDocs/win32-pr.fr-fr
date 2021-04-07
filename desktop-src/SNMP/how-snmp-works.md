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
# <a name="how-snmp-works"></a><span data-ttu-id="dc4f1-103">Fonctionnement de SNMP</span><span class="sxs-lookup"><span data-stu-id="dc4f1-103">How SNMP Works</span></span>

<span data-ttu-id="dc4f1-104">Les étapes suivantes décrivent comment une application de console de gestion SNMP tierce retourne des informations à partir du service SNMP :</span><span class="sxs-lookup"><span data-stu-id="dc4f1-104">The following steps outline how a third-party SNMP management console application returns information from the SNMP service:</span></span>

1.  <span data-ttu-id="dc4f1-105">L’application de la console de gestion SNMP formule un message SNMP basé sur l’entrée de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dc4f1-105">The SNMP management console application formulates an SNMP message based on input from the user.</span></span> <span data-ttu-id="dc4f1-106">Le message comprend une unité de données de protocole (PDU) et des informations d’authentification.</span><span class="sxs-lookup"><span data-stu-id="dc4f1-106">The message includes a protocol data unit (PDU) and authentication information.</span></span> <span data-ttu-id="dc4f1-107">L’application console de gestion peut utiliser la bibliothèque de l’API de gestion SNMP Microsoft (MGMTAPI.DLL) ou la bibliothèque de l' [API WinSNMP](winsnmp-api.md) microsoft (WSNMP32.DLL) pour effectuer cette étape.</span><span class="sxs-lookup"><span data-stu-id="dc4f1-107">The management console application can use the Microsoft SNMP Management API library (MGMTAPI.DLL) or the Microsoft [WinSNMP API](winsnmp-api.md) library (WSNMP32.DLL) to perform this step.</span></span>
2.  <span data-ttu-id="dc4f1-108">L’application de la console de gestion SNMP envoie le message SNMP au service SNMP, à l’aide des bibliothèques de service SNMP.</span><span class="sxs-lookup"><span data-stu-id="dc4f1-108">The SNMP management console application sends the SNMP message to the SNMP service, using the SNMP service libraries.</span></span>
3.  <span data-ttu-id="dc4f1-109">Le service SNMP reçoit la demande.</span><span class="sxs-lookup"><span data-stu-id="dc4f1-109">The SNMP service receives the request.</span></span> <span data-ttu-id="dc4f1-110">Il vérifie les informations d’authentification et l’adresse IP source.</span><span class="sxs-lookup"><span data-stu-id="dc4f1-110">It verifies the authentication information and the source IP address.</span></span>
4.  <span data-ttu-id="dc4f1-111">Le service SNMP sélectionne l’agent d’extension approprié et demande que l’agent récupère les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="dc4f1-111">The SNMP service selects the appropriate extension agent and requests that the agent retrieve the requested information.</span></span>
5.  <span data-ttu-id="dc4f1-112">Le service SNMP envoie la réponse à l’application de la console de gestion SNMP.</span><span class="sxs-lookup"><span data-stu-id="dc4f1-112">The SNMP service sends the response to the SNMP management console application.</span></span>

 

 




