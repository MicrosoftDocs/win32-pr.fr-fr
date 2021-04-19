---
description: Le système utilise des compteurs pour collecter les données de performances.
ms.assetid: d1f1a90c-425a-4606-b86d-2948305ea84a
title: Spécification d’un chemin d’accès au compteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f3a92f94b4bf3d2252903d92785f43bb0cac110
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529832"
---
# <a name="specifying-a-counter-path"></a><span data-ttu-id="dd7c8-103">Spécification d’un chemin d’accès au compteur</span><span class="sxs-lookup"><span data-stu-id="dd7c8-103">Specifying a Counter Path</span></span>

<span data-ttu-id="dd7c8-104">Le système utilise des compteurs pour collecter les données de performances.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-104">The system uses counters to collect performance data.</span></span> <span data-ttu-id="dd7c8-105">Chaque compteur est identifié de manière unique par son nom, son chemin d’accès ou son emplacement.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-105">Each counter is uniquely identified through its name and its path, or location.</span></span> <span data-ttu-id="dd7c8-106">La syntaxe du chemin d’accès aux compteurs est la suivante :</span><span class="sxs-lookup"><span data-stu-id="dd7c8-106">The syntax of a counter path is:</span></span>

``` syntax
\\Computer\PerfObject(ParentInstance/ObjectInstance#InstanceIndex)\Counter
```

<span data-ttu-id="dd7c8-107">L’élément ordinateur spécifie le nom ou l’adresse IP de l’ordinateur à partir duquel vous souhaitez interroger les données de performances.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-107">The Computer element specifies the name or IP address of the computer from which you want to query performance data.</span></span> <span data-ttu-id="dd7c8-108">Le nom de l’ordinateur est facultatif si le compteur se trouve sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-108">The computer name is optional if the counter is located on the local computer.</span></span>

<span data-ttu-id="dd7c8-109">L’élément PerfObject spécifie l’objet de performance à interroger.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-109">The PerfObject element specifies the performance object to query.</span></span> <span data-ttu-id="dd7c8-110">Un objet de performance peut être un composant physique, tel que des processeurs, des disques et de la mémoire, ou un objet système, tel que des processus et des threads.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-110">A performance object can be a physical component, such as processors, disks, and memory, or a system object, such as processes and threads.</span></span> <span data-ttu-id="dd7c8-111">Chaque objet système est lié à un élément fonctionnel au sein de l’ordinateur et est associé à un ensemble de compteurs standard.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-111">Each system object is related to a functional element within the computer and has a set of standard counters assigned to it.</span></span> <span data-ttu-id="dd7c8-112">Chaque ordinateur peut avoir un ensemble différent d’objets de performance et de compteurs installés sur celui-ci, car les applications peuvent installer leurs propres objets et compteurs de performances.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-112">Each computer may have a different set of performance objects and counters installed on it because applications can install their own performance objects and counters.</span></span> <span data-ttu-id="dd7c8-113">Pour obtenir la liste des objets et compteurs de performance installés sur votre ordinateur, consultez la boîte de dialogue **Ajouter des compteurs** dans l’outil performances de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-113">For a list of the performance objects and counters installed on your computer, see the **Add Counters** dialog box in the Performance tool on your computer.</span></span> <span data-ttu-id="dd7c8-114">Ces objets sont également répertoriés dans la boîte de dialogue de navigation PDH (voir [compteurs de navigation](browsing-counters.md)).</span><span class="sxs-lookup"><span data-stu-id="dd7c8-114">These objects are also listed in the PDH browse dialog box (see [Browsing Counters](browsing-counters.md)).</span></span> <span data-ttu-id="dd7c8-115">Pour obtenir la liste des compteurs et des objets de performance système, consultez [compteurs par objet](/previous-versions/windows/it-pro/windows-server-2003/cc783073(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="dd7c8-115">For a list of system performance objects and counters, see [Counters by Object](/previous-versions/windows/it-pro/windows-server-2003/cc783073(v=ws.10)).</span></span>

<span data-ttu-id="dd7c8-116">ParentInstance, ObjectInstance et InstanceIndex sont inclus dans le chemin d’accès si plusieurs instances de l’objet peuvent exister.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-116">The ParentInstance, ObjectInstance, and InstanceIndex are included in the path if multiple instances of the object can exist.</span></span> <span data-ttu-id="dd7c8-117">Par exemple, les processus et les threads sont des objets d’instance multiples, car plusieurs processus ou threads peuvent s’exécuter en même temps.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-117">For example, processes and threads are multiple instance objects because more than one process or thread can run at the same time.</span></span> <span data-ttu-id="dd7c8-118">Si un objet peut avoir plusieurs instances, le chemin d’accès au compteur doit spécifier une instance d’objet.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-118">If an object can have more than one instance, the counter path must specify an object instance.</span></span>

<span data-ttu-id="dd7c8-119">Le format des éléments liés à l’instance dépend du type d’objet.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-119">The format of the instance related elements depends on the object type.</span></span> <span data-ttu-id="dd7c8-120">Si l’objet a des instances simples, le format est uniquement le nom de l’instance entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-120">If the object has simple instances, then the format is only the instance name enclosed in parentheses.</span></span> <span data-ttu-id="dd7c8-121">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="dd7c8-121">For example:</span></span>

``` syntax
(Explorer)
```

<span data-ttu-id="dd7c8-122">Si l’instance de cet objet requiert également un nom d’instance parente, le nom de l’instance parente doit précéder l’instance de l’objet et être séparé par un caractère de barre oblique.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-122">If the instance of this object also requires a parent instance name, the parent instance name must come before the object instance and be separated by a forward slash character.</span></span> <span data-ttu-id="dd7c8-123">Par exemple, les threads appartiennent à des processus.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-123">For example, threads belong to processes.</span></span> <span data-ttu-id="dd7c8-124">Si vous interrogez un objet thread, vous devez également spécifier le processus auquel il appartient, comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="dd7c8-124">If you query a thread object, you must also specify the process to which it belongs as shown in the following example:</span></span>

``` syntax
(Explorer/0)
```

<span data-ttu-id="dd7c8-125">Si l’objet a plusieurs instances qui ont la même chaîne de nom, elles peuvent être indexées séquentiellement en spécifiant l’index d’instance préfixé par un signe dièse.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-125">If the object has multiple instances that have the same name string, they can be indexed sequentially by specifying the instance index prefixed by a pound sign.</span></span> <span data-ttu-id="dd7c8-126">Les index d’instance sont de base 0.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-126">Instance indexes are 0-based.</span></span> <span data-ttu-id="dd7c8-127">Si vous souhaitez interroger la première instance, n’incluez pas \# 0. spécifiez simplement le nom de l’instance.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-127">If you want to query the first instance, do not include \#0—just specify the instance name.</span></span> <span data-ttu-id="dd7c8-128">Pour spécifier la deuxième instance, utilisez \# 1 ; pour spécifier la troisième instance, utilisez \# 2, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-128">To specify the second instance, use \#1; to specify the third instance, use \#2; and so on.</span></span> <span data-ttu-id="dd7c8-129">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="dd7c8-129">For example:</span></span>

``` syntax
(Explorer/0#1)
```

<span data-ttu-id="dd7c8-130">L’élément Counter spécifie le compteur de performance que vous souhaitez interroger pour l’objet de performance donné.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-130">The Counter element specifies the performance counter that you want to query for the given the performance object.</span></span>

<span data-ttu-id="dd7c8-131">PDH utilise les caractères spéciaux suivants dans un chemin d’accès de compteur.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-131">PDH uses the following special characters in a counter path.</span></span> <span data-ttu-id="dd7c8-132">Les fournisseurs ne doivent pas utiliser ces caractères dans leurs noms.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-132">Providers should not use these characters in their names.</span></span> <span data-ttu-id="dd7c8-133">Si un fournisseur utilise ces caractères spéciaux, PDH ne peut pas analyser le chemin d’accès complet au compteur pour obtenir les noms des compteurs et des instances.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-133">If a provider uses these special characters, PDH cannot parse the full counter path to obtain the counter and instances names.</span></span>



| <span data-ttu-id="dd7c8-134">Caractère</span><span class="sxs-lookup"><span data-stu-id="dd7c8-134">Character</span></span> | <span data-ttu-id="dd7c8-135">Description</span><span class="sxs-lookup"><span data-stu-id="dd7c8-135">Description</span></span>                                                |
|-----------|------------------------------------------------------------|
| \\        | <span data-ttu-id="dd7c8-136">Séparateur générique pour l’ordinateur, l’objet et le compteur.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-136">Generic separator for computer, object, and counter.</span></span>       |
| <span data-ttu-id="dd7c8-137">(</span><span class="sxs-lookup"><span data-stu-id="dd7c8-137">(</span></span>         | <span data-ttu-id="dd7c8-138">Début du nom de l’instance.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-138">Beginning of instance name.</span></span>                                |
| <span data-ttu-id="dd7c8-139">)</span><span class="sxs-lookup"><span data-stu-id="dd7c8-139">)</span></span>         | <span data-ttu-id="dd7c8-140">Fin du nom de l’instance.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-140">Ending of instance name.</span></span>                                   |
| /         | <span data-ttu-id="dd7c8-141">Sépare l’instance et l’instance parente.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-141">Separates instance and parent instance.</span></span>                    |
| <span data-ttu-id="dd7c8-142">\#n</span><span class="sxs-lookup"><span data-stu-id="dd7c8-142">\#n</span></span>       | <span data-ttu-id="dd7c8-143">Identifie une occurrence spécifique d’une instance de même nom.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-143">Identifies a specific occurrence of a same-named instance.</span></span> |
| \*        | <span data-ttu-id="dd7c8-144">Caractère générique.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-144">Wildcard character.</span></span>                                        |



 

<span data-ttu-id="dd7c8-145">Les exemples suivants illustrent les formats possibles pour les chemins de compteur :</span><span class="sxs-lookup"><span data-stu-id="dd7c8-145">The following examples show the possible formats for counter paths:</span></span>

-   <span data-ttu-id="dd7c8-146">\\\\\\compteur objet ordinateur (index parent/instance \# ) \\</span><span class="sxs-lookup"><span data-stu-id="dd7c8-146">\\\\computer\\object(parent/instance\#index)\\counter</span></span>
-   <span data-ttu-id="dd7c8-147">\\\\\\compteur objet ordinateur (parent/instance) \\</span><span class="sxs-lookup"><span data-stu-id="dd7c8-147">\\\\computer\\object(parent/instance)\\counter</span></span>
-   <span data-ttu-id="dd7c8-148">\\\\\\compteur de l’objet ordinateur (index d’instance \# ) \\</span><span class="sxs-lookup"><span data-stu-id="dd7c8-148">\\\\computer\\object(instance\#index)\\counter</span></span>
-   <span data-ttu-id="dd7c8-149">\\\\\\compteur de l’objet ordinateur (instance) \\</span><span class="sxs-lookup"><span data-stu-id="dd7c8-149">\\\\computer\\object(instance)\\counter</span></span>
-   <span data-ttu-id="dd7c8-150">\\\\\\compteur d’objets ordinateur \\</span><span class="sxs-lookup"><span data-stu-id="dd7c8-150">\\\\computer\\object\\counter</span></span>
-   <span data-ttu-id="dd7c8-151">\\compteur de l’objet (index parent/instance \# ) \\</span><span class="sxs-lookup"><span data-stu-id="dd7c8-151">\\object(parent/instance\#index)\\counter</span></span>
-   <span data-ttu-id="dd7c8-152">\\compteur de l’objet (parent/instance) \\</span><span class="sxs-lookup"><span data-stu-id="dd7c8-152">\\object(parent/instance)\\counter</span></span>
-   <span data-ttu-id="dd7c8-153">\\compteur de l’objet (index d’instance \# ) \\</span><span class="sxs-lookup"><span data-stu-id="dd7c8-153">\\object(instance\#index)\\counter</span></span>
-   <span data-ttu-id="dd7c8-154">\\compteur de l’objet (instance) \\</span><span class="sxs-lookup"><span data-stu-id="dd7c8-154">\\object(instance)\\counter</span></span>
-   <span data-ttu-id="dd7c8-155">\\compteur d’objets \\</span><span class="sxs-lookup"><span data-stu-id="dd7c8-155">\\object\\counter</span></span>

## <a name="using-wildcard-characters"></a><span data-ttu-id="dd7c8-156">Utilisation de caractères génériques</span><span class="sxs-lookup"><span data-stu-id="dd7c8-156">Using wildcard characters</span></span>

<span data-ttu-id="dd7c8-157">Les chemins d’accès des compteurs peuvent contenir un caractère générique uniquement pour le nom de l’instance, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="dd7c8-157">Counter paths may contain a wildcard character only for the instance name as shown in the following example.</span></span>

``` syntax
\Process(*)\% Processor Time
```

<span data-ttu-id="dd7c8-158">Pour développer le caractère générique dans une liste de chemins de compteurs qui contiennent des instances trouvées sur l’ordinateur ou dans le fichier journal, appelez [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha).</span><span class="sxs-lookup"><span data-stu-id="dd7c8-158">To expand the wildcard into a list of counter paths that contain instances found on the computer or in the log file, call [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha).</span></span>

 

 
