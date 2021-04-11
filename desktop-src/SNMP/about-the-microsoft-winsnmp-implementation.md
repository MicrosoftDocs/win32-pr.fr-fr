---
title: À propos de l’implémentation de Microsoft WinSNMP
description: L’implémentation de Microsoft WinSNMP est conforme à la version 2,0 de WinSNMP.
ms.assetid: 99e11d30-d159-4d9b-94d0-baa6e49d82cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cbf142ba85458374105af5b80ca5af30a6c5082
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939557"
---
# <a name="about-the-microsoft-winsnmp-implementation"></a><span data-ttu-id="c4778-103">À propos de l’implémentation de Microsoft WinSNMP</span><span class="sxs-lookup"><span data-stu-id="c4778-103">About the Microsoft WinSNMP Implementation</span></span>

<span data-ttu-id="c4778-104">L’implémentation de Microsoft WinSNMP est conforme à la version 2,0 de WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="c4778-104">The Microsoft WinSNMP implementation complies with WinSNMP version 2.0.</span></span> <span data-ttu-id="c4778-105">Il prend en charge toutes les fonctions et opérations définies à la fois dans les spécifications de la version 1.1 de WinSNMP et dans l’addenda de la version 2,0 de l’WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="c4778-105">It supports all the functions and operations defined in both the WinSNMP version 1.1a specification and the WinSNMP version 2.0 Addendum.</span></span> <span data-ttu-id="c4778-106">L’implémentation fournit les services suivants pour les applications WinSNMP :</span><span class="sxs-lookup"><span data-stu-id="c4778-106">The implementation provides the following services for WinSNMP applications:</span></span>

-   <span data-ttu-id="c4778-107">Gère les communications vers et à partir des entités de gestion.</span><span class="sxs-lookup"><span data-stu-id="c4778-107">Manages communications to and from management entities.</span></span> <span data-ttu-id="c4778-108">L’entité peut résider sur l’ordinateur local ou être connectée via un réseau local ou étendu, ou Internet.</span><span class="sxs-lookup"><span data-stu-id="c4778-108">The entity can reside on the local computer or be connected through a local or wide-area network, or the Internet.</span></span> <span data-ttu-id="c4778-109">Pour plus d’informations, consultez [niveaux de prise en charge de SNMP](levels-of-snmp-support.md).</span><span class="sxs-lookup"><span data-stu-id="c4778-109">For more information, see [Levels of SNMP Support](levels-of-snmp-support.md).</span></span>
-   <span data-ttu-id="c4778-110">Masque les détails du protocole SNMP, le ASN (Abstract Syntax Notation One) et les règles de codage de base (BER) pour décrire la syntaxe de transfert.</span><span class="sxs-lookup"><span data-stu-id="c4778-110">Hides the details of SNMP protocol, Abstract Syntax Notation One (ASN.1), and the Basic Encoding Rules (BER) for describing transfer syntax.</span></span>
-   <span data-ttu-id="c4778-111">Vérifie l’exactitude des PDU et rejette les PDU non valides.</span><span class="sxs-lookup"><span data-stu-id="c4778-111">Verifies the correctness of PDUs and rejects invalid PDUs.</span></span> <span data-ttu-id="c4778-112">Pour plus d’informations, consultez [utilisation des unités de données de protocole](working-with-protocol-data-units.md).</span><span class="sxs-lookup"><span data-stu-id="c4778-112">For more information, see [Working with Protocol Data Units](working-with-protocol-data-units.md).</span></span>
-   <span data-ttu-id="c4778-113">Transforme les types de PDU SNMPv2C lorsque cela est nécessaire conformément aux RFC pertinentes.</span><span class="sxs-lookup"><span data-stu-id="c4778-113">Transforms SNMPv2C PDU types when necessary in accordance with the relevant RFCs.</span></span>
-   <span data-ttu-id="c4778-114">Convertit les interruptions SNMPv1 d’un agent SNMPv1 en interruptions SNMPv2C, conformément à la norme RFC 1908, « coexistence entre la version 1 et la version 2 de l’infrastructure de gestion de réseau Internet standard ».</span><span class="sxs-lookup"><span data-stu-id="c4778-114">Converts SNMPv1 traps from an SNMPv1 agent to SNMPv2C traps in accordance with RFC 1908, "Coexistence between Version 1 and Version 2 of the Internet-standard Network Management Framework."</span></span> <span data-ttu-id="c4778-115">Pour plus d’informations, consultez [conversion d’interruptions de SNMPv1 en SNMPv2C](translating-traps-from-snmpv1-to-snmpv2c.md).</span><span class="sxs-lookup"><span data-stu-id="c4778-115">For more information, see [Translating Traps from SNMPv1 to SNMPv2C](translating-traps-from-snmpv1-to-snmpv2c.md).</span></span>
-   <span data-ttu-id="c4778-116">Prend en charge la stratégie de retransmission de l’application et fournit la prise en charge de l’exécution de la retransmission.</span><span class="sxs-lookup"><span data-stu-id="c4778-116">Supports the application's retransmission policy and provides retransmission execution support.</span></span> <span data-ttu-id="c4778-117">Pour plus d’informations, consultez [la base de données WinSNMP](the-winsnmp-database.md) et [à propos de la retransmission](about-retransmission.md).</span><span class="sxs-lookup"><span data-stu-id="c4778-117">For more information, see [The WinSNMP Database](the-winsnmp-database.md) and [About Retransmission](about-retransmission.md).</span></span>
-   <span data-ttu-id="c4778-118">Fournit la prise en charge de la traduction des entités et des contextes pour l’application.</span><span class="sxs-lookup"><span data-stu-id="c4778-118">Provides entity and context translation support for the application.</span></span> <span data-ttu-id="c4778-119">Pour plus d’informations, consultez [la base de données WinSNMP](the-winsnmp-database.md) et [définition de l’entité et du mode de traduction du contexte](setting-the-entity-and-context-translation-mode.md).</span><span class="sxs-lookup"><span data-stu-id="c4778-119">For more information, see [The WinSNMP Database](the-winsnmp-database.md) and [Setting the Entity and Context Translation Mode](setting-the-entity-and-context-translation-mode.md).</span></span>

<span data-ttu-id="c4778-120">Pour plus d’informations sur la relation entre une application WinSNMP et l’implémentation, consultez l’article sur les [concepts de gestion des données WinSNMP](winsnmp-data-management-concepts.md) et les [sessions WinSNMP](winsnmp-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="c4778-120">For additional information about the relationship between a WinSNMP application and the implementation, see [WinSNMP Data Management Concepts](winsnmp-data-management-concepts.md) and [WinSNMP Sessions](winsnmp-sessions.md).</span></span>

 

 




