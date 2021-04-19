---
description: Décrit l’introduction de la hiérarchisation des index et des événements d’ensemble de lignes pour Windows 7.
ms.assetid: 6cdfb7d3-f849-432c-960f-912e5024c583
title: Indexation des événements d’ensemble de priorités et d’ensembles de lignes dans Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6610500a3c2fcd359f346e5239507fb15ad896d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106535731"
---
# <a name="indexing-prioritization-and-rowset-events-in-windows-7"></a><span data-ttu-id="738b9-103">Indexation des événements d’ensemble de priorités et d’ensembles de lignes dans Windows 7</span><span class="sxs-lookup"><span data-stu-id="738b9-103">Indexing Prioritization and Rowset Events in Windows 7</span></span>

<span data-ttu-id="738b9-104">Cette rubrique décrit l’introduction de la hiérarchisation des index et des événements d’ensemble de lignes pour Windows 7.</span><span class="sxs-lookup"><span data-stu-id="738b9-104">This topic outlines the introduction of indexing prioritization and rowset events for Windows 7.</span></span>

<span data-ttu-id="738b9-105">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="738b9-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="738b9-106">Indexation de la hiérarchisation et des événements d’ensemble de lignes</span><span class="sxs-lookup"><span data-stu-id="738b9-106">Indexing Prioritization and Rowset Events</span></span>](#indexing-prioritization-and-rowset-events)
    -   [<span data-ttu-id="738b9-107">Exemples IRowsetPriorization</span><span class="sxs-lookup"><span data-stu-id="738b9-107">IRowsetPriorization Examples</span></span>](#irowsetpriorization-examples)
    -   [<span data-ttu-id="738b9-108">Événements IRowsetPrioritization</span><span class="sxs-lookup"><span data-stu-id="738b9-108">IRowsetPrioritization Events</span></span>](#indexing-prioritization-and-rowset-events-in-windows-7)
-   [<span data-ttu-id="738b9-109">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="738b9-109">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="738b9-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="738b9-110">Related topics</span></span>](#related-topics)

## <a name="indexing-prioritization-and-rowset-events"></a><span data-ttu-id="738b9-111">Indexation de la hiérarchisation et des événements d’ensemble de lignes</span><span class="sxs-lookup"><span data-stu-id="738b9-111">Indexing Prioritization and Rowset Events</span></span>

<span data-ttu-id="738b9-112">Dans Windows 7 ? et versions ultérieures, il existe une pile de priorités dans laquelle le contexte d’une requête particulière, le client peut demander que les étendues utilisées dans cette requête soient hiérarchisées au-dessus de celles des éléments normaux.</span><span class="sxs-lookup"><span data-stu-id="738b9-112">In Windows 7?and later, there is a priority stack within which the context of any particular query, the client can request that the scopes used in that query be prioritized above that of normal items.</span></span>

<span data-ttu-id="738b9-113">Cette pile de définition de priorités présente les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="738b9-113">This prioritization stack has the following characteristics:</span></span>

-   <span data-ttu-id="738b9-114">Les éléments de la pile peuvent avoir une priorité de premier plan, haute ou basse :</span><span class="sxs-lookup"><span data-stu-id="738b9-114">Items in the stack can have foreground, high, or low priority:</span></span>
    -   <span data-ttu-id="738b9-115">**Premier plan**: la logique d’interruption est ignorée et l’indexation continue aussi rapidement que la machine l’autorise.</span><span class="sxs-lookup"><span data-stu-id="738b9-115">**Foreground**: Backoff logic is skipped and indexing proceeds as fast as the machine allows.</span></span>
    -   <span data-ttu-id="738b9-116">**Élevé**: la définition de la priorité a été demandée avec interruption.</span><span class="sxs-lookup"><span data-stu-id="738b9-116">**High**: Prioritization has been requested with backoff.</span></span>
    -   <span data-ttu-id="738b9-117">**Faible**: la définition de la priorité a été demandée, et non pas aux dépens des autres étendues de la pile, mais au-dessus de l’indexation non hiérarchisée.</span><span class="sxs-lookup"><span data-stu-id="738b9-117">**Low**: Prioritization has been requested, not at the expense of other scopes on the stack, but above non-prioritized indexing.</span></span>
-   <span data-ttu-id="738b9-118">Toute demande de priorité élevée ou de premier plan porte automatiquement la requête en haut de la pile.</span><span class="sxs-lookup"><span data-stu-id="738b9-118">Any request for high or foreground priority bumps the requesting query to the top of the stack automatically.</span></span>
-   <span data-ttu-id="738b9-119">Seul l’élément situé en haut de la pile peut avoir une priorité de premier plan.</span><span class="sxs-lookup"><span data-stu-id="738b9-119">Only the item on top of the stack can have foreground priority.</span></span>
-   <span data-ttu-id="738b9-120">Une requête avec une priorité de premier plan en priorité reçoit un événement l’informant qu’elle a perdu la priorité de premier plan et qu’elle est devenue une priorité élevée avec l’interruption.</span><span class="sxs-lookup"><span data-stu-id="738b9-120">A query with foreground priority that is bumped down in priority receives an event notifying it that it has lost foreground priority and has become a high priority with backoff.</span></span>

<span data-ttu-id="738b9-121">La pile de priorité définit une priorité globale des éléments traités dans l’indexeur comme suit :</span><span class="sxs-lookup"><span data-stu-id="738b9-121">The priority stack sets an overall priority of items that are processed in the indexer as follows:</span></span>

-   <span data-ttu-id="738b9-122">Les notifications de priorité élevée n’ont pas d’interruption et sont généralement envoyées uniquement pour un petit nombre d’éléments.</span><span class="sxs-lookup"><span data-stu-id="738b9-122">High Priority notifications have no backoff, and are typically sent only for a small number of items.</span></span> <span data-ttu-id="738b9-123">Par exemple, l’Explorateur Windows utilise cette priorité pour les opérations de moteur de copie de petite taille.</span><span class="sxs-lookup"><span data-stu-id="738b9-123">For example, Windows Explorer uses this priority for small copy engine operations.</span></span>
-   <span data-ttu-id="738b9-124">La pile de priorité est supérieure à la pile, a un intervalle et est la dernière requête prioritaire demandée.</span><span class="sxs-lookup"><span data-stu-id="738b9-124">Priority Stack is top of the stack, has backoff, and is the last requested priority query.</span></span>
-   <span data-ttu-id="738b9-125">Deuxième requête dans la pile.</span><span class="sxs-lookup"><span data-stu-id="738b9-125">Second query in the stack.</span></span>
-   <span data-ttu-id="738b9-126">Troisième requête dans la pile.</span><span class="sxs-lookup"><span data-stu-id="738b9-126">Third query in the stack.</span></span>
-   <span data-ttu-id="738b9-127">Quatrième requête dans la pile, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="738b9-127">Fourth query in the stack, and so forth.</span></span>
-   <span data-ttu-id="738b9-128">Éléments de priorité normaux.</span><span class="sxs-lookup"><span data-stu-id="738b9-128">Normal Priority items.</span></span>
-   <span data-ttu-id="738b9-129">Éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="738b9-129">Deleted items.</span></span>
    > [!Note]  
    > <span data-ttu-id="738b9-130">Les éléments de chaque groupe sont classés par ordre de priorité en interne par le biais de la sémantique par élément antérieure.</span><span class="sxs-lookup"><span data-stu-id="738b9-130">Items within each group are prioritized internally through the older per-item semantics.</span></span>

     

### <a name="irowsetpriorization-examples"></a><span data-ttu-id="738b9-131">Exemples IRowsetPriorization</span><span class="sxs-lookup"><span data-stu-id="738b9-131">IRowsetPriorization Examples</span></span>

<span data-ttu-id="738b9-132">L’API principale pour le travail de hiérarchisation est disponible via l’interface suivante, qui peut être appelée en interrogeant l’ensemble de lignes retourné :</span><span class="sxs-lookup"><span data-stu-id="738b9-132">The primary API for prioritization work is available through the following interface, which can be called by querying the returned rowset:</span></span>


```
typedef [v1_enum] enum
{
    PRIORITY_LEVEL_FOREGROUND           = 0,    // process items in the scope first as quickly as possible
    PRIORITY_LEVEL_HIGH                 = 1,    // process items in the scope first at the normal rate
    PRIORITY_LEVEL_LOW                  = 2,    // process items in this scope before those at the normal rate, but after any other prioritization requests
    PRIORITY_LEVEL_DEFAULT              = 3     // process items at the normal indexer rate
} PRIORITY_LEVEL;


[
    object,
    uuid(IRowsetPrioritization_GUID),
    pointer_default(unique)
]
interface IRowsetPrioritization : IUnknown
{
    // Sets or retrieves the current indexer prioritization level for the scope specified by
    // this query.

    HRESULT SetScopePriority( [in] PRIORITY_LEVEL priority, [in] DWORD scopeStatisticsEventFrequency );
    HRESULT GetScopePriority( [out] PRIORITY_LEVEL * priority, [out] DWORD * scopeStatisticsEventFrequency );

    // Gets information describing the scope specified by this query:
    // indexedDocumentCount     -   The total number of documents currently indexed in the scope
    // oustandingAddCount       -   The total number of documents yet to be indexed in the scope (those not yet included in indexedDocumentCount)
    // oustandingModifyCount    -   The total number of documents indexed in the scope that need to be re-indexed (included in indexedDocumentCount)
    
    HRESULT GetScopeStatistics( [out] DWORD * indexedDocumentCount, [out] DWORD * oustandingAddCount, [out] DWORD * oustandingModifyCount );
};
```



<span data-ttu-id="738b9-133">La hiérarchisation des ensembles de lignes fonctionne comme suit :</span><span class="sxs-lookup"><span data-stu-id="738b9-133">Rowset prioritization works as follows:</span></span>

1.  <span data-ttu-id="738b9-134">[**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) est acquis avec la [méthode IUnknown :: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur un ensemble de lignes d’indexeur.</span><span class="sxs-lookup"><span data-stu-id="738b9-134">[**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) is acquired with [IUnknown::QueryInterface Method](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on an indexer rowset.</span></span> <span data-ttu-id="738b9-135">**DBPROP \_ ENABLEROWSETEVENTS** doit avoir la valeur **true** avec la méthode OLE DB [ICommandProperties :: SetProperties](/previous-versions/windows/desktop/ms711497(v=vs.85)) avant d’exécuter la requête afin d’utiliser la hiérarchisation des ensembles de lignes.</span><span class="sxs-lookup"><span data-stu-id="738b9-135">**DBPROP\_ENABLEROWSETEVENTS** must be set to **TRUE** with the OLE DB [ICommandProperties::SetProperties](/previous-versions/windows/desktop/ms711497(v=vs.85)) method prior to executing the query in order to use rowset prioritization.</span></span>
2.  <span data-ttu-id="738b9-136">[**IRowsetPrioritization :: SetScopePriority**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-setscopepriority) définit la priorité des étendues appartenant à la requête, ainsi que l’intervalle auquel l’événement de statistiques d’étendue est déclenché lorsqu’il y a des documents en suspens à indexer dans les étendues de requête.</span><span class="sxs-lookup"><span data-stu-id="738b9-136">[**IRowsetPrioritization::SetScopePriority**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-setscopepriority) sets the prioritization for the scopes belonging to the query, and the interval the scope statistics event is raised when there are outstanding documents to be indexed within the query scopes.</span></span> <span data-ttu-id="738b9-137">Cet événement est déclenché si le niveau de priorité est défini sur la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="738b9-137">This event is raised if the priority level is set to default.</span></span>
3.  <span data-ttu-id="738b9-138">[**IRowsetPrioritization :: GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) peut être utilisé pour récupérer le nombre d’éléments indexés dans l’étendue, le nombre de documents en attente à ajouter dans l’étendue et le nombre de documents qui doivent être réindexés dans cette étendue.</span><span class="sxs-lookup"><span data-stu-id="738b9-138">[**IRowsetPrioritization::GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) can be used to get the number of indexed items in the scope, the number of outstanding documents to be added in the scope, and the number of documents that need to be re-indexed within this scope.</span></span>

### <a name="irowsetprioritization-events"></a><span data-ttu-id="738b9-139">Événements IRowsetPrioritization</span><span class="sxs-lookup"><span data-stu-id="738b9-139">IRowsetPrioritization Events</span></span>

<span data-ttu-id="738b9-140">Il existe trois événements rowset dans [**IRowsetEvents :: OnRowsetEvent**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetevents-onrowsetevent) dans l’énumération de [**\_ type ROWSETEVENT**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type) :</span><span class="sxs-lookup"><span data-stu-id="738b9-140">There are three rowset events in [**IRowsetEvents::OnRowsetEvent**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetevents-onrowsetevent) in the [**ROWSETEVENT\_TYPE**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type) enumeration:</span></span>


```
    // This method allows for future notifications of various actions about your rowset or items within
    // eventType:                               - An identifier of the particular event being sent
    // pVarEventData:                           - The expected value of the EventData for each event type
    //      ROWSETEVENT_TYPE_DATAEXPIRED        - VT_EMPTY
    //      ROWSETEVENT_TYPE_FOREGROUNDLOST     - VT_EMPTY
    //      ROWSETEVENT_TYPE_SCOPESTATISTICS    - VT_VECTOR | VT_UI4 - 3 elements (0 = indexed items, 1 = outstanding adds, 2 = oustanding modifies)

    HRESULT OnRowsetEvent( [in] ROWSETEVENT_TYPE eventType, [in] REFPROPVARIANT eventData );
```



<span data-ttu-id="738b9-141">Les événements de l’ensemble de lignes sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="738b9-141">The rowset events are as follows:</span></span>

-   <span data-ttu-id="738b9-142">L’événement **ROWSETEVENT de \_ type \_ DATAEXPIRED** indique que les données qui stockent l’ensemble de lignes ont expiré et qu’un nouvel ensemble de lignes doit être demandé.</span><span class="sxs-lookup"><span data-stu-id="738b9-142">The **ROWSETEVENT\_TYPE\_DATAEXPIRED** event indicates that data backing the rowset has expired, and that a new rowset should be requested.</span></span>
-   <span data-ttu-id="738b9-143">L' **événement \_ \_ FOREGROUNDLOST du type d’ensemble de lignes** indique qu’un élément ayant une priorité de premier plan dans la pile de définition des priorités a été rétrogradé, car une autre personne a classé sa priorité sur cette requête.</span><span class="sxs-lookup"><span data-stu-id="738b9-143">The **ROWSET\_TYPE\_FOREGROUNDLOST** event indicates that an item that did have foreground priority in the prioritization stack has been demoted, because someone else prioritized themselves ahead of this query.</span></span>
-   <span data-ttu-id="738b9-144">L’événement **ROWSETEVENT de \_ type \_ SCOPESTATISTICS** fournit les mêmes informations disponibles à partir de l’appel de la méthode [**IRowsetPrioritization :: GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) , mais via un mécanicien de type push, comme suit :</span><span class="sxs-lookup"><span data-stu-id="738b9-144">The **ROWSETEVENT\_TYPE\_SCOPESTATISTICS** event gives you the same information available from the [**IRowsetPrioritization::GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) method call, but through a push mechanic, as follows:</span></span>
    -   <span data-ttu-id="738b9-145">L’événement se produit si l’API de hiérarchisation a été utilisée pour demander un niveau de priorité non défini par défaut et une fréquence d’événement de statistiques différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="738b9-145">The event arises if the prioritization API has been used to request a non-default prioritization level, and a non-zero statistics event frequency.</span></span>
    -   <span data-ttu-id="738b9-146">L’événement se produit uniquement lorsque les statistiques changent réellement et que l’intervalle spécifié dans le [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) s’est écoulé (l’intervalle ne garantit pas la fréquence de l’événement).</span><span class="sxs-lookup"><span data-stu-id="738b9-146">The event arises only when statistics actually change, and the interval specified in the [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) has elapsed (the interval does not guarantee the frequency of the event).</span></span>
    -   <span data-ttu-id="738b9-147">Cet événement est garanti pour déclencher un État « rebond Zero » (zéro élément restant à ajouter, zéro modification restante), à condition qu’un événement différent de zéro ait été déclenché.</span><span class="sxs-lookup"><span data-stu-id="738b9-147">This event is guaranteed to raise a "bounce zero" state (zero items remaining to be added, zero modifies remaining), provided that a non-zero event has been raised.</span></span>
    -   <span data-ttu-id="738b9-148">L’indexeur peut traiter les éléments sans envoyer cet événement, si la file d’attente est vidée avant la fréquence d’événement des statistiques.</span><span class="sxs-lookup"><span data-stu-id="738b9-148">The indexer may process items without sending this event, if the queue empties before the statistics event frequency.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="738b9-149">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="738b9-149">Additional Resources</span></span>

<span data-ttu-id="738b9-150">Consultez les ressources suivantes relatives à la hiérarchisation et aux ensembles de lignes :</span><span class="sxs-lookup"><span data-stu-id="738b9-150">See the following resources related to prioritization and rowsets:</span></span>

-   <span data-ttu-id="738b9-151">Interfaces :</span><span class="sxs-lookup"><span data-stu-id="738b9-151">Interfaces:</span></span>
    -   [<span data-ttu-id="738b9-152">**IRowsetEvents**</span><span class="sxs-lookup"><span data-stu-id="738b9-152">**IRowsetEvents**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)
    -   [<span data-ttu-id="738b9-153">**IRowsetPrioritization**</span><span class="sxs-lookup"><span data-stu-id="738b9-153">**IRowsetPrioritization**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)
-   <span data-ttu-id="738b9-154">Énumérations :</span><span class="sxs-lookup"><span data-stu-id="738b9-154">Enumerations:</span></span>
    -   [<span data-ttu-id="738b9-155">**définir la priorité des \_ indicateurs**</span><span class="sxs-lookup"><span data-stu-id="738b9-155">**PRIORITIZE\_FLAGS**</span></span>](/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags)
    -   [<span data-ttu-id="738b9-156">**niveau de priorité \_**</span><span class="sxs-lookup"><span data-stu-id="738b9-156">**PRIORITY\_LEVEL**</span></span>](/windows/win32/api/searchapi/ne-searchapi-priority_level)
    -   [<span data-ttu-id="738b9-157">**ROWSETEVENT \_ ITEMSTATE**</span><span class="sxs-lookup"><span data-stu-id="738b9-157">**ROWSETEVENT\_ITEMSTATE**</span></span>](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)
    -   [<span data-ttu-id="738b9-158">**\_type ROWSETEVENT**</span><span class="sxs-lookup"><span data-stu-id="738b9-158">**ROWSETEVENT\_TYPE**</span></span>](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)

## <a name="related-topics"></a><span data-ttu-id="738b9-159">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="738b9-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="738b9-160">Recherche Windows 7</span><span class="sxs-lookup"><span data-stu-id="738b9-160">Windows 7 Search</span></span>](./-search-3x-wds-overview.md)
</dt> <dt>

[<span data-ttu-id="738b9-161">Nouvelle recherche pour Windows 7</span><span class="sxs-lookup"><span data-stu-id="738b9-161">New for Windows 7 Search</span></span>](new-for-windows-7-search.md)
</dt> <dt>

[<span data-ttu-id="738b9-162">Bibliothèques de shell Windows dans Windows 7</span><span class="sxs-lookup"><span data-stu-id="738b9-162">Windows Shell Libraries in Windows 7</span></span>](-search-win7-development-scenarios.md)
</dt> </dl>

 

 