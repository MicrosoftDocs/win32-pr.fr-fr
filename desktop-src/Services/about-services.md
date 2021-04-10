---
description: Le gestionnaire de contrôle des services (SCM) gère une base de données des services installés et des services de pilotes, et fournit un moyen unifié et sécurisé de les contrôler.
ms.assetid: a3af8340-d367-417b-9759-7282edf1d694
title: À propos des services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87aeec6dfcdc4e2dc0cc0ab3ef084b7927b2c3bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952365"
---
# <a name="about-services"></a><span data-ttu-id="a6862-103">À propos des services</span><span class="sxs-lookup"><span data-stu-id="a6862-103">About Services</span></span>

<span data-ttu-id="a6862-104">Le [Gestionnaire de contrôle](service-control-manager.md) des services (SCM) gère une base de données des services installés et des services de pilotes, et fournit un moyen unifié et sécurisé de les contrôler.</span><span class="sxs-lookup"><span data-stu-id="a6862-104">The [service control manager](service-control-manager.md) (SCM) maintains a database of installed services and driver services, and provides a unified and secure means of controlling them.</span></span> <span data-ttu-id="a6862-105">La base de données contient des informations sur la façon dont chaque service ou service de pilote doit être démarré.</span><span class="sxs-lookup"><span data-stu-id="a6862-105">The database includes information on how each service or driver service should be started.</span></span> <span data-ttu-id="a6862-106">Il permet également aux administrateurs système de personnaliser les exigences de sécurité pour chaque service et ainsi de contrôler l’accès au service.</span><span class="sxs-lookup"><span data-stu-id="a6862-106">It also enables system administrators to customize security requirements for each service and thereby control access to the service.</span></span>

<span data-ttu-id="a6862-107">Les types de programmes suivants utilisent les fonctions fournies par le SCM.</span><span class="sxs-lookup"><span data-stu-id="a6862-107">The following types of programs use the functions provided by the SCM.</span></span>



| <span data-ttu-id="a6862-108">Type</span><span class="sxs-lookup"><span data-stu-id="a6862-108">Type</span></span>                          | <span data-ttu-id="a6862-109">Description</span><span class="sxs-lookup"><span data-stu-id="a6862-109">Description</span></span>                                                                                                                                                                                                                                                                                                                               |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6862-110">Programme de service</span><span class="sxs-lookup"><span data-stu-id="a6862-110">Service program</span></span>               | <span data-ttu-id="a6862-111">Programme qui fournit du code exécutable pour un ou plusieurs services.</span><span class="sxs-lookup"><span data-stu-id="a6862-111">A program that provides executable code for one or more services.</span></span> <span data-ttu-id="a6862-112">Les programmes de service utilisent des fonctions qui se connectent au SCM et envoient des informations d’État au SCM.</span><span class="sxs-lookup"><span data-stu-id="a6862-112">Service programs use functions that connect to the SCM and send status information to the SCM.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="a6862-113">Programme de configuration de service</span><span class="sxs-lookup"><span data-stu-id="a6862-113">Service configuration program</span></span> | <span data-ttu-id="a6862-114">Programme qui interroge ou modifie la base de données de services.</span><span class="sxs-lookup"><span data-stu-id="a6862-114">A program that queries or modifies the services database.</span></span> <span data-ttu-id="a6862-115">Les programmes de configuration de service utilisent des fonctions qui ouvrent la base de données, installent ou suppriment des services dans la base de données, puis interrogent ou modifient les paramètres de configuration et de sécurité pour les services installés.</span><span class="sxs-lookup"><span data-stu-id="a6862-115">Service configuration programs use functions that open the database, install or delete services in the database, and query or modify the configuration and security parameters for installed services.</span></span> <span data-ttu-id="a6862-116">Les programmes de configuration de service gèrent les services et les pilotes.</span><span class="sxs-lookup"><span data-stu-id="a6862-116">Service configuration programs manage both services and driver services.</span></span> |
| <span data-ttu-id="a6862-117">Programme de contrôle de service</span><span class="sxs-lookup"><span data-stu-id="a6862-117">Service control program</span></span>       | <span data-ttu-id="a6862-118">Programme qui démarre et contrôle les services et les services de pilotes.</span><span class="sxs-lookup"><span data-stu-id="a6862-118">A program that starts and controls services and driver services.</span></span> <span data-ttu-id="a6862-119">Les programmes de contrôle de service utilisent des fonctions qui envoient des demandes au SCM, qui exécute la demande.</span><span class="sxs-lookup"><span data-stu-id="a6862-119">Service control programs use functions that send requests to the SCM, which carries out the request.</span></span>                                                                                                                                                                     |



 

<span data-ttu-id="a6862-120">Cette vue d’ensemble aborde les sujets suivants :</span><span class="sxs-lookup"><span data-stu-id="a6862-120">This overview discusses the following topics:</span></span>

-   [<span data-ttu-id="a6862-121">Gestionnaire de contrôle des services</span><span class="sxs-lookup"><span data-stu-id="a6862-121">Service Control Manager</span></span>](service-control-manager.md)
-   [<span data-ttu-id="a6862-122">Programmes de service</span><span class="sxs-lookup"><span data-stu-id="a6862-122">Service Programs</span></span>](service-programs.md)
-   [<span data-ttu-id="a6862-123">Programmes de configuration de service</span><span class="sxs-lookup"><span data-stu-id="a6862-123">Service Configuration Programs</span></span>](service-configuration-programs.md)
-   [<span data-ttu-id="a6862-124">Programmes de contrôle de service</span><span class="sxs-lookup"><span data-stu-id="a6862-124">Service Control Programs</span></span>](service-control-programs.md)
-   [<span data-ttu-id="a6862-125">Comptes d’utilisateur de service</span><span class="sxs-lookup"><span data-stu-id="a6862-125">Service User Accounts</span></span>](service-user-accounts.md)
-   [<span data-ttu-id="a6862-126">Services interactifs</span><span class="sxs-lookup"><span data-stu-id="a6862-126">Interactive Services</span></span>](interactive-services.md)
-   [<span data-ttu-id="a6862-127">Sécurité des services et droits d’accès</span><span class="sxs-lookup"><span data-stu-id="a6862-127">Service Security and Access Rights</span></span>](service-security-and-access-rights.md)
-   [<span data-ttu-id="a6862-128">Déboguer un service</span><span class="sxs-lookup"><span data-stu-id="a6862-128">Debugging a Service</span></span>](debugging-a-service.md)
-   [<span data-ttu-id="a6862-129">Événements de déclencheur de service</span><span class="sxs-lookup"><span data-stu-id="a6862-129">Service Trigger Events</span></span>](service-trigger-events.md)

 

 



