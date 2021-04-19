---
title: Scénario 3-compteurs de performance
description: Les compteurs de performances mesurent les quantités d’informations ou de données, en fonction du nombre, de la taille, de la durée et du taux de données demandées ou reçues.
ms.assetid: 1b264144-7600-402e-86f8-674a2d02f9f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de90607cbda0542ee385b83f44bec878927d509f
ms.sourcegitcommit: fc3f2a28a55e590ac38846048f10b64ba527a98d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2020
ms.locfileid: "106513753"
---
# <a name="scenario-3-performance-counters"></a><span data-ttu-id="c8d59-103">Scénario 3 : compteurs de performances</span><span class="sxs-lookup"><span data-stu-id="c8d59-103">Scenario 3: Performance Counters</span></span>

<span data-ttu-id="c8d59-104">Les compteurs de performances mesurent les quantités d’informations ou de données, en fonction du nombre, de la taille, de la durée et du taux de données demandées ou reçues.</span><span class="sxs-lookup"><span data-stu-id="c8d59-104">Performance counters measure quantities of information or data, according to the number, size, duration, and rate of data being requested or received.</span></span> <span data-ttu-id="c8d59-105">Vous ne devez pas vous attendre à obtenir la liste des détails d’un compteur, par exemple une liste de messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="c8d59-105">You should not expect to get a list of details from a counter, such as a list of error messages.</span></span> <span data-ttu-id="c8d59-106">Utilisez plutôt des compteurs de performances pour connaître les quantités, telles que le nombre de messages d’erreur depuis le démarrage ou la fréquence à laquelle les messages d’erreur sont générés.</span><span class="sxs-lookup"><span data-stu-id="c8d59-106">Instead, use performance counters to get quantities, such as the number of error message since startup or the rate at which error messages are being generated.</span></span>

## <a name="performance-counters-for-httpsys"></a><span data-ttu-id="c8d59-107">Compteurs de performances pour HTTP.sys</span><span class="sxs-lookup"><span data-stu-id="c8d59-107">Performance Counters for HTTP.sys</span></span>

<span data-ttu-id="c8d59-108">À compter de Windows Vista et de Windows Server 2008, HTTP.sys dispose des compteurs de métriques de performances suivants pour vous aider dans la surveillance, le diagnostic et la planification de la capacité des serveurs Web : le composant de l’API du serveur HTTP dispose des compteurs de performances suivants pour vous aider à surveiller, diagnostiquer et planifier la capacité des serveurs Web :</span><span class="sxs-lookup"><span data-stu-id="c8d59-108">Starting with Windows Vista and Windows Server 2008, HTTP.sys has the following performance metric counters to help you with monitoring, diagnosing, and capacity planning for Web servers: The HTTP Server API component has the following performance counters to help you with monitoring, diagnosing, and capacity planning for Web servers:</span></span>

- <span data-ttu-id="c8d59-109">Compteurs de service HTTP :</span><span class="sxs-lookup"><span data-stu-id="c8d59-109">HTTP Service Counters:</span></span>
  - <span data-ttu-id="c8d59-110">Nombre d’URI dans le cache, ajoutés depuis le démarrage, supprimé depuis le démarrage et nombre de vidages du cache</span><span class="sxs-lookup"><span data-stu-id="c8d59-110">Number of URIs in the cache, added since startup, deleted since startup, and number of cache flushes</span></span>
  - <span data-ttu-id="c8d59-111">Présences dans le cache/seconde et échecs dans le cache/seconde</span><span class="sxs-lookup"><span data-stu-id="c8d59-111">Cache hits/second and Cache misses/second</span></span>
- <span data-ttu-id="c8d59-112">Groupes d’URL de service HTTP :</span><span class="sxs-lookup"><span data-stu-id="c8d59-112">HTTP Service URL Groups:</span></span>
  - <span data-ttu-id="c8d59-113">Taux d’envoi des données, taux de réception des données, octets transférés (envoyés et reçus)</span><span class="sxs-lookup"><span data-stu-id="c8d59-113">Data send rate, data receive rate, bytes transferred (sent and received)</span></span>
  - <span data-ttu-id="c8d59-114">Nombre maximal de connexions, taux de tentatives de connexion, taux pour les demandes d’extraction et d’en-tête et nombre total de demandes</span><span class="sxs-lookup"><span data-stu-id="c8d59-114">Maximum number of connections, connection attempts rate, rate for GET and HEAD requests, and total number of requests</span></span>
- <span data-ttu-id="c8d59-115">Files d’attente de demandes de service HTTP :</span><span class="sxs-lookup"><span data-stu-id="c8d59-115">HTTP Service Request Queues:</span></span>
  - <span data-ttu-id="c8d59-116">Nombre de demandes dans la file d’attente, âge des requêtes les plus anciennes dans la file d’attente (âge de la dernière demande dans la file d’attente)</span><span class="sxs-lookup"><span data-stu-id="c8d59-116">Number of requests in queue, age of oldest requests in queue (age of the last request in the queue)</span></span>
  - <span data-ttu-id="c8d59-117">Taux d’arrivées de demande dans la file d’attente, taux de rejet, nombre total de demandes rejetées, taux d’accès au cache</span><span class="sxs-lookup"><span data-stu-id="c8d59-117">Rate of request arrivals into the queue, rate of rejection, total number of rejected requests, rate of cache hits</span></span>

<span data-ttu-id="c8d59-118">**Accès aux compteurs de performance**</span><span class="sxs-lookup"><span data-stu-id="c8d59-118">**Accessing Performance Counters**</span></span>

1.  <span data-ttu-id="c8d59-119">Tapez **Perfmon** à l’invite de commandes pour démarrer la console de diagnostic des performances.</span><span class="sxs-lookup"><span data-stu-id="c8d59-119">Type **perfmon** at the command prompt to start the Performance Diagnostic Console.</span></span>
2.  <span data-ttu-id="c8d59-120">Sélectionnez **Analyseur de performances** dans le contrôle d’arborescence, puis ouvrez l' **Ajouter des compteurs** en cliquant sur **+** .</span><span class="sxs-lookup"><span data-stu-id="c8d59-120">Select **Performance Monitor** in the tree control and then open the **Add Counters** by clicking **+**.</span></span>
3.  <span data-ttu-id="c8d59-121">À partir de **Ajouter des compteurs** , sélectionnez l’un des trois compteurs de performances : **service http**, **files d’attente de requêtes de service http** ou **groupes d’URL de service http**.</span><span class="sxs-lookup"><span data-stu-id="c8d59-121">From **Add Counters** select from the three Performance Counters sets: **HTTP Service**, **HTTP Service Request Queues** , or **HTTP Service Url Groups**.</span></span>
4.  <span data-ttu-id="c8d59-122">Pour afficher les compteurs des ensembles de compteurs **files d’attente de requêtes de service http** et **groupes d’URL de service http** , sélectionnez **instances** , puis cliquez sur **Ajouter** et sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="c8d59-122">To view counters from the **HTTP Service Request Queues** and **HTTP Service Url Groups** counter sets, select **instance(s)** and click **Add**, and then click **OK**.</span></span> <span data-ttu-id="c8d59-123">Pour afficher les compteurs du service HTTP, sélectionnez l’ensemble de compteurs dans le volet gauche, puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="c8d59-123">To view the HTTP Service counters, select the counter set in the left pane and click **Add**.</span></span>

> [!Note]  
> <span data-ttu-id="c8d59-124">Une seule instance des compteurs de l’API du serveur HTTP existe par ordinateur, car ces compteurs représentent l’État à l’ensemble du composant.</span><span class="sxs-lookup"><span data-stu-id="c8d59-124">Only one instance of the HTTP Server API counters exists per machine, as these counters represent the component-wide state.</span></span> <span data-ttu-id="c8d59-125">Avec les instances de compteurs de performance de groupe d’URL, l’ID d’instance (pour le compteur de performance) correspond à l’ID de groupe d’URL.</span><span class="sxs-lookup"><span data-stu-id="c8d59-125">With instances of Url Group performance counters, the instance ID (for the performance counter) will match the Url Group ID.</span></span> <span data-ttu-id="c8d59-126">L’ID de groupe d’URL peut être affiché en exécutant **netsh http show ServiceState**.</span><span class="sxs-lookup"><span data-stu-id="c8d59-126">The Url Group ID can be viewed by running **netsh http show servicestate**.</span></span> <span data-ttu-id="c8d59-127">Avec des instances de compteurs de performance de files d’attente de demandes, le nom d’instance correspond au nom de la file d’attente de demandes.</span><span class="sxs-lookup"><span data-stu-id="c8d59-127">With instances of Request Queues performance counters, the instance name corresponds to Request Queue Name.</span></span> <span data-ttu-id="c8d59-128">Le nom de la file d’attente des demandes (s’il en existe un) peut être affiché par le même **netsh http show ServiceState**.</span><span class="sxs-lookup"><span data-stu-id="c8d59-128">The Request Queue Name (if one exists) can be shown by the same **netsh http show servicestate**.</span></span> <span data-ttu-id="c8d59-129">Toutefois, certaines applications serveur peuvent avoir des files d’attente de demandes sans nom qui ne peuvent pas être mises en correspondance avec un ID d’instance de compteur de performance.</span><span class="sxs-lookup"><span data-stu-id="c8d59-129">However, some server applications may have unnamed Request Queues that cannot be matched to a performance counter instance ID.</span></span>

 

 

 




