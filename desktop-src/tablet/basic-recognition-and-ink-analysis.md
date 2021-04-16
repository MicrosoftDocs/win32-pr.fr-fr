---
description: Cette rubrique présente les API d’analyse d’encre.
ms.assetid: a3126930-2802-43c7-9e98-3a73498ac3f5
title: Reconnaissance de base et analyse de l’encre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9858ceedba245a733d4dc0055dd0747507654f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393240"
---
# <a name="basic-recognition-and-ink-analysis"></a><span data-ttu-id="a015b-103">Reconnaissance de base et analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="a015b-103">Basic Recognition and Ink Analysis</span></span>

<span data-ttu-id="a015b-104">Cette rubrique présente les API d’analyse d’encre.</span><span class="sxs-lookup"><span data-stu-id="a015b-104">This topic introduces the Ink Analysis APIs.</span></span>

## <a name="simple-recognition"></a><span data-ttu-id="a015b-105">Reconnaissance simple</span><span class="sxs-lookup"><span data-stu-id="a015b-105">Simple Recognition</span></span>

<span data-ttu-id="a015b-106">La fonctionnalité de base exposée par l’API d’analyse d’encre est l’accès aux résultats de la reconnaissance pour une partie donnée de l’encre.</span><span class="sxs-lookup"><span data-stu-id="a015b-106">The basic functionality exposed by the ink analysis API is access to the recognition results for a given piece of ink.</span></span> <span data-ttu-id="a015b-107">Cette opération est simple et simple, comme illustré dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="a015b-107">This is straightforward and simple to do, as shown in the following example code.</span></span>


```C++
// Instantiate a new InkAnalyzer object, passing in an Ink object and
// the synchronizing object.
InkAnalyzer ia = new InkAnalyzer(myInkOverlay.Ink, this);

// Associate the Strokes to be recognized with the InkAnalyzer.
ia.AddStrokes(myInkOverlay.Ink.Strokes);

// Synchronously recognize the Strokes.
ia.Analyze();

// Access the results and display.
string myResults = ia.GetRecognizedString();
MessageBox.Show(myResults);
```



<span data-ttu-id="a015b-108">Les résultats de l’opération de reconnaissance sont simplement une valeur de chaîne représentant la valeur reconnue de l’encre manuscrite.</span><span class="sxs-lookup"><span data-stu-id="a015b-108">The results of the recognition operation are simply a string value representing the recognized value of the handwritten ink.</span></span> <span data-ttu-id="a015b-109">L’API d’analyse d’encre expose une plus grande fonctionnalité de reconnaissance que la seule chaîne reconnue, mais c’est l’opération la plus courante.</span><span class="sxs-lookup"><span data-stu-id="a015b-109">The ink analysis API exposes much more recognition functionality than just the recognized string, but that is the most common operation.</span></span>

## <a name="incremental-recognition"></a><span data-ttu-id="a015b-110">Reconnaissance incrémentielle</span><span class="sxs-lookup"><span data-stu-id="a015b-110">Incremental Recognition</span></span>

<span data-ttu-id="a015b-111">Le processus de reconnaissance prend du temps, bloquant l’accès à l’application en bloquant le thread d’interface utilisateur de l’application.</span><span class="sxs-lookup"><span data-stu-id="a015b-111">The recognition process takes time to complete, blocking access to the application by blocking the application's UI thread.</span></span> <span data-ttu-id="a015b-112">Il peut donc être coûteux et frustrant pour l’utilisateur final d’attendre des résultats de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="a015b-112">It can therefore be costly and frustrating to the end-user to wait synchronously for results.</span></span> <span data-ttu-id="a015b-113">De nombreuses applications Tablet PC nécessitent la reconnaissance de plus de quelques lignes d’encre, et une approche incrémentielle pour la reconnaissance des traits sur un thread d’arrière-plan est la stratégie optimale.</span><span class="sxs-lookup"><span data-stu-id="a015b-113">Many Tablet PC applications require the recognition of more than a few lines of ink, and an incremental approach to recognizing strokes on a background thread is the optimal strategy.</span></span> <span data-ttu-id="a015b-114">L’avantage d’une approche incrémentielle au lieu d’une opération en bloc est qu’elle permet la reconnaissance des traits sur une période donnée, en étalant le travail sur le thread d’arrière-plan plutôt que de façon synchrone sur le thread de premier plan.</span><span class="sxs-lookup"><span data-stu-id="a015b-114">The advantage of an incremental approach instead of a bulk operation is that it allows the recognition of the strokes to happen over a period of time, spreading out the work on the background thread instead of synchronously on the foreground thread.</span></span> <span data-ttu-id="a015b-115">Pour prendre en charge l’analyse incrémentielle, l’objet [**InkAnalyzer**](inkanalyzer.md) possède une méthode [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) , qui gère la création et la gestion d’un thread d’arrière-plan pour l’application.</span><span class="sxs-lookup"><span data-stu-id="a015b-115">To support incremental analysis, the [**InkAnalyzer**](inkanalyzer.md) object has a [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) method, which handles the creation and management of a background thread for the application.</span></span> <span data-ttu-id="a015b-116">Le **InkAnalyzer** prend également automatiquement en charge la gestion de ce qui doit être reconnu et ce qui a déjà été reconnu.</span><span class="sxs-lookup"><span data-stu-id="a015b-116">The **InkAnalyzer** also automatically takes care of managing what needs to be recognized and what has already been recognized.</span></span>

<span data-ttu-id="a015b-117">Par conséquent, il existe deux mécanismes pour atteindre les résultats de la reconnaissance :</span><span class="sxs-lookup"><span data-stu-id="a015b-117">Thus, there are two mechanisms for attaining recognition results:</span></span>

-   <span data-ttu-id="a015b-118">La méthode [**analyze**](iinkanalyzer-analyze.md) (analyse synchrone), qui fonctionne le mieux pour :</span><span class="sxs-lookup"><span data-stu-id="a015b-118">The [**Analyze**](iinkanalyzer-analyze.md) method (synchronous analysis), which works best for:</span></span>

    -   <span data-ttu-id="a015b-119">Petites quantités d’encre.</span><span class="sxs-lookup"><span data-stu-id="a015b-119">Small amounts of ink.</span></span>
    -   <span data-ttu-id="a015b-120">Lorsque les résultats sont nécessaires avant de passer à l’opération suivante dans l’application, par exemple lors de l’affichage d’une interface utilisateur de correction.</span><span class="sxs-lookup"><span data-stu-id="a015b-120">When results are required before proceeding to the next operation in the application, such as when displaying a correction user interface.</span></span>

-   <span data-ttu-id="a015b-121">La méthode [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) (analyse asynchrone), qui fonctionne le mieux pour :</span><span class="sxs-lookup"><span data-stu-id="a015b-121">The [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) method (asynchronous analysis), which works best for:</span></span>

    -   <span data-ttu-id="a015b-122">Toute quantité d’encre.</span><span class="sxs-lookup"><span data-stu-id="a015b-122">Any amount of ink.</span></span>
    -   <span data-ttu-id="a015b-123">En cas d’utilisation avec un minuteur clignotant environ toutes les 600 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="a015b-123">When utilized with a timer pulsing approximately every 600 milliseconds.</span></span>

> [!Note]  
> <span data-ttu-id="a015b-124">la recommandation actuelle est de 600 millisecondes, mais ce minutage est susceptible de changer en attendant d’autres tests.</span><span class="sxs-lookup"><span data-stu-id="a015b-124">600 milliseconds is the current recommendation, but this timing is subject to change pending further testing.</span></span>

 

<span data-ttu-id="a015b-125">Pour utiliser l’opération [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) , l’objet [**InkCollector**](inkcollector-class.md) (ou des objets ou des contrôles similaires tels que [**RealTimeStylus**](realtimestylus-class.md) (RTS), [**InkOverlay**](inkoverlay-class.md)ou [InkCanvas](/dotnet/api/system.windows.controls.inkcanvas?view=netcore-3.1) dans Windows Presentation Foundation) gère la collection et le rendu des traits d’encre.</span><span class="sxs-lookup"><span data-stu-id="a015b-125">To use the [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) operation, the [**InkCollector**](inkcollector-class.md) object (or similar objects or controls such as the [**RealTimeStylus**](realtimestylus-class.md) (RTS), [**InkOverlay**](inkoverlay-class.md), or [InkCanvas](/dotnet/api/system.windows.controls.inkcanvas?view=netcore-3.1) in Windows Presentation Foundation) manages the collection and rendering of the ink strokes.</span></span> <span data-ttu-id="a015b-126">Si le formulaire **InkCollector** est associé aux API d’analyse d’encre, les applications peuvent conserver les résultats de la reconnaissance à jour en informant le [**InkAnalyzer**](inkanalyzer.md) sur chaque nouveau trait ajouté à l’application.</span><span class="sxs-lookup"><span data-stu-id="a015b-126">If the **InkCollector** is paired with the ink analysis APIs, applications can keep the recognition results updated by informing the [**InkAnalyzer**](inkanalyzer.md) about each new stroke added to the application.</span></span> <span data-ttu-id="a015b-127">Cela permet au **InkAnalyzer** de reconnaître les traits de manière incrémentielle et sur un thread d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="a015b-127">This allows for the **InkAnalyzer** to recognize the strokes incrementally and on a background thread.</span></span>

<span data-ttu-id="a015b-128">Pour effectuer une analyse incrémentielle en arrière-plan, les applications doivent implémenter trois étapes (affichées pour le code managé) :</span><span class="sxs-lookup"><span data-stu-id="a015b-128">To accomplish incremental background analysis, applications need to implement three steps (shown for managed code):</span></span>

1. <span data-ttu-id="a015b-129">Ajoutez le trait à [**InkAnalyzer**](inkanalyzer.md) chaque fois que l’événement [**Stroke**](inkoverlay-stroke.md) de l’objet [**InkOverlay**](inkoverlay-class.md) est déclenché :</span><span class="sxs-lookup"><span data-stu-id="a015b-129">Add the stroke to the [**InkAnalyzer**](inkanalyzer.md) whenever the [**InkOverlay**](inkoverlay-class.md) object's [**Stroke**](inkoverlay-stroke.md) event is raised:</span></span>


```C++
/// Event Handler from InkOverlay's Stroke event
/// This event is fired when a new stroke is drawn. 
/// In this case, it is necessary to update the ink analyzer's 
/// Strokes collection. The event is fired even when the eraser 
/// stroke is created.
/// The event handler must filter out the eraser strokes.
/// <param name="sender">The control that raised the event.</param>
/// <param name="e">The event arguments.</param>
private void myInkOverlay_Stroke(object sender, InkCollectorStrokeEventArgs e)
{
        // Add the new stroke to the InkAnalyzer's stroke collection
        theInkAnalyzer.AddStroke(e.Stroke);
        this.Refresh();
}
```



2. <span data-ttu-id="a015b-130">Appelle les opérations [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) à un intervalle défini.</span><span class="sxs-lookup"><span data-stu-id="a015b-130">Invoke the [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) operations at a set interval.</span></span>


```C++
//Setup a timer tick handler
private System.Windows.Forms.Timer analysisTimer;
analysisTimer = new Timer();
analysisTimer.Tick += new System.EventHandler(this.analysisTimer_Tick);

// The timer is enabled and set to tick every 600 milliseconds.
analysisTimer.Enabled = true;
analysisTimer.Interval = 600;
// ...
//The background analysis operation is invoked with every tick
private void analysisTimer_Tick(object sender, System.EventArgs e)
{
    theInkAnalyzer.BackgroundAnalyze();
}
```



> [!Note]  
> <span data-ttu-id="a015b-131">Remarque les applications ne doivent pas simplement appeler l’opération d’analyse en arrière-plan après chaque nouveau trait.</span><span class="sxs-lookup"><span data-stu-id="a015b-131">Note Applications should not simply invoke the background analysis operation after every new stroke.</span></span> <span data-ttu-id="a015b-132">Cela échoue (en retournant la valeur **false**) si une opération en arrière-plan est déjà en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a015b-132">This will fail (returning a value of **false**) if a background operation is already running.</span></span> <span data-ttu-id="a015b-133">La raison de ce comportement est de limiter le nombre de threads d’arrière-plan et d’opérations de réconciliation requis.</span><span class="sxs-lookup"><span data-stu-id="a015b-133">The reason for this behavior is to limit the number of background threads and reconciliation operations required.</span></span>

 

3. <span data-ttu-id="a015b-134">Écoutez l’événement [ResultsUpdated](/previous-versions/ms567607(v=vs.100)) (code managé) ou les événements de [**résultats**](-ianalysisevents-results.md) (code C++) pour déterminer à quel moment le processus en arrière-plan est terminé :</span><span class="sxs-lookup"><span data-stu-id="a015b-134">Listen for the [ResultsUpdated](/previous-versions/ms567607(v=vs.100)) event (managed code) or [**Results**](-ianalysisevents-results.md) event (C++ code) to determine when the background process has finished:</span></span>


```C++
// ...
theInkAnalyzer.Results += new ResultsEventHandler(ia_Results);
// ...

private void ia_Results(object sender, ResultsEventArgs e)
{
    String myResults = e.InkAnalyzer.GetRecognizedString();
    MessageBox.Show(myResults);
}
```



<span data-ttu-id="a015b-135">Maintenant que le traitement de l’encre est effectué sur un thread d’arrière-plan, l’application a la possibilité d’accepter les modifications apportées à l’encre pendant que l’opération en arrière-plan fonctionne.</span><span class="sxs-lookup"><span data-stu-id="a015b-135">Now that the processing of the ink is being done on a background thread, the application has the ability to accept changes to the ink while the background operation is working.</span></span> <span data-ttu-id="a015b-136">Si nous utilisons un thread synchrone, cela n’est pas possible.</span><span class="sxs-lookup"><span data-stu-id="a015b-136">If we use a synchronous thread this is not possible.</span></span> <span data-ttu-id="a015b-137">Le travail s’exécute sur le thread d’interface utilisateur, ce qui bloque la possibilité d’apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="a015b-137">The work executes on the UI thread, blocking the ability to make changes.</span></span> <span data-ttu-id="a015b-138">Les modifications incluent l’ajout d’une entrée manuscrite supplémentaire au document, la suppression de l’encre ou la transformation de l’emplacement ou de l’apparence de l’encre existante.</span><span class="sxs-lookup"><span data-stu-id="a015b-138">Changes include adding more ink to the document, deleting ink, or transforming the location or appearance of the existing ink.</span></span> <span data-ttu-id="a015b-139">Les modifications qui se produisent pendant l’opération d’arrière-plan peuvent en fait invalider les résultats.</span><span class="sxs-lookup"><span data-stu-id="a015b-139">Changes that occur during the background operation may in fact invalidate the results.</span></span> <span data-ttu-id="a015b-140">Par exemple, la suppression d’un trait d’un mot modifie la valeur de reconnaissance de ce mot.</span><span class="sxs-lookup"><span data-stu-id="a015b-140">For example, deleting a stroke from a word changes the recognition value of that word.</span></span> <span data-ttu-id="a015b-141">L’API [**InkAnalyzer**](inkanalyzer.md) a un processus de réconciliation intégré qui détermine automatiquement les parties de l’opération d’arrière-plan qui deviennent non valides en raison de la modification de l’encre lors de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="a015b-141">The [**InkAnalyzer**](inkanalyzer.md) API has a built-in reconciliation process that automatically determines what parts of the background operation become invalid as the result of the ink changing while analyzing.</span></span>

<span data-ttu-id="a015b-142">Le processus de réconciliation automatique est effectué en raison de trois facteurs :</span><span class="sxs-lookup"><span data-stu-id="a015b-142">The automatic reconciliation process is accomplished because of three factors:</span></span>

1.  <span data-ttu-id="a015b-143">Propriété [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) .</span><span class="sxs-lookup"><span data-stu-id="a015b-143">The [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) property.</span></span>

    -   <span data-ttu-id="a015b-144">Chaque fois que l’application ajoute (méthode [**AddStroke**](iinkanalyzer-addstroke.md) ) ou supprime (méthode [**RemoveStroke**](iinkanalyzer-removestroke.md) ) un trait vers ou à partir du [**InkAnalyzer**](inkanalyzer.md), l’emplacement physique du trait est capturé et la prochaine fois qu’une opération d’analyse est appelée, le **InkAnalyzer** garantit que ce trait, ou la zone occupée par ce trait, est analysé.</span><span class="sxs-lookup"><span data-stu-id="a015b-144">Each time the application adds ([**AddStroke**](iinkanalyzer-addstroke.md) method) or removes ([**RemoveStroke**](iinkanalyzer-removestroke.md) method) a stroke to or from the [**InkAnalyzer**](inkanalyzer.md), the physical location of the stroke is captured and the next time an analysis operation is invoked, the **InkAnalyzer** ensures that stroke, or the area occupied by that stroke, is analyzed.</span></span>
    -   <span data-ttu-id="a015b-145">Chaque fois que l’application modifie l’encre existante, modifie l’emplacement ou modifie d’autres attributs de dessin de l’encre, l’emplacement de la modification (les limites de l’encre) peut être ajouté à la propriété [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) de [**InkAnalyzer**](inkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="a015b-145">Whenever the application modifies existing ink, changes the location, or changes other drawing attributes of the ink, the location of the change (the bounds of the ink) can be added to the [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) property of the [**InkAnalyzer**](inkanalyzer.md).</span></span> <span data-ttu-id="a015b-146">Cela garantit que la prochaine fois que l’application démarre l’opération d’analyse, les résultats corrects sont vérifiés.</span><span class="sxs-lookup"><span data-stu-id="a015b-146">This ensures that the next time the application starts the analysis operation those areas are checked for correct results.</span></span>
    -   <span data-ttu-id="a015b-147">Par conséquent, la propriété [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) effectue le suivi, entre les exécutions d’analyse, les zones du document et, à tour de rôle, les traits qui doivent être vérifiés pour obtenir des résultats corrects d’analyse de l’encre et de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="a015b-147">Thus, the [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) property keeps track, between analysis runs, of what areas of the document and-in turn-which strokes need to be checked for correct ink analysis and recognition results.</span></span>

2.  <span data-ttu-id="a015b-148">Analyse limitée.</span><span class="sxs-lookup"><span data-stu-id="a015b-148">Limited analysis.</span></span>

    -   <span data-ttu-id="a015b-149">Chaque fois que l’application appelle l’opération d’analyse, la propriété [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) identifie les traits qui doivent être analysés.</span><span class="sxs-lookup"><span data-stu-id="a015b-149">Each time the application invokes the analysis operation, the [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) property identifies which strokes need to be analyzed.</span></span> <span data-ttu-id="a015b-150">Cela permet à l’opération d’analyse de limiter l’opération aux seules régions modifiées et d’ignorer toutes les autres régions, ce qui optimise la durée passée à analyser l’encre.</span><span class="sxs-lookup"><span data-stu-id="a015b-150">This allows the analysis operation to limit the operation to only the dirty regions and ignore all other regions, optimizing the amount of time spent re-analyzing ink.</span></span>
    -   <span data-ttu-id="a015b-151">Le [**InkAnalyzer**](inkanalyzer.md) n’ignore pas complètement toutes les autres régions de la page, mais peut à la place examiner les zones voisines pour déterminer si les modifications apportées à la région modifiée affectent ces régions voisines.</span><span class="sxs-lookup"><span data-stu-id="a015b-151">The [**InkAnalyzer**](inkanalyzer.md) does not completely ignore all other regions on the page, but instead may examine neighboring areas to determine if the changes made in the dirty region affect those neighboring regions.</span></span> <span data-ttu-id="a015b-152">Par exemple, l’analyseur classe « is », dans l’exemple d’encre suivant, en tant que type **InkWord** unique de la classe [**ContextNode**](icontextnode.md) :</span><span class="sxs-lookup"><span data-stu-id="a015b-152">For example, the analyzer classifies "Is", in the following ink sample, as a single **InkWord** type of the [**ContextNode**](icontextnode.md) class:</span></span>

![manuscrit « is »](images/b0e45d31-a0e5-4157-a345-a3a32de2566e.jpg)

<span data-ttu-id="a015b-154">La suppression de la « s » donne lieu à une région modifiée (marquée d’un cadre rouge).</span><span class="sxs-lookup"><span data-stu-id="a015b-154">Deleting the "s" results in a dirty region (marked with a red box).</span></span>

![manuscrit « i »](images/272a25a7-c730-40e6-b7d8-214ccbb85569.jpg)

<span data-ttu-id="a015b-156">Après l’analyse, l’analyseur change la classification de « I » en type **InkDrawing** , même si elle est en dehors de la région modifiée, car sans le trait « s » de prise en charge, l’analyseur d’encre a une chance de 50/50 de l’encre classée comme un dessin ou un mot.</span><span class="sxs-lookup"><span data-stu-id="a015b-156">After analysis, the analyzer changes the classification for the "I" to an **InkDrawing** type, even though it is outside of the dirty region, because without the supporting "s" stroke the ink analyzer has a 50/50 chance of the ink being classified as a drawing or a word.</span></span>

-   <span data-ttu-id="a015b-157">État mis en cache en interne.</span><span class="sxs-lookup"><span data-stu-id="a015b-157">Internally cached state.</span></span>

    -   <span data-ttu-id="a015b-158">Lorsqu’une application appelle une opération d’analyse en arrière-plan, [**InkAnalyzer**](inkanalyzer.md) met en cache une capture instantanée des données élaguées.</span><span class="sxs-lookup"><span data-stu-id="a015b-158">When an application invokes a background analysis operation the [**InkAnalyzer**](inkanalyzer.md) caches a snapshot of the pruned data.</span></span> <span data-ttu-id="a015b-159">En effectuant un instantané, le **InkAnalyzer** peut soit travailler sur l’analyse des données indépendamment des données utilisées par l’application, soit utiliser l’instantané comme point de comparaison pour déterminer les modifications apportées par l’application lors de l’analyse en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="a015b-159">By taking a snapshot the **InkAnalyzer** can either work on analyzing the data independently of the data being used by the application, or use the snapshot as the comparison point to determine what changes were made by the application while background analyzing.</span></span>
    -   <span data-ttu-id="a015b-160">La mise en cache de l’État et la comparaison des modifications sont préférables à la conservation d’une liste de toutes les modifications qui se sont produites pour une raison principale : proxy de données.</span><span class="sxs-lookup"><span data-stu-id="a015b-160">Caching the state and comparing changes is better than keeping a list of all changes that occurred for one primary reason: data proxy.</span></span> <span data-ttu-id="a015b-161">Il s’agit d’un scénario avancé décrit plus loin dans ce document, mais il implique que l’application met à jour les [**InkAnalyzer**](inkanalyzer.md) avec uniquement les données d’encre et de non-encre actuelles avant l’opération d’analyse appelée et avant le traitement des résultats d’une opération d’analyse.</span><span class="sxs-lookup"><span data-stu-id="a015b-161">This is an advanced scenario described later in this document, but it involves the application updating the [**InkAnalyzer**](inkanalyzer.md) with only the current ink and non-ink data prior to the invoked analysis operation and prior to processing the results of an analysis operation.</span></span>

## <a name="simple-ink-analysis"></a><span data-ttu-id="a015b-162">Analyse d’encre simple</span><span class="sxs-lookup"><span data-stu-id="a015b-162">Simple Ink Analysis</span></span>

<span data-ttu-id="a015b-163">Les deux scénarios précédents (reconnaissance simple et reconnaissance incrémentielle) décrivent comment accéder aux valeurs de reconnaissance, mais ne mentionnent pas comment accéder aux résultats de l’analyse ou de la classification de l’encre.</span><span class="sxs-lookup"><span data-stu-id="a015b-163">The previous two scenarios (simple recognition and incremental recognition) outline how to access recognition values but do not mention how to access the ink analysis or classification results.</span></span> <span data-ttu-id="a015b-164">La configuration par défaut de [**InkAnalyzer**](inkanalyzer.md)exécute à la fois les algorithmes d’analyse d’encre et les algorithmes de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="a015b-164">The default configuration of the [**InkAnalyzer**](inkanalyzer.md), runs both ink analysis algorithms and recognition algorithms.</span></span> <span data-ttu-id="a015b-165">Cette configuration produit les résultats les plus précis, car les deux technologies fonctionnent ensemble pour améliorer la précision.</span><span class="sxs-lookup"><span data-stu-id="a015b-165">This configuration yields the most accurate results, because the two technologies work together to increase accuracy.</span></span> <span data-ttu-id="a015b-166">Autrement dit, les moteurs d’analyse d’encre permettent de séparer le dessin de l’écriture et de normaliser l’écriture en angle dans un plan horizontal, qui est le plan d’entrée optimal pour les moteurs de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="a015b-166">That is, the ink analysis engines help to separate the drawing from the writing and normalize angled writing into a horizontal plane, which is the optimum input plane for the recognition engines.</span></span>

<span data-ttu-id="a015b-167">Pour accéder aux résultats de l’analyse de l’encre, votre application utilise les méthodes [**analyze**](iinkanalyzer-analyze.md) ou [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) exactement comme décrit dans les deux scénarios de reconnaissance précédents.</span><span class="sxs-lookup"><span data-stu-id="a015b-167">To access the ink analysis results, your application uses the [**Analyze**](iinkanalyzer-analyze.md) or [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) methods exactly as described in the previous two recognition scenarios.</span></span> <span data-ttu-id="a015b-168">Rien n’est modifié, car les algorithmes d’analyse et de reconnaissance de l’encre sont déjà en cours d’exécution lorsque ces méthodes sont appelées.</span><span class="sxs-lookup"><span data-stu-id="a015b-168">Nothing changes because the ink analysis and recognition algorithms are already being run when those methods are called.</span></span> <span data-ttu-id="a015b-169">Toutefois, l’accès aux résultats est plus complexe que la lecture de la valeur d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="a015b-169">However, accessing the results is more complicated than reading the value of a string.</span></span> <span data-ttu-id="a015b-170">À titre d’exemple, l’exemple de code suivant montre le regroupement et les emplacements de tous les segments **InkWord** et **InkDrawing** en affichant un rectangle autour du groupe de traits qui composent la classification.</span><span class="sxs-lookup"><span data-stu-id="a015b-170">As an example, the following code sample shows the grouping and locations of all the **InkWord** segments and **InkDrawing** segments by rendering a rectangle around the group of strokes that make up the classification.</span></span>

<span data-ttu-id="a015b-171">Cet exemple utilise simplement l’événement **Paint** du formulaire pour restituer les rectangles de couleur autour des mots ou des dessins.</span><span class="sxs-lookup"><span data-stu-id="a015b-171">This example simply uses the form's **Paint** event to render colored rectangles around the words or drawings.</span></span> <span data-ttu-id="a015b-172">La méthode [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) retourne une collection d’objets qui existe uniquement si l’opération d’analyse a été exécutée et les résultats contiennent des classifications avec le type [**ContextNode**](icontextnode.md) spécifié.</span><span class="sxs-lookup"><span data-stu-id="a015b-172">The [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method returns a collection of objects that exists only if the analysis operation has been executed and the results contain classifications with the specified [**ContextNode**](icontextnode.md) type.</span></span> <span data-ttu-id="a015b-173">S’il n’existe aucun **ContextNode** du type souhaité dans le document, les étapes de dessin des rectangles sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="a015b-173">If no **ContextNode** of the desired type exists in the document, the steps to draw the rectangles are skipped.</span></span>

<span data-ttu-id="a015b-174">Chaque objet retourné par la méthode [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) aura des propriétés qui sont liées à ce type de classification.</span><span class="sxs-lookup"><span data-stu-id="a015b-174">Each object returned from the [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method will have properties that relate to that kind of classification.</span></span> <span data-ttu-id="a015b-175">Par exemple, le **InkWordNode** fait référence à tous les traits qui composent un mot unique dans le document et référencent la chaîne reconnue pour ce mot.</span><span class="sxs-lookup"><span data-stu-id="a015b-175">For example the **InkWordNode** references all the strokes that make up a single word in the document and reference the recognized string for that word.</span></span> <span data-ttu-id="a015b-176">**InkDrawingNode** fait référence à tous les traits qui composent le dessin unique dans le document et référencent le nom de la forme pour ce dessin.</span><span class="sxs-lookup"><span data-stu-id="a015b-176">The **InkDrawingNode** references all the strokes that make up the single drawing in the document and reference the shape name for that drawing.</span></span>

<span data-ttu-id="a015b-177">La méthode [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) est très similaire à la méthode [**DivisionResult :: ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) qui retournait des collections de [**DivisionUnits**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits) de types d’écriture ou de dessin.</span><span class="sxs-lookup"><span data-stu-id="a015b-177">The [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method is very similar to the [**DivisionResult::ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) method that returned collections of [**DivisionUnits**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits) of either writing or drawing types.</span></span>


```C++
private void Form1_Paint(object sender, PaintEventArgs e)
{
    //Setup the pen to draw
    using(Pen penBox = new Pen(Color.Red, 1))
    {
        // Find all the InkWord ContextNodes in the results
        ContextNodeCollection InkWordNodes = theInkAnalyzer.FindNodesOfType(ContextNodeType.InkWord);
        // For each InkWord node found, cast the ContextNode to a type specific
        // "InkWordNode" to easily access the rotated bounding box property.
        foreach (ContextNode InkWord in InkWordNodes)
        {
            //Draw the rotated bounding box.
            e.Graphics.DrawPolygon(penBox,
                    ((InkWordNode)InkWord).GetRotatedBoundingBox());
        }

        // Find all the InkDrawing ContextNodes in the results
        ContextNodeBaseCollection InkDrawingNodes = theInkAnalyzer.FindNodesOfType(ContextNodeType.InkDrawing);

        penBox.Color = Color.Green;

        // For each InkDrawing node found, access the node's location property to
        // draw a rectangle around the drawing.
        foreach (ContextNode InkDrawing in InkDrawingNodes)
        {
            e.Graphics.DrawRectangle(penBox, InkDrawing.Location.GetBounds());
        }
    }
}
```



<span data-ttu-id="a015b-178">Pour mettre l’exemple de code précédent en perspective, considérez l’exemple d’encre suivant :</span><span class="sxs-lookup"><span data-stu-id="a015b-178">To put the previous code example into perspective, consider the following ink sample:</span></span>

![exemple d’encre « il s’agit d’une entrée manuscrite ».](images/f11cc578-d2eb-4246-af77-6bc768b0b91c.jpg)

<span data-ttu-id="a015b-181">Si vous appelez la méthode [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) et transmettez le champ static pour **InkWord**, l’analyseur retourne une collection de quatre objets **InkWordNode** :</span><span class="sxs-lookup"><span data-stu-id="a015b-181">If you call the [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method and pass in the static field for **InkWord**, the analyzer returns a collection of four **InkWordNode** objects:</span></span>

![résultat de l’analyseur, « il s’agit d’une entrée manuscrite »](images/16ae768a-d97c-494e-9e3d-16bce1bcb432.jpg)

<span data-ttu-id="a015b-183">Si vous appelez la méthode [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) et transmettez le champ static pour **InkDrawing**, l’analyseur retourne une collection d’un objet **InkDrawingNode** :</span><span class="sxs-lookup"><span data-stu-id="a015b-183">If you call the [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method and pass in the static field for **InkDrawing**, the analyzer returns a collection of one **InkDrawingNode** object:</span></span>

![image représentant « Oval », le résultat de l’analyseur InkDrawing](images/624b6a53-b6b9-4ccf-9bb8-c4c5629b88cf.jpg)

<span data-ttu-id="a015b-185">Une fois l’événement **Paint** déclenché, l’exemple de code affiche des rectangles autour de chacun des objets :</span><span class="sxs-lookup"><span data-stu-id="a015b-185">After the **Paint** event has fired, the sample code renders rectangles around each of the objects:</span></span>

![dessin original avec des rectangles rendus autour de l’objet et des mots](images/7fd9bcc3-8d7c-4cab-aa36-ba5ed78a25c0.jpg)

<span data-ttu-id="a015b-187">Cet exemple ne touche que la méthode [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) , mais comme les moteurs d’analyse d’encre peuvent détecter un ensemble plus riche de types d’encres, la méthode correspond également à tous les types de nœuds détectables par les moteurs d’analyse d’encre (tels que les lignes, les paragraphes et d’autres structures).</span><span class="sxs-lookup"><span data-stu-id="a015b-187">This example only touches on the [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method, but because the ink analysis engines can detect a richer set of ink types, the method also correspond to all types of nodes detectable by the ink analysis engines (such as lines, paragraphs, and other structures).</span></span>

## <a name="using-ink-analysis-with-point-erase"></a><span data-ttu-id="a015b-188">Utilisation de l’analyse de l’encre avec l’effacement de point</span><span class="sxs-lookup"><span data-stu-id="a015b-188">Using Ink Analysis with Point Erase</span></span>

<span data-ttu-id="a015b-189">Votre application doit effectuer des ajustements dans la façon dont elle met à jour les traits lors de l’effacement de point pour garantir de bonnes performances.</span><span class="sxs-lookup"><span data-stu-id="a015b-189">Your application needs to make adjustments in the way it updates strokes when performing point erase to ensure good performance.</span></span> <span data-ttu-id="a015b-190">Tout d’abord, au niveau de la couche d’application, remplacez le point du stylet du trait existant par le point du stylet du nouveau trait, puis appelez [**ClearStrokeData**](iinkanalyzer-clearstrokedata.md) sur ce trait et mettez à jour la région modifiée avec les limites du trait.</span><span class="sxs-lookup"><span data-stu-id="a015b-190">Firstly, at the application layer, replace the stylus point of the existing Stroke with the stylus point of the new stroke, then call [**ClearStrokeData**](iinkanalyzer-clearstrokedata.md) on that stroke and update the dirty region with the stroke's bounds.</span></span> <span data-ttu-id="a015b-191">Ainsi, le [**InkAnalyzer**](inkanalyzer.md) récupère les données de trait mises à jour lors du démarrage de l’analyse d’arrière-plan suivante.</span><span class="sxs-lookup"><span data-stu-id="a015b-191">This will cause the [**InkAnalyzer**](inkanalyzer.md) to fetch the updated stroke data when the next round of background analysis starts.</span></span> <span data-ttu-id="a015b-192">Cette technique est illustrée dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="a015b-192">This technique is demonstrated in the following example.</span></span>


```C++
using System;
using System.Diagnostics;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;

class PointEraseAnalysisSample : Application
{
  InkAnalyzer _analyzer;
  InkCanvas _canvas;
  bool _isPointErasing = false;
  bool _strokesManipulated = false;

  protected override void OnStartup(StartupEventArgs e)
  {
      base.OnStartup(e);
      Window win = new Window();

      _canvas = new InkCanvas();
      _canvas.Background = new LinearGradientBrush(Colors.Yellow, Colors.LightYellow, 60d);
      _canvas.EditingModeInverted = InkCanvasEditingMode.EraseByPoint;
      _canvas.Strokes.StrokesChanged += new StrokeCollectionChangedEventHandler(Strokes_StrokesChanged);
      _canvas.AddHandler(InkCanvas.MouseUpEvent, new MouseButtonEventHandler(_canvas_MouseUp), true);

      _analyzer = new InkAnalyzer(this.Dispatcher);
      _analyzer.ResultsUpdated += new ResultsUpdatedEventHandler(_analyzer_ResultsUpdated);

      win.Content = _canvas;
      win.Show();
  }

  void _analyzer_ResultsUpdated(object sender, ResultsUpdatedEventArgs e)
  {
      if (!_analyzer.DirtyRegion.IsEmpty)
      {
          _analyzer.BackgroundAnalyze();
          return;
      }

      Console.WriteLine(_analyzer.GetRecognizedString());
  }

  void _canvas_MouseUp(object sender, MouseButtonEventArgs e)
  {
      if (_isPointErasing)
      {
          _isPointErasing = false;
          _analyzer.BackgroundAnalyze();
      }
  }

  void Strokes_StrokesChanged(object sender, StrokeCollectionChangedEventArgs e)
  {
      if (_strokesManipulated)
      {
          // ignore StrokesChanged if we changed them ourselves
          _strokesManipulated = false;
          return;
      }

      if (_canvas.ActiveEditingMode == InkCanvasEditingMode.EraseByPoint &&
          e.Added.Count == 1 && e.Removed.Count == 1)
      {
          // set flag so we call BackgroundAnalyze in MouseUp
          _isPointErasing = true;

          // set flag so we ignore the next StrokesChanged
          _strokesManipulated = true;

          // replace the stylus points on the removed stroke with the added stroke
          e.Removed[0].StylusPoints = e.Added[0].StylusPoints;
          
          // force IA to update the stroke data for the removed stroke
          _analyzer.ClearStrokeData(e.Removed[0]);

          // replace the added stroke with the updated removed stroke back into InkCanvas
          _canvas.Strokes.Replace(e.Added[0], new StrokeCollection(new Stroke[] {e.Removed[0]})); 
          
          return;
      }

      if (e.Added.Count > 0)
      {
          _analyzer.AddStrokes(e.Added);
      }

      if (e.Removed.Count > 0)
      {
          _analyzer.RemoveStrokes(e.Removed);
      }

      _analyzer.BackgroundAnalyze();
  }

  [STAThread]
  static void Main(string[] args)
  {
      new PointEraseAnalysisSample().Run();
  }
}
```



## <a name="related-topics"></a><span data-ttu-id="a015b-193">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a015b-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a015b-194">Présentation de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="a015b-194">Ink Analysis Overview</span></span>](ink-analysis-overview.md)
</dt> <dt>

[<span data-ttu-id="a015b-195">Utilisation de l’API analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="a015b-195">Ink Analysis API Usage</span></span>](ink-analysis-api-usage.md)
</dt> </dl>

 

 
