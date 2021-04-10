---
description: Une application s’exécutant en tant qu’utilisateur standard communique avec un service exécuté en tant que système à l’aide d’un appel de procédure distante (RPC).
ms.assetid: c0bcebe3-f7eb-471f-a21d-5840d2e26729
title: Modèle de service du système d’exploitation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ce545c60da8e480247c8fc8b02cfc01e4487340
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952387"
---
# <a name="operating-system-service-model"></a><span data-ttu-id="4989b-103">Modèle de service du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="4989b-103">Operating System Service Model</span></span>

<span data-ttu-id="4989b-104">Dans le modèle de service du système d’exploitation, une application qui s’exécute en tant qu’utilisateur standard communique avec un service exécuté en tant que **système** à l’aide d’un [appel de procédure distante](/windows/desktop/Rpc/rpc-start-page) (RPC).</span><span class="sxs-lookup"><span data-stu-id="4989b-104">In the operating system service model, an application running as a standard user communicates with a service running as **SYSTEM** by using [Remote Procedure Call](/windows/desktop/Rpc/rpc-start-page) (RPC).</span></span>

<span data-ttu-id="4989b-105">L’application utilisateur standard est marquée dans le manifeste de l’application avec un **requestedExecutionLevel** de **asInvoker**.</span><span class="sxs-lookup"><span data-stu-id="4989b-105">The standard user application is marked in the application manifest with a **requestedExecutionLevel** of **asInvoker**.</span></span> <span data-ttu-id="4989b-106">Pour effectuer une opération qui requiert des privilèges d’administrateur, l’application utilisateur standard envoie une demande au service.</span><span class="sxs-lookup"><span data-stu-id="4989b-106">To perform an operation that requires administrator privilege, the standard user application makes a request to the service.</span></span>

<span data-ttu-id="4989b-107">Une utilisation pour le modèle de service du système d’exploitation consiste à gérer les applications qui peuvent avoir un impact sur le système, telles que les antivirus ou autres logiciels indésirables et logiciels espions.</span><span class="sxs-lookup"><span data-stu-id="4989b-107">One use for the operating system service model is to manage applications that could impact the system, such as antivirus or other unwanted software and spyware.</span></span> <span data-ttu-id="4989b-108">L’application utilisateur standard permet à l’utilisateur connecté de contrôler certains aspects du service.</span><span class="sxs-lookup"><span data-stu-id="4989b-108">The standard user application allows the logged on user to control some aspects of the service.</span></span> <span data-ttu-id="4989b-109">Le service est chargé de déterminer les opérations qu’il effectue pour une application utilisateur standard.</span><span class="sxs-lookup"><span data-stu-id="4989b-109">The service is responsible for determining which operations it performs for a standard user application.</span></span> <span data-ttu-id="4989b-110">Par exemple, un service antivirus peut permettre à un utilisateur standard de démarrer une analyse du système, mais il risque de ne pas autoriser un utilisateur standard à désactiver la vérification des virus en temps réel.</span><span class="sxs-lookup"><span data-stu-id="4989b-110">For example, an antivirus service might allow a standard user to start a scan of the system, but it might not allow a standard user to disable real-time virus checking.</span></span>

<span data-ttu-id="4989b-111">L’un des principaux avantages de l’utilisation du modèle de service du système d’exploitation est qu’aucune invite d’élévation n’est requise.</span><span class="sxs-lookup"><span data-stu-id="4989b-111">A major benefit of using the operating system service model is that no elevation prompting is required.</span></span>

<span data-ttu-id="4989b-112">L’un des inconvénients de l’utilisation du modèle de service du système d’exploitation est qu’un service s’exécutant sur le système utilise plus de ressources qu’une tâche et qu’un service ne peut pas être arrêté par un utilisateur standard.</span><span class="sxs-lookup"><span data-stu-id="4989b-112">One drawback of using the operating system service model is that a service running on the system uses more resources than a task, and a service cannot be stopped by a standard user.</span></span> <span data-ttu-id="4989b-113">Envisagez d’utiliser le [modèle de tâche avec élévation de privilèges](elevated-task-model.md) si cela suffit.</span><span class="sxs-lookup"><span data-stu-id="4989b-113">Consider using the [Elevated Task Model](elevated-task-model.md) if it suffices.</span></span>

<span data-ttu-id="4989b-114">Pour implémenter le modèle de service du système d’exploitation, créez une application cliente utilisateur standard et un service de système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="4989b-114">To implement the operating system service model, create a standard user client application and an operating system service.</span></span> <span data-ttu-id="4989b-115">Installez le service dans le système d’exploitation pendant l’heure d’installation du produit.</span><span class="sxs-lookup"><span data-stu-id="4989b-115">Install the service in the operating system during product installation time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4989b-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4989b-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4989b-117">Développement d’applications nécessitant des privilèges d’administrateur</span><span class="sxs-lookup"><span data-stu-id="4989b-117">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[<span data-ttu-id="4989b-118">Modèle de Broker administrateur</span><span class="sxs-lookup"><span data-stu-id="4989b-118">Administrator Broker Model</span></span>](administrator-broker-model.md)
</dt> <dt>

[<span data-ttu-id="4989b-119">Modèle d’objet COM administrateur</span><span class="sxs-lookup"><span data-stu-id="4989b-119">Administrator COM Object Model</span></span>](administrator-com-object-model.md)
</dt> <dt>

[<span data-ttu-id="4989b-120">Modèle de tâche avec élévation de privilèges</span><span class="sxs-lookup"><span data-stu-id="4989b-120">Elevated Task Model</span></span>](elevated-task-model.md)
</dt> </dl>

 

 
