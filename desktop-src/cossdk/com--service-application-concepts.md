---
description: Concepts des applications de service COM+
ms.assetid: d6b1cf4a-ca39-4d50-a33d-aa639937ef9e
title: Concepts des applications de service COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b24db7a031ed0520f30891d98688af67e853ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483065"
---
# <a name="com-service-application-concepts"></a><span data-ttu-id="37f37-103">Concepts des applications de service COM+</span><span class="sxs-lookup"><span data-stu-id="37f37-103">COM+ Service Application Concepts</span></span>

<span data-ttu-id="37f37-104">Vous pouvez utiliser l’outil d’administration Services de composants pour configurer une application serveur COM+ en tant qu’application de service.</span><span class="sxs-lookup"><span data-stu-id="37f37-104">You can use the Component Services administrative tool to configure a COM+ server application as a service application.</span></span> <span data-ttu-id="37f37-105">L’exécution d’une application serveur COM+ en tant que service offre les avantages suivants :</span><span class="sxs-lookup"><span data-stu-id="37f37-105">Running a COM+ server application as a service offers the following advantages:</span></span>

-   <span data-ttu-id="37f37-106">Si votre application doit toujours être en cours d’exécution, les services de composants peuvent éventuellement démarrer le serveur automatiquement et redémarrer le serveur s’il expire. Par exemple, si un ordinateur exécutant les composants de l’écouteur de composants en file d’attente est redémarré, les écouteurs de composants en file d’attente peuvent être démarrés automatiquement s’ils sont configurés en tant que service.</span><span class="sxs-lookup"><span data-stu-id="37f37-106">If your application always needs to be running, Component Services can optionally have the server started automatically and can also restart the server if it times out. For example, if a computer running Queued Components listener components is rebooted, the Queued Components listeners can be started automatically if they are configured as a service.</span></span>
-   <span data-ttu-id="37f37-107">Si votre application doit effectuer des opérations privilégiées, l’application peut s’exécuter en tant que compte système local.</span><span class="sxs-lookup"><span data-stu-id="37f37-107">If your application needs to perform privileged operations, the application can run as the local system account.</span></span> <span data-ttu-id="37f37-108">Seuls les services NT sont autorisés à s’exécuter avec ce niveau de sécurité.</span><span class="sxs-lookup"><span data-stu-id="37f37-108">Only NT services are allowed to run with this level of security.</span></span> <span data-ttu-id="37f37-109">L’application est compatible avec Windows service de cluster, qui gère les services pendant le basculement du système.</span><span class="sxs-lookup"><span data-stu-id="37f37-109">The application will be compatible with the Windows Cluster service, which manages services during system failover.</span></span>
-   <span data-ttu-id="37f37-110">Si d’autres services doivent être marqués comme étant dépendants, les services de composants fournissent cette option.</span><span class="sxs-lookup"><span data-stu-id="37f37-110">If other services need to be marked as dependent, Component Services provides that option.</span></span> <span data-ttu-id="37f37-111">Par exemple, si votre application utilise des fonctionnalités fournies par un autre service, le service marqué comme dépendant sera démarré avant le démarrage de votre application.</span><span class="sxs-lookup"><span data-stu-id="37f37-111">For example, if your application makes use of functionality provided by another service, the service marked as dependent will be started before your application starts.</span></span>

## <a name="starting-an-application-automatically"></a><span data-ttu-id="37f37-112">Démarrage automatique d’une application</span><span class="sxs-lookup"><span data-stu-id="37f37-112">Starting an Application Automatically</span></span>

<span data-ttu-id="37f37-113">Lorsque l’application serveur COM+ est démarrée automatiquement, elle agit comme un service, ce qui oblige le développeur à gérer le serveur à l’aide de l’outil d’administration Services.</span><span class="sxs-lookup"><span data-stu-id="37f37-113">When the COM+ server application is started automatically, it acts like a service, requiring the developer to manage the server using the Services administrative tool.</span></span>

> [!Note]  
> <span data-ttu-id="37f37-114">L’outil d’administration Services est accessible en lançant l’outil d’administration Services de composants, puis en cliquant sur **services (local)**.</span><span class="sxs-lookup"><span data-stu-id="37f37-114">The Services administrative tool can be accessed by launching the Component Services administrative tool and then clicking **Services (Local)**.</span></span>

 

## <a name="starting-an-application-manually"></a><span data-ttu-id="37f37-115">Démarrage manuel d’une application</span><span class="sxs-lookup"><span data-stu-id="37f37-115">Starting an Application Manually</span></span>

<span data-ttu-id="37f37-116">Lorsque l’application serveur COM+ est démarrée manuellement, elle agit comme un hôte DLL avec les paramètres de sécurité d’un service.</span><span class="sxs-lookup"><span data-stu-id="37f37-116">When the COM+ server application is started manually, it acts like a DLL host with the security settings of a service.</span></span> <span data-ttu-id="37f37-117">Le service est démarré manuellement lorsqu’il est activé et arrêté automatiquement lorsqu’il expire.</span><span class="sxs-lookup"><span data-stu-id="37f37-117">The service will be started up manually when activated and shut down automatically when it times out.</span></span>

## <a name="service-configurations"></a><span data-ttu-id="37f37-118">Configurations de service</span><span class="sxs-lookup"><span data-stu-id="37f37-118">Service Configurations</span></span>

<span data-ttu-id="37f37-119">Quel que soit le type de démarrage, l’application peut être configurée pour s’exécuter en tant que compte système local ou être affectée à un compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="37f37-119">Regardless of the startup type, the application can be configured to run as a local system account or assigned to a user account.</span></span> <span data-ttu-id="37f37-120">Le compte système local et le compte d’utilisateur peuvent être configurés au moment de la création du service.</span><span class="sxs-lookup"><span data-stu-id="37f37-120">The local system and user account can be configured at the time of creating the service.</span></span> <span data-ttu-id="37f37-121">Pour configurer les paramètres de sécurité, l’outil d’administration Services doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="37f37-121">To configure the security settings, the Services administrative tool will have to be used.</span></span> <span data-ttu-id="37f37-122">Il est également possible de définir des dépendances pour le service.</span><span class="sxs-lookup"><span data-stu-id="37f37-122">Dependencies can also be set for the service.</span></span>

<span data-ttu-id="37f37-123">L’application peut également être démarrée dans n’importe quel ordre particulier en sélectionnant dépendances dans une liste d’autres services système.</span><span class="sxs-lookup"><span data-stu-id="37f37-123">The application can also be started in any particular order by selecting dependencies from a list of other system services.</span></span> <span data-ttu-id="37f37-124">Par exemple, les services système peuvent être marqués comme étant dépendants et ne démarrent pas l’application tant que les services système n’ont pas été démarrés dans l’ordre spécifié.</span><span class="sxs-lookup"><span data-stu-id="37f37-124">For example, the system services can be marked as dependent and will not start the application until the system services have been started in the specified order.</span></span> <span data-ttu-id="37f37-125">L’application de service sera correctement initialisée avant d’être utilisée.</span><span class="sxs-lookup"><span data-stu-id="37f37-125">This will properly initialize the service application before it is used.</span></span>

<span data-ttu-id="37f37-126">Pour obtenir des instructions pas à pas sur la configuration d’une application COM+ pour qu’elle s’exécute en tant que service, consultez [configuration d’une application serveur com+ en tant qu’application de service](configuring-a-com--server-application-as-a-service-application.md).</span><span class="sxs-lookup"><span data-stu-id="37f37-126">For a step-by-step instruction on how to configure a COM+ application to run as a service, see [Configuring a COM+ Server Application as a Service Application](configuring-a-com--server-application-as-a-service-application.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="37f37-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="37f37-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37f37-128">Tâches de l’application de service COM+</span><span class="sxs-lookup"><span data-stu-id="37f37-128">COM+ Service Application Tasks</span></span>](com--service-application-tasks.md)
</dt> </dl>

 

 



