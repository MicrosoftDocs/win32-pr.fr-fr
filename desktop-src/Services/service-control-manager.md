---
description: Le gestionnaire de contrôle des services (SCM) est démarré au démarrage du système. Il s’agit d’un serveur d’appel de procédure distante (RPC), afin que les programmes de configuration de service et de contrôle de service puissent manipuler des services sur des ordinateurs distants.
ms.assetid: 56ad011d-17c4-4410-b598-6ef47fb3638f
title: Gestionnaire de contrôle des services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a8a35fd34bd2714d22d40ccf618c89a8b66a6c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516856"
---
# <a name="service-control-manager"></a><span data-ttu-id="efd0e-104">Gestionnaire de contrôle des services</span><span class="sxs-lookup"><span data-stu-id="efd0e-104">Service Control Manager</span></span>

<span data-ttu-id="efd0e-105">Le gestionnaire de contrôle des services (SCM) est démarré au démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="efd0e-105">The service control manager (SCM) is started at system boot.</span></span> <span data-ttu-id="efd0e-106">Il s’agit d’un serveur d’appel de procédure distante (RPC), afin que les programmes de configuration de service et de contrôle de service puissent manipuler des services sur des ordinateurs distants.</span><span class="sxs-lookup"><span data-stu-id="efd0e-106">It is a remote procedure call (RPC) server, so that service configuration and service control programs can manipulate services on remote machines.</span></span>

<span data-ttu-id="efd0e-107">Les fonctions de service fournissent une interface pour les tâches suivantes effectuées par le SCM :</span><span class="sxs-lookup"><span data-stu-id="efd0e-107">The service functions provide an interface for the following tasks performed by the SCM:</span></span>

-   <span data-ttu-id="efd0e-108">Maintenance de la base de données des services installés.</span><span class="sxs-lookup"><span data-stu-id="efd0e-108">Maintaining the database of installed services.</span></span>
-   <span data-ttu-id="efd0e-109">Démarrage des services et des services de pilote lors du démarrage du système ou à la demande.</span><span class="sxs-lookup"><span data-stu-id="efd0e-109">Starting services and driver services either upon system startup or upon demand.</span></span>
-   <span data-ttu-id="efd0e-110">Énumération des services installés et des services de pilote.</span><span class="sxs-lookup"><span data-stu-id="efd0e-110">Enumerating installed services and driver services.</span></span>
-   <span data-ttu-id="efd0e-111">Gestion des informations d’État pour les services en cours d’exécution et les services de pilote.</span><span class="sxs-lookup"><span data-stu-id="efd0e-111">Maintaining status information for running services and driver services.</span></span>
-   <span data-ttu-id="efd0e-112">Transmission des demandes de contrôle aux services en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="efd0e-112">Transmitting control requests to running services.</span></span>
-   <span data-ttu-id="efd0e-113">Verrouillage et déverrouillage de la base de données du service.</span><span class="sxs-lookup"><span data-stu-id="efd0e-113">Locking and unlocking the service database.</span></span>

<span data-ttu-id="efd0e-114">Les sections suivantes décrivent le SCM plus en détail :</span><span class="sxs-lookup"><span data-stu-id="efd0e-114">The following sections describe the SCM in more detail:</span></span>

-   [<span data-ttu-id="efd0e-115">Base de données des services installés</span><span class="sxs-lookup"><span data-stu-id="efd0e-115">Database of Installed Services</span></span>](database-of-installed-services.md)
-   [<span data-ttu-id="efd0e-116">Démarrage automatique des services</span><span class="sxs-lookup"><span data-stu-id="efd0e-116">Automatically Starting Services</span></span>](automatically-starting-services.md)
-   [<span data-ttu-id="efd0e-117">Démarrage des services à la demande</span><span class="sxs-lookup"><span data-stu-id="efd0e-117">Starting Services on Demand</span></span>](starting-services-on-demand.md)
-   [<span data-ttu-id="efd0e-118">Liste des enregistrements de service</span><span class="sxs-lookup"><span data-stu-id="efd0e-118">Service Record List</span></span>](service-record-list.md)
-   [<span data-ttu-id="efd0e-119">Handles SCM</span><span class="sxs-lookup"><span data-stu-id="efd0e-119">SCM Handles</span></span>](scm-handles.md)

 

 



