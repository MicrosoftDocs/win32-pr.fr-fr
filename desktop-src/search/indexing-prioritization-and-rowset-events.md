---
description: décrit l’introduction de la hiérarchisation des index et des événements d’ensemble de lignes pour Windows 7.
ms.assetid: 6cdfb7d3-f849-432c-960f-912e5024c583
title: indexation de la hiérarchisation et des événements d’ensemble de lignes dans Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92491300127c60ebdf2a265583fca77e77a09907b7f42b471f6d3d047a7f6aa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117680500"
---
# <a name="indexing-prioritization-and-rowset-events-in-windows-7"></a>indexation de la hiérarchisation et des événements d’ensemble de lignes dans Windows 7

cette rubrique décrit l’introduction de la hiérarchisation des index et des événements d’ensemble de lignes pour Windows 7.

Cette rubrique est organisée comme suit :

-   [Indexation de la hiérarchisation et des événements d’ensemble de lignes](#indexing-prioritization-and-rowset-events)
    -   [Exemples IRowsetPriorization](#irowsetpriorization-examples)
    -   [Événements IRowsetPrioritization](#indexing-prioritization-and-rowset-events-in-windows-7)
-   [Ressources supplémentaires](#additional-resources)
-   [Rubriques connexes](#related-topics)

## <a name="indexing-prioritization-and-rowset-events"></a>Indexation de la hiérarchisation et des événements d’ensemble de lignes

dans Windows 7 ? et versions ultérieures, il existe une pile de priorités dans laquelle le contexte d’une requête particulière, le client peut demander que les étendues utilisées dans cette requête soient hiérarchisées au-dessus de celles des éléments normaux.

Cette pile de définition de priorités présente les caractéristiques suivantes :

-   Les éléments de la pile peuvent avoir une priorité de premier plan, haute ou basse :
    -   **Premier plan**: la logique d’interruption est ignorée et l’indexation continue aussi rapidement que la machine l’autorise.
    -   **Élevé**: la définition de la priorité a été demandée avec interruption.
    -   **Faible**: la définition de la priorité a été demandée, et non pas aux dépens des autres étendues de la pile, mais au-dessus de l’indexation non hiérarchisée.
-   Toute demande de priorité élevée ou de premier plan porte automatiquement la requête en haut de la pile.
-   Seul l’élément situé en haut de la pile peut avoir une priorité de premier plan.
-   Une requête avec une priorité de premier plan en priorité reçoit un événement l’informant qu’elle a perdu la priorité de premier plan et qu’elle est devenue une priorité élevée avec l’interruption.

La pile de priorité définit une priorité globale des éléments traités dans l’indexeur comme suit :

-   Les notifications de priorité élevée n’ont pas d’interruption et sont généralement envoyées uniquement pour un petit nombre d’éléments. par exemple, Windows Explorer utilise cette priorité pour les opérations de moteur de copie de petite taille.
-   La pile de priorité est supérieure à la pile, a un intervalle et est la dernière requête prioritaire demandée.
-   Deuxième requête dans la pile.
-   Troisième requête dans la pile.
-   Quatrième requête dans la pile, et ainsi de suite.
-   Éléments de priorité normaux.
-   Éléments supprimés.
    > [!Note]  
    > Les éléments de chaque groupe sont classés par ordre de priorité en interne par le biais de la sémantique par élément antérieure.

     

### <a name="irowsetpriorization-examples"></a>Exemples IRowsetPriorization

L’API principale pour le travail de hiérarchisation est disponible via l’interface suivante, qui peut être appelée en interrogeant l’ensemble de lignes retourné :


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



La hiérarchisation des ensembles de lignes fonctionne comme suit :

1.  [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) est acquis avec la [méthode IUnknown :: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur un ensemble de lignes d’indexeur. **DBPROP \_ ENABLEROWSETEVENTS** doit avoir la valeur **true** avec la méthode OLE DB [ICommandProperties :: SetProperties](/previous-versions/windows/desktop/ms711497(v=vs.85)) avant d’exécuter la requête afin d’utiliser la hiérarchisation des ensembles de lignes.
2.  [**IRowsetPrioritization :: SetScopePriority**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-setscopepriority) définit la priorité des étendues appartenant à la requête, ainsi que l’intervalle auquel l’événement de statistiques d’étendue est déclenché lorsqu’il y a des documents en suspens à indexer dans les étendues de requête. Cet événement est déclenché si le niveau de priorité est défini sur la valeur par défaut.
3.  [**IRowsetPrioritization :: GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) peut être utilisé pour récupérer le nombre d’éléments indexés dans l’étendue, le nombre de documents en attente à ajouter dans l’étendue et le nombre de documents qui doivent être réindexés dans cette étendue.

### <a name="irowsetprioritization-events"></a>Événements IRowsetPrioritization

Il existe trois événements rowset dans [**IRowsetEvents :: OnRowsetEvent**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetevents-onrowsetevent) dans l’énumération de [**\_ type ROWSETEVENT**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type) :


```
    // This method allows for future notifications of various actions about your rowset or items within
    // eventType:                               - An identifier of the particular event being sent
    // pVarEventData:                           - The expected value of the EventData for each event type
    //      ROWSETEVENT_TYPE_DATAEXPIRED        - VT_EMPTY
    //      ROWSETEVENT_TYPE_FOREGROUNDLOST     - VT_EMPTY
    //      ROWSETEVENT_TYPE_SCOPESTATISTICS    - VT_VECTOR | VT_UI4 - 3 elements (0 = indexed items, 1 = outstanding adds, 2 = oustanding modifies)

    HRESULT OnRowsetEvent( [in] ROWSETEVENT_TYPE eventType, [in] REFPROPVARIANT eventData );
```



Les événements de l’ensemble de lignes sont les suivants :

-   L’événement **ROWSETEVENT de \_ type \_ DATAEXPIRED** indique que les données qui stockent l’ensemble de lignes ont expiré et qu’un nouvel ensemble de lignes doit être demandé.
-   L' **événement \_ \_ FOREGROUNDLOST du type d’ensemble de lignes** indique qu’un élément ayant une priorité de premier plan dans la pile de définition des priorités a été rétrogradé, car une autre personne a classé sa priorité sur cette requête.
-   L’événement **ROWSETEVENT de \_ type \_ SCOPESTATISTICS** fournit les mêmes informations disponibles à partir de l’appel de la méthode [**IRowsetPrioritization :: GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) , mais via un mécanicien de type push, comme suit :
    -   L’événement se produit si l’API de hiérarchisation a été utilisée pour demander un niveau de priorité non défini par défaut et une fréquence d’événement de statistiques différente de zéro.
    -   L’événement se produit uniquement lorsque les statistiques changent réellement et que l’intervalle spécifié dans le [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) s’est écoulé (l’intervalle ne garantit pas la fréquence de l’événement).
    -   Cet événement est garanti pour déclencher un État « rebond Zero » (zéro élément restant à ajouter, zéro modification restante), à condition qu’un événement différent de zéro ait été déclenché.
    -   L’indexeur peut traiter les éléments sans envoyer cet événement, si la file d’attente est vidée avant la fréquence d’événement des statistiques.

## <a name="additional-resources"></a>Ressources supplémentaires

Consultez les ressources suivantes relatives à la hiérarchisation et aux ensembles de lignes :

-   Interfaces :
    -   [**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)
    -   [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)
-   Énumérations :
    -   [**définir la priorité des \_ indicateurs**](/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags)
    -   [**niveau de priorité \_**](/windows/win32/api/searchapi/ne-searchapi-priority_level)
    -   [**ROWSETEVENT \_ ITEMSTATE**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)
    -   [**\_type ROWSETEVENT**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[recherche Windows 7](./-search-3x-wds-overview.md)
</dt> <dt>

[nouveautés pour la recherche de Windows 7](new-for-windows-7-search.md)
</dt> <dt>

[Windows bibliothèques Shell dans Windows 7](-search-win7-development-scenarios.md)
</dt> </dl>

 

 