---
description: Une session de suivi d’événements privée est une session de suivi d’événements en mode utilisateur qui s’exécute dans le même processus que ses fournisseurs de suivi d’événements&\# 8212 ; la session privée et les fournisseurs qu’elle active doivent tous être dans le même processus.
ms.assetid: fb6a3899-194e-4cb7-b9e5-a7ff85fb7891
title: Configuration et démarrage d’une session de journalisation privée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ef13728bfb3516197ab153cf90b301d5930ff2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485280"
---
# <a name="configuring-and-starting-a-private-logger-session"></a><span data-ttu-id="3f8aa-103">Configuration et démarrage d’une session de journalisation privée</span><span class="sxs-lookup"><span data-stu-id="3f8aa-103">Configuring and Starting a Private Logger Session</span></span>

<span data-ttu-id="3f8aa-104">Une session de suivi d’événements privée est une session de suivi d’événements en mode utilisateur qui s’exécute dans le même processus que ses fournisseurs de suivi d’événements : la session privée et les fournisseurs qu’elle active doivent tous être dans le même processus.</span><span class="sxs-lookup"><span data-stu-id="3f8aa-104">A private event tracing session is a user-mode event tracing session that runs in the same process as its event trace providers—the private session and the providers that it enables must all be in the same process.</span></span> <span data-ttu-id="3f8aa-105">L’avantage de l’utilisation d’une session privée est que la session privée ne compte pas au maximum de 64 sessions de suivi d’événements s’exécutant simultanément.</span><span class="sxs-lookup"><span data-stu-id="3f8aa-105">The benefit of using a private session is that the private session does not count against the maximum of 64 event tracing sessions executing simultaneously.</span></span>

<span data-ttu-id="3f8aa-106">La configuration et le démarrage d’une session privée sont similaires au démarrage d’une session de suivi d’événements normale.</span><span class="sxs-lookup"><span data-stu-id="3f8aa-106">Configuring and starting a private session is similar to starting a normal event trace session.</span></span> <span data-ttu-id="3f8aa-107">La différence réside dans le fait que le membre **Wnode. Guid** de la structure des [**\_ \_ Propriétés de trace d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) doit contenir le **GUID** du fournisseur, et non la session, et que le fournisseur doit déjà avoir inscrit le GUID.</span><span class="sxs-lookup"><span data-stu-id="3f8aa-107">The difference is that **Wnode.Guid** member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure must contain the **GUID** of the provider, not the session, and the provider must have already registered the GUID.</span></span> <span data-ttu-id="3f8aa-108">Notez que si vous définissez également le \_ suivi \_ d’événement privé \_ en mode de \_ journalisation de procédure, vous pouvez utiliser un **GUID** différent pour la session et le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3f8aa-108">Note that if you also set the EVENT\_TRACE\_PRIVATE\_IN\_PROC logging mode, you can use a different **GUID** for the session and provider.</span></span> <span data-ttu-id="3f8aa-109">Pour plus d’informations sur le démarrage d’une session de suivi d’événements normale, consultez [configuration et démarrage d’une session de suivi d’événements](configuring-and-starting-an-event-tracing-session.md).</span><span class="sxs-lookup"><span data-stu-id="3f8aa-109">For details on starting a normal event trace session, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

<span data-ttu-id="3f8aa-110">Notez que vous ne pouvez pas démarrer, arrêter ou vider une session de trace privée à partir de DllMain ; vous devez le faire dans les routines d’initialisation et de finalisation de la DLL.</span><span class="sxs-lookup"><span data-stu-id="3f8aa-110">Note that you cannot start, stop, or flush a private trace session from DllMain; you should do so in the initialization and finalization routines of the DLL.</span></span>

<span data-ttu-id="3f8aa-111">Des Windows 8.1 à Windows 10, version 1607, la charge utile d’événement, la portée et les filtres de parcours de pile peuvent être utilisés par la fonction [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) et les structures de [**\_ \_ descripteur de filtre d’événement**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) et de [**\_ \_ paramètres de trace**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) pour filtrer sur des conditions spécifiques dans une session de journalisation.</span><span class="sxs-lookup"><span data-stu-id="3f8aa-111">From Windows 8.1 to Windows 10, version 1607, event payload, scope, and stack walk filters can be used by the [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) function and the [**ENABLE\_TRACE\_PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) and [**EVENT\_FILTER\_DESCRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) structures to filter on specific conditions in a logger session.</span></span> <span data-ttu-id="3f8aa-112">Pour plus d’informations sur les filtres de charge utile d’événement, consultez les fonctions [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)et [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) , ainsi que les structures de prédicat **activer les \_ \_ paramètres de trace**, **\_ \_ descripteur de filtre d’événement** et de [**\_ filtre \_ de charge utile**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) .</span><span class="sxs-lookup"><span data-stu-id="3f8aa-112">For more information on event payload filters, see the [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter), and [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) functions and the **ENABLE\_TRACE\_PARAMETERS**, **EVENT\_FILTER\_DESCRIPTOR**, and [**PAYLOAD\_FILTER\_PREDICATE**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) structures.</span></span>

<span data-ttu-id="3f8aa-113">À compter de Windows 10, version 1703, les utilisateurs à faibles privilèges peuvent désormais démarrer une session d’enregistreur d’événements privée dans les processus qu’ils ont démarré.</span><span class="sxs-lookup"><span data-stu-id="3f8aa-113">Starting with Windows 10, version 1703, low privilege users can now start a private logger session in processes they started.</span></span> <span data-ttu-id="3f8aa-114">Le fournisseur n’a plus besoin d’être inscrit avant l’activation ou le démarrage de la session privée, ce qui signifie que le fournisseur est « pré-activé », de la même façon que les fournisseurs de session non privés.</span><span class="sxs-lookup"><span data-stu-id="3f8aa-114">The provider no longer needs to be registered prior to enabling or starting the private session, meaning the provider is "pre-enabled" similar to how non-private session providers are.</span></span> <span data-ttu-id="3f8aa-115">Il existe une limite de 8 enregistreurs d’événements privés au niveau du système pour un processus individuel.</span><span class="sxs-lookup"><span data-stu-id="3f8aa-115">There is a limit of 8 system wide private loggers to an individual process.</span></span> <span data-ttu-id="3f8aa-116">Pour des performances accrues dans les scénarios inter-processus, il est recommandé d’utiliser le filtrage pour les API de session (notamment [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea), [**QueryTrace**](/windows/win32/api/evntrace/nf-evntrace-querytrace), [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)et [**StopTrace**](/windows/win32/api/evntrace/nf-evntrace-stoptrace)) lors du démarrage d’un enregistreur d’événements privés du système.</span><span class="sxs-lookup"><span data-stu-id="3f8aa-116">For increased performance in cross process scenarios, it's recommended to use filtering for session APIs (including [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea), [**QueryTrace**](/windows/win32/api/evntrace/nf-evntrace-querytrace), [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea), and [**StopTrace**](/windows/win32/api/evntrace/nf-evntrace-stoptrace)) when starting a system wide private logger.</span></span> <span data-ttu-id="3f8aa-117">Notez que les mêmes filtres doivent être passés à toutes les API de session.</span><span class="sxs-lookup"><span data-stu-id="3f8aa-117">Note that the same filters should be passed to all session APIs.</span></span> <span data-ttu-id="3f8aa-118">Pour plus d’informations sur les filtres, consultez [**Event \_ trace \_ Properties \_ v2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2).</span><span class="sxs-lookup"><span data-stu-id="3f8aa-118">For more information about filters, see [**EVENT\_TRACE\_PROPERTIES\_V2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2).</span></span>

<span data-ttu-id="3f8aa-119">Pour plus d’informations sur le démarrage d’une session de suivi d’événements, consultez [configuration et démarrage d’une session de suivi d’événements](configuring-and-starting-an-event-tracing-session.md).</span><span class="sxs-lookup"><span data-stu-id="3f8aa-119">For details on starting an event tracing session, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

<span data-ttu-id="3f8aa-120">Pour plus d’informations sur le démarrage d’une session de journal de noyau NT, consultez [configuration et démarrage de la session de journalisation du noyau NT](configuring-and-starting-the-nt-kernel-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="3f8aa-120">For details on starting an NT Kernel Logger session, see [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span></span>

<span data-ttu-id="3f8aa-121">Pour plus d’informations sur le démarrage d’une session de journalisation globale, consultez [configuration et démarrage d’une session de journalisation globale](configuring-and-starting-the-global-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="3f8aa-121">For details on starting a Global Logger session, see [Configuring and Starting a Global Logger Session](configuring-and-starting-the-global-logger-session.md).</span></span>

<span data-ttu-id="3f8aa-122">Pour plus d’informations sur le démarrage d’une session de journalisation automatique, consultez [configuration et démarrage d’une session de journalisation](configuring-and-starting-an-autologger-session.md)automatique.</span><span class="sxs-lookup"><span data-stu-id="3f8aa-122">For details on starting an AutoLogger session, see [Configuring and Starting an AutoLogger Session](configuring-and-starting-an-autologger-session.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f8aa-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3f8aa-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f8aa-124">Configuration et démarrage d’une session SystemTraceProvider</span><span class="sxs-lookup"><span data-stu-id="3f8aa-124">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[<span data-ttu-id="3f8aa-125">Configuration et démarrage d’une session de journalisation automatique</span><span class="sxs-lookup"><span data-stu-id="3f8aa-125">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[<span data-ttu-id="3f8aa-126">Configuration et démarrage d’une session de suivi d’événements</span><span class="sxs-lookup"><span data-stu-id="3f8aa-126">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="3f8aa-127">Configuration et démarrage de la session de journalisation du noyau NT</span><span class="sxs-lookup"><span data-stu-id="3f8aa-127">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[<span data-ttu-id="3f8aa-128">**EnableTraceEx2**</span><span class="sxs-lookup"><span data-stu-id="3f8aa-128">**EnableTraceEx2**</span></span>](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[<span data-ttu-id="3f8aa-129">**ACTIVER \_ les \_ paramètres de trace**</span><span class="sxs-lookup"><span data-stu-id="3f8aa-129">**ENABLE\_TRACE\_PARAMETERS**</span></span>](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[<span data-ttu-id="3f8aa-130">**Propriétés de la trace d’événements \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3f8aa-130">**EVENT\_TRACE\_PROPERTIES**</span></span>](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[<span data-ttu-id="3f8aa-131">**Propriétés de la trace d’événements \_ \_ \_ v2**</span><span class="sxs-lookup"><span data-stu-id="3f8aa-131">**EVENT\_TRACE\_PROPERTIES\_V2**</span></span>](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2)
</dt> <dt>

[<span data-ttu-id="3f8aa-132">**descripteur de filtre d’événements \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3f8aa-132">**EVENT\_FILTER\_DESCRIPTOR**</span></span>](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[<span data-ttu-id="3f8aa-133">**\_prédicat de filtre de charge utile \_**</span><span class="sxs-lookup"><span data-stu-id="3f8aa-133">**PAYLOAD\_FILTER\_PREDICATE**</span></span>](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[<span data-ttu-id="3f8aa-134">**TdhAggregatePayloadFilters**</span><span class="sxs-lookup"><span data-stu-id="3f8aa-134">**TdhAggregatePayloadFilters**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[<span data-ttu-id="3f8aa-135">**TdhCreatePayloadFilter**</span><span class="sxs-lookup"><span data-stu-id="3f8aa-135">**TdhCreatePayloadFilter**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[<span data-ttu-id="3f8aa-136">Mise à jour d’une session de suivi d’événements</span><span class="sxs-lookup"><span data-stu-id="3f8aa-136">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
