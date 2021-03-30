---
description: La session de suivi de noyau NT est une session de suivi d’événements qui enregistre un ensemble prédéfini d’événements de noyau.
ms.assetid: 3c4258d8-8073-4cc5-a29d-ce485a3fdc14
title: Configuration et démarrage de la session de journalisation du noyau NT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d13cb0d429bc4b0e01e02c33e2686040f0b7454b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973846"
---
# <a name="configuring-and-starting-the-nt-kernel-logger-session"></a><span data-ttu-id="6ab33-103">Configuration et démarrage de la session de journalisation du noyau NT</span><span class="sxs-lookup"><span data-stu-id="6ab33-103">Configuring and Starting the NT Kernel Logger Session</span></span>

<span data-ttu-id="6ab33-104">La session de suivi de noyau NT est une session de suivi d’événements qui enregistre un ensemble prédéfini d’événements de noyau.</span><span class="sxs-lookup"><span data-stu-id="6ab33-104">The NT Kernel Logger session is an event tracing session that records a predefined set of kernel events.</span></span> <span data-ttu-id="6ab33-105">Vous n’appelez pas la fonction [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) pour activer les fournisseurs de noyau.</span><span class="sxs-lookup"><span data-stu-id="6ab33-105">You do not call the [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) function to enable the kernel providers.</span></span> <span data-ttu-id="6ab33-106">Au lieu de cela, vous utilisez le membre **EnableFlags** de la structure des [**Propriétés de \_ trace \_ d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) pour spécifier les événements de noyau que vous souhaitez recevoir.</span><span class="sxs-lookup"><span data-stu-id="6ab33-106">Instead, you use the **EnableFlags** member of [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure to specify the kernel events that you want to receive.</span></span> <span data-ttu-id="6ab33-107">La fonction [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) utilise les indicateurs Enable que vous spécifiez pour activer les fournisseurs de noyau.</span><span class="sxs-lookup"><span data-stu-id="6ab33-107">The [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function uses the enable flags that you specify to enable the kernel providers.</span></span>

<span data-ttu-id="6ab33-108">Il n’existe qu’une seule session de journalisation du noyau NT.</span><span class="sxs-lookup"><span data-stu-id="6ab33-108">There is only one NT Kernel Logger session.</span></span> <span data-ttu-id="6ab33-109">Si la session est déjà en cours d’utilisation, la fonction [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) renvoie une erreur \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="6ab33-109">If the session is already in use, the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function returns ERROR\_ALREADY\_EXISTS.</span></span>

<span data-ttu-id="6ab33-110">Pour plus d’informations sur le démarrage d’une session de suivi d’événements, consultez [configuration et démarrage d’une session de suivi d’événements](configuring-and-starting-an-event-tracing-session.md).</span><span class="sxs-lookup"><span data-stu-id="6ab33-110">For details on starting an event tracing session, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

<span data-ttu-id="6ab33-111">Pour plus d’informations sur le démarrage d’une session privée de journalisation, consultez [configuration et démarrage d’une session de journalisation privée](configuring-and-starting-a-private-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="6ab33-111">For details on starting a private logger session, see [Configuring and Starting a Private Logger Session](configuring-and-starting-a-private-logger-session.md).</span></span>

<span data-ttu-id="6ab33-112">Pour plus d’informations sur le démarrage d’une session de journalisation globale, consultez [configuration et démarrage de la session de journalisation globale](configuring-and-starting-the-global-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="6ab33-112">For details on starting a Global Logger session, see [Configuring and Starting the Global Logger Session](configuring-and-starting-the-global-logger-session.md).</span></span>

<span data-ttu-id="6ab33-113">Pour plus d’informations sur le démarrage d’une session de journalisation automatique, consultez [configuration et démarrage d’une session de journalisation](configuring-and-starting-an-autologger-session.md)automatique.</span><span class="sxs-lookup"><span data-stu-id="6ab33-113">For details on starting an AutoLogger session, see [Configuring and Starting an AutoLogger Session](configuring-and-starting-an-autologger-session.md).</span></span>

<span data-ttu-id="6ab33-114">L’exemple suivant montre comment configurer et démarrer une session d’enregistrement de noyau NT qui collecte les événements de noyau réseau TCP/IP et les écrit dans un fichier circulaire de 5 Mo.</span><span class="sxs-lookup"><span data-stu-id="6ab33-114">The following example shows how to configure and start an NT Kernel Logger session that collects network TCP/IP kernel events and writes them to a 5MB circular file.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="6ab33-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6ab33-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ab33-116">Configuration et démarrage d’une session de journalisation privée</span><span class="sxs-lookup"><span data-stu-id="6ab33-116">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[<span data-ttu-id="6ab33-117">Configuration et démarrage d’une session SystemTraceProvider</span><span class="sxs-lookup"><span data-stu-id="6ab33-117">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[<span data-ttu-id="6ab33-118">Configuration et démarrage d’une session de journalisation automatique</span><span class="sxs-lookup"><span data-stu-id="6ab33-118">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[<span data-ttu-id="6ab33-119">Configuration et démarrage d’une session de suivi d’événements</span><span class="sxs-lookup"><span data-stu-id="6ab33-119">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="6ab33-120">Mise à jour d’une session de suivi d’événements</span><span class="sxs-lookup"><span data-stu-id="6ab33-120">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
