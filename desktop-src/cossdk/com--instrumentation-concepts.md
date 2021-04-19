---
description: Le service d’instrumentation COM+ vous permet de créer vos propres programmes de gestion et de journalisation des événements COM+ lorsque vous souhaitez afficher diverses mesures de performances pour vos composants COM+.
ms.assetid: 07f68734-a382-4fe5-86af-90805f61c68d
title: Concepts d’instrumentation COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d86b5dbb7bb3f6db14d82220d88c58dbc0a8255
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515562"
---
# <a name="com-instrumentation-concepts"></a><span data-ttu-id="c929d-103">Concepts d’instrumentation COM+</span><span class="sxs-lookup"><span data-stu-id="c929d-103">COM+ Instrumentation Concepts</span></span>

<span data-ttu-id="c929d-104">Le service d’instrumentation COM+ vous permet de créer vos propres programmes de gestion et de journalisation des événements COM+ lorsque vous souhaitez afficher diverses mesures de performances pour vos composants COM+.</span><span class="sxs-lookup"><span data-stu-id="c929d-104">The COM+ instrumentation service enables you to build your own COM+ event management and logging programs when you want to display various performance metrics for your COM+ components.</span></span> <span data-ttu-id="c929d-105">L’instrumentation COM+ peut également être utilisée pour configurer des événements définis par l’utilisateur et pour convertir des événements COM+ au format Visual Studio Analyzer (VSA) lors de la mise à niveau des packages MTS qui reçoivent des événements MTS.</span><span class="sxs-lookup"><span data-stu-id="c929d-105">COM+ instrumentation can also be used to configure user-defined events and to convert COM+ events to Visual Studio Analyzer (VSA) format when you are upgrading MTS packages that are receiving MTS events.</span></span>

> [!Note]  
> <span data-ttu-id="c929d-106">À partir de Windows Server 2003, seuls les administrateurs ont des privilèges d’accès en lecture aux journaux de suivi pour les événements système.</span><span class="sxs-lookup"><span data-stu-id="c929d-106">As of Windows Server 2003, only administrators have read access privileges to the trace logs for system events.</span></span>

 

<span data-ttu-id="c929d-107">En s’abonnant aux événements publiés par l’éditeur des événements système, les clients peuvent implémenter les [interfaces d’instrumentation com+](com--instrumentation-interfaces.md) pour recevoir des notifications pour diverses mesures de performances de com+, telles que des informations sur des objets com+ spécifiques, des applications com+ et des services com+.</span><span class="sxs-lookup"><span data-stu-id="c929d-107">By subscribing to the events published by the system events publisher, clients can implement the [COM+ instrumentation interfaces](com--instrumentation-interfaces.md) to receive notifications for a variety of COM+ performance metrics, such as information about specific COM+ objects, COM+ applications, and COM+ services.</span></span> <span data-ttu-id="c929d-108">Les métriques sont publiées sur le client à l’aide du [service d’événements com+](com--events.md), un système d’événements (LCE) faiblement couplés qui stocke les informations d’événements provenant de différents serveurs de publication dans un magasin d’événements du catalogue com+.</span><span class="sxs-lookup"><span data-stu-id="c929d-108">The metrics are published to the client by using the [COM+ events service](com--events.md), a loosely coupled events (LCE) system that stores event information from different publishers in an event store in the COM+ catalog.</span></span>

> [!Note]  
> <span data-ttu-id="c929d-109">L’instrumentation COM+ ne garantit pas la remise d’un événement.</span><span class="sxs-lookup"><span data-stu-id="c929d-109">COM+ instrumentation does not guarantee the delivery of an event.</span></span>

 

<span data-ttu-id="c929d-110">Chaque mesure a un horodateur qui indique l’heure à laquelle la mesure a été générée, et non l’heure à laquelle elle a été distribuée ou reçue.</span><span class="sxs-lookup"><span data-stu-id="c929d-110">Every metric has a timestamp that indicates the time when the metric was generated, not the time that it was dispatched or received.</span></span> <span data-ttu-id="c929d-111">Le client peut corréler l’horodateur et déterminer le coût de l’exécution d’une application COM+, le coût d’une transaction exécutée dans une application COM+, ou le coût d’un appel de méthode au sein d’une application COM+.</span><span class="sxs-lookup"><span data-stu-id="c929d-111">The client can correlate the timestamp and find out the cost of running a COM+ application, the cost of a transaction executed inside a COM+ application, or the cost of a method call inside of a COM+ application.</span></span>

<span data-ttu-id="c929d-112">Vous pouvez également utiliser le service d’instrumentation COM+ pour filtrer les informations de métriques de performances spécifiques que vous souhaitez afficher.</span><span class="sxs-lookup"><span data-stu-id="c929d-112">You can also use the COM+ Instrumentation service to filter for the specific performance metrics information that you want to see.</span></span> <span data-ttu-id="c929d-113">Par exemple, lorsque vous vous abonnez à une interface ou une méthode d’instrumentation COM+, vous pouvez spécifier des propriétés pour l’abonnement dans la structure [**COMSVCSEVENTINFO**](/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo) , telles que l’ID d’application (membre **guidApp** ) ou l’ID de processus (membre **dwPid** ).</span><span class="sxs-lookup"><span data-stu-id="c929d-113">For example, when you subscribe to a COM+ instrumentation interface or method, you can specify properties for the subscription in the [**COMSVCSEVENTINFO**](/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo) structure, such as the application ID (**guidApp** member) or the process ID (**dwPid** member).</span></span>

<span data-ttu-id="c929d-114">Lorsque l’ID d’application est spécifié, vous recevez uniquement les métriques de l’application spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c929d-114">When the application ID is specified, you receive only the metrics from the specified application.</span></span> <span data-ttu-id="c929d-115">Lorsque l’ID de processus est spécifié, vous recevez des métriques de l’application serveur spécifiée et des applications de bibliothèque qui sont chargées dans ce processus.</span><span class="sxs-lookup"><span data-stu-id="c929d-115">When the process ID is specified, you receive metrics from the specified server application and library applications that are loaded in that process.</span></span> <span data-ttu-id="c929d-116">L’utilisateur peut spécifier l’ID d’application et l’ID de processus, mais l’ID d’application doit être celui de l’application serveur en cours d’exécution dans le processus avec l’ID de processus spécifié.</span><span class="sxs-lookup"><span data-stu-id="c929d-116">The user can specify both the application ID and the process ID, but the application ID has to be that of the server application running in the process with the specified process ID.</span></span> <span data-ttu-id="c929d-117">Si aucun de ces paramètres n’est spécifié, l’utilisateur reçoit des métriques à partir de toutes les applications serveur et de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="c929d-117">If neither is specified, the user receives metrics from all the server and library applications.</span></span>

<span data-ttu-id="c929d-118">Les métriques d’instrumentation COM+ fournissent suffisamment d’informations pour que l’application de surveillance les mette en corrélation avec les métriques du système d’exploitation pour l’analyse des performances, la planification de la capacité et la modélisation et la prédiction.</span><span class="sxs-lookup"><span data-stu-id="c929d-118">The COM+ instrumentation metrics provide enough information for the monitoring application to correlate them with the operating system metrics for performance analysis, capacity planning, and for modeling and prediction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c929d-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c929d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c929d-120">Interfaces d’instrumentation COM+</span><span class="sxs-lookup"><span data-stu-id="c929d-120">COM+ Instrumentation Interfaces</span></span>](com--instrumentation-interfaces.md)
</dt> </dl>

 

 



