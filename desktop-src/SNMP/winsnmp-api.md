---
title: API WinSNMP
description: L’interface de programmation d’applications SNMP de Microsoft Windows (l’API WinSNMP) versions 1.1 a et 2,0 vous permettent de développer des applications de gestion de réseau basées sur SNMP qui s’exécutent dans l’environnement Windows.
ms.assetid: 54d9b61a-815a-41c3-9365-ec4478acc3f2
keywords:
- API WinSNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12d502060daa2931ca67c4476448347602159c98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031575"
---
# <a name="winsnmp-api"></a><span data-ttu-id="f43a1-104">API WinSNMP</span><span class="sxs-lookup"><span data-stu-id="f43a1-104">WinSNMP API</span></span>

<span data-ttu-id="f43a1-105">\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="f43a1-105">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f43a1-106">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="f43a1-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="f43a1-107">Utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="f43a1-107">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="f43a1-108">L’interface de programmation d’applications SNMP de Microsoft Windows (l’API WinSNMP) versions 1.1 a et 2,0 vous permettent de développer des applications de gestion de réseau basées sur SNMP qui s’exécutent dans l’environnement Windows.</span><span class="sxs-lookup"><span data-stu-id="f43a1-108">The Microsoft Windows SNMP Application Programming Interface (the WinSNMP API) versions 1.1a and 2.0 allow you to develop SNMP-based network management applications that execute in the Windows environment.</span></span> <span data-ttu-id="f43a1-109">Le protocole SNMP (simple Network Management Protocol) est un protocole de requête-réponse qui transfère les informations de gestion entre les entités de protocole.</span><span class="sxs-lookup"><span data-stu-id="f43a1-109">The Simple Network Management Protocol (SNMP) is a request-response protocol that transfers management information between protocol entities.</span></span>

<span data-ttu-id="f43a1-110">WinSNMP a été développé conjointement avec la collaboration, l’entrée et la prise en charge de plusieurs sociétés, associations et individus.</span><span class="sxs-lookup"><span data-stu-id="f43a1-110">WinSNMP has been jointly developed with the cooperation, input, and support from several companies, associations and individuals.</span></span>

<span data-ttu-id="f43a1-111">La première partie de cette vue d’ensemble fournit des informations sur l’Addendum 2,0 de WinSNMP, les versions SNMP et une liste des RFC (Request for Comments) appropriées.</span><span class="sxs-lookup"><span data-stu-id="f43a1-111">The first part of this overview provides information about the WinSNMP 2.0 Addendum, SNMP versions, and a list of the relevant Requests for Comments (RFCs).</span></span> <span data-ttu-id="f43a1-112">Il décrit également le modèle WinSNMP, ainsi que les composants et fonctionnalités de l’implémentation de Microsoft WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="f43a1-112">It also describes the WinSNMP model, and the components and features of the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="f43a1-113">Il fournit également des informations sur les concepts de gestion et de communication des données que vous devez programmer dans l’environnement WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="f43a1-113">It also provides information about data management and communications concepts you need to program in the WinSNMP environment.</span></span>

<span data-ttu-id="f43a1-114">La deuxième section traite des fonctions WinSNMP et des tâches de programmation WinSNMP associées suivantes :</span><span class="sxs-lookup"><span data-stu-id="f43a1-114">The second section discusses the WinSNMP functions and the following related WinSNMP programming tasks:</span></span>

-   [<span data-ttu-id="f43a1-115">Ouverture et fermeture d’une application WinSNMP</span><span class="sxs-lookup"><span data-stu-id="f43a1-115">Opening and closing a WinSNMP application</span></span>](opening-and-closing-a-winsnmp-application.md)
-   [<span data-ttu-id="f43a1-116">Ouverture et fermeture d’une session WinSNMP</span><span class="sxs-lookup"><span data-stu-id="f43a1-116">Opening and closing a WinSNMP session</span></span>](opening-and-closing-a-winsnmp-session.md)
-   [<span data-ttu-id="f43a1-117">Gestion des interruptions et des notifications</span><span class="sxs-lookup"><span data-stu-id="f43a1-117">Managing traps and notifications</span></span>](managing-traps-and-notifications.md)
-   [<span data-ttu-id="f43a1-118">Utilisation des listes de liaisons de variables</span><span class="sxs-lookup"><span data-stu-id="f43a1-118">Working with variable binding lists</span></span>](working-with-variable-binding-lists.md)
-   [<span data-ttu-id="f43a1-119">Utilisation d’unités de données de protocole</span><span class="sxs-lookup"><span data-stu-id="f43a1-119">Working with protocol data units</span></span>](working-with-protocol-data-units.md)
-   [<span data-ttu-id="f43a1-120">Envoi de messages SNMP</span><span class="sxs-lookup"><span data-stu-id="f43a1-120">Sending SNMP messages</span></span>](sending-snmp-messages.md)
-   [<span data-ttu-id="f43a1-121">Réception des messages SNMP</span><span class="sxs-lookup"><span data-stu-id="f43a1-121">Receiving SNMP messages</span></span>](receiving-snmp-messages.md)
-   [<span data-ttu-id="f43a1-122">Gestion des identificateurs d’objets</span><span class="sxs-lookup"><span data-stu-id="f43a1-122">Managing object identifiers</span></span>](managing-object-identifiers.md)
-   [<span data-ttu-id="f43a1-123">Libération des descripteurs WinSNMP</span><span class="sxs-lookup"><span data-stu-id="f43a1-123">Freeing WinSNMP descriptors</span></span>](freeing-winsnmp-descriptors.md)
-   [<span data-ttu-id="f43a1-124">Définition du mode de traduction entité et contexte</span><span class="sxs-lookup"><span data-stu-id="f43a1-124">Setting the entity and context translation mode</span></span>](setting-the-entity-and-context-translation-mode.md)
-   [<span data-ttu-id="f43a1-125">Gestion de la stratégie de retransmission</span><span class="sxs-lookup"><span data-stu-id="f43a1-125">Managing the retransmission policy</span></span>](managing-the-retransmission-policy.md)
-   [<span data-ttu-id="f43a1-126">Écriture d’applications WinSNMP avec plusieurs threads</span><span class="sxs-lookup"><span data-stu-id="f43a1-126">Writing WinSNMP applications with multiple threads</span></span>](writing-winsnmp-applications-with-multiple-threads.md)
-   [<span data-ttu-id="f43a1-127">Inscription d’une application d’agent SNMP</span><span class="sxs-lookup"><span data-stu-id="f43a1-127">Registering an SNMP agent application</span></span>](registering-an-snmp-agent-application.md)

<span data-ttu-id="f43a1-128">Avant de lire cette vue d’ensemble, vous devez être familiarisé avec les concepts de base de la programmation SNMP et Windows.</span><span class="sxs-lookup"><span data-stu-id="f43a1-128">You should be familiar with the basic concepts of SNMP and Windows programming before reading this overview.</span></span> <span data-ttu-id="f43a1-129">Pour plus d’informations sur SNMP, voir [protocole de gestion de réseau simple](simple-network-management-protocol-snmp-.md) et les RFC (Request for Comments) pertinents publiés par l’IETF (Internet Engineering Task Force).</span><span class="sxs-lookup"><span data-stu-id="f43a1-129">For more information about SNMP, see [Simple Network Management Protocol](simple-network-management-protocol-snmp-.md) and the relevant Requests for Comments (RFCs) which are published by the Internet Engineering Task Force (IETF).</span></span>

 

 