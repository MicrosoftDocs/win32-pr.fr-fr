---
description: La \_ structure d’en-tête WNODE est un membre de la structure des propriétés de trace d’événements \_ \_ .
ms.assetid: 862a8f46-a326-48c6-92b7-8bb667837bb7
title: Structure WNODE_HEADER (Wmistr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WNODE_HEADER
api_type:
- HeaderDef
api_location:
- Wmistr.h
ms.openlocfilehash: 6a2ed615d2b67cbd47a817234a14b7cf1221f601
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "104982834"
---
# <a name="wnode_header-structure"></a><span data-ttu-id="fa94a-103">\_Structure d’en-tête WNODE</span><span class="sxs-lookup"><span data-stu-id="fa94a-103">WNODE\_HEADER structure</span></span>

<span data-ttu-id="fa94a-104">La structure d' **\_ en-tête WNODE** est un membre de la structure des [**\_ \_ Propriétés de trace d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) .</span><span class="sxs-lookup"><span data-stu-id="fa94a-104">The **WNODE\_HEADER** structure is a member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa94a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa94a-105">Syntax</span></span>


```C++
typedef struct _WNODE_HEADER {
  ULONG BufferSize;
  ULONG ProviderId;
  union {
    ULONG64 HistoricalContext;
    struct {
      ULONG Version;
      ULONG Linkage;
    };
  };
  union {
    HANDLE        KernelHandle;
    LARGE_INTEGER TimeStamp;
  };
  GUID  Guid;
  ULONG ClientContext;
  ULONG Flags;
} WNODE_HEADER, *PWNODE_HEADER;
```



## <a name="members"></a><span data-ttu-id="fa94a-106">Membres</span><span class="sxs-lookup"><span data-stu-id="fa94a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fa94a-107">**BufferSize**</span><span class="sxs-lookup"><span data-stu-id="fa94a-107">**BufferSize**</span></span>
</dt> <dd>

<span data-ttu-id="fa94a-108">Taille totale de la mémoire allouée, en octets, pour les propriétés de session de suivi d’événements.</span><span class="sxs-lookup"><span data-stu-id="fa94a-108">Total size of memory allocated, in bytes, for the event tracing session properties.</span></span> <span data-ttu-id="fa94a-109">La taille de la mémoire doit inclure la place de la structure des [**\_ \_ Propriétés**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) de la trace d’événements plus la chaîne de nom de session et la chaîne de nom de fichier journal qui suivent la structure en mémoire.</span><span class="sxs-lookup"><span data-stu-id="fa94a-109">The size of memory must include the room for the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure plus the session name string and log file name string that follow the structure in memory.</span></span>

</dd> <dt>

<span data-ttu-id="fa94a-110">**ProviderId**</span><span class="sxs-lookup"><span data-stu-id="fa94a-110">**ProviderId**</span></span>
</dt> <dd>

<span data-ttu-id="fa94a-111">Réservé à un usage interne.</span><span class="sxs-lookup"><span data-stu-id="fa94a-111">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="fa94a-112">**HistoricalContext**</span><span class="sxs-lookup"><span data-stu-id="fa94a-112">**HistoricalContext**</span></span>
</dt> <dd>

<span data-ttu-id="fa94a-113">Lors de la sortie, handle vers la session de suivi d’événements.</span><span class="sxs-lookup"><span data-stu-id="fa94a-113">On output, the handle to the event tracing session.</span></span>

</dd> <dt>

<span data-ttu-id="fa94a-114">**Version**</span><span class="sxs-lookup"><span data-stu-id="fa94a-114">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="fa94a-115">Réservé à un usage interne.</span><span class="sxs-lookup"><span data-stu-id="fa94a-115">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="fa94a-116">**Liaison**</span><span class="sxs-lookup"><span data-stu-id="fa94a-116">**Linkage**</span></span>
</dt> <dd>

<span data-ttu-id="fa94a-117">Réservé à un usage interne.</span><span class="sxs-lookup"><span data-stu-id="fa94a-117">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="fa94a-118">**KernelHandle**</span><span class="sxs-lookup"><span data-stu-id="fa94a-118">**KernelHandle**</span></span>
</dt> <dd>

<span data-ttu-id="fa94a-119">Réservé à un usage interne.</span><span class="sxs-lookup"><span data-stu-id="fa94a-119">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="fa94a-120">**Confirmé**</span><span class="sxs-lookup"><span data-stu-id="fa94a-120">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="fa94a-121">Heure à laquelle les informations de cette structure ont été mises à jour, en intervalles de 100 nanosecondes depuis le 1er janvier 1601 à minuit.</span><span class="sxs-lookup"><span data-stu-id="fa94a-121">Time at which the information in this structure was updated, in 100-nanosecond intervals since midnight, January 1, 1601.</span></span>

</dd> <dt>

<span data-ttu-id="fa94a-122">**Uniques**</span><span class="sxs-lookup"><span data-stu-id="fa94a-122">**Guid**</span></span>
</dt> <dd>

<span data-ttu-id="fa94a-123">GUID que vous définissez pour la session.</span><span class="sxs-lookup"><span data-stu-id="fa94a-123">The GUID that you define for the session.</span></span>

<span data-ttu-id="fa94a-124">Pour une session de journal de noyau NT, définissez ce membre sur **SystemTraceControlGuid**.</span><span class="sxs-lookup"><span data-stu-id="fa94a-124">For an NT Kernel Logger session, set this member to **SystemTraceControlGuid**.</span></span>

<span data-ttu-id="fa94a-125">Si ce membre a la valeur **SystemTraceControlGuid** ou **GlobalLoggerGuid**, l’enregistreur d’événements est un journal système.</span><span class="sxs-lookup"><span data-stu-id="fa94a-125">If this member is set to **SystemTraceControlGuid** or **GlobalLoggerGuid**, the logger will be a system logger.</span></span>

<span data-ttu-id="fa94a-126">Pour une session d’enregistreur d’événements privée, définissez ce membre sur le GUID du fournisseur que vous allez activer pour la session.</span><span class="sxs-lookup"><span data-stu-id="fa94a-126">For a private logger session, set this member to the provider's GUID that you are going to enable for the session.</span></span>

<span data-ttu-id="fa94a-127">Si vous démarrez une session qui n’est pas une session de journalisation de noyau ou privée, vous n’êtes pas obligé de spécifier un GUID de session.</span><span class="sxs-lookup"><span data-stu-id="fa94a-127">If you start a session that is not a kernel logger or private logger session, you do not have to specify a session GUID.</span></span> <span data-ttu-id="fa94a-128">Si vous ne spécifiez pas de GUID, ETW en crée un pour vous.</span><span class="sxs-lookup"><span data-stu-id="fa94a-128">If you do not specify a GUID, ETW creates one for you.</span></span> <span data-ttu-id="fa94a-129">Vous devez spécifier un GUID de session uniquement si vous souhaitez modifier les autorisations par défaut associées à une session spécifique.</span><span class="sxs-lookup"><span data-stu-id="fa94a-129">You need to specify a session GUID only if you want to change the default permissions associated with a specific session.</span></span> <span data-ttu-id="fa94a-130">Pour plus d’informations, consultez la fonction EventAccessControl.</span><span class="sxs-lookup"><span data-stu-id="fa94a-130">For details, see the EventAccessControl function.</span></span>

<span data-ttu-id="fa94a-131">Vous ne pouvez pas démarrer plusieurs sessions avec le même GUID de session.</span><span class="sxs-lookup"><span data-stu-id="fa94a-131">You cannot start more than one session with the same session GUID.</span></span>

<span data-ttu-id="fa94a-132">**Avant Windows Vista :** Vous pouvez démarrer plusieurs sessions avec le même GUID de session.</span><span class="sxs-lookup"><span data-stu-id="fa94a-132">**Prior to Windows Vista:** You can start more than one session with the same session GUID.</span></span>

</dd> <dt>

<span data-ttu-id="fa94a-133">**ClientContext**</span><span class="sxs-lookup"><span data-stu-id="fa94a-133">**ClientContext**</span></span>
</dt> <dd>

<span data-ttu-id="fa94a-134">Résolution d’horloge à utiliser lors de la journalisation de l’horodatage pour chaque événement.</span><span class="sxs-lookup"><span data-stu-id="fa94a-134">Clock resolution to use when logging the time stamp for each event.</span></span> <span data-ttu-id="fa94a-135">La valeur par défaut est le compteur de performance des requêtes (QPC).</span><span class="sxs-lookup"><span data-stu-id="fa94a-135">The default is Query performance counter (QPC).</span></span>

<span data-ttu-id="fa94a-136">**Avant Windows Vista :** La valeur par défaut est l’heure système.</span><span class="sxs-lookup"><span data-stu-id="fa94a-136">**Prior to Windows Vista:** The default is system time.</span></span>

<span data-ttu-id="fa94a-137">**Avant Windows 10, version 1703 :** Deux types d’horloge distincts ne peuvent pas être utilisés simultanément par les enregistreurs d’événements système.</span><span class="sxs-lookup"><span data-stu-id="fa94a-137">**Prior to Windows 10, version 1703:** No more than 2 distinct clock types can be used simultaneously by any system loggers.</span></span>

<span data-ttu-id="fa94a-138">**À compter de Windows 10, version 1703 :** La restriction de type d’horloge a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="fa94a-138">**Starting with Windows 10, version 1703:** The clock type restriction has been removed.</span></span> <span data-ttu-id="fa94a-139">Les trois types d’horloge peuvent maintenant être utilisés simultanément par les enregistreurs d’événements système.</span><span class="sxs-lookup"><span data-stu-id="fa94a-139">All three clock types can now be used simultaneously by system loggers.</span></span>

<span data-ttu-id="fa94a-140">Vous pouvez spécifier l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="fa94a-140">You can specify one of the following values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fa94a-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa94a-141">Value</span></span></th>
<th><span data-ttu-id="fa94a-142">Signification</span><span class="sxs-lookup"><span data-stu-id="fa94a-142">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="fa94a-143"><dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="fa94a-143"><dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="fa94a-144">Compteur de performance des requêtes (QPC).</span><span class="sxs-lookup"><span data-stu-id="fa94a-144">Query performance counter (QPC).</span></span> <span data-ttu-id="fa94a-145">Le compteur QPC fournit un horodatage haute résolution qui n’est pas affecté par les réglages de l’horloge système.</span><span class="sxs-lookup"><span data-stu-id="fa94a-145">The QPC counter provides a high-resolution time stamp that is not affected by adjustments to the system clock.</span></span> <span data-ttu-id="fa94a-146">L’horodatage stocké dans l’événement est équivalent à la valeur retournée par l’API QueryPerformanceCounter.</span><span class="sxs-lookup"><span data-stu-id="fa94a-146">The time stamp stored in the event is equivalent to the value returned from the QueryPerformanceCounter API.</span></span> <span data-ttu-id="fa94a-147">Pour plus d’informations sur les caractéristiques de cet horodatage, consultez <a href="/windows/win32/sysinfo/acquiring-high-resolution-time-stamps">acquisition d’horodatages haute résolution</a>.</span><span class="sxs-lookup"><span data-stu-id="fa94a-147">For more information on the characteristics of this time stamp, see <a href="/windows/win32/sysinfo/acquiring-high-resolution-time-stamps">Acquiring high-resolution time stamps</a>.</span></span><br/> <span data-ttu-id="fa94a-148">Vous devez utiliser cette résolution si vous avez des taux d’événements élevés ou si le consommateur fusionne les événements à partir de mémoires tampons différentes.</span><span class="sxs-lookup"><span data-stu-id="fa94a-148">You should use this resolution if you have high event rates or if the consumer merges events from different buffers.</span></span> <span data-ttu-id="fa94a-149">Dans ces cas, la précision et la stabilité de l’horodatage QPC permettent une meilleure précision de l’ordonnancement des événements à partir de mémoires tampons différentes.</span><span class="sxs-lookup"><span data-stu-id="fa94a-149">In these cases, the precision and stability of the QPC time stamp allows for better accuracy in ordering the events from different buffers.</span></span> <span data-ttu-id="fa94a-150">Toutefois, l’horodatage QPC ne reflète pas les mises à jour de l’horloge système, par exemple, si l’horloge système est avancée en raison de la synchronisation avec un serveur NTP pendant que la trace est en cours, les horodatages QPC dans la trace continuent de refléter le temps comme si aucune mise à jour n’avait eu lieu.</span><span class="sxs-lookup"><span data-stu-id="fa94a-150">However, the QPC time stamp will not reflect updates to the system clock, e.g. if the system clock is adjusted forward due to synchronization with an NTP server while the trace is in progress, the QPC time stamps in the trace will continue to reflect time as if no update had occurred.</span></span><br/> <span data-ttu-id="fa94a-151">Pour déterminer la résolution, utilisez le membre <strong>PerfFreq</strong> de <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> lors de l’utilisation de l’événement.</span><span class="sxs-lookup"><span data-stu-id="fa94a-151">To determine the resolution, use the <strong>PerfFreq</strong> member of <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> when consuming the event.</span></span><br/> <span data-ttu-id="fa94a-152">Pour convertir l’horodatage d’un événement en unités 100-ns, utilisez la formule de conversion suivante :</span><span class="sxs-lookup"><span data-stu-id="fa94a-152">To convert an event’s time stamp into 100-ns units, use the following conversion formula:</span></span> <br/> <span data-ttu-id="fa94a-153">scaledTimestamp = eventRecord. EventHeader. TimeStamp. QuadPart \* 10000000,0/logfileHeader. PerfFreq. QuadPart</span><span class="sxs-lookup"><span data-stu-id="fa94a-153">scaledTimestamp = eventRecord.EventHeader.TimeStamp.QuadPart \* 10000000.0 / logfileHeader.PerfFreq.QuadPart</span></span><br/> <span data-ttu-id="fa94a-154">Notez que sur les ordinateurs plus anciens, l’horodatage peut ne pas être précis, car le compteur ignore parfois les transferts en raison d’erreurs matérielles.</span><span class="sxs-lookup"><span data-stu-id="fa94a-154">Note that on older computers, the time stamp may not be accurate because the counter sometimes skips forward due to hardware errors.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="fa94a-155"><dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="fa94a-155"><dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="fa94a-156">Heure système.</span><span class="sxs-lookup"><span data-stu-id="fa94a-156">System time.</span></span> <span data-ttu-id="fa94a-157">L’heure système fournit un horodatage qui effectue le suivi des modifications apportées à l’horloge du système, par exemple, si l’horloge système est avancée en raison de la synchronisation avec un serveur NTP pendant que la trace est en cours, les horodatages de l’heure système dans la trace se poursuivent également pour correspondre au nouveau paramètre de l’horloge système.</span><span class="sxs-lookup"><span data-stu-id="fa94a-157">The system time provides a time stamp that tracks changes to the system’s clock, e.g. if the system clock is adjusted forward due to synchronization with an NTP server while the trace is in progress, the System Time time stamps in the trace will also jump forward to match the new setting of the system clock.</span></span> <br/>
<ul>
<li><span data-ttu-id="fa94a-158">Sur les systèmes antérieurs à Windows 10, l’horodatage stocké dans l’événement est équivalent à la valeur retournée par l’API GetSystemTimeAsFileTime.</span><span class="sxs-lookup"><span data-stu-id="fa94a-158">On systems prior to Windows 10, the time stamp stored in the event is equivalent to the value returned from the GetSystemTimeAsFileTime API.</span></span></li>
<li><span data-ttu-id="fa94a-159">Sur Windows 10 ou version ultérieure, l’horodatage stocké dans l’événement est équivalent à la valeur retournée par l’API GetSystemTimePreciseAsFileTime.</span><span class="sxs-lookup"><span data-stu-id="fa94a-159">On Windows 10 or later, the time stamp stored in the event is equivalent to the value returned from the GetSystemTimePreciseAsFileTime API.</span></span></li>
</ul>
<span data-ttu-id="fa94a-160">Avant Windows 10, la résolution de cet horodatage était la résolution d’un cycle d’horloge système, comme indiqué par le membre TimerResolution de TRACE_LOGFILE_HEADER.</span><span class="sxs-lookup"><span data-stu-id="fa94a-160">Prior to Windows 10, the resolution of this time stamp was the resolution of a system clock tick, as indicated by the TimerResolution member of TRACE_LOGFILE_HEADER.</span></span> <span data-ttu-id="fa94a-161">À compter de Windows 10, la résolution de cet horodatage correspond à la résolution du compteur de performances, comme indiqué par le membre PerfFreq de TRACE_LOGFILE_HEADER.</span><span class="sxs-lookup"><span data-stu-id="fa94a-161">Starting with Windows 10, the resolution of this time stamp is the performance counter resolution, as indicated by the PerfFreq member of TRACE_LOGFILE_HEADER.</span></span><br/> <span data-ttu-id="fa94a-162">Pour convertir l’horodatage d’un événement en unités 100-ns, utilisez la formule de conversion suivante :</span><span class="sxs-lookup"><span data-stu-id="fa94a-162">To convert an event’s time stamp into 100-ns units, use the following conversion formula:</span></span> <br/> <span data-ttu-id="fa94a-163">scaledTimestamp = eventRecord. EventHeader. TimeStamp. QuadPart</span><span class="sxs-lookup"><span data-stu-id="fa94a-163">scaledTimestamp = eventRecord.EventHeader.TimeStamp.QuadPart</span></span><br/> <span data-ttu-id="fa94a-164">Notez que lorsque les événements sont capturés sur un système exécutant un système d’exploitation antérieur à Windows 10, si le volume d’événements est élevé, la résolution de l’heure système peut ne pas être suffisamment précise pour déterminer la séquence d’événements.</span><span class="sxs-lookup"><span data-stu-id="fa94a-164">Note that when events are captured on a system running an OS prior to Windows 10, if the volume of events is high, the resolution for system time may not be fine enough to determine the sequence of events.</span></span> <span data-ttu-id="fa94a-165">Dans ce cas, un ensemble d’événements aura le même horodatage, mais l’ordre dans lequel ETW remet les événements peut ne pas être correct.</span><span class="sxs-lookup"><span data-stu-id="fa94a-165">In this case, a set of events will have the same time stamp, but the order in which ETW delivers the events may not be correct.</span></span> <span data-ttu-id="fa94a-166">À partir de Windows 10, l’horodatage est capturé avec une précision supplémentaire, bien qu’une certaine instabilité puisse encore se produire dans les cas où l’horloge système a été réglée lors de la capture de la trace.</span><span class="sxs-lookup"><span data-stu-id="fa94a-166">Starting with Windows 10, the time stamp is captured with additional precision, though some instability may still occur in cases where the system clock was adjusted while the trace was being captured.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="fa94a-167"><dt>1,3</dt> </span><span class="sxs-lookup"><span data-stu-id="fa94a-167"><dt>3</dt> </span></span></dl></td>
<td><span data-ttu-id="fa94a-168">Compteur du cycle de l’UC.</span><span class="sxs-lookup"><span data-stu-id="fa94a-168">CPU cycle counter.</span></span> <span data-ttu-id="fa94a-169">Le compteur UC fournit l’horodatage de résolution le plus élevé et est le moins gourmand en ressources à récupérer.</span><span class="sxs-lookup"><span data-stu-id="fa94a-169">The CPU counter provides the highest resolution time stamp and is the least resource-intensive to retrieve.</span></span> <span data-ttu-id="fa94a-170">Toutefois, le compteur UC n’est pas fiable et ne doit pas être utilisé en production.</span><span class="sxs-lookup"><span data-stu-id="fa94a-170">However, the CPU counter is unreliable and should not be used in production.</span></span> <span data-ttu-id="fa94a-171">Par exemple, sur certains ordinateurs, les minuteurs changent de fréquence en raison des modifications de la température et de l’alimentation, en plus de s’arrêter dans certains États.</span><span class="sxs-lookup"><span data-stu-id="fa94a-171">For example, on some computers, the timers will change frequency due to thermal and power changes, in addition to stopping in some states.</span></span><br/> <span data-ttu-id="fa94a-172">Pour déterminer la résolution, utilisez le membre <strong>CpuSpeedInMHz</strong> de <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> lors de l’utilisation de l’événement.</span><span class="sxs-lookup"><span data-stu-id="fa94a-172">To determine the resolution, use the <strong>CpuSpeedInMHz</strong> member of <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> when consuming the event.</span></span><br/> <span data-ttu-id="fa94a-173">Si votre matériel ne prend pas en charge ce type d’horloge, ETW utilise l’heure système.</span><span class="sxs-lookup"><span data-stu-id="fa94a-173">If your hardware does not support this clock type, ETW uses system time.</span></span><br/> <span data-ttu-id="fa94a-174"><strong>Windows Server 2003, Windows XP avec SP1 et Windows XP :</strong> Cette valeur n’est pas prise en charge, elle a été introduite dans Windows Server 2003 avec SP1 et Windows XP avec SP2.</span><span class="sxs-lookup"><span data-stu-id="fa94a-174"><strong>Windows Server 2003, Windows XP with SP1 and Windows XP:</strong> This value is not supported, it was introduced in Windows Server 2003 with SP1 and Windows XP with SP2.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="fa94a-175">**Windows 2000 :** Le membre **ClientContext** n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="fa94a-175">**Windows 2000:** The **ClientContext** member is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="fa94a-176">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="fa94a-176">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="fa94a-177">Doit contenir **le \_ \_ \_ GUID suivi de l’indicateur WNODE** pour indiquer que la structure contient des informations de suivi d’événements.</span><span class="sxs-lookup"><span data-stu-id="fa94a-177">Must contain **WNODE\_FLAG\_TRACED\_GUID** to indicate that the structure contains event tracing information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fa94a-178">Notes</span><span class="sxs-lookup"><span data-stu-id="fa94a-178">Remarks</span></span>

<span data-ttu-id="fa94a-179">Veillez à initialiser la mémoire pour cette structure à zéro avant de définir les membres.</span><span class="sxs-lookup"><span data-stu-id="fa94a-179">Be sure to initialize the memory for this structure to zero before setting any members.</span></span>

<span data-ttu-id="fa94a-180">Pour convertir un horodatage ETW en FILETIME, utilisez la procédure suivante :</span><span class="sxs-lookup"><span data-stu-id="fa94a-180">To convert an ETW timestamp into a FILETIME, use the following procedure:</span></span>

<dl> 1. <span data-ttu-id="fa94a-181">Pour chaque session ou fichier journal en cours de traitement (par exemple, pour chaque journal de suivi d’événements \_ \_ ), consultez le champ logfile. ProcessTraceMode pour déterminer si l' \_ indicateur de datage brut du mode de trace du processus \_ \_ \_ est défini.</span><span class="sxs-lookup"><span data-stu-id="fa94a-181">For each session or log file being processed (i.e. for each EVENT\_TRACE\_LOGFILE), check the logFile.ProcessTraceMode field to determine whether the PROCESS\_TRACE\_MODE\_RAW\_TIMESTAMP flag is set.</span></span> <span data-ttu-id="fa94a-182">Par défaut, cet indicateur n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="fa94a-182">By default, this flag is not set.</span></span> <span data-ttu-id="fa94a-183">Si cet indicateur n’est pas défini, le runtime ETW convertit automatiquement l’horodateur de chaque enregistrement d’événement \_ en FILETIME avant d’envoyer l' \_ enregistrement d’événement à votre fonction EventRecordCallback, de sorte qu’aucun traitement supplémentaire n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="fa94a-183">If this flag is not set, the ETW runtime will automatically convert the timestamp of each EVENT\_RECORD into a FILETIME before sending the EVENT\_RECORD to your EventRecordCallback function, so no additional processing is needed.</span></span> <span data-ttu-id="fa94a-184">Les étapes suivantes doivent être utilisées uniquement si la trace est en cours de traitement avec \_ l' \_ indicateur d’horodateur brut du mode de trace processus \_ \_ défini.</span><span class="sxs-lookup"><span data-stu-id="fa94a-184">The following steps should only be used if the trace is being processed with the PROCESS\_TRACE\_MODE\_RAW\_TIMESTAMP flag set.</span></span>  
2. <span data-ttu-id="fa94a-185">Pour chaque session ou fichier journal en cours de traitement (par exemple, pour chaque journal de suivi d’événements \_ \_ ), consultez le champ logfile. LogfileHeader. ReservedFlags pour déterminer l’échelle de l’horodatage du fichier journal.</span><span class="sxs-lookup"><span data-stu-id="fa94a-185">For each session or log file being processed (i.e. for each EVENT\_TRACE\_LOGFILE), check the logFile.LogfileHeader.ReservedFlags field to determine the time stamp scale for the log file.</span></span> <span data-ttu-id="fa94a-186">En fonction de la valeur de ReservedFlags, effectuez l’une des étapes suivantes pour déterminer la valeur à utiliser pour timeStampScale dans les étapes restantes :</span><span class="sxs-lookup"><span data-stu-id="fa94a-186">Based on the value of ReservedFlags, follow one of these steps to determine the value to use for timeStampScale in the remaining steps:</span></span> <dl> <span data-ttu-id="fa94a-187">a.</span><span class="sxs-lookup"><span data-stu-id="fa94a-187">a.</span></span> <span data-ttu-id="fa94a-188">Si ReservedFlags = = 1 (QPC) : DOUBLE timeStampScale = 10000000,0/logFile. LogfileHeader. PerfFreq. QuadPart ;</span><span class="sxs-lookup"><span data-stu-id="fa94a-188">If ReservedFlags == 1 (QPC): DOUBLE timeStampScale = 10000000.0 / logFile.LogfileHeader.PerfFreq.QuadPart;</span></span>  
<span data-ttu-id="fa94a-189">b.</span><span class="sxs-lookup"><span data-stu-id="fa94a-189">b.</span></span> <span data-ttu-id="fa94a-190">Si ReservedFlags = = 2 (heure système) : DOUBLE timeStampScale = 1,0 ;</span><span class="sxs-lookup"><span data-stu-id="fa94a-190">If ReservedFlags == 2 (System time): DOUBLE timeStampScale = 1.0;</span></span>  
<span data-ttu-id="fa94a-191">Notez que les étapes restantes ne sont pas nécessaires pour les événements qui utilisent l’heure système, car les événements fournissent déjà leurs horodatages dans les unités FILETIME.</span><span class="sxs-lookup"><span data-stu-id="fa94a-191">Note that the remaining steps are unnecessary for events using system time, since the events already provide their time stamps in FILETIME units.</span></span> <span data-ttu-id="fa94a-192">Les étapes restantes fonctionnent, mais elles ne sont pas nécessaires et introduisent une petite erreur d’arrondi.</span><span class="sxs-lookup"><span data-stu-id="fa94a-192">The remaining steps will work but are unnecessary and will introduce a small rounding error.</span></span>  
<span data-ttu-id="fa94a-193">c.</span><span class="sxs-lookup"><span data-stu-id="fa94a-193">c.</span></span> <span data-ttu-id="fa94a-194">Si ReservedFlags = = 3 (compteur de cycle UC) : DOUBLE timeStampScale = 10,0/logFile. LogfileHeader. CpuSpeedInMHz ;</span><span class="sxs-lookup"><span data-stu-id="fa94a-194">If ReservedFlags == 3 (CPU cycle counter): DOUBLE timeStampScale = 10.0 / logFile.LogfileHeader.CpuSpeedInMHz;</span></span>  
</dl> </dd> 3. On the FIRST call to your EventRecordCallback function for a particular log file, use data from the logFile (EVENT\_TRACE\_LOGFILE) and from the eventRecord (EVENT\_RECORD) to compute the timeStampBase that will be used for the remaining events in the log file: INT64 timeStampBase = logFile.LogfileHeader.StartTime.QuadPart - (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
4. For each eventRecord (EVENT\_RECORD), convert the event’s timestamp into FILETIME as follows, using the timeStampScale and timeStampBase values calculated in steps 2 and 3: INT64 timeStampInFileTime = timeStampBase + (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
</dl>

## <a name="requirements"></a><span data-ttu-id="fa94a-195">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fa94a-195">Requirements</span></span>



| <span data-ttu-id="fa94a-196">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa94a-196">Requirement</span></span> | <span data-ttu-id="fa94a-197">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa94a-197">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fa94a-198">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa94a-198">Minimum supported client</span></span><br/> | <span data-ttu-id="fa94a-199">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="fa94a-199">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                   |
| <span data-ttu-id="fa94a-200">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa94a-200">Minimum supported server</span></span><br/> | <span data-ttu-id="fa94a-201">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="fa94a-201">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                         |
| <span data-ttu-id="fa94a-202">En-tête</span><span class="sxs-lookup"><span data-stu-id="fa94a-202">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa94a-203"><dt>Wmistr. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa94a-203"><dt>Wmistr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa94a-204">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa94a-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa94a-205">*ControlCallback*</span><span class="sxs-lookup"><span data-stu-id="fa94a-205">*ControlCallback*</span></span>](/windows/win32/api/evntrace/nc-evntrace-wmidprequest)
</dt> <dt>

[<span data-ttu-id="fa94a-206">**Propriétés de la trace d’événements \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fa94a-206">**EVENT\_TRACE\_PROPERTIES**</span></span>](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[<span data-ttu-id="fa94a-207">**GetTraceLoggerHandle**</span><span class="sxs-lookup"><span data-stu-id="fa94a-207">**GetTraceLoggerHandle**</span></span>](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle)
</dt> <dt>

[<span data-ttu-id="fa94a-208">**\_entier long**</span><span class="sxs-lookup"><span data-stu-id="fa94a-208">**LARGE\_INTEGER**</span></span>](/windows/win32/api/winnt/ns-winnt-large_integer-r1)
</dt> </dl>

 

 
