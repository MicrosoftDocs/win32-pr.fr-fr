---
description: La session de suivi de noyau NT est une session de suivi d’événements qui enregistre un ensemble prédéfini d’événements de noyau.
ms.assetid: 3c4258d8-8073-4cc5-a29d-ce485a3fdc14
title: Configuration et démarrage de la session de journalisation du noyau NT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a41398c9caac3ecd090af68a18bfb148095632d96b8c75eaaee7f04a551360fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901219"
---
# <a name="configuring-and-starting-the-nt-kernel-logger-session"></a>Configuration et démarrage de la session de journalisation du noyau NT

La session de suivi de noyau NT est une session de suivi d’événements qui enregistre un ensemble prédéfini d’événements de noyau. Vous n’appelez pas la fonction [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) pour activer les fournisseurs de noyau. Au lieu de cela, vous utilisez le membre **EnableFlags** de la structure des [**Propriétés de \_ trace \_ d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) pour spécifier les événements de noyau que vous souhaitez recevoir. La fonction [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) utilise les indicateurs Enable que vous spécifiez pour activer les fournisseurs de noyau.

Il n’existe qu’une seule session de journalisation du noyau NT. Si la session est déjà en cours d’utilisation, la fonction [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) renvoie une erreur \_ \_ .

Pour plus d’informations sur le démarrage d’une session de suivi d’événements, consultez [configuration et démarrage d’une session de suivi d’événements](configuring-and-starting-an-event-tracing-session.md).

Pour plus d’informations sur le démarrage d’une session privée de journalisation, consultez [configuration et démarrage d’une session de journalisation privée](configuring-and-starting-a-private-logger-session.md).

Pour plus d’informations sur le démarrage d’une session de journalisation globale, consultez [configuration et démarrage de la session de journalisation globale](configuring-and-starting-the-global-logger-session.md).

Pour plus d’informations sur le démarrage d’une session de journalisation automatique, consultez [configuration et démarrage d’une session de journalisation](configuring-and-starting-an-autologger-session.md)automatique.

L’exemple suivant montre comment configurer et démarrer une session d’enregistrement de noyau NT qui collecte les événements de noyau réseau TCP/IP et les écrit dans un fichier circulaire de 5 Mo.


```C++
#define INITGUID  // Include this #define to use SystemTraceControlGuid in Evntrace.h.

#include <windows.h>
#include <stdio.h>
#include <conio.h>
#include <strsafe.h>
#include <wmistr.h>
#include <evntrace.h>

#define LOGFILE_PATH L"<FULLPATHTOTHELOGFILE.etl>"

void wmain(void)
{
    ULONG status = ERROR_SUCCESS;
    TRACEHANDLE SessionHandle = 0;
    EVENT_TRACE_PROPERTIES* pSessionProperties = NULL;
    ULONG BufferSize = 0;

    // Allocate memory for the session properties. The memory must
    // be large enough to include the log file name and session name,
    // which get appended to the end of the session properties structure.
    
    BufferSize = sizeof(EVENT_TRACE_PROPERTIES) + sizeof(LOGFILE_PATH) + sizeof(KERNEL_LOGGER_NAME);
    pSessionProperties = (EVENT_TRACE_PROPERTIES*) malloc(BufferSize);    
    if (NULL == pSessionProperties)
    {
        wprintf(L"Unable to allocate %d bytes for properties structure.\n", BufferSize);
        goto cleanup;
    }
    
    // Set the session properties. You only append the log file name
    // to the properties structure; the StartTrace function appends
    // the session name for you.

    ZeroMemory(pSessionProperties, BufferSize);
    pSessionProperties->Wnode.BufferSize = BufferSize;
    pSessionProperties->Wnode.Flags = WNODE_FLAG_TRACED_GUID;
    pSessionProperties->Wnode.ClientContext = 1; //QPC clock resolution
    pSessionProperties->Wnode.Guid = SystemTraceControlGuid; 
    pSessionProperties->EnableFlags = EVENT_TRACE_FLAG_NETWORK_TCPIP;
    pSessionProperties->LogFileMode = EVENT_TRACE_FILE_MODE_CIRCULAR;
    pSessionProperties->MaximumFileSize = 5;  // 5 MB
    pSessionProperties->LoggerNameOffset = sizeof(EVENT_TRACE_PROPERTIES);
    pSessionProperties->LogFileNameOffset = sizeof(EVENT_TRACE_PROPERTIES) + sizeof(KERNEL_LOGGER_NAME); 
    StringCbCopy((LPWSTR)((char*)pSessionProperties + pSessionProperties->LogFileNameOffset), sizeof(LOGFILE_PATH), LOGFILE_PATH);

    // Create the trace session.

    status = StartTrace((PTRACEHANDLE)&SessionHandle, KERNEL_LOGGER_NAME, pSessionProperties);

    if (ERROR_SUCCESS != status)
    {
        if (ERROR_ALREADY_EXISTS == status)
        {
            wprintf(L"The NT Kernel Logger session is already in use.\n");
        }
        else
        {
            wprintf(L"EnableTrace() failed with %lu\n", status);
        }

        goto cleanup;
    }

    wprintf(L"Press any key to end trace session ");
    _getch();

cleanup:

    if (SessionHandle)
    {
        status = ControlTrace(SessionHandle, KERNEL_LOGGER_NAME, pSessionProperties, EVENT_TRACE_CONTROL_STOP);

        if (ERROR_SUCCESS != status)
        {
            wprintf(L"ControlTrace(stop) failed with %lu\n", status);
        }
    }

    if (pSessionProperties)
        free(pSessionProperties);
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

[Mise à jour d’une session de suivi d’événements](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
