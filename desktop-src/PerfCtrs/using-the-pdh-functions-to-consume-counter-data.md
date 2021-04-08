---
description: Vous utilisez les fonctions PDH pour collecter les données de performances.
ms.assetid: 2510480e-cfea-4f7c-af0b-6d229c150c91
title: Utilisation des fonctions PDH pour consommer des données de compteur
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 431bf160ef6ca54b4a37363d7fe6ed48bb25d953
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865089"
---
# <a name="using-the-pdh-functions-to-consume-counter-data"></a><span data-ttu-id="1286d-103">Utilisation des fonctions PDH pour consommer des données de compteur</span><span class="sxs-lookup"><span data-stu-id="1286d-103">Using the PDH Functions to Consume Counter Data</span></span>

<span data-ttu-id="1286d-104">Utilisez les fonctions PDH pour collecter les données de performances.</span><span class="sxs-lookup"><span data-stu-id="1286d-104">Use the PDH functions to collect performance data.</span></span> <span data-ttu-id="1286d-105">Les fonctions PDH sont plus faciles à utiliser que les [fonctions de Registre](using-the-registry-functions-to-consume-counter-data.md) et peuvent être utilisées pour accéder aux données de compteur à la fois dans les fournisseurs v1 et v2.</span><span class="sxs-lookup"><span data-stu-id="1286d-105">The PDH functions are easier to use than the [registry functions](using-the-registry-functions-to-consume-counter-data.md) and can be used to access counter data both V1 and V2 providers.</span></span> <span data-ttu-id="1286d-106">PDH possède des API pour la collecte des données de performances actuelles, l’enregistrement des données de performances dans des fichiers journaux et la lecture de données à partir de fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="1286d-106">PDH has APIs for collecting current performance data, saving performance data to log files, and reading data from log files.</span></span>

> [!Note]
> <span data-ttu-id="1286d-107">Vous ne pouvez pas utiliser les fonctions de couche d’abstraction d’assistance des données de performances si vous écrivez des applications Windows OneCore.</span><span class="sxs-lookup"><span data-stu-id="1286d-107">You cannot use the Performance Data Helper abstraction-layer functions if you are writing Windows OneCore apps.</span></span> <span data-ttu-id="1286d-108">Utilisez plutôt des [fonctions de consommateur de Perflib v2](using-the-perflib-functions-to-consume-counter-data.md).</span><span class="sxs-lookup"><span data-stu-id="1286d-108">Instead, use [PerfLib V2 Consumer functions](using-the-perflib-functions-to-consume-counter-data.md).</span></span>

<span data-ttu-id="1286d-109">PDH est une API de haut niveau qui simplifie la collecte des données des compteurs de performances.</span><span class="sxs-lookup"><span data-stu-id="1286d-109">PDH is a high-level API that simplifies collecting performance counter data.</span></span> <span data-ttu-id="1286d-110">Elle facilite l’analyse des requêtes, la mise en cache des métadonnées, la correspondance des instances entre les exemples, le calcul des valeurs mises en forme à partir des valeurs brutes, la lecture des données des fichiers journaux et l’enregistrement des données dans les fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="1286d-110">It helps with query parsing, metadata caching, matching up instances between samples, computing formatted values from raw values, reading data from log files, and saving data to log files.</span></span> <span data-ttu-id="1286d-111">PDH utilise automatiquement les [fonctions de Registre](using-the-registry-functions-to-consume-counter-data.md) lors de la collecte de données à partir de **fournisseurs v1** et il utilise les [fonctions de consommateur v2](using-the-perflib-functions-to-consume-counter-data.md) lors de la collecte de données à partir de **fournisseurs v2**.</span><span class="sxs-lookup"><span data-stu-id="1286d-111">PDH automatically uses the [registry functions](using-the-registry-functions-to-consume-counter-data.md) when collecting data from **V1 providers** and it uses the [V2 Consumer functions](using-the-perflib-functions-to-consume-counter-data.md) when collecting data from **V2 providers**.</span></span>

<span data-ttu-id="1286d-112">Pour collecter des données de performances à l’aide des fonctions PDH, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="1286d-112">To collect performance data using the PDH functions, perform the following steps.</span></span>

1. [<span data-ttu-id="1286d-113">Créer une requête</span><span class="sxs-lookup"><span data-stu-id="1286d-113">Create a query</span></span>](creating-a-query.md)
2. [<span data-ttu-id="1286d-114">Ajouter des compteurs à la requête</span><span class="sxs-lookup"><span data-stu-id="1286d-114">Add counters to the query</span></span>](creating-a-query.md)
3. [<span data-ttu-id="1286d-115">Collecter les données de performances</span><span class="sxs-lookup"><span data-stu-id="1286d-115">Collect the performance data</span></span>](collecting-performance-data.md)
4. [<span data-ttu-id="1286d-116">Afficher les données de performances</span><span class="sxs-lookup"><span data-stu-id="1286d-116">Display the performance data</span></span>](displaying-performance-data.md)
5. [<span data-ttu-id="1286d-117">Fermer la requête</span><span class="sxs-lookup"><span data-stu-id="1286d-117">Close the query</span></span>](creating-a-query.md)

<span data-ttu-id="1286d-118">Vous pouvez collecter des données de performances à partir de sources ou de fichiers journaux en temps réel.</span><span class="sxs-lookup"><span data-stu-id="1286d-118">You can collect performance data from either real-time sources or log files.</span></span> <span data-ttu-id="1286d-119">Pour plus d’informations sur la façon d’écrire des données de performances dans des fichiers journaux, consultez [utilisation des fichiers journaux](working-with-log-files.md).</span><span class="sxs-lookup"><span data-stu-id="1286d-119">For more information on how to write performance data to log files, see [Working with Log Files](working-with-log-files.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="1286d-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1286d-120">See also</span></span>

- [<span data-ttu-id="1286d-121">Collecte des données de performances</span><span class="sxs-lookup"><span data-stu-id="1286d-121">Collecting Performance Data</span></span>](collecting-performance-data.md)
- [<span data-ttu-id="1286d-122">Exploration des compteurs</span><span class="sxs-lookup"><span data-stu-id="1286d-122">Browsing Counters</span></span>](browsing-counters.md)
- [<span data-ttu-id="1286d-123">Vérification des valeurs de retour de l’interface PDH</span><span class="sxs-lookup"><span data-stu-id="1286d-123">Checking PDH Interface Return Values</span></span>](checking-pdh-interface-return-values.md)
- [<span data-ttu-id="1286d-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="1286d-124">Examples</span></span>](examples.md)
