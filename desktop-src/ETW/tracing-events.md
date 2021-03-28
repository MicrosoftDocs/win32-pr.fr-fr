---
description: Avant de pouvoir écrire des événements dans une session de trace, vous devez inscrire votre fournisseur.
ms.assetid: 21f62b5d-0a2d-468c-af88-2fab1512f0ec
title: Écriture d’événements MOF (Classic)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3d041e2792540d4a05637bcffdb67e1164a95b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973826"
---
# <a name="writing-mof-classic-events"></a><span data-ttu-id="84e4e-103">Écriture d’événements MOF (Classic)</span><span class="sxs-lookup"><span data-stu-id="84e4e-103">Writing MOF (Classic) Events</span></span>

<span data-ttu-id="84e4e-104">Avant de pouvoir écrire des événements dans une session de trace, vous devez inscrire votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="84e4e-104">Before you can write events to a trace session, you must register your provider.</span></span> <span data-ttu-id="84e4e-105">L’inscription d’un fournisseur indique à ETW que votre fournisseur est prêt à écrire des événements dans une session de suivi.</span><span class="sxs-lookup"><span data-stu-id="84e4e-105">Registering a provider tells ETW that your provider is ready to write events to a trace session.</span></span> <span data-ttu-id="84e4e-106">Un processus peut inscrire jusqu’à 1 024 GUID de fournisseur ; Toutefois, vous devez limiter le nombre de fournisseurs que votre processus inscrit à un ou deux.</span><span class="sxs-lookup"><span data-stu-id="84e4e-106">A process can register up to 1,024 provider GUIDs; however, you should limit the number of providers that your process registers to one or two.</span></span>

<span data-ttu-id="84e4e-107">**Avant Windows Vista :** Il n’existe aucune limite au nombre de fournisseurs qu’un processus peut inscrire.</span><span class="sxs-lookup"><span data-stu-id="84e4e-107">**Prior to Windows Vista:** There is no limit to the number of providers that a process can register.</span></span>

<span data-ttu-id="84e4e-108">Pour inscrire un fournisseur classique, appelez la fonction [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) .</span><span class="sxs-lookup"><span data-stu-id="84e4e-108">To register a classic provider, call the [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function.</span></span> <span data-ttu-id="84e4e-109">La fonction enregistre le GUID du fournisseur, les GUID de classe de trace d’événements et identifie le rappel que ETW appelle lorsqu’un contrôleur active ou désactive le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="84e4e-109">The function registers the provider's GUID, event trace class GUIDs, and identifies the callback that ETW calls when a controller enables or disables the provider.</span></span>

<span data-ttu-id="84e4e-110">Si le fournisseur appelle la fonction [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) pour consigner les événements, vous n’avez pas besoin d’inclure le tableau de GUID de classe (peut être **null**) lors de l’appel de la fonction [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) .</span><span class="sxs-lookup"><span data-stu-id="84e4e-110">If the provider calls the [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) function to log events, you do not need to include the array of class GUIDs (can be **NULL**) when calling the [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function.</span></span> <span data-ttu-id="84e4e-111">Vous devez inclure le tableau uniquement si le fournisseur appelle la fonction [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) pour enregistrer les événements.</span><span class="sxs-lookup"><span data-stu-id="84e4e-111">You only need to include the array if the provider calls the [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) function to log events.</span></span>

<span data-ttu-id="84e4e-112">**Windows XP et windows 2000 :** Vous devez toujours inclure le tableau de GUID de classe (ne peut pas être **null**).</span><span class="sxs-lookup"><span data-stu-id="84e4e-112">**Windows XP and Windows 2000:** You always need to include the array of class GUIDs (cannot be **NULL**).</span></span>

<span data-ttu-id="84e4e-113">Une fois qu’un fournisseur s’est inscrit lui-même et qu’il est activé par le contrôleur, le fournisseur peut consigner des événements dans la session de trace du contrôleur.</span><span class="sxs-lookup"><span data-stu-id="84e4e-113">After a provider registers itself and is enabled by the controller, the provider can log events to the controller's trace session.</span></span>

<span data-ttu-id="84e4e-114">Avant de quitter le fournisseur, appelez la fonction [**UnregisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-unregistertraceguids) pour supprimer l’inscription du fournisseur dans ETW.</span><span class="sxs-lookup"><span data-stu-id="84e4e-114">Before the provider exits, call the [**UnregisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-unregistertraceguids) function to remove the provider's registration from ETW.</span></span> <span data-ttu-id="84e4e-115">La fonction [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) retourne le handle d’inscription que vous transmettez à la fonction **UnregisterTraceGuids** .</span><span class="sxs-lookup"><span data-stu-id="84e4e-115">The [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function returns the registration handle that you pass to the **UnregisterTraceGuids** function.</span></span>

<span data-ttu-id="84e4e-116">Si votre fournisseur enregistre des événements dans la session de journalisation globale uniquement, il n’est pas nécessaire d’inscrire votre fournisseur avec ETW, car le contrôleur d’enregistreur global n’active pas ou ne désactive pas les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="84e4e-116">If your provider logs events to the Global Logger session only, you do not have to register your provider with ETW because the Global Logger controller does not enable or disable providers.</span></span> <span data-ttu-id="84e4e-117">Pour plus d’informations, consultez [configuration et démarrage de la session d’enregistreur](configuring-and-starting-the-global-logger-session.md)d’événements globale.</span><span class="sxs-lookup"><span data-stu-id="84e4e-117">For details, see [Configuring and Starting the Global Logger Session](configuring-and-starting-the-global-logger-session.md).</span></span>

<span data-ttu-id="84e4e-118">Tous les fournisseurs [classiques](about-event-tracing.md) (à l’exception de ceux qui tracent des événements dans la session de journalisation globale) doivent implémenter la fonction [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) .</span><span class="sxs-lookup"><span data-stu-id="84e4e-118">All [classic](about-event-tracing.md) providers (except those that trace events to the Global Logger session) must implement the [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) function.</span></span> <span data-ttu-id="84e4e-119">Le fournisseur utilise les informations du rappel pour déterminer s’il est activé ou désactivé et quels événements il doit écrire.</span><span class="sxs-lookup"><span data-stu-id="84e4e-119">The provider uses the information in the callback to determine if it is enabled or disabled and which events it should write.</span></span>

<span data-ttu-id="84e4e-120">Le fournisseur spécifie le nom de la fonction de rappel lorsqu’il appelle la fonction [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) pour s’inscrire.</span><span class="sxs-lookup"><span data-stu-id="84e4e-120">The provider specifies the name of the callback function when it calls the [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function to register itself.</span></span> <span data-ttu-id="84e4e-121">ETW appelle la fonction de rappel lorsque le contrôleur appelle la fonction [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) pour activer ou désactiver le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="84e4e-121">ETW calls the callback function when the controller calls the [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) function to enable or disable the provider.</span></span>

<span data-ttu-id="84e4e-122">Dans votre implémentation de [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) , vous devez appeler la fonction [**GetTraceLoggerHandle**](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle) pour récupérer le handle de session. vous utilisez le descripteur de session lors de l’appel de la fonction [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) .</span><span class="sxs-lookup"><span data-stu-id="84e4e-122">In your [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) implementation, you must call the [**GetTraceLoggerHandle**](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle) function to retrieve the session handle; you use the session handle when calling the [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) function.</span></span> <span data-ttu-id="84e4e-123">Il vous suffit d’appeler la fonction [**GetTraceEnableFlags**](/windows/win32/api/evntrace/nf-evntrace-gettraceenableflags) ou la fonction [**GetTraceEnableLevel**](/windows/win32/api/evntrace/nf-evntrace-gettraceenablelevel) dans votre implémentation **ControlCallback** si votre fournisseur utilise le niveau activer ou activer les indicateurs.</span><span class="sxs-lookup"><span data-stu-id="84e4e-123">You only need to call the [**GetTraceEnableFlags**](/windows/win32/api/evntrace/nf-evntrace-gettraceenableflags) function or the [**GetTraceEnableLevel**](/windows/win32/api/evntrace/nf-evntrace-gettraceenablelevel) function in your **ControlCallback** implementation if your provider uses the enable level or enable flags.</span></span>

<span data-ttu-id="84e4e-124">Un fournisseur peut consigner des événements de trace dans une seule session, mais il n’y a rien à empêcher plusieurs contrôleurs d’activer un seul fournisseur.</span><span class="sxs-lookup"><span data-stu-id="84e4e-124">A provider can log trace events to only one session, but there is nothing to prevent multiple controllers from enabling a single provider.</span></span> <span data-ttu-id="84e4e-125">Pour empêcher un autre contrôleur de rediriger vos événements de trace vers sa session, vous souhaiterez peut-être ajouter une logique à votre implémentation [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) pour comparer les handles de session et ignorer les demandes d’activation d’autres contrôleurs.</span><span class="sxs-lookup"><span data-stu-id="84e4e-125">To prevent another controller from redirecting your trace events to its session, you may want to add logic to your [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) implementation to compare session handles and ignore enable requests from other controllers.</span></span>

<span data-ttu-id="84e4e-126">Pour consigner des événements, les fournisseurs [classiques](about-event-tracing.md) appellent la fonction [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) .</span><span class="sxs-lookup"><span data-stu-id="84e4e-126">To log events, [classic](about-event-tracing.md) providers call the [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) function.</span></span> <span data-ttu-id="84e4e-127">Un événement se compose de la structure d' [**\_ \_ en-tête de suivi d’événement**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) et de toutes les données spécifiques à l’événement qui sont ajoutées à l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="84e4e-127">An event consists of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure and any event-specific data that is appended to the header.</span></span>

<span data-ttu-id="84e4e-128">L’en-tête doit contenir les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="84e4e-128">The header must contain the following information:</span></span>

-   <span data-ttu-id="84e4e-129">Le membre de **taille** doit contenir le nombre total d’octets à enregistrer pour l’événement (y compris la taille de la structure d' [**\_ \_ en-tête de suivi d’événement**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) et toutes les données spécifiques à l’événement qui sont ajoutées à l’en-tête).</span><span class="sxs-lookup"><span data-stu-id="84e4e-129">The **Size** member must contain the total number of bytes to be recorded for the event (including the size of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure and of any event-specific data that is appended to the header).</span></span>
-   <span data-ttu-id="84e4e-130">Le membre **GUID** doit contenir le GUID de classe de l’événement (ou le membre **GuidPtr** doit contenir un pointeur vers le GUID de la classe).</span><span class="sxs-lookup"><span data-stu-id="84e4e-130">The **Guid** member must contain the class GUID of the event (or the **GuidPtr** member must contain a pointer to the class GUID).</span></span>

    <span data-ttu-id="84e4e-131">**Windows XP et windows 2000 :** Le GUID de la classe doit avoir été inscrit précédemment à l’aide de la fonction [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) .</span><span class="sxs-lookup"><span data-stu-id="84e4e-131">**Windows XP and Windows 2000:** The class GUID must have been registered previously using the [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function.</span></span>

-   <span data-ttu-id="84e4e-132">Le membre **Flags** doit contenir l’indicateur **\_ \_ \_ GUID suivi de l’indicateur WNODE** .</span><span class="sxs-lookup"><span data-stu-id="84e4e-132">The **Flags** member must contain the **WNODE\_FLAG\_TRACED\_GUID** flag.</span></span> <span data-ttu-id="84e4e-133">Si vous spécifiez le GUID de classe à l’aide du membre **GuidPtr** , ajoutez également l’indicateur **\_ ptr WNODE Flag \_ use \_ GUID \_** .</span><span class="sxs-lookup"><span data-stu-id="84e4e-133">If you specify the class GUID using the **GuidPtr** member, also add the **WNODE\_FLAG\_USE\_GUID\_PTR** flag.</span></span>
-   <span data-ttu-id="84e4e-134">Le membre **Class. type** doit contenir le type d’événement, si vous utilisez MOF pour publier la disposition de vos données d’événement.</span><span class="sxs-lookup"><span data-stu-id="84e4e-134">The **Class.Type** member must contain the event type, if you use MOF to publish the layout of your event data.</span></span>
-   <span data-ttu-id="84e4e-135">Le membre **Class. version** doit contenir la version de l’événement, si vous utilisez MOF pour publier la disposition de vos données d’événement.</span><span class="sxs-lookup"><span data-stu-id="84e4e-135">The **Class.Version** member must contain the event version, if you use MOF to publish the layout of your event data.</span></span> <span data-ttu-id="84e4e-136">La version est utilisée pour distinguer les révisions des données d’événement.</span><span class="sxs-lookup"><span data-stu-id="84e4e-136">The version is used to distinguish between revisions to the event data.</span></span> <span data-ttu-id="84e4e-137">Définissez le numéro de version initiale sur 0.</span><span class="sxs-lookup"><span data-stu-id="84e4e-137">Set the initial version number to 0.</span></span>

<span data-ttu-id="84e4e-138">Si vous écrivez le fournisseur et le consommateur, vous pouvez utiliser une structure pour renseigner les données spécifiques à l’événement qui sont ajoutées à l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="84e4e-138">If you write both the provider and the consumer, you can use a structure to populate the event-specific data that is appended to the header.</span></span> <span data-ttu-id="84e4e-139">Toutefois, si vous utilisez MOF pour publier les données spécifiques à l’événement afin que tout consommateur puisse traiter l’événement, vous ne devez pas utiliser une structure pour ajouter les données spécifiques à l’événement à l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="84e4e-139">However, if you use MOF to publish the event-specific data so that any consumer can process the event, you should not use a structure to append the event-specific data to the header.</span></span> <span data-ttu-id="84e4e-140">Cela est dû au fait que le compilateur peut ajouter des octets supplémentaires aux données spécifiques à l’événement pour l’alignement des octets.</span><span class="sxs-lookup"><span data-stu-id="84e4e-140">This is because the compiler may add extra bytes to the event-specific data for byte alignment purposes.</span></span> <span data-ttu-id="84e4e-141">Étant donné que la définition MOF ne prend pas en compte les octets supplémentaires, le consommateur peut récupérer des données qui ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="84e4e-141">Because the MOF definition does not account for the extra bytes, the consumer may retrieve data that is not valid.</span></span>

<span data-ttu-id="84e4e-142">Vous devez soit allouer un bloc de mémoire pour l’événement et copier chaque élément de données d’événement dans la mémoire, soit créer une structure qui comprend un tableau de structures de [**\_ champs MOF**](/windows/win32/api/evntrace/ns-evntrace-mof_field) ; la plupart des applications créent une structure qui comprend un tableau de structures de **\_ champs MOF** .</span><span class="sxs-lookup"><span data-stu-id="84e4e-142">You should either allocate a block of memory for the event and copy each event data item to the memory, or create a structure that includes an array of [**MOF\_FIELD**](/windows/win32/api/evntrace/ns-evntrace-mof_field) structures; most applications will create a structure that includes an array of **MOF\_FIELD** structures.</span></span> <span data-ttu-id="84e4e-143">Assurez-vous que l' **en-tête. Size** reflète le nombre réel de structures de **\_ champs MOF** qui sont réellement définies avant l’enregistrement de l’événement.</span><span class="sxs-lookup"><span data-stu-id="84e4e-143">Make sure that **Header.Size** reflects the actual number of **MOF\_FIELD** structures that are actually set before logging the event.</span></span> <span data-ttu-id="84e4e-144">Par exemple, si l’événement contient trois champs de données, définissez **header. Size** sur sizeof (Event \_ trace \_ header) + (sizeof ( \_ Field MOF) \* 3).</span><span class="sxs-lookup"><span data-stu-id="84e4e-144">For example, if the event contains three data fields, set **Header.Size** to sizeof(EVENT\_TRACE\_HEADER) + (sizeof(MOF\_FIELD) \* 3).</span></span>

<span data-ttu-id="84e4e-145">Pour plus d’informations sur les événements associés au suivi, consultez [écriture d’événements connexes dans un scénario de bout en bout](writing-related-events-in-an-end-to-end-scenario.md).</span><span class="sxs-lookup"><span data-stu-id="84e4e-145">For information on tracing related events, see [Writing Related Events in an End-to-End Scenario](writing-related-events-in-an-end-to-end-scenario.md).</span></span>

<span data-ttu-id="84e4e-146">L’exemple suivant montre comment appeler la fonction [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) pour consigner des événements.</span><span class="sxs-lookup"><span data-stu-id="84e4e-146">The following example shows how to call the [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) function to log events.</span></span> <span data-ttu-id="84e4e-147">L’exemple fait référence aux événements définis dans la [publication de votre schéma d’événement pour un fournisseur Classic](publishing-your-event-schema-for-a-classic-provider.md).</span><span class="sxs-lookup"><span data-stu-id="84e4e-147">The example references the events defined in [Publishing Your Event Schema for a Classic Provider](publishing-your-event-schema-for-a-classic-provider.md).</span></span>


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



 

 
