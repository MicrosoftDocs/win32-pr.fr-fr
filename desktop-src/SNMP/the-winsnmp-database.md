---
title: La base de données WinSNMP
description: L’implémentation de Microsoft WinSNMP gère un magasin d’informations administratives dans une base de données.
ms.assetid: 0a0d9731-d800-4eaa-8230-25469a0b0285
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea83573cad12c05f6dd4b7e2375df5941e05fadb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462134"
---
# <a name="the-winsnmp-database"></a><span data-ttu-id="82ea5-103">La base de données WinSNMP</span><span class="sxs-lookup"><span data-stu-id="82ea5-103">The WinSNMP Database</span></span>

<span data-ttu-id="82ea5-104">L’implémentation de Microsoft WinSNMP gère un magasin d’informations administratives dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="82ea5-104">The Microsoft WinSNMP implementation maintains a store of administrative information in a database.</span></span> <span data-ttu-id="82ea5-105">La base de données comprend les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="82ea5-105">The database includes the following information:</span></span>

-   <span data-ttu-id="82ea5-106">Propriétés du réseau et de la version.</span><span class="sxs-lookup"><span data-stu-id="82ea5-106">Network and version properties.</span></span>

    <span data-ttu-id="82ea5-107">L’implémentation utilise ces propriétés pour déterminer le protocole de transport réseau et la structure de la version SNMP à utiliser pour effectuer les demandes de transmission.</span><span class="sxs-lookup"><span data-stu-id="82ea5-107">The implementation uses these properties to determine which network transport protocol and SNMP version framework to use to complete transmission requests.</span></span> <span data-ttu-id="82ea5-108">Pour plus d’informations, consultez [à propos des versions SNMP](about-snmp-versions.md).</span><span class="sxs-lookup"><span data-stu-id="82ea5-108">For more information, see [About SNMP Versions](about-snmp-versions.md).</span></span>

-   <span data-ttu-id="82ea5-109">Mode de traduction entité et contexte.</span><span class="sxs-lookup"><span data-stu-id="82ea5-109">Entity and context translation mode.</span></span>

    <span data-ttu-id="82ea5-110">L’implémentation utilise ce mode pour interpréter des noms conviviaux pour les entités et les contextes SNMP.</span><span class="sxs-lookup"><span data-stu-id="82ea5-110">The implementation uses this mode to interpret user-friendly names for SNMP entities and contexts.</span></span> <span data-ttu-id="82ea5-111">Pour plus d’informations, consultez [définition du mode de traduction entité et contexte](setting-the-entity-and-context-translation-mode.md).</span><span class="sxs-lookup"><span data-stu-id="82ea5-111">For more information, see [Setting the Entity and Context Translation Mode](setting-the-entity-and-context-translation-mode.md).</span></span>

-   <span data-ttu-id="82ea5-112">Paramètre de stratégie de retransmission.</span><span class="sxs-lookup"><span data-stu-id="82ea5-112">Retransmission policy setting.</span></span>

    <span data-ttu-id="82ea5-113">L’implémentation utilise ce paramètre pour déterminer s’il doit ou non exécuter la stratégie de retransmission de l’application.</span><span class="sxs-lookup"><span data-stu-id="82ea5-113">The implementation uses this setting to determine whether or not it should execute the application's retransmission policy.</span></span> <span data-ttu-id="82ea5-114">L’implémentation stocke une valeur de délai d’attente et un nombre de tentatives pour chaque entité de destination.</span><span class="sxs-lookup"><span data-stu-id="82ea5-114">The implementation stores a time-out value and a retry count for each destination entity.</span></span> <span data-ttu-id="82ea5-115">Pour plus d’informations, consultez [à propos de la retransmission](about-retransmission.md) et de [la gestion de la stratégie de retransmission](managing-the-retransmission-policy.md).</span><span class="sxs-lookup"><span data-stu-id="82ea5-115">For more information, see [About Retransmission](about-retransmission.md) and [Managing the Retransmission Policy](managing-the-retransmission-policy.md).</span></span>

 

 




