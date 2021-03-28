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
# <a name="updating-an-event-tracing-session"></a>Mise à jour d’une session de suivi d’événements

Pour mettre à jour les propriétés d’une session de suivi d’événements, appelez la fonction [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) à l’aide du code de contrôle de **\_ \_ \_ mise à jour** du contrôle de trace d’événements. Vous pouvez spécifier la session à mettre à jour à l’aide d’un handle de session obtenu à partir d’un appel antérieur à [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)ou d’un nom de session. Les propriétés de la session de suivi d’événements sont mises à jour à l’aide des valeurs spécifiées dans la structure des [**\_ \_ Propriétés de suivi d’événement**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) . Vous ne pouvez mettre à jour qu’un sous-ensemble des propriétés. Pour obtenir la liste des propriétés que vous pouvez mettre à jour, consultez le paramètre *Properties* de la fonction **ControlTrace** .

Si l’appel [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) réussit, la structure des propriétés de la [**\_ trace \_ d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) est mise à jour pour refléter les nouvelles valeurs de propriété. La structure contiendra également les nouvelles statistiques d’exécution pour la session de suivi d’événements.

L’exemple suivant montre comment mettre à jour la session de suivi d’événements du noyau. L’exemple recherche les valeurs de propriété actuelles et met à jour la structure avant de mettre à jour la session.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration et démarrage d’une session de journalisation privée](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[Configuration et démarrage d’une session SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Configuration et démarrage d’une session de journalisation automatique](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[Configuration et démarrage d’une session de suivi d’événements](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[Configuration et démarrage de la session de journalisation du noyau NT](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> </dl>

 

 
