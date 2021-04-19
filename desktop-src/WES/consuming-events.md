---
title: Consommation d’événements (Journal des événements Windows)
description: Vous pouvez consommer des événements à partir de canaux ou de fichiers journaux.
ms.assetid: 17204d3f-0875-42c5-9af4-caca6349a67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb3fb1b36a0cd4ecf836a8893bc1abc14e46451
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106513574"
---
# <a name="consuming-events-windows-event-log"></a><span data-ttu-id="5e687-103">Consommation d’événements (Journal des événements Windows)</span><span class="sxs-lookup"><span data-stu-id="5e687-103">Consuming Events (Windows Event Log)</span></span>

<span data-ttu-id="5e687-104">Vous pouvez consommer des événements à partir de canaux ou de fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="5e687-104">You can consume events from channels or from log files.</span></span> <span data-ttu-id="5e687-105">Pour consommer des événements, vous pouvez utiliser tous les événements ou vous pouvez spécifier une expression XPath qui identifie les événements que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="5e687-105">To consume events, you can consume all events or you can specify an XPath expression that identifies the events that you want to consume.</span></span> <span data-ttu-id="5e687-106">Pour déterminer les éléments et les attributs d’un événement que vous pouvez utiliser dans votre expression XPath, consultez [schéma d’événement](eventschema-schema.md).</span><span class="sxs-lookup"><span data-stu-id="5e687-106">To determine the elements and attributes of an event that you can use in your XPath expression, see [Event Schema](eventschema-schema.md).</span></span>

<span data-ttu-id="5e687-107">Le journal des événements Windows prend en charge un sous-ensemble de XPath 1,0.</span><span class="sxs-lookup"><span data-stu-id="5e687-107">Windows Event Log supports a subset of XPath 1.0.</span></span> <span data-ttu-id="5e687-108">Pour plus d’informations sur les limitations, consultez [limitations de XPath 1,0](#xpath-10-limitations).</span><span class="sxs-lookup"><span data-stu-id="5e687-108">For details on the limitations, see [XPath 1.0 limitations](#xpath-10-limitations).</span></span>

<span data-ttu-id="5e687-109">Les exemples suivants illustrent des expressions XPath simples.</span><span class="sxs-lookup"><span data-stu-id="5e687-109">The following examples show simple XPath expressions.</span></span>


```XML
// The following query selects all events from the channel or log file
XPath Query: *

// The following query selects all the LowOnMemory events from the channel or log file
XPath Query: *[UserData/LowOnMemory]

// The following query selects all events with a severity level of 1 (Critical) from the channel or log file
XPath Query: *[System/Level=1]

// The following query shows a compound expression that selects all events from the channel or log file
// where the printer's name is MyPrinter and severity level is 1.
XPath Query: *[UserData/*/PrinterName="MyPrinter" and System/Level=1]

// The following query selects all events from the channel or log file where the severity level is
// less than or equal to 3 and the event occurred in the last 24 hour period.
XPath Query: *[System[(Level <= 3) and TimeCreated[timediff(@SystemTime) <= 86400000]]]
```



<span data-ttu-id="5e687-110">Vous pouvez utiliser les expressions XPath directement lors de l’appel des fonctions [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) ou [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) , ou vous pouvez utiliser une requête XML structurée qui contient l’expression XPath.</span><span class="sxs-lookup"><span data-stu-id="5e687-110">You can use the XPath expressions directly when calling the [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) or [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) functions or you can use a structured XML query that contains the XPath expression.</span></span> <span data-ttu-id="5e687-111">Pour les requêtes simples qui interrogent des événements à partir d’une seule source, l’utilisation d’une expression XPath est correcte.</span><span class="sxs-lookup"><span data-stu-id="5e687-111">For simple queries that query events from a single source, using an XPath expression is fine.</span></span> <span data-ttu-id="5e687-112">Si l’expression XPath est une expression composée qui contient plus de 20 expressions ou si vous interrogez des événements à partir de plusieurs sources, vous devez utiliser une requête XML structurée.</span><span class="sxs-lookup"><span data-stu-id="5e687-112">If the XPath expression is a compound expression that contains more than 20 expressions or you are querying for events from multiple sources, then you must use a structured XML query.</span></span> <span data-ttu-id="5e687-113">Pour plus d’informations sur les éléments d’une requête XML structurée, consultez [schéma de requête](queryschema-schema.md).</span><span class="sxs-lookup"><span data-stu-id="5e687-113">For details on the elements of a structured XML query, see [Query Schema](queryschema-schema.md).</span></span>

<span data-ttu-id="5e687-114">Une requête structurée identifie la source des événements et un ou plusieurs sélecteurs ou suppressions.</span><span class="sxs-lookup"><span data-stu-id="5e687-114">A structured query identifies the source of the events and one or more selectors or suppressors.</span></span> <span data-ttu-id="5e687-115">Un sélecteur contient des expressions XPath qui sélectionnent les événements de la source et un suppresseur contient une expression XPath qui empêche la sélection des événements.</span><span class="sxs-lookup"><span data-stu-id="5e687-115">A selector contains an XPath expressions that selects events from the source and a suppressor contains an XPath expression that prevents events from being selected.</span></span> <span data-ttu-id="5e687-116">Vous pouvez sélectionner des événements à partir de plusieurs sources.</span><span class="sxs-lookup"><span data-stu-id="5e687-116">You can select events from more than one source.</span></span> <span data-ttu-id="5e687-117">Si un sélecteur et un suppresseur identifient le même événement, l’événement n’est pas inclus dans le résultat.</span><span class="sxs-lookup"><span data-stu-id="5e687-117">If a selector and suppressor identify the same event, the event is not included in the result.</span></span>

<span data-ttu-id="5e687-118">L’exemple suivant montre une requête XML structurée qui spécifie un ensemble de sélecteurs et de suppressions.</span><span class="sxs-lookup"><span data-stu-id="5e687-118">The following shows a structured XML query that specifies a set of selectors and suppressors.</span></span>


```XML
<QueryList>
  <Query Id="0">
    <Select Path="Application">
        *[System[(Level <= 3) and 
        TimeCreated[timediff(@SystemTime) <= 86400000]]]
    </Select>
    <Suppress Path="Application">
        *[System[(Level = 2)]]
    </Suppress>
    <Select Path="System">
        *[System[(Level=1  or Level=2 or Level=3) and 
        TimeCreated[timediff(@SystemTime) <= 86400000]]]
    </Select>
  </Query>
</QueryList>
```



<span data-ttu-id="5e687-119">Le jeu de résultats de la requête ne contient pas d’instantané des événements au moment de la requête.</span><span class="sxs-lookup"><span data-stu-id="5e687-119">The result set from the query does not contain a snapshot of the events at the time of the query.</span></span> <span data-ttu-id="5e687-120">Au lieu de cela, le jeu de résultats comprend les événements au moment de la requête et contient également tous les nouveaux événements qui sont générés et qui correspondent aux critères de la requête lors de l’énumération des résultats.</span><span class="sxs-lookup"><span data-stu-id="5e687-120">Instead, the result set includes the events at the time of the query and will also contain all new events that are raised that match the query criteria while you are enumerating the results.</span></span>

> [!Note]  
> <span data-ttu-id="5e687-121">L’ordre des événements est préservé pour les événements écrits par le même thread.</span><span class="sxs-lookup"><span data-stu-id="5e687-121">The order of the events is preserved for events that are written by the same thread.</span></span> <span data-ttu-id="5e687-122">Toutefois, il est possible que les événements écrits par des threads distincts sur différents processeurs d’un ordinateur à plusieurs processeurs apparaissent dans le désordre.</span><span class="sxs-lookup"><span data-stu-id="5e687-122">However, it is possible for events written by separate threads on different processors of a multiple processor computer to appear out of order.</span></span>

 

<span data-ttu-id="5e687-123">Pour plus d’informations sur l’utilisation des événements, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="5e687-123">For details on consuming events, see the following topics:</span></span>

-   [<span data-ttu-id="5e687-124">Interrogation des événements</span><span class="sxs-lookup"><span data-stu-id="5e687-124">Querying for Events</span></span>](querying-for-events.md)
-   [<span data-ttu-id="5e687-125">Abonnement à des événements</span><span class="sxs-lookup"><span data-stu-id="5e687-125">Subscribing to Events</span></span>](subscribing-to-events.md)
-   [<span data-ttu-id="5e687-126">Événements de rendu</span><span class="sxs-lookup"><span data-stu-id="5e687-126">Rendering Events</span></span>](rendering-events.md)
-   [<span data-ttu-id="5e687-127">Mise en forme des messages d’événement</span><span class="sxs-lookup"><span data-stu-id="5e687-127">Formatting Event Messages</span></span>](formatting-event-messages.md)
-   [<span data-ttu-id="5e687-128">Événements de signets</span><span class="sxs-lookup"><span data-stu-id="5e687-128">Bookmarking Events</span></span>](bookmarking-events.md)

<span data-ttu-id="5e687-129">Les outils de l’utilisateur final standard pour l’événement de consommation sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="5e687-129">The standard end user tools for consuming event are:</span></span>

-   <span data-ttu-id="5e687-130">[Observateur d'événements](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="5e687-130">[Event Viewer](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11))</span></span>
-   <span data-ttu-id="5e687-131">L’applet de commande Windows PowerShell [-WinEvent](/previous-versions//dd367894(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="5e687-131">The Windows PowerShell [Get-WinEvent](/previous-versions//dd367894(v=technet.10)) cmdlet</span></span>
-   [<span data-ttu-id="5e687-132">**WevtUtil**</span><span class="sxs-lookup"><span data-stu-id="5e687-132">**WevtUtil**</span></span>](windows-event-log-tools.md)

## <a name="xpath-10-limitations"></a><span data-ttu-id="5e687-133">Limitations de XPath 1,0</span><span class="sxs-lookup"><span data-stu-id="5e687-133">XPath 1.0 limitations</span></span>

<span data-ttu-id="5e687-134">Le journal des événements Windows prend en charge un sous-ensemble de XPath 1,0.</span><span class="sxs-lookup"><span data-stu-id="5e687-134">Windows Event Log supports a subset of XPath 1.0.</span></span> <span data-ttu-id="5e687-135">La restriction principale est que seuls les éléments XML qui représentent des événements peuvent être sélectionnés par un sélecteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="5e687-135">The primary restriction is that only XML elements that represent events can be selected by an event selector.</span></span> <span data-ttu-id="5e687-136">Une requête XPath qui ne sélectionne pas d’événement n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5e687-136">An XPath query that does not select an event is not valid.</span></span> <span data-ttu-id="5e687-137">Tous les chemins de sélecteur valides commencent par \* ou « Event ».</span><span class="sxs-lookup"><span data-stu-id="5e687-137">All valid selector paths start with \* or "Event".</span></span> <span data-ttu-id="5e687-138">Tous les chemins d’accès d’emplacement fonctionnent sur les nœuds d’événement et sont composés d’une série d’étapes.</span><span class="sxs-lookup"><span data-stu-id="5e687-138">All location paths operate on the event nodes and are composed of a series of steps.</span></span> <span data-ttu-id="5e687-139">Chaque étape est une structure de trois parties : l’axe, le test de nœud et le prédicat.</span><span class="sxs-lookup"><span data-stu-id="5e687-139">Each step is a structure of three parts: the axis, node test, and predicate.</span></span> <span data-ttu-id="5e687-140">Pour plus d’informations sur ces éléments et sur XPath 1,0, consultez [XML Path Language (XPath)](https://www.w3.org/TR/xpath).</span><span class="sxs-lookup"><span data-stu-id="5e687-140">For more information about these parts and about XPath 1.0, see [XML Path Language (XPath)](https://www.w3.org/TR/xpath).</span></span> <span data-ttu-id="5e687-141">Le journal des événements Windows impose les restrictions suivantes sur l’expression :</span><span class="sxs-lookup"><span data-stu-id="5e687-141">Windows Event Log places the following restrictions on the expression:</span></span>

-   <span data-ttu-id="5e687-142">Axe : seuls les axes enfant (valeur par défaut) et attribut (et son raccourci « @ ») sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5e687-142">Axis: Only the Child (default) and Attribute (and its shorthand "@") axis are supported.</span></span>
-   <span data-ttu-id="5e687-143">Tests de nœud : seuls les noms de nœuds et les tests NCName sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5e687-143">Node Tests: Only node names and NCName tests are supported.</span></span> <span data-ttu-id="5e687-144">Le \* caractère «», qui sélectionne n’importe quel caractère, est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5e687-144">The "\*" character, which selects any character, is supported.</span></span>
-   <span data-ttu-id="5e687-145">Prédicats : toute expression XPath valide est acceptable si les chemins d’accès d’emplacement sont conformes aux restrictions suivantes :</span><span class="sxs-lookup"><span data-stu-id="5e687-145">Predicates: Any valid XPath expression is acceptable if the location paths conform to the following restrictions:</span></span>
    -   <span data-ttu-id="5e687-146">Les opérateurs standard **ou**, **et**, =, ! =, <=, <, >=, > et les parenthèses sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5e687-146">Standard operators **OR**, **AND**, =, !=, <=, <, >=, >, and parentheses are supported.</span></span>
    -   <span data-ttu-id="5e687-147">La génération d’une valeur de chaîne pour un nom de nœud n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5e687-147">Generating a string value for a node name is not supported.</span></span>
    -   <span data-ttu-id="5e687-148">L’évaluation dans l’ordre inverse n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5e687-148">Evaluation in reverse order is not supported.</span></span>
    -   <span data-ttu-id="5e687-149">Les jeux de nœuds ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5e687-149">Node sets are not supported.</span></span>
    -   <span data-ttu-id="5e687-150">L’étendue de l’espace de noms n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5e687-150">Namespace scoping is not supported.</span></span>
    -   <span data-ttu-id="5e687-151">Les nœuds d’espace de noms, de traitement et de commentaire ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5e687-151">Namespace, processing, and comment nodes are not supported.</span></span>
    -   <span data-ttu-id="5e687-152">La taille du contexte n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5e687-152">Context size is not supported.</span></span>
    -   <span data-ttu-id="5e687-153">Les liaisons de variables ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="5e687-153">Variable bindings are not supported.</span></span>
    -   <span data-ttu-id="5e687-154">La fonction position et sa référence de tableau abrégée sont prises en charge (sur les nœuds terminaux uniquement).</span><span class="sxs-lookup"><span data-stu-id="5e687-154">The position function, and its shorthand array reference, is supported (on leaf nodes only).</span></span>
    -   <span data-ttu-id="5e687-155">La fonction de bande est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5e687-155">The Band function is supported.</span></span> <span data-ttu-id="5e687-156">La fonction effectue une opération de bits AND pour deux arguments de nombre entier.</span><span class="sxs-lookup"><span data-stu-id="5e687-156">The function performs a bitwise AND for two integer number arguments.</span></span> <span data-ttu-id="5e687-157">Si le résultat de l’opération de bits AND est différent de zéro, la fonction prend la valeur true ; dans le cas contraire, la fonction prend la valeur false.</span><span class="sxs-lookup"><span data-stu-id="5e687-157">If the result of the bitwise AND is nonzero, the function evaluates to true; otherwise, the function evaluates to false.</span></span>
    -   <span data-ttu-id="5e687-158">La fonction timediff est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5e687-158">The timediff function is supported.</span></span> <span data-ttu-id="5e687-159">La fonction calcule la différence entre le deuxième argument et le premier argument.</span><span class="sxs-lookup"><span data-stu-id="5e687-159">The function computes the difference between the second argument and the first argument.</span></span> <span data-ttu-id="5e687-160">L’un des arguments doit être un nombre littéral.</span><span class="sxs-lookup"><span data-stu-id="5e687-160">One of the arguments must be a literal number.</span></span> <span data-ttu-id="5e687-161">Les arguments doivent utiliser la représentation FILETIME.</span><span class="sxs-lookup"><span data-stu-id="5e687-161">The arguments must use FILETIME representation.</span></span> <span data-ttu-id="5e687-162">Le résultat est le nombre de millisecondes entre les deux heures.</span><span class="sxs-lookup"><span data-stu-id="5e687-162">The result is the number of milliseconds between the two times.</span></span> <span data-ttu-id="5e687-163">Le résultat est positif si le deuxième argument représente une heure ultérieure ; dans le cas contraire, il est négatif.</span><span class="sxs-lookup"><span data-stu-id="5e687-163">The result is positive if the second argument represents a later time; otherwise, it is negative.</span></span> <span data-ttu-id="5e687-164">Lorsque le deuxième argument n’est pas fourni, l’heure système actuelle est utilisée.</span><span class="sxs-lookup"><span data-stu-id="5e687-164">When the second argument is not provided, the current system time is used.</span></span>

 

 
