---
title: Interrogation des événements
description: Vous pouvez rechercher des événements à partir d’un canal ou d’un fichier journal.
ms.assetid: 929bedbf-6dce-428e-b2c0-de9dcfe4531b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 981e4a8c39daebbce641c79e7d26331b9b36845d3c71fd1902ea667ca85c5dbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587800"
---
# <a name="querying-for-events"></a>Interrogation des événements

Vous pouvez rechercher des événements à partir d’un canal ou d’un fichier journal. Le canal ou le fichier journal peut exister sur l’ordinateur local ou sur un ordinateur distant. Pour spécifier les événements que vous souhaitez obtenir à partir du canal ou du fichier journal, vous utilisez une requête XPath ou une requête XML de structure. Pour plus d’informations sur l’écriture de la requête, consultez [consommation d’événements](consuming-events.md).

Pour interroger des événements, appelez la fonction [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) . Vous pouvez spécifier l’ordre dans lequel les événements sont retournés (le plus ancien au plus récent (valeur par défaut) ou le plus récent au plus ancien) et s’il faut tolérer des expressions XPath mal formées dans la requête (pour plus d’informations sur la façon dont la fonction ignore les expressions mal formées, consultez l’indicateur [**EvtQueryTolerateQueryErrors**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_flags) ).

L’exemple suivant montre comment interroger des événements à partir d’un canal à l’aide d’une expression XPath.


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



L’exemple suivant montre comment interroger des événements à partir d’un canal à l’aide d’une requête XML structurée. Les événements sont retournés dans l’ordre, du plus récent au plus ancien.


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



Si vous utilisez une requête XML structurée et que vous transmettez l’indicateur EvtQueryTolerateQueryErrors à [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery), la fonction réussit, même si une ou plusieurs des requêtes de la requête structurée ont peut-être échoué. Pour déterminer les requêtes de la requête structurée ayant réussi ou échoué, appelez la fonction [**EvtGetQueryInfo**](/windows/desktop/api/WinEvt/nf-winevt-evtgetqueryinfo) . Si vous ne transmettez pas l’indicateur EvtQueryTolerateQueryErrors, la fonction **EvtQuery** échouera avec la première erreur qu’elle trouve dans la requête. Si la requête échoue avec l' \_ erreur \_ evt \_ requête non valide, appelez la fonction [**EvtGetExtendedStatus**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) pour obtenir une chaîne de message décrivant l’erreur XPath.

L’exemple suivant montre comment déterminer la réussite ou l’échec de chaque requête dans une requête structurée lors du passage de l’indicateur EvtQueryTolerateQueryErrors à [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery).


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



## <a name="reading-events-from-the-result-set"></a>Lecture d’événements à partir du jeu de résultats

Pour énumérer les événements dans le jeu de résultats, appelez la fonction [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) dans une boucle jusqu’à ce que la fonction retourne **false** et que la fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l’erreur plus \_ aucun \_ \_ élément. Les événements dans le jeu de résultats ne sont pas statiques ; les nouveaux événements écrits dans le canal seront inclus dans le jeu de résultats jusqu’à ce que l’erreur \_ n' \_ ait plus aucun \_ élément défini. Pour améliorer les performances, récupérez les événements du jeu de résultats par lots (en tenant compte de la taille de chaque événement lors de la détermination du nombre d’événements à extraire).

L’exemple suivant montre comment énumérer les événements d’un jeu de résultats.


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



Pour plus d’informations sur le rendu des événements que vous obtenez à partir du jeu de résultats, consultez [rendu des événements](rendering-events.md).

Si vous souhaitez rechercher les événements à partir de l’endroit où vous vous êtes arrêté, créez un signet du dernier événement que vous avez lu et utilisez-le lors de la prochaine exécution de votre requête. Pour plus d’informations, consultez [signets d’événements](bookmarking-events.md).

 

 