---
title: Interrogation des événements
description: Vous pouvez rechercher des événements à partir d’un canal ou d’un fichier journal.
ms.assetid: 929bedbf-6dce-428e-b2c0-de9dcfe4531b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6fa69f9b1308cd7ebbc4e4510692bb25ab031ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106513553"
---
# <a name="querying-for-events"></a><span data-ttu-id="68d5d-103">Interrogation des événements</span><span class="sxs-lookup"><span data-stu-id="68d5d-103">Querying for Events</span></span>

<span data-ttu-id="68d5d-104">Vous pouvez rechercher des événements à partir d’un canal ou d’un fichier journal.</span><span class="sxs-lookup"><span data-stu-id="68d5d-104">You can query for events from a channel or a log file.</span></span> <span data-ttu-id="68d5d-105">Le canal ou le fichier journal peut exister sur l’ordinateur local ou sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="68d5d-105">The channel or log file can exist on the local computer or a remote computer.</span></span> <span data-ttu-id="68d5d-106">Pour spécifier les événements que vous souhaitez obtenir à partir du canal ou du fichier journal, vous utilisez une requête XPath ou une requête XML de structure.</span><span class="sxs-lookup"><span data-stu-id="68d5d-106">To specify the events that you want to get from the channel or log file, you use an XPath query or a structure XML query.</span></span> <span data-ttu-id="68d5d-107">Pour plus d’informations sur l’écriture de la requête, consultez [consommation d’événements](consuming-events.md).</span><span class="sxs-lookup"><span data-stu-id="68d5d-107">For details on writing the query, see [Consuming Events](consuming-events.md).</span></span>

<span data-ttu-id="68d5d-108">Pour interroger des événements, appelez la fonction [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) .</span><span class="sxs-lookup"><span data-stu-id="68d5d-108">To query events, call the [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) function.</span></span> <span data-ttu-id="68d5d-109">Vous pouvez spécifier l’ordre dans lequel les événements sont retournés (le plus ancien au plus récent (valeur par défaut) ou le plus récent au plus ancien) et s’il faut tolérer des expressions XPath mal formées dans la requête (pour plus d’informations sur la façon dont la fonction ignore les expressions mal formées, consultez l’indicateur [**EvtQueryTolerateQueryErrors**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_flags) ).</span><span class="sxs-lookup"><span data-stu-id="68d5d-109">You can specify the order in which the events are returned (oldest to newest (the default) or newest to oldest) and whether to tolerate malformed XPath expressions in the query (for details on how the function ignores the malformed expressions, see the [**EvtQueryTolerateQueryErrors**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_flags) flag).</span></span>

<span data-ttu-id="68d5d-110">L’exemple suivant montre comment interroger des événements à partir d’un canal à l’aide d’une expression XPath.</span><span class="sxs-lookup"><span data-stu-id="68d5d-110">The following example shows how to query events from a channel using an XPath expression.</span></span>


```C++
#include <windows.h>
#include <sddl.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

#define ARRAY_SIZE 10
#define TIMEOUT 1000  // 1 second; Set and use in place of INFINITE in EvtNext call

DWORD PrintResults(EVT_HANDLE hResults);
DWORD PrintEvent(EVT_HANDLE hEvent); // Shown in the Rendering Events topic

void main(void)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hResults = NULL;
    LPWSTR pwsPath = L"<Name of the channel goes here>";
    LPWSTR pwsQuery = L"Event/System[EventID=4]";

    hResults = EvtQuery(NULL, pwsPath, pwsQuery, EvtQueryChannelPath | EvtQueryReverseDirection);
    if (NULL == hResults)
    {
        status = GetLastError();

        if (ERROR_EVT_CHANNEL_NOT_FOUND == status)
            wprintf(L"The channel was not found.\n");
        else if (ERROR_EVT_INVALID_QUERY == status)
            // You can call the EvtGetExtendedStatus function to try to get 
            // additional information as to what is wrong with the query.
            wprintf(L"The query is not valid.\n");
        else
            wprintf(L"EvtQuery failed with %lu.\n", status);

        goto cleanup;
    }

    PrintResults(hResults);

cleanup:

    if (hResults)
        EvtClose(hResults);

}
```



<span data-ttu-id="68d5d-111">L’exemple suivant montre comment interroger des événements à partir d’un canal à l’aide d’une requête XML structurée.</span><span class="sxs-lookup"><span data-stu-id="68d5d-111">The following example shows how to query events from a channel using a structured XML query.</span></span> <span data-ttu-id="68d5d-112">Les événements sont retournés dans l’ordre, du plus récent au plus ancien.</span><span class="sxs-lookup"><span data-stu-id="68d5d-112">The events are returned in order from newest to oldest.</span></span>


```C++
#include <windows.h>
#include <sddl.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

#define ARRAY_SIZE 10
#define TIMEOUT 1000  // 1 second; Set and use in place of INFINITE in EvtNext call

// The structured XML query.
#define QUERY \
    L"<QueryList>" \
    L"  <Query Path='Name of the channel goes here'>" \
    L"    <Select>Event/System[EventID=4]</Select>" \
    L"  </Query>" \
    L"</QueryList>"

DWORD PrintQueryStatuses(EVT_HANDLE hResults);
DWORD GetQueryStatusProperty(EVT_QUERY_PROPERTY_ID Id, EVT_HANDLE hResults, PEVT_VARIANT& pProperty);
DWORD PrintResults(EVT_HANDLE hResults);
DWORD PrintEvent(EVT_HANDLE hEvent);  // Shown in the Rendering Events topic

void main(void)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hResults = NULL;

    hResults = EvtQuery(NULL, NULL, QUERY, EvtQueryChannelPath | EvtQueryTolerateQueryErrors);
    if (NULL == hResults)
    {
        // Handle error.
        goto cleanup;
    }

    // Print the status of each query. If all the queries succeeded,
    // print the events in the result set. The status can be
    // ERROR_EVT_CHANNEL_NOT_FOUND or ERROR_EVT_INVALID_QUERY among others.
    if (ERROR_SUCCESS == PrintQueryStatuses(hResults))
        PrintResults(hResults);

cleanup:

    if (hResults)
        EvtClose(hResults);

}
```



<span data-ttu-id="68d5d-113">Si vous utilisez une requête XML structurée et que vous transmettez l’indicateur EvtQueryTolerateQueryErrors à [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery), la fonction réussit, même si une ou plusieurs des requêtes de la requête structurée ont peut-être échoué.</span><span class="sxs-lookup"><span data-stu-id="68d5d-113">If you are using a structured XML query and pass the EvtQueryTolerateQueryErrors flag to [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery), the function succeeds even though one or more of the queries in the structured query may have actually failed.</span></span> <span data-ttu-id="68d5d-114">Pour déterminer les requêtes de la requête structurée ayant réussi ou échoué, appelez la fonction [**EvtGetQueryInfo**](/windows/desktop/api/WinEvt/nf-winevt-evtgetqueryinfo) .</span><span class="sxs-lookup"><span data-stu-id="68d5d-114">To determine which queries in the structured query succeeded or failed, call the [**EvtGetQueryInfo**](/windows/desktop/api/WinEvt/nf-winevt-evtgetqueryinfo) function.</span></span> <span data-ttu-id="68d5d-115">Si vous ne transmettez pas l’indicateur EvtQueryTolerateQueryErrors, la fonction **EvtQuery** échouera avec la première erreur qu’elle trouve dans la requête.</span><span class="sxs-lookup"><span data-stu-id="68d5d-115">If you do not pass the EvtQueryTolerateQueryErrors flag, the **EvtQuery** function will fail with the first error that it finds in the query.</span></span> <span data-ttu-id="68d5d-116">Si la requête échoue avec l' \_ erreur \_ evt \_ requête non valide, appelez la fonction [**EvtGetExtendedStatus**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) pour obtenir une chaîne de message décrivant l’erreur XPath.</span><span class="sxs-lookup"><span data-stu-id="68d5d-116">If the query fails with ERROR\_EVT\_INVALID\_QUERY, call the [**EvtGetExtendedStatus**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) function to get a message string that describes the XPath error.</span></span>

<span data-ttu-id="68d5d-117">L’exemple suivant montre comment déterminer la réussite ou l’échec de chaque requête dans une requête structurée lors du passage de l’indicateur EvtQueryTolerateQueryErrors à [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery).</span><span class="sxs-lookup"><span data-stu-id="68d5d-117">The following example shows how to determine the success or failure of each query in a structured query when passing the EvtQueryTolerateQueryErrors flag to [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery).</span></span>


```C++
// Get the list of paths in the query and the status for each path. Return
// the sum of the statuses, so the caller can decide whether to enumerate 
// the results.
DWORD PrintQueryStatuses(EVT_HANDLE hResults)
{
    DWORD status = ERROR_SUCCESS;
    PEVT_VARIANT pPaths = NULL;
    PEVT_VARIANT pStatuses = NULL;

    wprintf(L"List of channels/logs that were queried and their status\n\n");

    if (status = GetQueryStatusProperty(EvtQueryNames, hResults, pPaths))
        goto cleanup;

    if (status = GetQueryStatusProperty(EvtQueryStatuses, hResults, pStatuses))
        goto cleanup;

    for (DWORD i = 0; i < pPaths->Count; i++)
    {
        wprintf(L"%s (%lu)\n", pPaths->StringArr[i], pStatuses->UInt32Arr[i]);
        status += pStatuses->UInt32Arr[i];
    }

cleanup:

    if (pPaths)
        free(pPaths);

    if (pStatuses)
        free(pStatuses);

    return status;
}


// Get the list of paths specified in the query or the list of status values 
// for each path.
DWORD GetQueryStatusProperty(EVT_QUERY_PROPERTY_ID Id, EVT_HANDLE hResults, PEVT_VARIANT& pProperty)
{
    DWORD status = ERROR_SUCCESS;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;

    if  (!EvtGetQueryInfo(hResults, Id, dwBufferSize, pProperty, &dwBufferUsed))
    {
        status = GetLastError();
        if (ERROR_INSUFFICIENT_BUFFER == status)
        {
            dwBufferSize = dwBufferUsed;
            pProperty = (PEVT_VARIANT)malloc(dwBufferSize);
            if (pProperty)
            {
                EvtGetQueryInfo(hResults, Id, dwBufferSize, pProperty, &dwBufferUsed);
            }
            else
            {
                wprintf(L"realloc failed\n");
                status = ERROR_OUTOFMEMORY;
                goto cleanup;
            }
        }

        if (ERROR_SUCCESS != (status = GetLastError()))
        {
            wprintf(L"EvtGetQueryInfo failed with %d\n", GetLastError());
            goto cleanup;
        }
    }

cleanup:

    return status;
}
```



## <a name="reading-events-from-the-result-set"></a><span data-ttu-id="68d5d-118">Lecture d’événements à partir du jeu de résultats</span><span class="sxs-lookup"><span data-stu-id="68d5d-118">Reading events from the result set</span></span>

<span data-ttu-id="68d5d-119">Pour énumérer les événements dans le jeu de résultats, appelez la fonction [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) dans une boucle jusqu’à ce que la fonction retourne **false** et que la fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l’erreur plus \_ aucun \_ \_ élément.</span><span class="sxs-lookup"><span data-stu-id="68d5d-119">To enumerate the events in the result set, call the [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) function in a loop until the function returns **FALSE** and the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns ERROR\_NO\_MORE\_ITEMS.</span></span> <span data-ttu-id="68d5d-120">Les événements dans le jeu de résultats ne sont pas statiques ; les nouveaux événements écrits dans le canal seront inclus dans le jeu de résultats jusqu’à ce que l’erreur \_ n' \_ ait plus aucun \_ élément défini.</span><span class="sxs-lookup"><span data-stu-id="68d5d-120">The events in the result set are not static; new events that are written to the channel will be included in the result set until ERROR\_NO\_MORE\_ITEMS is set.</span></span> <span data-ttu-id="68d5d-121">Pour améliorer les performances, récupérez les événements du jeu de résultats par lots (en tenant compte de la taille de chaque événement lors de la détermination du nombre d’événements à extraire).</span><span class="sxs-lookup"><span data-stu-id="68d5d-121">To improve performance, fetch events from the result set in batches (taking into account the size of each event when determining the number of events to fetch).</span></span>

<span data-ttu-id="68d5d-122">L’exemple suivant montre comment énumérer les événements d’un jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="68d5d-122">The following example shows how to enumerate the events in a result set.</span></span>


```C++
// Enumerate all the events in the result set. 
DWORD PrintResults(EVT_HANDLE hResults)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hEvents[ARRAY_SIZE];
    DWORD dwReturned = 0;

    while (true)
    {
        // Get a block of events from the result set.
        if (!EvtNext(hResults, ARRAY_SIZE, hEvents, INFINITE, 0, &dwReturned))
        {
            if (ERROR_NO_MORE_ITEMS != (status = GetLastError()))
            {
                wprintf(L"EvtNext failed with %lu\n", status);
            }

            goto cleanup;
        }

        // For each event, call the PrintEvent function which renders the
        // event for display. PrintEvent is shown in RenderingEvents.
        for (DWORD i = 0; i < dwReturned; i++)
        {
            if (ERROR_SUCCESS == (status = PrintEvent(hEvents[i])))
            {
                EvtClose(hEvents[i]);
                hEvents[i] = NULL;
            }
            else
            {
                goto cleanup;
            }
        }
    }

cleanup:

    for (DWORD i = 0; i < dwReturned; i++)
    {
        if (NULL != hEvents[i])
            EvtClose(hEvents[i]);
    }

    return status;
}
```



<span data-ttu-id="68d5d-123">Pour plus d’informations sur le rendu des événements que vous obtenez à partir du jeu de résultats, consultez [rendu des événements](rendering-events.md).</span><span class="sxs-lookup"><span data-stu-id="68d5d-123">For details on rendering the events that you get from the result set, see [Rendering Events](rendering-events.md).</span></span>

<span data-ttu-id="68d5d-124">Si vous souhaitez rechercher les événements à partir de l’endroit où vous vous êtes arrêté, créez un signet du dernier événement que vous avez lu et utilisez-le lors de la prochaine exécution de votre requête.</span><span class="sxs-lookup"><span data-stu-id="68d5d-124">If you want to query for events from where you left off, create a bookmark of the last event that you read and use it the next time you run your query.</span></span> <span data-ttu-id="68d5d-125">Pour plus d’informations, consultez [signets d’événements](bookmarking-events.md).</span><span class="sxs-lookup"><span data-stu-id="68d5d-125">For details, see [Bookmarking Events](bookmarking-events.md).</span></span>

 

 