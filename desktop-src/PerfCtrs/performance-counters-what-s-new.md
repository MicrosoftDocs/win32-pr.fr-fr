---
description: Cette section décrit les nouvelles fonctionnalités qui ont été ajoutées aux compteurs de performance pour chaque version.
ms.assetid: 14bdae6c-9dcd-401e-8c43-5391e00cf7e3
title: Nouveautés (compteurs de performances)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f0c1189a185351eabae438a01c6f111952f164e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517850"
---
# <a name="whats-new-with-performance-counters"></a><span data-ttu-id="b67ca-103">Nouveautés des compteurs de performances</span><span class="sxs-lookup"><span data-stu-id="b67ca-103">What's New with Performance Counters</span></span>

<span data-ttu-id="b67ca-104">Cette section décrit les nouvelles fonctionnalités qui ont été ajoutées aux compteurs de performance pour chaque version.</span><span class="sxs-lookup"><span data-stu-id="b67ca-104">This section describes the new features that were added to Performance Counters for each release.</span></span>

## <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="b67ca-105">Windows 7 et Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b67ca-105">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="b67ca-106">L’outil [CTRPP](ctrpp.md) a été modifié pour améliorer et simplifier la génération de code.</span><span class="sxs-lookup"><span data-stu-id="b67ca-106">The [CTRPP](ctrpp.md) tool was changed to improve and simplify code generation.</span></span> <span data-ttu-id="b67ca-107">L’outil génère désormais uniquement un fichier d’en-tête et un fichier de ressources.</span><span class="sxs-lookup"><span data-stu-id="b67ca-107">The tool now generates only a header and resource file.</span></span> <span data-ttu-id="b67ca-108">Si vous souhaitez un ancien comportement de génération de code (non recommandé), vous pouvez utiliser le nouvel `-legacy` argument.</span><span class="sxs-lookup"><span data-stu-id="b67ca-108">If you want to old code generation behavior (not recommended), you can use the new `-legacy` argument.</span></span>

- <span data-ttu-id="b67ca-109">Vous devez maintenant spécifier les nouveaux `-o` `-rc` arguments et qui spécifient respectivement le nom et l’emplacement de l’en-tête et du fichier de ressources.</span><span class="sxs-lookup"><span data-stu-id="b67ca-109">You must now specify the new `-o` and `-rc` arguments that specify the name and location of the header and resource file, respectively.</span></span>
- <span data-ttu-id="b67ca-110">Vous pouvez utiliser l’argument New facultatif `-prefix` pour spécifier une chaîne à ajouter au début des variables globales et des fonctions définies dans le fichier d’en-tête généré.</span><span class="sxs-lookup"><span data-stu-id="b67ca-110">You can use the optional new `-prefix` argument to specify a string to add to the beginning of global variables and functions defined in the generated header file.</span></span>
- <span data-ttu-id="b67ca-111">Si vous devez mettre à jour votre manifeste de compteurs, l’utilisation de la nouvelle génération de code élimine la nécessité de fusionner votre implémentation de rappel précédente avec le nouveau code généré, car les rappels ne sont plus inclus dans le code généré.</span><span class="sxs-lookup"><span data-stu-id="b67ca-111">If you have to update your counters manifest, using the new code generation eliminates the need to merge your previous callback implementation with the new generated code since the callbacks are no longer included in the generated code.</span></span>

<span data-ttu-id="b67ca-112">Un nouvel `symbol` attribut est disponible pour les éléments de manifeste suivants :</span><span class="sxs-lookup"><span data-stu-id="b67ca-112">A new `symbol` attribute is available for the following manifest elements:</span></span>

- [<span data-ttu-id="b67ca-113">moteur</span><span class="sxs-lookup"><span data-stu-id="b67ca-113">provider</span></span>](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element)
- [<span data-ttu-id="b67ca-114">counterSet</span><span class="sxs-lookup"><span data-stu-id="b67ca-114">counterSet</span></span>](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element)
- [<span data-ttu-id="b67ca-115">)</span><span class="sxs-lookup"><span data-stu-id="b67ca-115">counter</span></span>](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element)

<span data-ttu-id="b67ca-116">L' `symbol` attribut est requis pour [Provider](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) et [counterSet](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element), et est facultatif pour [Counter](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element).</span><span class="sxs-lookup"><span data-stu-id="b67ca-116">The `symbol` attribute is required for [provider](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) and [counterSet](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element), and is optional for [counter](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element).</span></span> <span data-ttu-id="b67ca-117">L’attribut vous permet de fournir un nom symbolique que vous pouvez utiliser pour référencer chaque élément lors de l’appel des fonctions du fournisseur (par exemple, vous pouvez utiliser le nom symbolique de l’ensemble de compteurs lors de l’appel de [PerfCreateInstance](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)).</span><span class="sxs-lookup"><span data-stu-id="b67ca-117">The attribute lets you provide a symbolic name that you can use to reference each element when calling the provider functions (for example, you can use the counter set symbolic name when calling [PerfCreateInstance](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)).</span></span>

## <a name="windows-vista"></a><span data-ttu-id="b67ca-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b67ca-118">Windows Vista</span></span>

<span data-ttu-id="b67ca-119">L’architecture des compteurs de performance pour la fourniture de données de compteur a été complètement modifiée pour cette version.</span><span class="sxs-lookup"><span data-stu-id="b67ca-119">The Performance Counters architecture for providing counter data was completely changed for this release.</span></span>

<span data-ttu-id="b67ca-120">Précédemment, vous avez utilisé un fichier INI pour définir vos données de compteur et vous avez implémenté une DLL de performance qui a été exécutée dans le processus du consommateur pour fournir les données lorsqu’un consommateur l’a demandée.</span><span class="sxs-lookup"><span data-stu-id="b67ca-120">Previously, you used an INI file to define your counter data and you implemented a performance DLL which ran in the consumer's process to provide the data when a consumer requested it.</span></span> <span data-ttu-id="b67ca-121">Cette architecture est déconseillée et n’est pas recommandée pour le nouveau code en raison de problèmes importants en matière de performances et de fiabilité.</span><span class="sxs-lookup"><span data-stu-id="b67ca-121">This architecture is deprecated and is not recommended for new code due to significant performance and reliability issues.</span></span>

<span data-ttu-id="b67ca-122">La nouvelle architecture utilise un manifeste pour définir les données de compteur et exécute le code dans le processus du fournisseur pour fournir les données lorsqu’un consommateur le demande.</span><span class="sxs-lookup"><span data-stu-id="b67ca-122">The new architecture uses a manifest to define the counter data and runs code in the provider's process to provide the data when a consumer requests it.</span></span> <span data-ttu-id="b67ca-123">Pour plus d’informations, consultez [fourniture de données de compteur à l’aide de la Version 2,0](providing-counter-data-using-version-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="b67ca-123">For additional details, see [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md).</span></span>

<span data-ttu-id="b67ca-124">Les fonctions suivantes ont été ajoutées pour cette version :</span><span class="sxs-lookup"><span data-stu-id="b67ca-124">The following functions were added for this release:</span></span>

- [<span data-ttu-id="b67ca-125">ControlCallback</span><span class="sxs-lookup"><span data-stu-id="b67ca-125">ControlCallback</span></span>](/windows/desktop/api/Perflib/nc-perflib-perflibrequest)
- [<span data-ttu-id="b67ca-126">PerfCreateInstance</span><span class="sxs-lookup"><span data-stu-id="b67ca-126">PerfCreateInstance</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)
- [<span data-ttu-id="b67ca-127">PerfDeleteInstance</span><span class="sxs-lookup"><span data-stu-id="b67ca-127">PerfDeleteInstance</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance)
- [<span data-ttu-id="b67ca-128">PerfQueryInstance</span><span class="sxs-lookup"><span data-stu-id="b67ca-128">PerfQueryInstance</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfqueryinstance)
- [<span data-ttu-id="b67ca-129">PerfSetCounterSetInfo</span><span class="sxs-lookup"><span data-stu-id="b67ca-129">PerfSetCounterSetInfo</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo)
- [<span data-ttu-id="b67ca-130">PerfSetULongCounterValue</span><span class="sxs-lookup"><span data-stu-id="b67ca-130">PerfSetULongCounterValue</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
- [<span data-ttu-id="b67ca-131">PerfSetULongLongCounterValue</span><span class="sxs-lookup"><span data-stu-id="b67ca-131">PerfSetULongLongCounterValue</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
- [<span data-ttu-id="b67ca-132">PerfSetCounterRefValue</span><span class="sxs-lookup"><span data-stu-id="b67ca-132">PerfSetCounterRefValue</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)
- [<span data-ttu-id="b67ca-133">PerfStartProvider</span><span class="sxs-lookup"><span data-stu-id="b67ca-133">PerfStartProvider</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider)
- [<span data-ttu-id="b67ca-134">PerfStopProvider</span><span class="sxs-lookup"><span data-stu-id="b67ca-134">PerfStopProvider</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider)

<span data-ttu-id="b67ca-135">Les structures suivantes ont été ajoutées pour cette version :</span><span class="sxs-lookup"><span data-stu-id="b67ca-135">The following structures were added for this release:</span></span>

- [<span data-ttu-id="b67ca-136">\_identité du compteur de performances \_</span><span class="sxs-lookup"><span data-stu-id="b67ca-136">PERF\_COUNTER\_IDENTITY</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [<span data-ttu-id="b67ca-137">\_informations sur le compteur de performances \_</span><span class="sxs-lookup"><span data-stu-id="b67ca-137">PERF\_COUNTER\_INFO</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [<span data-ttu-id="b67ca-138">\_informations du COUNTERSET de performance \_</span><span class="sxs-lookup"><span data-stu-id="b67ca-138">PERF\_COUNTERSET\_INFO</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [<span data-ttu-id="b67ca-139">\_instance du COUNTERSET de performance \_</span><span class="sxs-lookup"><span data-stu-id="b67ca-139">PERF\_COUNTERSET\_INSTANCE</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)

<span data-ttu-id="b67ca-140">Pour obtenir la liste des éléments XML que vous utilisez dans votre manifeste pour définir vos compteurs, consultez [schéma des compteurs de performances](performance-counters-schema.md).</span><span class="sxs-lookup"><span data-stu-id="b67ca-140">For a list of the XML elements that you use in your manifest to define your counters, see [Performance Counters Schema](performance-counters-schema.md).</span></span>

<span data-ttu-id="b67ca-141">Pour plus d’informations sur l’outil de pré-processeur CTRPP qui analyse votre manifeste et génère le code que vous utilisez comme point de départ pour votre fournisseur, consultez [CTRPP](ctrpp.md).</span><span class="sxs-lookup"><span data-stu-id="b67ca-141">For information on the CTRPP pre-processor tool that parses your manifest and generates the code that you use as the starting point for your provider, see [CTRPP](ctrpp.md).</span></span>
