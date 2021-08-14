---
description: En savoir plus sur l’écriture d’événements MOF dans une session de suivi. Commencez par inscrire votre fournisseur, afin qu’il soit prêt à écrire des événements dans une session de trace.
ms.assetid: 21f62b5d-0a2d-468c-af88-2fab1512f0ec
title: Écriture d’événements MOF (Classic)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c29b5d753c40bb2fca5313340638a63d2a5e55c5eaf6dcef14e8388906cb190a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393658"
---
# <a name="writing-mof-classic-events"></a>Écriture d’événements MOF (Classic)

Avant de pouvoir écrire des événements dans une session de trace, vous devez inscrire votre fournisseur. L’inscription d’un fournisseur indique à ETW que votre fournisseur est prêt à écrire des événements dans une session de suivi. Un processus peut inscrire jusqu’à 1 024 GUID de fournisseur ; Toutefois, vous devez limiter le nombre de fournisseurs que votre processus inscrit à un ou deux.

**avant Windows Vista :** Il n’existe aucune limite au nombre de fournisseurs qu’un processus peut inscrire.

Pour inscrire un fournisseur classique, appelez la fonction [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) . La fonction enregistre le GUID du fournisseur, les GUID de classe de trace d’événements et identifie le rappel que ETW appelle lorsqu’un contrôleur active ou désactive le fournisseur.

Si le fournisseur appelle la fonction [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) pour consigner les événements, vous n’avez pas besoin d’inclure le tableau de GUID de classe (peut être **null**) lors de l’appel de la fonction [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) . Vous devez inclure le tableau uniquement si le fournisseur appelle la fonction [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) pour enregistrer les événements.

**Windows XP et Windows 2000 :** Vous devez toujours inclure le tableau de GUID de classe (ne peut pas être **null**).

Une fois qu’un fournisseur s’est inscrit lui-même et qu’il est activé par le contrôleur, le fournisseur peut consigner des événements dans la session de trace du contrôleur.

Avant de quitter le fournisseur, appelez la fonction [**UnregisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-unregistertraceguids) pour supprimer l’inscription du fournisseur dans ETW. La fonction [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) retourne le handle d’inscription que vous transmettez à la fonction **UnregisterTraceGuids** .

Si votre fournisseur enregistre des événements dans la session de journalisation globale uniquement, il n’est pas nécessaire d’inscrire votre fournisseur avec ETW, car le contrôleur d’enregistreur global n’active pas ou ne désactive pas les fournisseurs. Pour plus d’informations, consultez [configuration et démarrage de la session d’enregistreur](configuring-and-starting-the-global-logger-session.md)d’événements globale.

Tous les fournisseurs [classiques](about-event-tracing.md) (à l’exception de ceux qui tracent des événements dans la session de journalisation globale) doivent implémenter la fonction [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) . Le fournisseur utilise les informations du rappel pour déterminer s’il est activé ou désactivé et quels événements il doit écrire.

Le fournisseur spécifie le nom de la fonction de rappel lorsqu’il appelle la fonction [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) pour s’inscrire. ETW appelle la fonction de rappel lorsque le contrôleur appelle la fonction [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) pour activer ou désactiver le fournisseur.

Dans votre implémentation de [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) , vous devez appeler la fonction [**GetTraceLoggerHandle**](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle) pour récupérer le handle de session. vous utilisez le descripteur de session lors de l’appel de la fonction [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) . Il vous suffit d’appeler la fonction [**GetTraceEnableFlags**](/windows/win32/api/evntrace/nf-evntrace-gettraceenableflags) ou la fonction [**GetTraceEnableLevel**](/windows/win32/api/evntrace/nf-evntrace-gettraceenablelevel) dans votre implémentation **ControlCallback** si votre fournisseur utilise le niveau activer ou activer les indicateurs.

Un fournisseur peut consigner des événements de trace dans une seule session, mais il n’y a rien à empêcher plusieurs contrôleurs d’activer un seul fournisseur. Pour empêcher un autre contrôleur de rediriger vos événements de trace vers sa session, vous souhaiterez peut-être ajouter une logique à votre implémentation [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) pour comparer les handles de session et ignorer les demandes d’activation d’autres contrôleurs.

Pour consigner des événements, les fournisseurs [classiques](about-event-tracing.md) appellent la fonction [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) . Un événement se compose de la structure d' [**\_ \_ en-tête de suivi d’événement**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) et de toutes les données spécifiques à l’événement qui sont ajoutées à l’en-tête.

L’en-tête doit contenir les informations suivantes :

-   Le membre de **taille** doit contenir le nombre total d’octets à enregistrer pour l’événement (y compris la taille de la structure d' [**\_ \_ en-tête de suivi d’événement**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) et toutes les données spécifiques à l’événement qui sont ajoutées à l’en-tête).
-   Le membre **GUID** doit contenir le GUID de classe de l’événement (ou le membre **GuidPtr** doit contenir un pointeur vers le GUID de la classe).

    **Windows XP et Windows 2000 :** Le GUID de la classe doit avoir été inscrit précédemment à l’aide de la fonction [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) .

-   Le membre **Flags** doit contenir l’indicateur **\_ \_ \_ GUID suivi de l’indicateur WNODE** . Si vous spécifiez le GUID de classe à l’aide du membre **GuidPtr** , ajoutez également l’indicateur **\_ ptr WNODE Flag \_ use \_ GUID \_** .
-   Le membre **Class. type** doit contenir le type d’événement, si vous utilisez MOF pour publier la disposition de vos données d’événement.
-   Le membre **Class. version** doit contenir la version de l’événement, si vous utilisez MOF pour publier la disposition de vos données d’événement. La version est utilisée pour distinguer les révisions des données d’événement. Définissez le numéro de version initiale sur 0.

Si vous écrivez le fournisseur et le consommateur, vous pouvez utiliser une structure pour renseigner les données spécifiques à l’événement qui sont ajoutées à l’en-tête. Toutefois, si vous utilisez MOF pour publier les données spécifiques à l’événement afin que tout consommateur puisse traiter l’événement, vous ne devez pas utiliser une structure pour ajouter les données spécifiques à l’événement à l’en-tête. Cela est dû au fait que le compilateur peut ajouter des octets supplémentaires aux données spécifiques à l’événement pour l’alignement des octets. Étant donné que la définition MOF ne prend pas en compte les octets supplémentaires, le consommateur peut récupérer des données qui ne sont pas valides.

Vous devez soit allouer un bloc de mémoire pour l’événement et copier chaque élément de données d’événement dans la mémoire, soit créer une structure qui comprend un tableau de structures de [**\_ champs MOF**](/windows/win32/api/evntrace/ns-evntrace-mof_field) ; la plupart des applications créent une structure qui comprend un tableau de structures de **\_ champs MOF** . Assurez-vous que l' **en-tête. Size** reflète le nombre réel de structures de **\_ champs MOF** qui sont réellement définies avant l’enregistrement de l’événement. Par exemple, si l’événement contient trois champs de données, définissez **header. Size** sur sizeof (Event \_ trace \_ header) + (sizeof ( \_ Field MOF) \* 3).

Pour plus d’informations sur les événements associés au suivi, consultez [écriture d’événements connexes dans un scénario de bout en bout](writing-related-events-in-an-end-to-end-scenario.md).

L’exemple suivant montre comment appeler la fonction [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) pour consigner des événements. L’exemple fait référence aux événements définis dans la [publication de votre schéma d’événement pour un fournisseur Classic](publishing-your-event-schema-for-a-classic-provider.md).


```C++
#include <windows.h>
#include <stdio.h>
#include <wmistr.h>
#include <evntrace.h>

// GUID that identifies the category of events that the provider can log. 
// The GUID is also used in the event MOF class. 
// Remember to change this GUID if you copy and paste this example.

// {B49D5931-AD85-4070-B1B1-3F81F1532875}
static const GUID MyCategoryGuid = 
{ 0xb49d5931, 0xad85, 0x4070, { 0xb1, 0xb1, 0x3f, 0x81, 0xf1, 0x53, 0x28, 0x75 } };

// GUID that identifies the provider that you are registering.
// The GUID is also used in the provider MOF class. 
// Remember to change this GUID if you copy and paste this example.

// {7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}
static const GUID ProviderGuid = 
{ 0x7c214fb1, 0x9cac, 0x4b8d, { 0xba, 0xed, 0x7b, 0xf4, 0x8b, 0xf6, 0x3b, 0xb3 } };

// Identifies the event type within the MyCategoryGuid category 
// of events to be logged. This is the same value as the EventType 
// qualifier that is defined in the event type MOF class for one of 
// the MyCategoryGuid category of events.

#define MY_EVENT_TYPE 1

// Event passed to TraceEvent

typedef struct _event
{
    EVENT_TRACE_HEADER Header;
    MOF_FIELD Data[MAX_MOF_FIELDS];  // Event-specific data
} MY_EVENT, *PMY_EVENT;

#define MAX_INDICES            3
#define MAX_SIGNATURE_LEN      32
#define EVENT_DATA_FIELDS_CNT  6

// Application data to be traced for Version 1 of the MOF class.

typedef struct _evtdata
{
    LONG Cost;
    DWORD Indices[MAX_INDICES];
    WCHAR Signature[MAX_SIGNATURE_LEN];
    BOOL IsComplete;
    GUID ID;
    DWORD Size;
}EVENT_DATA, *PEVENT_DATA;

// GUID used as the value for EVENT_DATA.ID.

// {25BAEDA9-C81A-4889-8764-184FE56750F2}
static const GUID tempID = 
{ 0x25baeda9, 0xc81a, 0x4889, { 0x87, 0x64, 0x18, 0x4f, 0xe5, 0x67, 0x50, 0xf2 } };

// Global variables to store tracing state information.

TRACEHANDLE g_SessionHandle = 0; // The handle to the session that enabled the provider.
ULONG g_EnableFlags = 0; // Determines which class of events to log.
UCHAR g_EnableLevel = 0; // Determines the severity of events to log.
BOOL g_TraceOn = FALSE;  // Used by the provider to determine whether it should log events.

ULONG WINAPI ControlCallback(WMIDPREQUESTCODE RequestCode, PVOID Context, ULONG* Reserved, PVOID Header);

// For this example to log the event, run the session example
// to enable the provider before running this example.

void wmain(void)
{
    ULONG status = ERROR_SUCCESS;
    EVENT_DATA EventData;
    MY_EVENT MyEvent; 
    TRACEHANDLE RegistrationHandle = 0; 
    TRACE_GUID_REGISTRATION EventClassGuids[] = {
        (LPGUID)&MyCategoryGuid, NULL
        };

    // Register the provider and specify the control callback function
    // that receives the enable/disable notifications.

    status = RegisterTraceGuids(
        (WMIDPREQUEST)ControlCallback,
        NULL,
        (LPGUID)&ProviderGuid,
        sizeof(EventClassGuids)/sizeof(TRACE_GUID_REGISTRATION),
        EventClassGuids,
        NULL,
        NULL,
        &RegistrationHandle
        );

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegisterTraceGuids failed with %lu\n", status);
        goto cleanup;
    }

    // Set the event-specific data.

    EventData.Cost = 32;
    EventData.ID = tempID;
    EventData.Indices[0] = 4;
    EventData.Indices[1] = 5;
    EventData.Indices[2] = 6;
    EventData.IsComplete = TRUE;
    wcscpy_s(EventData.Signature, MAX_SIGNATURE_LEN, L"Signature");
    EventData.Size = 1024;

    // Log the event if the provider is enabled and the session
    // passed a severity level value >= TRACE_LEVEL_ERROR (or zero).
    // If your provider generates more than one class of events, you
    // would also need to check g_EnableFlags.

    if (g_TraceOn && (0 == g_EnableLevel || TRACE_LEVEL_ERROR <= g_EnableLevel))
    {
        // Initialize the event data structure.

        ZeroMemory(&MyEvent, sizeof(MY_EVENT));
        MyEvent.Header.Size = sizeof(EVENT_TRACE_HEADER) + (sizeof(MOF_FIELD) * EVENT_DATA_FIELDS_CNT);
        MyEvent.Header.Flags = WNODE_FLAG_TRACED_GUID | WNODE_FLAG_USE_MOF_PTR;
        MyEvent.Header.Guid = MyCategoryGuid;
        MyEvent.Header.Class.Type = MY_EVENT_TYPE;
        MyEvent.Header.Class.Version = 1;
        MyEvent.Header.Class.Level = g_EnableLevel;

        // Load the event data. You can also use the DEFINE_TRACE_MOF_FIELD
        // macro defined in evntrace.h to set the MOF_FIELD members. For example,
        // DEFINE_TRACE_MOF_FIELD(&EventData.Data[0], &EventData.Cost, sizeof(EventData.Cost), 0);

        MyEvent.Data[0].DataPtr = (ULONG64) &(EventData.Cost);
        MyEvent.Data[0].Length = sizeof(EventData.Cost);
        MyEvent.Data[1].DataPtr = (ULONG64) &(EventData.Indices);
        MyEvent.Data[1].Length = sizeof(EventData.Indices);
        MyEvent.Data[2].DataPtr = (ULONG64) &(EventData.Signature);
        MyEvent.Data[2].Length = (ULONG)(wcslen(EventData.Signature) + 1) * sizeof(WCHAR);
        MyEvent.Data[3].DataPtr = (ULONG64) &(EventData.IsComplete);
        MyEvent.Data[3].Length = sizeof(EventData.IsComplete);
        MyEvent.Data[4].DataPtr = (ULONG64) &(EventData.ID);
        MyEvent.Data[4].Length = sizeof(EventData.ID);
        MyEvent.Data[5].DataPtr = (ULONG64) &(EventData.Size);
        MyEvent.Data[5].Length = sizeof(EventData.Size);

        // Write the event.

        status = TraceEvent(g_SessionHandle, &(MyEvent.Header));

        if (ERROR_SUCCESS != status)
        {
            // Decide how you want to handle failures. Typically, you do not
            // want to terminate the application because you failed to
            // log an event. If the error is a memory failure, you may
            // may want to log a message to the system event log or turn
            // off logging.

            wprintf(L"TraceEvent() event failed with %lu\n", status);
            g_TraceOn = FALSE;
        }
    }

cleanup:

    if (RegistrationHandle)
    {
        UnregisterTraceGuids(RegistrationHandle);
    }
}


// The callback function that receives enable/disable notifications
// from one or more ETW sessions. Because more than one session
// can enable the provider, this example ignores requests from other 
// sessions if it is already enabled.

ULONG WINAPI ControlCallback(
    WMIDPREQUESTCODE RequestCode,
    PVOID Context,
    ULONG* Reserved, 
    PVOID Header
    )
{
    UNREFERENCED_PARAMETER(Context);
    UNREFERENCED_PARAMETER(Reserved);

    ULONG status = ERROR_SUCCESS;
    TRACEHANDLE TempSessionHandle = 0; 

    switch (RequestCode)
    {
        case WMI_ENABLE_EVENTS:  // Enable the provider.
        {
            SetLastError(0);

            // If the provider is already enabled to a provider, ignore 
            // the request. Get the session handle of the enabling session.
            // You need the session handle to call the TraceEvent function.
            // The session could be enabling the provider or it could be
            // updating the level and enable flags.

            TempSessionHandle = GetTraceLoggerHandle(Header);
            if (INVALID_HANDLE_VALUE == (HANDLE)TempSessionHandle)
            {
                wprintf(L"GetTraceLoggerHandle failed. Error code is %lu.\n", status = GetLastError());
                break;
            }

            if (0 == g_SessionHandle)
            {
                g_SessionHandle = TempSessionHandle;
            }
            else if (g_SessionHandle != TempSessionHandle)
            {
                break;
            }

            // Get the severity level of the events that the
            // session wants you to log.

            g_EnableLevel = GetTraceEnableLevel(g_SessionHandle); 
            if (0 == g_EnableLevel)
            {
                // If zero, determine whether the session passed zero
                // or an error occurred.

                if (ERROR_SUCCESS == (status = GetLastError()))
                {
                    // Decide what a zero enable level means to your provider.
                    // For this example, it means log all events.
                    ; 
                }
                else
                {
                    wprintf(L"GetTraceEnableLevel failed with, %lu.\n", status);
                    break;
                } 
            }

            // Get the enable flags that indicate the events that the
            // session wants you to log. The provider determines the
            // flags values. How it articulates the flag values and 
            // meanings to perspective sessions is up to it.

            g_EnableFlags = GetTraceEnableFlags(g_SessionHandle);
            if (0 == g_EnableFlags)
            {
                // If zero, determine whether the session passed zero
                // or an error occurred.

                if (ERROR_SUCCESS == (status = GetLastError()))
                {
                    // Decide what a zero enable flags value means to your provider.
                    ; 
                }
                else
                {
                    wprintf(L"GetTraceEnableFlags failed with, %lu.\n", status);
                    break;
                }
            }

            g_TraceOn = TRUE;
            break;
        }
 
        case WMI_DISABLE_EVENTS:  // Disable the provider.
        {
            // Disable the provider only if the request is coming from the
            // session that enabled the provider.

            TempSessionHandle = GetTraceLoggerHandle(Header);
            if (INVALID_HANDLE_VALUE == (HANDLE)TempSessionHandle)
            {
                wprintf(L"GetTraceLoggerHandle failed. Error code is %lu.\n", status = GetLastError());
                break;
            }

            if (g_SessionHandle == TempSessionHandle)
            {
                g_TraceOn = FALSE;
                g_SessionHandle = 0;
            }
            break;
        }

        default:
        {
            status = ERROR_INVALID_PARAMETER;
            break;
        }
    }

    return status;
}
```



 

 
