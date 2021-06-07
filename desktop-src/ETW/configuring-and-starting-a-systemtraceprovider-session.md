---
description: SystemTraceProvider est un fournisseur de noyaux avec un ensemble prédéfini d’événements de noyau pris en charge sur Windows 7, Windows Server 2008 R2 et versions ultérieures.
ms.assetid: 6808EC45-C8C3-45D7-9E4C-337F6A4CF9C8
title: Configuration et démarrage d’une session SystemTraceProvider
ms.topic: article
ms.date: 06/02/2021
ms.openlocfilehash: 66e9d672a7c8e6358c2a92e7661e0d4e2a5878ab
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386739"
---
# <a name="configuring-and-starting-a-systemtraceprovider-session"></a><span data-ttu-id="a1810-103">Configuration et démarrage d’une session SystemTraceProvider</span><span class="sxs-lookup"><span data-stu-id="a1810-103">Configuring and Starting a SystemTraceProvider Session</span></span>

<span data-ttu-id="a1810-104">SystemTraceProvider est un fournisseur de noyaux avec un ensemble prédéfini d’événements de noyau pris en charge sur Windows 7, Windows Server 2008 R2 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a1810-104">The SystemTraceProvider is a kernel provider with a predefined sets of kernel events supported on Windows 7, Windows Server 2008 R2, and later.</span></span> <span data-ttu-id="a1810-105">Sur Windows 7 et Windows Server 2008 R2, SystemTraceProvider ne peut être utilisé que pour la session de journalisation du noyau NT.</span><span class="sxs-lookup"><span data-stu-id="a1810-105">On Windows 7 and Windows Server 2008 R2, the SystemTraceProvider could only be used for the NT Kernel Logger session.</span></span>

<span data-ttu-id="a1810-106">Sur Windows 8, Windows Server 2012 et versions ultérieures, les SystemTraceProvider peuvent être multiplexés pour jusqu’à 8 sessions d’enregistreur d’événements.</span><span class="sxs-lookup"><span data-stu-id="a1810-106">On Windows 8, Windows Server 2012, and later, the SystemTraceProvider can be multiplexed for up to 8 logger sessions.</span></span> <span data-ttu-id="a1810-107">Les deux premiers emplacements pour les sessions de journalisation sont réservés pour l’enregistreur d’événements de noyau NT et le journal de contexte de noyau circulaire.</span><span class="sxs-lookup"><span data-stu-id="a1810-107">The first two slots for logger sessions are reserved for the NT Kernel Logger and the Circular Kernel Context Logger .</span></span>

<span data-ttu-id="a1810-108">Pour plus d’informations sur l’utilisation de la session de journalisation du noyau NT en tant que fournisseur de trace, consultez [configuration et démarrage de la session de journalisation du noyau NT](configuring-and-starting-the-nt-kernel-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="a1810-108">For more information on using the NT Kernel Logger session as a trace provider, see [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span></span>

<span data-ttu-id="a1810-109">Dans le kit de développement logiciel (SDK) Windows 10 version 20348 et versions ultérieures, les SystemTraceProvider peuvent être configurés via des fournisseurs système distincts, qui peuvent être contrôlés avec [EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) comme des fournisseurs d’événements suivi d’v nements pour Windows standard.</span><span class="sxs-lookup"><span data-stu-id="a1810-109">On Windows 10 SDK build 20348 and later, the SystemTraceProvider can be configured via separate System Providers, which can be controlled with [EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) like standard Event Tracing for Windows event providers.</span></span> <span data-ttu-id="a1810-110">Pour obtenir la liste complète des fournisseurs système, des mots clés et des groupes et indicateurs hérités correspondants, consultez [fournisseurs système](system-providers.md) .</span><span class="sxs-lookup"><span data-stu-id="a1810-110">For a full list of system providers, keywords, and corresponding legacy flags and groups, see [System Providers](system-providers.md)</span></span>

## <a name="enable-a-systemtraceprovider-session"></a><span data-ttu-id="a1810-111">Activer une session SystemTraceProvider</span><span class="sxs-lookup"><span data-stu-id="a1810-111">Enable a SystemTraceProvider session</span></span>

<span data-ttu-id="a1810-112">Pour permettre à SystemTraceProvider de démarrer une session autre que l’enregistreur d’événements de noyau NT, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="a1810-112">To enable the SystemTraceProvider to start a session other than the NT Kernel Logger, execute the following command:</span></span>

<span data-ttu-id="a1810-113">**tracelog-Start MySession-f c : \\ Kernel1. etl-EFLAG Proc \_ thread + Loader + CSWITCH**</span><span class="sxs-lookup"><span data-stu-id="a1810-113">**tracelog -start MySession -f c:\\Kernel1.etl -eflag PROC\_THREAD+LOADER+CSWITCH**</span></span>

<span data-ttu-id="a1810-114">Pour activer par programmation le SystemTraceProvider pour démarrer une session autre que l’enregistreur d’événements de noyau NT, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="a1810-114">To programmatically enable the SystemTraceProvider to start a session other than the NT Kernel Logger, use the following steps.</span></span>

-   <span data-ttu-id="a1810-115">Définissez un nom de journal privé.</span><span class="sxs-lookup"><span data-stu-id="a1810-115">Define a private logger name.</span></span>

    <span data-ttu-id="a1810-116">**\#définir le nom d’enregistreur d’événements privé \_ \_ L "session de trace privée"**</span><span class="sxs-lookup"><span data-stu-id="a1810-116">**\#define PRIVATE\_LOGGER\_NAME L”Some Private Trace Session”**</span></span>

-   <span data-ttu-id="a1810-117">Au niveau du contrôleur, définissez les membres suivants de la structure des [**\_ \_ Propriétés**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) de la trace d’événements.</span><span class="sxs-lookup"><span data-stu-id="a1810-117">At the controller, set the following members of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure.</span></span>

    <span data-ttu-id="a1810-118">Définissez **LogFileMode** sur **Event \_ trace \_ système \_ logger \_ mode**.</span><span class="sxs-lookup"><span data-stu-id="a1810-118">Set **LogFileMode** to **EVENT\_TRACE\_SYSTEM\_LOGGER\_MODE**.</span></span>

    <span data-ttu-id="a1810-119">Définissez **LoggerName** sur Logger privé, au lieu **de \_ \_ nom d’enregistreur de noyau**.</span><span class="sxs-lookup"><span data-stu-id="a1810-119">Set **LoggerName** to private logger, instead of **KERNEL\_LOGGER\_NAME**.</span></span>

    <span data-ttu-id="a1810-120">Assurez-vous que le membre **Wnode. Guid** de la structure des [**\_ \_ Propriétés de trace d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) n’a pas la valeur **SystemTraceControlGuid**.</span><span class="sxs-lookup"><span data-stu-id="a1810-120">Make sure the **Wnode.Guid** member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure is not set to **SystemTraceControlGuid**.</span></span> <span data-ttu-id="a1810-121">Vous devez assigner un nouveau **GUID** à ce membre.</span><span class="sxs-lookup"><span data-stu-id="a1810-121">You must assign a new **GUID** to this member.</span></span>

-   <span data-ttu-id="a1810-122">Au niveau du consommateur, définissez le membre **LoggerName** de la structure du [**\_ \_ fichier journal de suivi d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) sur cet enregistreur d’événements privé.</span><span class="sxs-lookup"><span data-stu-id="a1810-122">At the consumer, set the **LoggerName** member of the [**EVENT\_TRACE\_LOGFILE**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) structure to this private logger.</span></span>

> [!Note]  
> <span data-ttu-id="a1810-123">Si vous souhaitez qu’un non-administrateur ou un processus non-TCB puisse démarrer une session de suivi de profilage à l’aide de SystemTraceProvider pour le compte d’applications tierces, vous devez accorder le privilège de profil utilisateur, puis ajouter cet utilisateur au **GUID** de session (créé pour la session de journalisation) et au **GUID** du fournisseur de trace système pour activer le fournisseur de trace système.</span><span class="sxs-lookup"><span data-stu-id="a1810-123">If you want a non-administrators or a non-TCB process to be able to start a profiling trace session using the SystemTraceProvider on behalf of third party applications, then you need to grant the user profile privilege and then add this user to both the session **GUID** (created for the logger session) and the system trace provider **GUID** to enable the system trace provider.</span></span> <span data-ttu-id="a1810-124">Pour plus d’informations, consultez la fonction [**EventAccessControl**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol) .</span><span class="sxs-lookup"><span data-stu-id="a1810-124">For more information, see the [**EventAccessControl**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol) function.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a1810-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a1810-125">Related topics</span></span>

[<span data-ttu-id="a1810-126">Configuration et démarrage d’une session de journalisation privée</span><span class="sxs-lookup"><span data-stu-id="a1810-126">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)

[<span data-ttu-id="a1810-127">Configuration et démarrage d’une session de journalisation automatique</span><span class="sxs-lookup"><span data-stu-id="a1810-127">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)

[<span data-ttu-id="a1810-128">Configuration et démarrage d’une session de suivi d’événements</span><span class="sxs-lookup"><span data-stu-id="a1810-128">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)

[<span data-ttu-id="a1810-129">Configuration et démarrage de la session de journalisation du noyau NT</span><span class="sxs-lookup"><span data-stu-id="a1810-129">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)

[<span data-ttu-id="a1810-130">Fournisseurs système</span><span class="sxs-lookup"><span data-stu-id="a1810-130">System Providers</span></span>](system-providers.md)

[<span data-ttu-id="a1810-131">Mise à jour d’une session de suivi d’événements</span><span class="sxs-lookup"><span data-stu-id="a1810-131">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)

 

 
