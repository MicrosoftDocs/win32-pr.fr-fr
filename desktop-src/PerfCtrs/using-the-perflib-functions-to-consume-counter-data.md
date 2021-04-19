---
title: Utilisation des fonctions PerfLib pour consommer des données de compteurs
description: Les fonctions de l’API PerfLib peuvent être utilisées pour consommer des données de compteur de performances v2 directement lorsque PDH ne peut pas être utilisé.
ms.date: 08/17/2020
ms.topic: article
ms.openlocfilehash: 9fec3bb97ec32ff98e2b317b737023da81147bdd
ms.sourcegitcommit: f7cf41ffc79d1ffead9de2fc61677201f94b423a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2020
ms.locfileid: "106513745"
---
# <a name="using-the-perflib-functions-to-consume-counter-data"></a><span data-ttu-id="35bde-103">Utilisation des fonctions PerfLib pour consommer des données de compteurs</span><span class="sxs-lookup"><span data-stu-id="35bde-103">Using the PerfLib Functions to Consume Counter Data</span></span>

<span data-ttu-id="35bde-104">Utilisez les fonctions de consommateur PerfLib pour consommer des données de performances à partir de fournisseurs de données de performances v2 lorsque vous ne pouvez pas utiliser les [fonctions d’assistance des données de performance (PDH)](using-the-pdh-functions-to-consume-counter-data.md).</span><span class="sxs-lookup"><span data-stu-id="35bde-104">Use the PerfLib Consumer functions to consume performance data from V2 performance data providers when you cannot use the [Performance Data Helper (PDH) functions](using-the-pdh-functions-to-consume-counter-data.md).</span></span> <span data-ttu-id="35bde-105">Ces fonctions peuvent être utilisées lors de l’écriture d’applications OneCore pour collecter des countersets v2 ou lorsque vous devez collecter des countersets v2 avec des dépendances et une surcharge minimales.</span><span class="sxs-lookup"><span data-stu-id="35bde-105">These functions might be used when writing OneCore applications to collect V2 countersets or when you need to collect V2 countersets with minimal dependencies and overhead.</span></span>

> [!TIP]
> <span data-ttu-id="35bde-106">Les fonctions de consommateur de PerfLib v2 sont plus difficiles à utiliser que les fonctions de performance Data Helper (PDH) et ne prennent en charge que la collecte de données à partir de fournisseurs v2.</span><span class="sxs-lookup"><span data-stu-id="35bde-106">The PerfLib V2 Consumer functions are harder to use than the Performance Data Helper (PDH) functions and only support collecting data from V2 providers.</span></span> <span data-ttu-id="35bde-107">Les fonctions PDH doivent être préférées pour la plupart des applications.</span><span class="sxs-lookup"><span data-stu-id="35bde-107">The PDH functions should be preferred for most applications.</span></span>

<span data-ttu-id="35bde-108">Les fonctions de consommateur de PerfLib v2 sont l’API de bas niveau pour la collecte de données à partir de **fournisseurs v2**.</span><span class="sxs-lookup"><span data-stu-id="35bde-108">The PerfLib V2 Consumer functions are the low-level API for collecting data from **V2 providers**.</span></span> <span data-ttu-id="35bde-109">Les fonctions de consommateur de PerfLib v2 ne prennent pas en charge la collecte de données à partir de **fournisseurs v1**.</span><span class="sxs-lookup"><span data-stu-id="35bde-109">The PerfLib V2 Consumer functions do not support collecting data from **V1 providers**.</span></span>

> [!WARNING]
> <span data-ttu-id="35bde-110">Les fonctions de consommateur de PerfLib v2 peuvent potentiellement collecter des données à partir de sources non approuvées, par exemple, à partir de services locaux à privilèges limités ou à partir d’ordinateurs distants.</span><span class="sxs-lookup"><span data-stu-id="35bde-110">The PerfLib V2 consumer functions can potentially collect data from untrusted sources, e.g. from limited-privilege local services or from remote machines.</span></span> <span data-ttu-id="35bde-111">Les fonctions de consommateur de PerfLib v2 ne valident pas les données pour l’intégrité ou la cohérence.</span><span class="sxs-lookup"><span data-stu-id="35bde-111">The PerfLib V2 consumer functions do not validate the data for integrity or consistency.</span></span> <span data-ttu-id="35bde-112">Il revient à votre application consommateur de vérifier que les données retournées sont cohérentes, par exemple, que les valeurs de taille dans le bloc de données retourné ne dépassent pas la taille réelle du bloc de données retourné.</span><span class="sxs-lookup"><span data-stu-id="35bde-112">It is up to your consumer application to verify that the returned data is consistent, e.g. that the Size values in the returned data block do not exceed the actual size of the returned data block.</span></span> <span data-ttu-id="35bde-113">Cela est particulièrement important lorsque l’application consommateur s’exécute avec des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="35bde-113">This is especially important when the consumer application runs at elevated privilege.</span></span>

## <a name="perflib-usage"></a><span data-ttu-id="35bde-114">Utilisation de PerfLib</span><span class="sxs-lookup"><span data-stu-id="35bde-114">PerfLib Usage</span></span>

<span data-ttu-id="35bde-115">L' `perflib.h` en-tête comprend les déclarations utilisées par les fournisseurs en mode utilisateur V2 (c’est-à-dire l’API du fournisseur Perflib) et les consommateurs v2 (c’est-à-dire l’API du consommateur Perflib).</span><span class="sxs-lookup"><span data-stu-id="35bde-115">The `perflib.h` header includes the declarations used by V2 user-mode providers (i.e. the PerfLib Provider API) and V2 consumers (i.e. the PerfLib Consumer API).</span></span> <span data-ttu-id="35bde-116">Elle déclare les fonctions suivantes pour la consommation des données de performances v2 :</span><span class="sxs-lookup"><span data-stu-id="35bde-116">It declares the following functions for consuming V2 performance data:</span></span>

- <span data-ttu-id="35bde-117">Utilisez [**PerfEnumerateCounterSet**](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecounterset) pour récupérer les GUID des countersets inscrits par les fournisseurs v2 sur le système.</span><span class="sxs-lookup"><span data-stu-id="35bde-117">Use [**PerfEnumerateCounterSet**](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecounterset) to get the GUIDs of the countersets that are registered by the V2 providers on the system.</span></span>
- <span data-ttu-id="35bde-118">Utilisez [**PerfQueryCounterSetRegistrationInfo**](/windows/desktop/api/Perflib/nf-perflib-perfquerycountersetregistrationinfo) pour obtenir des informations sur un CounterSet particulier, tel que le nom, la description, le type (instance unique ou multi-instance) du CounterSet, les types de compteurs, les noms de compteurs et les descriptions de compteurs.</span><span class="sxs-lookup"><span data-stu-id="35bde-118">Use [**PerfQueryCounterSetRegistrationInfo**](/windows/desktop/api/Perflib/nf-perflib-perfquerycountersetregistrationinfo) to get information about a particular counterset such as the counterset's name, description, type (single-instance or multi-instance), counter types, counter names, and counter descriptions.</span></span>
- <span data-ttu-id="35bde-119">Utilisez [**PerfEnumerateCounterSetInstances**](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecountersetinstances) pour obtenir les noms des instances actuellement actives d’un CounterSet multi-instance.</span><span class="sxs-lookup"><span data-stu-id="35bde-119">Use [**PerfEnumerateCounterSetInstances**](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecountersetinstances) to get the names of the currently-active instances of a multi-instance counterset.</span></span>
- <span data-ttu-id="35bde-120">Utilisez [**PerfOpenQueryHandle**](/windows/desktop/api/Perflib/nf-perflib-perfopenqueryhandle) pour créer un nouveau descripteur de requête à utiliser pour collecter des données à partir d’un ou plusieurs countersets.</span><span class="sxs-lookup"><span data-stu-id="35bde-120">Use [**PerfOpenQueryHandle**](/windows/desktop/api/Perflib/nf-perflib-perfopenqueryhandle) to create a new query handle to use for collecting data from one or more countersets.</span></span>
- <span data-ttu-id="35bde-121">Utilisez [**PerfCloseQueryHandle**](/windows/desktop/api/Perflib/nf-perflib-perfclosequeryhandle) pour fermer un handle de requête.</span><span class="sxs-lookup"><span data-stu-id="35bde-121">Use [**PerfCloseQueryHandle**](/windows/desktop/api/Perflib/nf-perflib-perfclosequeryhandle) to close a query handle.</span></span>
- <span data-ttu-id="35bde-122">Utilisez [**PerfAddCounters**](/windows/desktop/api/Perflib/nf-perflib-perfaddcounters) pour ajouter une requête à un handle de requête.</span><span class="sxs-lookup"><span data-stu-id="35bde-122">Use [**PerfAddCounters**](/windows/desktop/api/Perflib/nf-perflib-perfaddcounters) to add a query to a query handle.</span></span>
- <span data-ttu-id="35bde-123">Utilisez [**PerfDeleteCounters**](/windows/desktop/api/Perflib/nf-perflib-perfdeletecounters) pour supprimer une requête d’un handle de requête.</span><span class="sxs-lookup"><span data-stu-id="35bde-123">Use [**PerfDeleteCounters**](/windows/desktop/api/Perflib/nf-perflib-perfdeletecounters) to remove a query from a query handle.</span></span>
- <span data-ttu-id="35bde-124">Utilisez [**PerfQueryCounterInfo**](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterinfo) pour obtenir des informations sur les requêtes en cours sur un handle de requête.</span><span class="sxs-lookup"><span data-stu-id="35bde-124">Use [**PerfQueryCounterInfo**](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterinfo) to get information about the current queries on a query handle.</span></span>
- <span data-ttu-id="35bde-125">Utilisez [**PerfQueryCounterData**](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterdata) pour collecter les données de performances à partir d’un handle de requête.</span><span class="sxs-lookup"><span data-stu-id="35bde-125">Use [**PerfQueryCounterData**](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterdata) to collect the performance data from a query handle.</span></span>

<span data-ttu-id="35bde-126">Si votre consommateur consomme des données uniquement à partir d’un fournisseur spécifique où le GUID et les index de compteur sont stables et que vous avez accès au fichier de symboles généré par [CTRPP](ctrpp.md)(à partir du `-ch` paramètre ctrpp), vous pouvez coder en dur le GUID du CounterSet et les valeurs d’index de compteur dans votre consommateur.</span><span class="sxs-lookup"><span data-stu-id="35bde-126">If your consumer will be consuming data only from a specific provider where the GUID and counter indexes are stable and you have access to the [CTRPP](ctrpp.md)-generated symbol file (from the CTRPP `-ch` parameter), you can hard-code the counterset GUID and counter index values into your consumer.</span></span>

<span data-ttu-id="35bde-127">Dans le cas contraire, vous devrez charger les métadonnées du CounterSet pour déterminer le (s) GUID (s) du CounterSet et les index de compteur à utiliser dans votre requête comme suit :</span><span class="sxs-lookup"><span data-stu-id="35bde-127">Otherwise, you will need to load counterset metadata to determine the counterset GUID(s) and counter indexes to use in your query as follows:</span></span>

- <span data-ttu-id="35bde-128">Utilisez **PerfEnumerateCounterSet** pour obtenir la liste des GUID du CounterSet pris en charge.</span><span class="sxs-lookup"><span data-stu-id="35bde-128">Use **PerfEnumerateCounterSet** to get a list of supported counterset GUIDs.</span></span>
- <span data-ttu-id="35bde-129">Pour chaque GUID, utilisez **PerfQueryCounterSetRegistrationInfo** pour charger le nom du CounterSet.</span><span class="sxs-lookup"><span data-stu-id="35bde-129">For each GUID, use **PerfQueryCounterSetRegistrationInfo** to load the counterset name.</span></span> <span data-ttu-id="35bde-130">Arrêtez quand vous trouvez le nom que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="35bde-130">Stop when you find the name you are looking for.</span></span>
- <span data-ttu-id="35bde-131">Utilisez **PerfQueryCounterSetRegistrationInfo** pour charger les métadonnées restantes (configuration du CounterSet, noms des compteurs, index de compteurs, types de compteurs) pour ce CounterSet.</span><span class="sxs-lookup"><span data-stu-id="35bde-131">Use **PerfQueryCounterSetRegistrationInfo** to load the remaining metadata (counterset configuration, counter names, counter indexes, counter types) for that counterset.</span></span>

<span data-ttu-id="35bde-132">Si vous avez simplement besoin de connaître les noms des instances actuellement actives d’un CounterSet (c’est-à-dire si vous n’avez pas besoin des valeurs de données de performances réelles), vous pouvez utiliser **PerfEnumerateCounterSetInstances**.</span><span class="sxs-lookup"><span data-stu-id="35bde-132">If you just need to know the names of the currently-active instances of a counterset (i.e. if you do not need the actual performance data values), you can use **PerfEnumerateCounterSetInstances**.</span></span> <span data-ttu-id="35bde-133">Cela prend un GUID du CounterSet comme entrée et retourne un `PERF_INSTANCE_HEADER` bloc avec les noms et les ID des instances actuellement actives du CounterSet donné.</span><span class="sxs-lookup"><span data-stu-id="35bde-133">This takes a counterset GUID as input and returns a `PERF_INSTANCE_HEADER` block with the names and IDs of the currently-active instances of the given counterset.</span></span>

### <a name="queries"></a><span data-ttu-id="35bde-134">Requêtes</span><span class="sxs-lookup"><span data-stu-id="35bde-134">Queries</span></span>

<span data-ttu-id="35bde-135">Pour collecter des données de performances, vous devez créer un descripteur de requête, y ajouter des requêtes et collecter les données à partir des requêtes.</span><span class="sxs-lookup"><span data-stu-id="35bde-135">To collect performance data, you need to create a query handle, add queries to it, and collect the data from the queries.</span></span>

<span data-ttu-id="35bde-136">Plusieurs requêtes peuvent être associées à un descripteur de requête.</span><span class="sxs-lookup"><span data-stu-id="35bde-136">A query handle can have many queries associated with it.</span></span> <span data-ttu-id="35bde-137">Quand vous appelez **PerfQueryCounterData** pour un handle de requête, perflib exécute toutes les requêtes du handle et collecte tous les résultats.</span><span class="sxs-lookup"><span data-stu-id="35bde-137">When you call **PerfQueryCounterData** for a query handle, PerfLib will execute all of the handle's queries and collect all of the results.</span></span>

<span data-ttu-id="35bde-138">Chaque requête spécifie un GUID du CounterSet, un filtre de nom d’instance, un filtre d’ID d’instance facultatif et un filtre d’ID de compteur facultatif.</span><span class="sxs-lookup"><span data-stu-id="35bde-138">Each query specifies a counterset GUID, an instance name filter, an optional instance ID filter, and an optional counter ID filter.</span></span>

- <span data-ttu-id="35bde-139">Le GUID du CounterSet est requis.</span><span class="sxs-lookup"><span data-stu-id="35bde-139">The counterset GUID is required.</span></span> <span data-ttu-id="35bde-140">Elle indique le GUID du CounterSet à partir duquel la requête collectera les données.</span><span class="sxs-lookup"><span data-stu-id="35bde-140">It indicates the GUID of the counterset from which the query will collect data.</span></span> <span data-ttu-id="35bde-141">Cela est similaire à la `FROM` clause d’une requête SQL.</span><span class="sxs-lookup"><span data-stu-id="35bde-141">This is similar to the `FROM` clause of a SQL query.</span></span>
- <span data-ttu-id="35bde-142">Le filtre de nom d’instance est requis.</span><span class="sxs-lookup"><span data-stu-id="35bde-142">The instance name filter is required.</span></span> <span data-ttu-id="35bde-143">Il indique un modèle de caractère générique que le nom d’instance doit mettre en correspondance pour que l’instance soit incluse dans la requête, en `*` indiquant « tout caractère » et en `?` indiquant « un caractère ».</span><span class="sxs-lookup"><span data-stu-id="35bde-143">It indicates a wildcard pattern that the instance name must match for the instance to be included in the query, with `*` indicating "any characters" and `?` indicating "one character".</span></span> <span data-ttu-id="35bde-144">Pour les countersets d’instance unique, cette valeur **doit** être une chaîne de longueur nulle `""` .</span><span class="sxs-lookup"><span data-stu-id="35bde-144">For single-instance countersets this **MUST** be set to a zero-length string `""`.</span></span> <span data-ttu-id="35bde-145">Pour les countersets multi-instances, cette valeur **doit** être une chaîne non vide (utilisez `"*"` pour accepter tous les noms d’instance).</span><span class="sxs-lookup"><span data-stu-id="35bde-145">For multi-instance countersets this **MUST** be set to a non-empty string (use `"*"` to accept all instance names).</span></span> <span data-ttu-id="35bde-146">Cela est similaire à une `WHERE InstanceName LIKE NameFilter` clause d’une requête SQL.</span><span class="sxs-lookup"><span data-stu-id="35bde-146">This is similar to a `WHERE InstanceName LIKE NameFilter` clause of a SQL query.</span></span>
- <span data-ttu-id="35bde-147">Le filtre de l’ID d’instance est facultatif.</span><span class="sxs-lookup"><span data-stu-id="35bde-147">The instance ID filter is optional.</span></span> <span data-ttu-id="35bde-148">S’il est présent (par exemple, s’il est défini sur une valeur autre que `0xFFFFFFFF` ), il indique que la requête doit uniquement collecter les instances où l’ID d’instance correspond à l’ID spécifié.</span><span class="sxs-lookup"><span data-stu-id="35bde-148">If present (i.e. if set to a value other than `0xFFFFFFFF`), it indicates that the query should only collect instances where the instance ID matches the specified ID.</span></span> <span data-ttu-id="35bde-149">En cas d’absence (c’est-à-dire si `0xFFFFFFFF` la valeur est), elle indique que la requête doit accepter tous les ID d’instance.</span><span class="sxs-lookup"><span data-stu-id="35bde-149">If absent (i.e. if set to `0xFFFFFFFF`), it indicates that the query should accept all instance IDs.</span></span> <span data-ttu-id="35bde-150">Cela est similaire à une `WHERE InstanceId == IdFilter` clause d’une requête SQL.</span><span class="sxs-lookup"><span data-stu-id="35bde-150">This is similar to a `WHERE InstanceId == IdFilter` clause of a SQL query.</span></span>
- <span data-ttu-id="35bde-151">Le filtre de l’ID de compteur est facultatif.</span><span class="sxs-lookup"><span data-stu-id="35bde-151">The counter ID filter is optional.</span></span> <span data-ttu-id="35bde-152">Si elle est présente (c’est-à-dire si elle est définie sur une valeur autre que `PERF_WILDCARD_COUNTER` ), elle indique que la requête doit collecter un compteur unique, similaire à une `SELECT CounterName` clause d’une requête SQL.</span><span class="sxs-lookup"><span data-stu-id="35bde-152">If present (i.e. if set to a value other than `PERF_WILDCARD_COUNTER`), it indicates that the query should collect a single counter, similar to a `SELECT CounterName` clause of a SQL query.</span></span> <span data-ttu-id="35bde-153">En cas d’absence (c’est-à-dire si `PERF_WILDCARD_COUNTER` la valeur est), elle indique que la requête doit collecter tous les compteurs disponibles, comme dans une `SELECT *` clause d’une requête SQL.</span><span class="sxs-lookup"><span data-stu-id="35bde-153">If absent (i.e. if set to `PERF_WILDCARD_COUNTER`), it indicates that the query should collect all available counters, similar to a `SELECT *` clause of a SQL query.</span></span>

<span data-ttu-id="35bde-154">Utilisez **PerfAddCounters** pour ajouter des requêtes à un handle de requête.</span><span class="sxs-lookup"><span data-stu-id="35bde-154">Use **PerfAddCounters** to add queries to a query handle.</span></span> <span data-ttu-id="35bde-155">Utilisez **PerfDeleteCounters** pour supprimer des requêtes d’un handle de requête.</span><span class="sxs-lookup"><span data-stu-id="35bde-155">Use **PerfDeleteCounters** to remove queries from a query handle.</span></span>

<span data-ttu-id="35bde-156">Après avoir modifié les requêtes dans un handle de requête, utilisez **PerfQueryCounterInfo** pour obtenir les index de requête.</span><span class="sxs-lookup"><span data-stu-id="35bde-156">After changing the queries in a query handle, use **PerfQueryCounterInfo** to obtain the query indexes.</span></span> <span data-ttu-id="35bde-157">Les index indiquent l’ordre dans lequel les résultats de la requête sont retournés par **PerfQueryCounterData** (les résultats ne correspondent pas toujours à l’ordre dans lequel les requêtes ont été ajoutées).</span><span class="sxs-lookup"><span data-stu-id="35bde-157">The indexes indicate the order in which the query results will be returned by **PerfQueryCounterData** (the results will not always match the order in which the queries were added).</span></span>

<span data-ttu-id="35bde-158">Une fois que le handle de requête est prêt, utilisez **PerfQueryCounterData** pour collecter les données.</span><span class="sxs-lookup"><span data-stu-id="35bde-158">Once the query handle is ready, use **PerfQueryCounterData** to collect the data.</span></span> <span data-ttu-id="35bde-159">Normalement, vous collectez les données régulièrement (une fois par seconde ou une fois par minute), puis traitez les données en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="35bde-159">You will normally collect the data periodically (once a second or once a minute) then process the data as needed.</span></span>

> [!NOTE]
> <span data-ttu-id="35bde-160">Les compteurs de performance ne sont pas conçus pour être collectés plusieurs fois par seconde.</span><span class="sxs-lookup"><span data-stu-id="35bde-160">Performance counters are not designed to be collected more than once per second.</span></span>

<span data-ttu-id="35bde-161">**PerfQueryCounterData** retourne un `PERF_DATA_HEADER` bloc, qui se compose d’un en-tête de données avec des horodateurs suivis d’une séquence de `PERF_COUNTER_HEADER` blocs, chacun contenant les résultats d’une requête.</span><span class="sxs-lookup"><span data-stu-id="35bde-161">**PerfQueryCounterData** will return a `PERF_DATA_HEADER` block, which consists of a data header with timestamps followed by a sequence of `PERF_COUNTER_HEADER` blocks, each containing the results of one query.</span></span>

<span data-ttu-id="35bde-162">`PERF_COUNTER_HEADER`Peut contenir plusieurs types de données différents, comme indiqué par la valeur du `dwType` champ :</span><span class="sxs-lookup"><span data-stu-id="35bde-162">The `PERF_COUNTER_HEADER` may contain various different kinds of data, as indicated by the value of the `dwType` field:</span></span>

- <span data-ttu-id="35bde-163">`PERF_ERROR_RETURN` -PerfLib ne peut pas récupérer les données de compteur valides à partir du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="35bde-163">`PERF_ERROR_RETURN` - PerfLib cannot get valid counter data back from provider.</span></span>
- <span data-ttu-id="35bde-164">`PERF_SINGLE_COUNTER` -La requête était destinée à un compteur unique à partir d’un CounterSet à instance unique.</span><span class="sxs-lookup"><span data-stu-id="35bde-164">`PERF_SINGLE_COUNTER` - The query was for a single counter from a single-instance counterset.</span></span> <span data-ttu-id="35bde-165">Les résultats contiennent uniquement la valeur de compteur demandée.</span><span class="sxs-lookup"><span data-stu-id="35bde-165">The results contain only the requested counter value.</span></span>
- <span data-ttu-id="35bde-166">`PERF_MULTIPLE_COUNTERS` -La requête était destinée à plusieurs compteurs à partir d’un CounterSet à instance unique.</span><span class="sxs-lookup"><span data-stu-id="35bde-166">`PERF_MULTIPLE_COUNTERS` - The query was for multiple counters from a single-instance counterset.</span></span> <span data-ttu-id="35bde-167">Le résultat contient les valeurs de compteur, ainsi que des informations permettant de faire correspondre chaque valeur avec le compteur correspondant (c’est-à-dire les en-têtes de colonne).</span><span class="sxs-lookup"><span data-stu-id="35bde-167">The result contains the counter values along with information for matching each value up with the corresponding counter (i.e. column headings).</span></span>
- <span data-ttu-id="35bde-168">`PERF_MULTIPLE_INSTANCES` -La requête était destinée à un compteur unique à partir d’un CounterSet multi-instance.</span><span class="sxs-lookup"><span data-stu-id="35bde-168">`PERF_MULTIPLE_INSTANCES` - The query was for a single counter from a multi-instance counterset.</span></span> <span data-ttu-id="35bde-169">Les résultats contiennent les informations d’instance (par exemple, les en-têtes de ligne) et une valeur de compteur par instance.</span><span class="sxs-lookup"><span data-stu-id="35bde-169">The results contain the instance information (i.e. row headings) and one counter value per instance.</span></span>
- <span data-ttu-id="35bde-170">`PERF_COUNTERSET` -La requête était destinée à plusieurs compteurs d’un CounterSet multi-instance.</span><span class="sxs-lookup"><span data-stu-id="35bde-170">`PERF_COUNTERSET` - The query was for multiple counters from a multi-instance counterset.</span></span> <span data-ttu-id="35bde-171">Les résultats contiennent les informations d’instance (par exemple, les en-têtes de ligne), les valeurs de compteur pour chaque instance et les informations pour faire correspondre chaque valeur avec le compteur correspondant (c’est-à-dire les en-têtes de colonne).</span><span class="sxs-lookup"><span data-stu-id="35bde-171">The results contain the instance information (i.e. row headings), the counter values for each instance, and information for matching each value up with the corresponding counter (i.e. column headings).</span></span>

<span data-ttu-id="35bde-172">Les valeurs retournées par **PerfQueryCounterData** sont des `UINT32` `UINT64` valeurs brutes ou.</span><span class="sxs-lookup"><span data-stu-id="35bde-172">The values returned by **PerfQueryCounterData** are `UINT32` or `UINT64` raw values.</span></span> <span data-ttu-id="35bde-173">Elles nécessitent généralement un traitement pour produire les valeurs mises en forme attendues.</span><span class="sxs-lookup"><span data-stu-id="35bde-173">These usually require some processing to produce the expected formatted values.</span></span> <span data-ttu-id="35bde-174">Le traitement requis dépend du type du compteur.</span><span class="sxs-lookup"><span data-stu-id="35bde-174">The required processing depends on the counter's type.</span></span> <span data-ttu-id="35bde-175">De nombreux types de compteurs requièrent des informations supplémentaires pour un traitement complet, par exemple un horodateur ou une valeur d’un compteur « base » dans le même échantillon.</span><span class="sxs-lookup"><span data-stu-id="35bde-175">Many counter types require additional information for complete processing, such as a timestamp or a value from a "base" counter in the same sample.</span></span>

<span data-ttu-id="35bde-176">Certains types de compteurs sont des compteurs « Delta » qui ne sont significatifs que lorsqu’ils sont comparés aux données d’un exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="35bde-176">Some counter types are "delta" counters that are only meaningful when compared with the data from a previous sample.</span></span> <span data-ttu-id="35bde-177">Par exemple, un compteur de type `PERF_SAMPLE_COUNTER` a une valeur mise en forme censée afficher un taux (le nombre de fois qu’une opération particulière s’est produite par seconde sur l’intervalle échantillon), mais la valeur brute réelle est simplement un nombre (le nombre de fois qu’une chose particulière s’est produite au total).</span><span class="sxs-lookup"><span data-stu-id="35bde-177">For example, a counter of type `PERF_SAMPLE_COUNTER` has a formatted value that is expected to show a rate (the number of times a particular thing happened per second over the sample interval), but the actual raw value is just a count (the number of times a particular thing has happened in total).</span></span> <span data-ttu-id="35bde-178">Pour produire la valeur « Rate » mise en forme, vous devez appliquer la formule correspondant au type de compteur.</span><span class="sxs-lookup"><span data-stu-id="35bde-178">To produce the formatted "rate" value, you must apply the formula corresponding to the counter type.</span></span> <span data-ttu-id="35bde-179">La formule pour `PERF_SAMPLE_COUNTER` est `(N1 - N0) / ((T1 - T0) / F)` : soustraire la valeur de l’exemple actuel de la valeur de l’exemple précédent (en indiquant le nombre de fois où l’événement s’est produit au cours de l’intervalle échantillon), puis divisez le résultat par le nombre de secondes dans l’intervalle échantillon (obtenu en soustrayant l’horodateur de l’exemple actuel de l’horodateur de l’exemple précédent et en divisant par</span><span class="sxs-lookup"><span data-stu-id="35bde-179">The formula for `PERF_SAMPLE_COUNTER` is `(N1 - N0) / ((T1 - T0) / F)`: subtract the current sample's value from the previous sample's value (giving the number of times the event occurred during the sample interval) then divide the result by the number of seconds in the sample interval (obtained by subtracting the current sample's timestamp from the previous sample's timestamp and dividing by frequency to convert the timespan into seconds).</span></span>

<span data-ttu-id="35bde-180">Pour plus d’informations sur le calcul des valeurs mises en forme à partir de valeurs brutes, consultez [calcul des valeurs de compteur](calculating-counter-values.md) .</span><span class="sxs-lookup"><span data-stu-id="35bde-180">Refer to [Calculating Counter Values](calculating-counter-values.md) for more information on computing formatted values from raw values.</span></span>

## <a name="sample"></a><span data-ttu-id="35bde-181">Exemple</span><span class="sxs-lookup"><span data-stu-id="35bde-181">Sample</span></span>

<span data-ttu-id="35bde-182">Le code suivant implémente un consommateur qui utilise les fonctions de consommateur de PerfLib v2 pour lire les informations de performances de l’UC à partir du CounterSet « informations sur le processeur ».</span><span class="sxs-lookup"><span data-stu-id="35bde-182">The following code implements a consumer that uses the PerfLib V2 Consumer functions to read CPU performance information from the "Processor Information" counterset.</span></span>

<span data-ttu-id="35bde-183">Le consommateur est organisé comme suit :</span><span class="sxs-lookup"><span data-stu-id="35bde-183">The consumer is organized as follows:</span></span>

- <span data-ttu-id="35bde-184">La `CpuPerfCounters` classe implémente la logique de consommation des données de performances.</span><span class="sxs-lookup"><span data-stu-id="35bde-184">The `CpuPerfCounters` class implements the logic for consuming performance data.</span></span> <span data-ttu-id="35bde-185">Il encapsule un handle de requête et une mémoire tampon de données dans laquelle les résultats de la requête sont enregistrés.</span><span class="sxs-lookup"><span data-stu-id="35bde-185">It encapsulates a query handle and a data buffer into which query results are recorded.</span></span>
- <span data-ttu-id="35bde-186">La `CpuPerfTimestamp` structure stocke les informations d’horodatage pour un exemple.</span><span class="sxs-lookup"><span data-stu-id="35bde-186">The `CpuPerfTimestamp` struct stores the timestamp information for a sample.</span></span> <span data-ttu-id="35bde-187">Chaque fois que des données sont collectées, l’appelant reçoit une seule `CpuPerfTimestamp` .</span><span class="sxs-lookup"><span data-stu-id="35bde-187">Each time data is collected the caller receives a single `CpuPerfTimestamp`.</span></span>
- <span data-ttu-id="35bde-188">La `CpuPerfData` structure stocke les informations de performance (nom de l’instance et valeurs de performances brutes) pour un processeur.</span><span class="sxs-lookup"><span data-stu-id="35bde-188">The `CpuPerfData` struct stores the performance information (instance name and raw performance values) for one CPU.</span></span> <span data-ttu-id="35bde-189">Chaque fois que des données sont collectées, l’appelant reçoit un tableau de `CpuPerfData` (un par UC).</span><span class="sxs-lookup"><span data-stu-id="35bde-189">Each time data is collected the caller receives an array of `CpuPerfData` (one per CPU).</span></span>

<span data-ttu-id="35bde-190">Cet exemple utilise des valeurs GUID et ID de compteur codées en dur, car il est optimisé pour un CounterSet (informations de processeur) spécifique qui ne change pas les valeurs GUID ou ID.</span><span class="sxs-lookup"><span data-stu-id="35bde-190">This sample uses hard-coded counterset GUID and counter ID values because it is optimized for a specific counterset (Processor Information) that will not change GUID or ID values.</span></span> <span data-ttu-id="35bde-191">Une classe plus générique qui lit les données de performances à partir de countersets arbitraires doit utiliser **PerfQueryCounterSetRegistrationInfo** pour rechercher le mappage entre les ID de compteur et les valeurs de compteur au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="35bde-191">A more-generic class that reads performance data from arbitrary countersets would need to use **PerfQueryCounterSetRegistrationInfo** to look up the mapping between counter IDs and counter values at runtime.</span></span>

<span data-ttu-id="35bde-192">Un `CpuPerfCountersConsumer.cpp` programme simple montre comment utiliser les valeurs de la `CpuPerfCounters` classe.</span><span class="sxs-lookup"><span data-stu-id="35bde-192">A simple `CpuPerfCountersConsumer.cpp` program shows how to use the values from the `CpuPerfCounters` class.</span></span>

### <a name="cpuperfcountersh"></a><span data-ttu-id="35bde-193">CpuPerfCounters. h</span><span class="sxs-lookup"><span data-stu-id="35bde-193">CpuPerfCounters.h</span></span>

```cpp
#pragma once
#include <sal.h>

// Contains timestamp data for a Processor Information data collection.
struct CpuPerfTimestamp
{
    __int64 PerfTimeStamp;   // Timestamp from the high-resolution clock.
    __int64 PerfTime100NSec; // The number of 100 nanosecond intervals since January 1, 1601, in Coordinated Universal Time (UTC).
    __int64 PerfFreq;        // The frequency of the high-resolution clock.
};

// Contains the raw data from a Processor Information sample.
// Note that the values returned are raw data. Converting from raw data to a
// friendly value may require computation, and the computation may require
// two samples of data. The computation depends on the Type, and the formula
// to use for each type can be found on MSDN.
// For example, ProcessorTime contains raw data of type PERF_100NSEC_TIMER_INV.
// Given two samples of data, s0 at time t0 and s1 at time t1, the friendly
// "% Processor Time" value is computed as:
// 100*(1-(s1.ProcessorTime-s0.ProcessorTime)/(t1.PerfTime100NSec-t0.PerfTime100NSec))
struct CpuPerfData
{
    wchar_t Name[16]; // Format: "NumaNode,NumaIndex", "NumaNode,_Total", or "_Total".
    __int64 unsigned ProcessorTime; // % Processor Time (#0, Type=PERF_100NSEC_TIMER_INV)
    __int64 unsigned UserTime; // % User Time (#1, Type=PERF_100NSEC_TIMER)
    __int64 unsigned PrivilegedTime; // % Privileged Time (#2, Type=PERF_100NSEC_TIMER)
    __int32 unsigned Interrupts; // Interrupts / sec (#3, Type=PERF_COUNTER_COUNTER)
    __int64 unsigned DpcTime; // % DPC Time (#4, Type=PERF_100NSEC_TIMER)
    __int64 unsigned InterruptTime; // % Interrupt Time (#5, Type=PERF_100NSEC_TIMER)
    __int32 unsigned DpcsQueued; // DPCs Queued / sec (#6, Type=PERF_COUNTER_COUNTER)
    __int32 unsigned Dpcs; // DPC Rate (#7, Type=PERF_COUNTER_RAWCOUNT)
    __int64 unsigned IdleTime; // % Idle Time (#8, Type=PERF_100NSEC_TIMER)
    __int64 unsigned C1Time; // % C1 Time (#9, Type=PERF_100NSEC_TIMER)
    __int64 unsigned C2Time; // % C2 Time (#10, Type=PERF_100NSEC_TIMER)
    __int64 unsigned C3Time; // % C3 Time (#11, Type=PERF_100NSEC_TIMER)
    __int64 unsigned C1Transitions; // C1 Transitions / sec (#12, Type=PERF_COUNTER_BULK_COUNT)
    __int64 unsigned C2Transitions; // C2 Transitions / sec (#13, Type=PERF_COUNTER_BULK_COUNT)
    __int64 unsigned C3Transitions; // C3 Transitions / sec (#14, Type=PERF_COUNTER_BULK_COUNT)
    __int64 unsigned PriorityTime; // % Priority Time (#15, Type=PERF_100NSEC_TIMER_INV)
    __int32 unsigned ParkingStatus; // Parking Status (#16, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned ProcessorFrequency; // Processor Frequency (#17, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned PercentMaximumFrequency; // % of Maximum Frequency (#18, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned ProcessorStateFlags; // Processor State Flags (#19, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned ClockInterrupts; // Clock Interrupts / sec (#20, Type=PERF_COUNTER_COUNTER)
    __int64 unsigned AverageIdleTime; // Average Idle Time (#21, Type=PERF_PRECISION_100NS_TIMER)
    __int64 unsigned AverageIdleTimeBase; // Average Idle Time Base (#22, Type=PERF_PRECISION_TIMESTAMP)
    __int64 unsigned IdleBreakEvents; // Idle Break Events / sec (#23, Type=PERF_COUNTER_BULK_COUNT)
    __int64 unsigned ProcessorPerformance; // % Processor Performance (#24, Type=PERF_AVERAGE_BULK)
    __int32 unsigned ProcessorPerformanceBase; // % Processor Performance Base (#25, Type=PERF_AVERAGE_BASE)
    __int64 unsigned ProcessorUtility; // % Processor Utility (#26, Type=PERF_AVERAGE_BULK)
    __int64 unsigned PrivilegedUtility; // % Privileged Utility (#28, Type=PERF_AVERAGE_BULK)
    __int32 unsigned UtilityBase; // % Utility Base (#27, Type=PERF_AVERAGE_BASE)
    __int32 unsigned PercentPerformanceLimit; // % Performance Limit (#30, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned PerformanceLimitFlags; // Performance Limit Flags (#31, Type=PERF_COUNTER_RAWCOUNT)
};

// Performs data collection from the Processor Information performance counter.
class CpuPerfCounters
{
public:

    CpuPerfCounters(CpuPerfCounters const&) = delete;
    void operator=(CpuPerfCounters const&) = delete;

    ~CpuPerfCounters();
    CpuPerfCounters() noexcept;

    // Reads CPU performance counter data.
    // Returns ERROR_SUCCESS (0) on success, ERROR_MORE_DATA if bufferCount is
    // too small, or another Win32 error code on failure.
    _Success_(return == 0)
    unsigned
    ReadData(
        _Out_opt_ CpuPerfTimestamp* timestamp,
        _Out_cap_post_count_(bufferCount, *bufferUsed) CpuPerfData* buffer,
        unsigned bufferCount,
        _Out_ unsigned* bufferUsed) noexcept;

private:

    void* m_hQuery;
    void* m_pData;
    unsigned m_cbData;
};
```

### <a name="cpuperfcounterscpp"></a><span data-ttu-id="35bde-194">CpuPerfCounters. cpp</span><span class="sxs-lookup"><span data-stu-id="35bde-194">CpuPerfCounters.cpp</span></span>

```cpp
#include "CpuPerfCounters.h"
#include <windows.h>
#include <perflib.h>
#include <winperf.h>
#include <stdlib.h>

_Check_return_ _Ret_maybenull_ _Post_writable_byte_size_(cb)
static void*
AllocateBytes(unsigned cb) noexcept
{
    return malloc(cb);
}

static void
FreeBytes(_Pre_maybenull_ _Post_invalid_ void* p) noexcept
{
    if (p)
    {
        free(p);
    }
    return;
}

static void
AssignCounterValue(
    _Inout_ __int32 unsigned* pVar,
    _In_ PERF_COUNTER_DATA const* pData) noexcept
{
    if (pData->dwDataSize == 4 ||
        pData->dwDataSize == 8)
    {
        *pVar = *reinterpret_cast<__int32 unsigned const*>(pData + 1);
    }
}

static void
AssignCounterValue(
    _Inout_ __int64 unsigned* pVar,
    _In_ PERF_COUNTER_DATA const* pData) noexcept
{
    if (pData->dwDataSize == 8)
    {
        *pVar = *reinterpret_cast<__int64 unsigned const*>(pData + 1);
    }
    else if (pData->dwDataSize == 4)
    {
        *pVar = *reinterpret_cast<__int32 unsigned const*>(pData + 1);
    }
}

CpuPerfCounters::~CpuPerfCounters()
{
    if (m_hQuery)
    {
        PerfCloseQueryHandle(m_hQuery);
    }

    FreeBytes(m_pData);
}

CpuPerfCounters::CpuPerfCounters() noexcept
    : m_hQuery()
    , m_pData()
    , m_cbData()
{
    return;
}

_Success_(return == 0)
unsigned
CpuPerfCounters::ReadData(
    _Out_opt_ CpuPerfTimestamp* timestamp,
    _Out_cap_post_count_(bufferCount, *bufferUsed) CpuPerfData* buffer,
    unsigned bufferCount,
    _Out_ unsigned* bufferUsed) noexcept
{
    unsigned status;
    DWORD cbData;
    PERF_DATA_HEADER* pDataHeader;
    PERF_COUNTER_HEADER const* pCounterHeader;
    PERF_MULTI_COUNTERS const* pMultiCounters;
    PERF_MULTI_INSTANCES const* pMultiInstances;
    PERF_INSTANCE_HEADER const* pInstanceHeader;
    unsigned cInstances = 0;

    if (m_hQuery == nullptr)
    {
        HANDLE hQuery = 0;
        status = PerfOpenQueryHandle(nullptr, &hQuery);
        if (ERROR_SUCCESS != status)
        {
            goto Done;
        }

        struct
        {
            PERF_COUNTER_IDENTIFIER Identifier;
            WCHAR Name[4];
        } querySpec = {
            {
                // ProcessorCounterSetGuid
                { 0xb4fc721a, 0x378, 0x476f, 0x89, 0xba, 0xa5, 0xa7, 0x9f, 0x81, 0xb, 0x36 },
                0,
                sizeof(querySpec),
                PERF_WILDCARD_COUNTER, // Get all data for each CPU.
                0xFFFFFFFF // Get data for all instance IDs.
            },
            L"*" // Get data for all instance names.
        };

        status = PerfAddCounters(hQuery, &querySpec.Identifier, sizeof(querySpec));
        if (ERROR_SUCCESS == status)
        {
            status = querySpec.Identifier.Status;
        }

        if (ERROR_SUCCESS != status)
        {
            PerfCloseQueryHandle(hQuery);
            goto Done;
        }

        // NOTE: A program that adds more than one query to the handle would need to call
        // PerfQueryCounterInfo to determine the order of the query results.

        m_hQuery = hQuery;
    }

    for (;;)
    {
        cbData = 0;
        pDataHeader = static_cast<PERF_DATA_HEADER*>(m_pData);
        status = PerfQueryCounterData(m_hQuery, pDataHeader, m_cbData, &cbData);
        if (ERROR_SUCCESS == status)
        {
            break;
        }
        else if (ERROR_NOT_ENOUGH_MEMORY != status)
        {
            goto Done;
        }

        FreeBytes(m_pData);
        m_cbData = 0;

        m_pData = AllocateBytes(cbData);
        if (nullptr == m_pData)
        {
            status = ERROR_OUTOFMEMORY;
            goto Done;
        }

        m_cbData = cbData;
    }

    // PERF_DATA_HEADER block = PERF_DATA_HEADER + dwNumCounters PERF_COUNTER_HEADER blocks
    if (cbData < sizeof(PERF_DATA_HEADER) ||
        cbData < pDataHeader->dwTotalSize ||
        pDataHeader->dwTotalSize < sizeof(PERF_DATA_HEADER) ||
        pDataHeader->dwNumCounters != 1)
    {
        status = ERROR_INVALID_DATA;
        goto Done;
    }

    // PERF_COUNTERSET block = PERF_COUNTER_HEADER + PERF_MULTI_COUNTERS block + PERF_MULTI_INSTANCES block
    cbData = pDataHeader->dwTotalSize - sizeof(PERF_DATA_HEADER);
    pCounterHeader = reinterpret_cast<PERF_COUNTER_HEADER*>(pDataHeader + 1);
    if (cbData < sizeof(PERF_COUNTER_HEADER) ||
        cbData < pCounterHeader->dwSize ||
        pCounterHeader->dwSize < sizeof(PERF_COUNTER_HEADER) ||
        PERF_COUNTERSET != pCounterHeader->dwType)
    {
        status = ERROR_INVALID_DATA;
        goto Done;
    }

    // PERF_MULTI_COUNTERS block = PERF_MULTI_COUNTERS + dwCounters DWORDs
    cbData = pCounterHeader->dwSize - sizeof(PERF_COUNTER_HEADER);
    pMultiCounters = reinterpret_cast<PERF_MULTI_COUNTERS const*>(pCounterHeader + 1);
    if (cbData < sizeof(PERF_MULTI_COUNTERS) ||
        cbData < pMultiCounters->dwSize ||
        pMultiCounters->dwSize < sizeof(PERF_MULTI_COUNTERS) ||
        (pMultiCounters->dwSize - sizeof(PERF_MULTI_COUNTERS)) / sizeof(DWORD) < pMultiCounters->dwCounters)
    {
        status = ERROR_INVALID_DATA;
        goto Done;
    }

    // PERF_MULTI_INSTANCES block = PERF_MULTI_INSTANCES + dwInstances instance data blocks
    cbData -= pMultiCounters->dwSize;
    pMultiInstances = reinterpret_cast<PERF_MULTI_INSTANCES const*>((LPCBYTE)pMultiCounters + pMultiCounters->dwSize);
    if (cbData < sizeof(PERF_MULTI_INSTANCES) ||
        cbData < pMultiInstances->dwTotalSize ||
        pMultiInstances->dwTotalSize < sizeof(PERF_MULTI_INSTANCES))
    {
        status = ERROR_INVALID_DATA;
        goto Done;
    }

    cInstances = pMultiInstances->dwInstances;
    if (bufferCount < cInstances)
    {
        status = ERROR_MORE_DATA;
        goto Done;
    }

    memset(buffer, 0, sizeof(buffer[0]) * cInstances);

    cbData = pMultiInstances->dwTotalSize - sizeof(PERF_MULTI_INSTANCES);
    pInstanceHeader = reinterpret_cast<PERF_INSTANCE_HEADER const*>(pMultiInstances + 1);
    for (unsigned iInstance = 0; iInstance != pMultiInstances->dwInstances; iInstance += 1)
    {
        CpuPerfData& d = buffer[iInstance];

        // instance data block = PERF_INSTANCE_HEADER block + dwCounters PERF_COUNTER_DATA blocks
        if (cbData < sizeof(PERF_INSTANCE_HEADER) ||
            cbData < pInstanceHeader->Size ||
            pInstanceHeader->Size < sizeof(PERF_INSTANCE_HEADER))
        {
            status = ERROR_INVALID_DATA;
            goto Done;
        }

        unsigned const instanceNameMax = (pInstanceHeader->Size - sizeof(PERF_INSTANCE_HEADER)) / sizeof(WCHAR);
        WCHAR const* const instanceName = reinterpret_cast<WCHAR const*>(pInstanceHeader + 1);
        if (instanceNameMax == wcsnlen(instanceName, instanceNameMax))
        {
            status = ERROR_INVALID_DATA;
            goto Done;
        }

        wcsncpy_s(d.Name, instanceName, _TRUNCATE);

        cbData -= pInstanceHeader->Size;
        PERF_COUNTER_DATA const* pCounterData = reinterpret_cast<PERF_COUNTER_DATA const*>((LPCBYTE)pInstanceHeader + pInstanceHeader->Size);
        for (unsigned iCounter = 0; iCounter != pMultiCounters->dwCounters; iCounter += 1)
        {
            if (cbData < sizeof(PERF_COUNTER_DATA) ||
                cbData < pCounterData->dwSize ||
                pCounterData->dwSize < sizeof(PERF_COUNTER_DATA) + 8 ||
                pCounterData->dwSize - sizeof(PERF_COUNTER_DATA) < pCounterData->dwDataSize)
            {
                status = ERROR_INVALID_DATA;
                goto Done;
            }

            DWORD const* pCounterIds = reinterpret_cast<DWORD const*>(pMultiCounters + 1);
            switch (pCounterIds[iCounter])
            {
            case 0: // PERF_100NSEC_TIMER_INV
                AssignCounterValue(&d.ProcessorTime, pCounterData);
                break;
            case 1: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.UserTime, pCounterData);
                break;
            case 2: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.PrivilegedTime, pCounterData);
                break;
            case 3: // PERF_COUNTER_COUNTER
                AssignCounterValue(&d.Interrupts, pCounterData);
                break;
            case 4: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.DpcTime, pCounterData);
                break;
            case 5: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.InterruptTime, pCounterData);
                break;
            case 6: // PERF_COUNTER_COUNTER
                AssignCounterValue(&d.DpcsQueued, pCounterData);
                break;
            case 7: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.Dpcs, pCounterData);
                break;
            case 8: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.IdleTime, pCounterData);
                break;
            case 9: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.C1Time, pCounterData);
                break;
            case 10: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.C2Time, pCounterData);
                break;
            case 11: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.C3Time, pCounterData);
                break;
            case 12: // PERF_COUNTER_BULK_COUNT
                AssignCounterValue(&d.C1Transitions, pCounterData);
                break;
            case 13: // PERF_COUNTER_BULK_COUNT
                AssignCounterValue(&d.C2Transitions, pCounterData);
                break;
            case 14: // PERF_COUNTER_BULK_COUNT
                AssignCounterValue(&d.C3Transitions, pCounterData);
                break;
            case 15: // PERF_100NSEC_TIMER_INV
                AssignCounterValue(&d.PriorityTime, pCounterData);
                break;
            case 16: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.ParkingStatus, pCounterData);
                break;
            case 17: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.ProcessorFrequency, pCounterData);
                break;
            case 18: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.PercentMaximumFrequency, pCounterData);
                break;
            case 19: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.ProcessorStateFlags, pCounterData);
                break;
            case 20: // PERF_COUNTER_COUNTER
                AssignCounterValue(&d.ClockInterrupts, pCounterData);
                break;
            case 21: // PERF_PRECISION_100NS_TIMER
                AssignCounterValue(&d.AverageIdleTime, pCounterData);
                break;
            case 22: // PERF_PRECISION_TIMESTAMP
                AssignCounterValue(&d.AverageIdleTimeBase, pCounterData);
                break;
            case 23: // PERF_COUNTER_BULK_COUNT
                AssignCounterValue(&d.IdleBreakEvents, pCounterData);
                break;
            case 24: // PERF_AVERAGE_BULK
                AssignCounterValue(&d.ProcessorPerformance, pCounterData);
                break;
            case 25: // PERF_AVERAGE_BASE
                AssignCounterValue(&d.ProcessorPerformanceBase, pCounterData);
                break;
            case 26: // PERF_AVERAGE_BULK
                AssignCounterValue(&d.ProcessorUtility, pCounterData);
                break;
            case 28: // PERF_AVERAGE_BULK
                AssignCounterValue(&d.PrivilegedUtility, pCounterData);
                break;
            case 27: // PERF_AVERAGE_BASE
                AssignCounterValue(&d.UtilityBase, pCounterData);
                break;
            case 30: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.PercentPerformanceLimit, pCounterData);
                break;
            case 31: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.PerformanceLimitFlags, pCounterData);
                break;
            }

            cbData -= pCounterData->dwSize;
            pCounterData = reinterpret_cast<PERF_COUNTER_DATA const*>((LPCBYTE)pCounterData + pCounterData->dwSize);
        }

        pInstanceHeader = reinterpret_cast<PERF_INSTANCE_HEADER const*>(pCounterData);
    }

    if (nullptr != timestamp)
    {
        timestamp->PerfTimeStamp = pDataHeader->PerfTimeStamp;
        timestamp->PerfTime100NSec = pDataHeader->PerfTime100NSec;
        timestamp->PerfFreq = pDataHeader->PerfFreq;
    }

    status = ERROR_SUCCESS;

Done:

    *bufferUsed = cInstances;
    return status;
}
```

### <a name="cpuperfcountersconsumercpp"></a><span data-ttu-id="35bde-195">CpuPerfCountersConsumer. cpp</span><span class="sxs-lookup"><span data-stu-id="35bde-195">CpuPerfCountersConsumer.cpp</span></span>

```cpp
#include <windows.h>
#include <stdio.h>
#include "CpuPerfCounters.h"
#include <utility>

int wmain()
{
    unsigned status;
    unsigned const dataMax = 30; // Support up to 30 instances
    CpuPerfCounters cpc;
    CpuPerfTimestamp timestamp[2];
    CpuPerfTimestamp* t0 = timestamp + 0;
    CpuPerfTimestamp* t1 = timestamp + 1;
    CpuPerfData data[dataMax * 2];
    CpuPerfData* d0 = data + 0;
    CpuPerfData* d1 = data + dataMax;
    unsigned used;

    status = cpc.ReadData(t0, d0, dataMax, &used);
    printf("ReadData0 used=%u, status=%u\n", used, status);

    for (unsigned iSample = 1; iSample != 10; iSample += 1)
    {
        Sleep(1000);
        status = cpc.ReadData(t1, d1, dataMax, &used);
        printf("ReadData%u used=%u, status=%u\n", iSample, used, status);

        if (status == ERROR_SUCCESS && used != 0)
        {
            // Show the ProcessorTime value from instance #0 (usually the "_Total" instance):
            auto& s0 = d0[0];
            auto& s1 = d1[0];
            printf("  %ls/%ls = %f\n", s0.Name, s1.Name,
                100.0 * (1.0 - static_cast<double>(s1.ProcessorTime - s0.ProcessorTime) / static_cast<double>(t1->PerfTime100NSec - t0->PerfTime100NSec)));

            std::swap(t0, t1); // Swap "current" and "previous" timestamp pointers.
            std::swap(d0, d1); // Swap "current" and "previous" sample pointers.
        }
    }

    return status;
}
```
