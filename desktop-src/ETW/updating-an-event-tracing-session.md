---
description: Pour mettre à jour les propriétés d’une session de suivi d’événements, appelez la fonction ControlTrace à l’aide du \_ \_ Code de contrôle de mise à jour du contrôle de trace d’événements \_ .
ms.assetid: 1496bf88-a989-4fa1-888a-90385c4ca8ee
title: Mise à jour d’une session de suivi d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e580c2e84dec6682e5fad323fe0cad427300a21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951368"
---
# <a name="updating-an-event-tracing-session"></a><span data-ttu-id="88fcc-103">Mise à jour d’une session de suivi d’événements</span><span class="sxs-lookup"><span data-stu-id="88fcc-103">Updating an Event Tracing Session</span></span>

<span data-ttu-id="88fcc-104">Pour mettre à jour les propriétés d’une session de suivi d’événements, appelez la fonction [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) à l’aide du code de contrôle de **\_ \_ \_ mise à jour** du contrôle de trace d’événements.</span><span class="sxs-lookup"><span data-stu-id="88fcc-104">To update the properties of an event tracing session, call the [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) function using the **EVENT\_TRACE\_CONTROL\_UPDATE** control code.</span></span> <span data-ttu-id="88fcc-105">Vous pouvez spécifier la session à mettre à jour à l’aide d’un handle de session obtenu à partir d’un appel antérieur à [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)ou d’un nom de session.</span><span class="sxs-lookup"><span data-stu-id="88fcc-105">You can specify the session to update using a session handle obtained from an earlier call to [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea), or a session name.</span></span> <span data-ttu-id="88fcc-106">Les propriétés de la session de suivi d’événements sont mises à jour à l’aide des valeurs spécifiées dans la structure des [**\_ \_ Propriétés de suivi d’événement**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) .</span><span class="sxs-lookup"><span data-stu-id="88fcc-106">The properties of the event tracing session are updated using the values specified in the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure.</span></span> <span data-ttu-id="88fcc-107">Vous ne pouvez mettre à jour qu’un sous-ensemble des propriétés.</span><span class="sxs-lookup"><span data-stu-id="88fcc-107">You can update only a subset of the properties.</span></span> <span data-ttu-id="88fcc-108">Pour obtenir la liste des propriétés que vous pouvez mettre à jour, consultez le paramètre *Properties* de la fonction **ControlTrace** .</span><span class="sxs-lookup"><span data-stu-id="88fcc-108">For a list of the properties you can update, see the *Properties* parameter of the **ControlTrace** function.</span></span>

<span data-ttu-id="88fcc-109">Si l’appel [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) réussit, la structure des propriétés de la [**\_ trace \_ d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) est mise à jour pour refléter les nouvelles valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="88fcc-109">If the [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) call is successful, the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure is updated to reflect the new property values.</span></span> <span data-ttu-id="88fcc-110">La structure contiendra également les nouvelles statistiques d’exécution pour la session de suivi d’événements.</span><span class="sxs-lookup"><span data-stu-id="88fcc-110">The structure will also contain the new run statistics for the event tracing session.</span></span>

<span data-ttu-id="88fcc-111">L’exemple suivant montre comment mettre à jour la session de suivi d’événements du noyau.</span><span class="sxs-lookup"><span data-stu-id="88fcc-111">The following example shows how to update the kernel event tracing session.</span></span> <span data-ttu-id="88fcc-112">L’exemple recherche les valeurs de propriété actuelles et met à jour la structure avant de mettre à jour la session.</span><span class="sxs-lookup"><span data-stu-id="88fcc-112">The example queries for the current property values and updates the structure before updating the session.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <wmistr.h>
#include <evntrace.h>

#define MAX_SESSION_NAME_LEN 1024
#define MAX_LOGFILE_PATH_LEN 1024

void wmain(void)
{
    ULONG status = ERROR_SUCCESS;
    EVENT_TRACE_PROPERTIES* pSessionProperties = NULL;
    ULONG BufferSize = 0;

    // Allocate memory for the session properties. The memory must
    // be large enough to include the log file name and session name.
    // This example specifies the maximum size for the session name 
    // and log file name.
    
    BufferSize = sizeof(EVENT_TRACE_PROPERTIES) + 
        (MAX_SESSION_NAME_LEN * sizeof(WCHAR)) + 
        (MAX_LOGFILE_PATH_LEN * sizeof(WCHAR));

    pSessionProperties = (EVENT_TRACE_PROPERTIES*) malloc(BufferSize);    
    if (NULL == pSessionProperties)
    {
        wprintf(L"Unable to allocate %d bytes for properties structure.\n", BufferSize);
        goto cleanup;
    }
    
    ZeroMemory(pSessionProperties, BufferSize);
    pSessionProperties->Wnode.BufferSize = BufferSize;

    // Query for the kernel trace session's current property values.

    status = ControlTrace((TRACEHANDLE)NULL, KERNEL_LOGGER_NAME, pSessionProperties, EVENT_TRACE_CONTROL_QUERY);

    if (ERROR_SUCCESS != status)
    {
        if (ERROR_WMI_INSTANCE_NOT_FOUND == status)
        {
            wprintf(L"The Kernel Logger is not running.\n");
        }
        else
        {
            wprintf(L"ControlTrace(query) failed with %lu\n", status);
        }

        goto cleanup;
    }

    // Update the enable flags to also enable the Process and Thread providers.

    pSessionProperties->LogFileNameOffset = 0;  // Zero tells ETW not to update the file name
    pSessionProperties->Wnode.Flags = WNODE_FLAG_TRACED_GUID;
    pSessionProperties->EnableFlags |= EVENT_TRACE_FLAG_PROCESS | EVENT_TRACE_FLAG_THREAD;

    // Update the session's properties.

    status = ControlTrace((TRACEHANDLE)NULL, KERNEL_LOGGER_NAME, pSessionProperties, EVENT_TRACE_CONTROL_UPDATE);
    if (ERROR_SUCCESS != status)
    {
        wprintf(L"ControlTrace(update) failed with %lu.\n", status);
        goto cleanup;
    }

    wprintf(L"\nUpdated session");

cleanup:

    if (pSessionProperties)
    {
        free(pSessionProperties);
        pSessionProperties = NULL;
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="88fcc-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="88fcc-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88fcc-114">Configuration et démarrage d’une session de journalisation privée</span><span class="sxs-lookup"><span data-stu-id="88fcc-114">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[<span data-ttu-id="88fcc-115">Configuration et démarrage d’une session SystemTraceProvider</span><span class="sxs-lookup"><span data-stu-id="88fcc-115">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[<span data-ttu-id="88fcc-116">Configuration et démarrage d’une session de journalisation automatique</span><span class="sxs-lookup"><span data-stu-id="88fcc-116">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[<span data-ttu-id="88fcc-117">Configuration et démarrage d’une session de suivi d’événements</span><span class="sxs-lookup"><span data-stu-id="88fcc-117">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="88fcc-118">Configuration et démarrage de la session de journalisation du noyau NT</span><span class="sxs-lookup"><span data-stu-id="88fcc-118">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> </dl>

 

 
