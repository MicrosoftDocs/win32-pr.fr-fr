---
title: Suivi des modifications
description: Certaines applications doivent assurer la cohérence entre les données spécifiques stockées dans le service d’annuaire Active Directory et d’autres données.
ms.assetid: f4539482-1170-4c0c-b817-b39e58049d39
ms.tgt_platform: multiple
keywords:
- Active Directory, utilisation, suivi des modifications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dc772f883b97eb4e7305b39f0a582448a8bc021
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103940790"
---
# <a name="tracking-changes"></a><span data-ttu-id="dfd93-104">Suivi des modifications</span><span class="sxs-lookup"><span data-stu-id="dfd93-104">Tracking Changes</span></span>

<span data-ttu-id="dfd93-105">Certaines applications doivent assurer la cohérence entre les données spécifiques stockées dans le service d’annuaire Active Directory et d’autres données.</span><span class="sxs-lookup"><span data-stu-id="dfd93-105">Some applications must maintain consistency between specific data stored in the Active Directory directory service and other data.</span></span> <span data-ttu-id="dfd93-106">Les autres données peuvent être stockées dans le répertoire, dans une table SQL Server, dans un fichier ou dans le registre.</span><span class="sxs-lookup"><span data-stu-id="dfd93-106">The other data might be stored in the directory, in a SQL Server table, in a file, or in the registry.</span></span> <span data-ttu-id="dfd93-107">Lorsque les données stockées dans le répertoire changent, il peut être nécessaire de modifier les autres données afin de rester cohérentes.</span><span class="sxs-lookup"><span data-stu-id="dfd93-107">When data stored in the directory changes, the other data may be required to change in order to remain consistent.</span></span> <span data-ttu-id="dfd93-108">Les applications qui ont cette exigence sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="dfd93-108">Applications that have this requirement include:</span></span>

<span data-ttu-id="dfd93-109">Cette section ne couvre pas les mécanismes utilisés par les applications de surveillance.</span><span class="sxs-lookup"><span data-stu-id="dfd93-109">This section does not cover mechanisms used by monitoring applications.</span></span> <span data-ttu-id="dfd93-110">Il s’agit d’applications qui surveillent les modifications de l’annuaire afin de conserver des données cohérentes entre des magasins distincts, mais en tant qu’outil de gestion du système.</span><span class="sxs-lookup"><span data-stu-id="dfd93-110">These are applications that monitor directory changes not for the purpose of maintaining consistent data between separate stores, but as a system management tool.</span></span> <span data-ttu-id="dfd93-111">Bien que l’analyse des applications puisse utiliser les mêmes mécanismes que ceux qui prennent en charge les applications de suivi des modifications, les mécanismes suivants sont spécifiquement conçus pour la surveillance des applications :</span><span class="sxs-lookup"><span data-stu-id="dfd93-111">Although monitoring applications can use the same mechanisms that support change-tracking applications, the following mechanisms are specifically designed for monitoring applications:</span></span>

-   <span data-ttu-id="dfd93-112">Audit de sécurité.</span><span class="sxs-lookup"><span data-stu-id="dfd93-112">Security auditing.</span></span> <span data-ttu-id="dfd93-113">En modifiant la partie système de contrôle d’accès système (SACL) du descripteur de sécurité d’un objet, vous pouvez faire en sorte que les accès à l’objet sur un contrôleur de domaine donné génère des enregistrements d’audit dans le journal des événements de sécurité sur ce contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="dfd93-113">By modifying the system access-control list (SACL) portion of an object security descriptor, you can cause accesses to the object on a given domain controller to generate audit records in the security event log on that DC.</span></span> <span data-ttu-id="dfd93-114">Vous pouvez auditer les lectures, les écritures, ou les deux. vous pouvez auditer la totalité de l’objet ou des attributs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="dfd93-114">You can audit reads, writes, or both; you can audit the entire object or specific attributes.</span></span> <span data-ttu-id="dfd93-115">Pour plus d’informations, consultez [récupération de la liste SACL](retrieving-an-objectampaposs-sacl.md) et [génération d’audit](/windows/desktop/SecAuthZ/audit-generation)d’un objet.</span><span class="sxs-lookup"><span data-stu-id="dfd93-115">For more information, see [Retrieving an Object's SACL](retrieving-an-objectampaposs-sacl.md) and [Audit Generation](/windows/desktop/SecAuthZ/audit-generation).</span></span>
-   <span data-ttu-id="dfd93-116">Journalisation des événements</span><span class="sxs-lookup"><span data-stu-id="dfd93-116">Event logging.</span></span> <span data-ttu-id="dfd93-117">En modifiant les paramètres du Registre sur un contrôleur de domaine donné, vous pouvez modifier les types d’événements consignés dans le journal des événements du service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="dfd93-117">By modifying registry settings on a given domain controller, you can change the kinds of events logged to the directory service event log.</span></span> <span data-ttu-id="dfd93-118">Plus précisément, pour consigner toutes les modifications, affectez la valeur 4 à la valeur d' **accès au répertoire 8** sous la clé de Registre suivante.</span><span class="sxs-lookup"><span data-stu-id="dfd93-118">Specifically, to log all modifications, set the **8 Directory Access** value under the following registry key to 4.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Services
                NTDS
                   Diagnostics
    ```

    <span data-ttu-id="dfd93-119">Pour plus d’informations, consultez [journalisation des événements](/windows/desktop/EventLog/event-logging).</span><span class="sxs-lookup"><span data-stu-id="dfd93-119">For more information, see [Event Logging](/windows/desktop/EventLog/event-logging).</span></span>

-   <span data-ttu-id="dfd93-120">le suivi d’événement.</span><span class="sxs-lookup"><span data-stu-id="dfd93-120">Event tracing.</span></span> <span data-ttu-id="dfd93-121">Windows 2000 a introduit une API de suivi d’événements pour le suivi et la journalisation des événements intéressants dans les logiciels ou le matériel.</span><span class="sxs-lookup"><span data-stu-id="dfd93-121">Windows 2000 introduced an Event Tracing API for tracing and logging interesting events in software or hardware.</span></span> <span data-ttu-id="dfd93-122">Le système d’exploitation Windows, et Active Directory Domain Services en particulier, prennent en charge l’utilisation du suivi d’événements pour la planification de la capacité et l’analyse détaillée des performances.</span><span class="sxs-lookup"><span data-stu-id="dfd93-122">The Windows operating system, and Active Directory Domain Services in particular, support the use of event tracing for capacity planning and detailed performance analysis.</span></span> <span data-ttu-id="dfd93-123">Pour plus d’informations, consultez [suivi d’événements](/windows/desktop/ETW/event-tracing-portal) et [suivi d’événements dans ADSI](/windows/desktop/ADSI/adsi-and-etw).</span><span class="sxs-lookup"><span data-stu-id="dfd93-123">For more information, see [Event Tracing](/windows/desktop/ETW/event-tracing-portal) and [Event Tracing in ADSI](/windows/desktop/ADSI/adsi-and-etw).</span></span>

<span data-ttu-id="dfd93-124">Cette section comprend les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="dfd93-124">This section includes the following topics:</span></span>

-   [<span data-ttu-id="dfd93-125">Vue d’ensemble des techniques de Change Tracking</span><span class="sxs-lookup"><span data-stu-id="dfd93-125">Overview of Change Tracking Techniques</span></span>](overview-of-change-tracking-techniques.md)
-   [<span data-ttu-id="dfd93-126">Notifications de modifications dans Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="dfd93-126">Change Notifications in Active Directory Domain Services</span></span>](change-notifications-in-active-directory-domain-services.md)
-   [<span data-ttu-id="dfd93-127">Interrogation des modifications à l’aide du contrôle DirSync</span><span class="sxs-lookup"><span data-stu-id="dfd93-127">Polling for Changes Using the DirSync Control</span></span>](polling-for-changes-using-the-dirsync-control.md)
-   [<span data-ttu-id="dfd93-128">Interrogation des modifications à l’aide de USNChanged</span><span class="sxs-lookup"><span data-stu-id="dfd93-128">Polling for Changes Using USNChanged</span></span>](polling-for-changes-using-usnchanged.md)

 

 