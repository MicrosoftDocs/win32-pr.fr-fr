---
description: Classe de type d’événement pour l’événement d’en-tête du fichier journal. Cette classe contient des informations sur la session de suivi d’événements.
ms.assetid: 3d0c4044-da06-4850-95c4-99b4ea28fcd9
title: Classe EventTrace_Header
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTrace_Header
- EventTrace_Header.BufferSize
- EventTrace_Header.Version
- EventTrace_Header.ProviderVersion
- EventTrace_Header.NumberOfProcessors
- EventTrace_Header.EndTime
- EventTrace_Header.TimerResolution
- EventTrace_Header.MaxFileSize
- EventTrace_Header.LogFileMode
- EventTrace_Header.BuffersWritten
- EventTrace_Header.StartBuffers
- EventTrace_Header.PointerSize
- EventTrace_Header.EventsLost
- EventTrace_Header.CPUSpeed
- EventTrace_Header.LoggerName
- EventTrace_Header.LogFileName
- EventTrace_Header.TimeZoneInformation
- EventTrace_Header.BootTime
- EventTrace_Header.PerfFreq
- EventTrace_Header.StartTime
- EventTrace_Header.ReservedFlags
- EventTrace_Header.BuffersLost
api_type:
- NA
api_location: ''
ms.openlocfilehash: dea803849d6aa15c2a3a14deb850d85ade569116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526865"
---
# <a name="eventtrace_header-class"></a><span data-ttu-id="afd14-104">\_Classe d’en-tête EventTrace</span><span class="sxs-lookup"><span data-stu-id="afd14-104">EventTrace\_Header class</span></span>

<span data-ttu-id="afd14-105">Classe de type d’événement pour l’événement d’en-tête du fichier journal.</span><span class="sxs-lookup"><span data-stu-id="afd14-105">The event type class for the log file header event.</span></span> <span data-ttu-id="afd14-106">Cette classe contient des informations sur la session de suivi d’événements.</span><span class="sxs-lookup"><span data-stu-id="afd14-106">This class contains information about the event tracing session.</span></span>

<span data-ttu-id="afd14-107">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="afd14-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="afd14-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="afd14-108">Syntax</span></span>

``` syntax
[EventType(0)]
class EventTrace_Header : EventTraceEvent
{
  uint32 BufferSize;
  uint32 Version;
  uint32 ProviderVersion;
  uint32 NumberOfProcessors;
  uint64 EndTime;
  uint32 TimerResolution;
  uint32 MaxFileSize;
  uint32 LogFileMode;
  uint32 BuffersWritten;
  uint32 StartBuffers;
  uint32 PointerSize;
  uint32 EventsLost;
  uint32 CPUSpeed;
  uint32 LoggerName;
  uint32 LogFileName;
  uint8  TimeZoneInformation[];
  uint64 BootTime;
  uint64 PerfFreq;
  uint64 StartTime;
  uint32 ReservedFlags;
  uint32 BuffersLost;
};
```

## <a name="members"></a><span data-ttu-id="afd14-109">Membres</span><span class="sxs-lookup"><span data-stu-id="afd14-109">Members</span></span>

<span data-ttu-id="afd14-110">La classe d' **\_ en-tête EventTrace** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="afd14-110">The **EventTrace\_Header** class has these types of members:</span></span>

-   [<span data-ttu-id="afd14-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="afd14-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="afd14-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="afd14-112">Properties</span></span>

<span data-ttu-id="afd14-113">La classe d' **\_ en-tête EventTrace** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="afd14-113">The **EventTrace\_Header** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="afd14-114">**BootTime**</span><span class="sxs-lookup"><span data-stu-id="afd14-114">**BootTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afd14-115">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="afd14-115">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="afd14-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="afd14-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afd14-117">Qualificateurs : **WmiDataId** (17)</span><span class="sxs-lookup"><span data-stu-id="afd14-117">Qualifiers: **WmiDataId** (17)</span></span>
</dt> </dl>

<span data-ttu-id="afd14-118">Heure à laquelle le système a été démarré, en intervalles de 100 nanosecondes depuis le 1er janvier 1601 à minuit.</span><span class="sxs-lookup"><span data-stu-id="afd14-118">Time at which the system was started, in 100-nanosecond intervals since midnight, January 1, 1601.</span></span>

</dd> <dt>

<span data-ttu-id="afd14-119">**BufferSize**</span><span class="sxs-lookup"><span data-stu-id="afd14-119">**BufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afd14-120">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="afd14-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="afd14-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="afd14-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afd14-122">Qualificateurs : **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="afd14-122">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="afd14-123">Taille des tampons de la session de suivi d’événements, en kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="afd14-123">Size of the event tracing session's buffers, in kilobytes.</span></span>

</dd> <dt>

<span data-ttu-id="afd14-124">**BuffersLost**</span><span class="sxs-lookup"><span data-stu-id="afd14-124">**BuffersLost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afd14-125">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="afd14-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="afd14-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="afd14-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afd14-127">Qualificateurs : **WmiDataId** (21)</span><span class="sxs-lookup"><span data-stu-id="afd14-127">Qualifiers: **WmiDataId** (21)</span></span>
</dt> </dl>

<span data-ttu-id="afd14-128">Nombre total de mémoires tampons perdues.</span><span class="sxs-lookup"><span data-stu-id="afd14-128">Total number of buffers lost.</span></span>

</dd> <dt>

<span data-ttu-id="afd14-129">**BuffersWritten**</span><span class="sxs-lookup"><span data-stu-id="afd14-129">**BuffersWritten**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afd14-130">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="afd14-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="afd14-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="afd14-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afd14-132">Qualificateurs : **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="afd14-132">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="afd14-133">Nombre total de mémoires tampons écrites par la session de suivi d’événements.</span><span class="sxs-lookup"><span data-stu-id="afd14-133">Total number of buffers written by the event tracing session.</span></span>

</dd> <dt>

<span data-ttu-id="afd14-134">**CPUSpeed**</span><span class="sxs-lookup"><span data-stu-id="afd14-134">**CPUSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afd14-135">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="afd14-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="afd14-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="afd14-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afd14-137">Qualificateurs : **WmiDataId** (13)</span><span class="sxs-lookup"><span data-stu-id="afd14-137">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="afd14-138">Vitesse du processeur, en mégahertz.</span><span class="sxs-lookup"><span data-stu-id="afd14-138">CPU speed, in megahertz.</span></span>

<span data-ttu-id="afd14-139">**Windows 2000 :** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="afd14-139">**Windows 2000:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="afd14-140">**EndTime**</span><span class="sxs-lookup"><span data-stu-id="afd14-140">**EndTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afd14-141">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="afd14-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="afd14-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="afd14-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afd14-143">Qualificateurs : **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="afd14-143">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="afd14-144">Heure à laquelle la session de suivi d’événements s’est arrêtée, en intervalles de 100 nanosecondes depuis le 1er janvier 1601 à minuit.</span><span class="sxs-lookup"><span data-stu-id="afd14-144">Time at which the event tracing session stopped, in 100-nanosecond intervals since midnight, January 1, 1601.</span></span> <span data-ttu-id="afd14-145">Cette valeur peut être 0 si vous consommez des événements en temps réel ou à partir d’un fichier journal dans lequel le fournit des événements de journalisation continue.</span><span class="sxs-lookup"><span data-stu-id="afd14-145">This value may be 0 if you are consuming events in real time or from a log file to which the provide is still logging events.</span></span>

</dd> <dt>

<span data-ttu-id="afd14-146">**EventsLost**</span><span class="sxs-lookup"><span data-stu-id="afd14-146">**EventsLost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afd14-147">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="afd14-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="afd14-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="afd14-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afd14-149">Qualificateurs : **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="afd14-149">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="afd14-150">Nombre d’événements perdus pendant la session de suivi d’événements.</span><span class="sxs-lookup"><span data-stu-id="afd14-150">Number of events lost during the event tracing session.</span></span>

</dd> <dt>

<span data-ttu-id="afd14-151">**LogFileMode**</span><span class="sxs-lookup"><span data-stu-id="afd14-151">**LogFileMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afd14-152">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="afd14-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="afd14-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="afd14-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afd14-154">Qualificateurs : **WmiDataId** (8), **format ("x")**</span><span class="sxs-lookup"><span data-stu-id="afd14-154">Qualifiers: **WmiDataId** (8), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="afd14-155">Mode de journalisation actuel pour la session de suivi d’événements.</span><span class="sxs-lookup"><span data-stu-id="afd14-155">Current logging mode for the event tracing session.</span></span> <span data-ttu-id="afd14-156">Pour obtenir la liste des valeurs, consultez constantes de mode de journalisation.</span><span class="sxs-lookup"><span data-stu-id="afd14-156">For a list of values, see Logging Mode Constants.</span></span>

</dd> <dt>

<span data-ttu-id="afd14-157">**Nomdefichierjournal**</span><span class="sxs-lookup"><span data-stu-id="afd14-157">**LogFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afd14-158">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="afd14-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="afd14-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="afd14-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afd14-160">Qualificateurs : **WmiDataId** (15), **pointeur**</span><span class="sxs-lookup"><span data-stu-id="afd14-160">Qualifiers: **WmiDataId** (15), **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="afd14-161">Nom du fichier journal de suivi d’événements qui contient les événements.</span><span class="sxs-lookup"><span data-stu-id="afd14-161">Name of the event tracing log file that contains the events.</span></span>

</dd> <dt>

<span data-ttu-id="afd14-162">**LoggerName**</span><span class="sxs-lookup"><span data-stu-id="afd14-162">**LoggerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afd14-163">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="afd14-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="afd14-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="afd14-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afd14-165">Qualificateurs : **WmiDataId** (14), **pointeur**</span><span class="sxs-lookup"><span data-stu-id="afd14-165">Qualifiers: **WmiDataId** (14), **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="afd14-166">Nom de la session de suivi d’événements.</span><span class="sxs-lookup"><span data-stu-id="afd14-166">Name of the event tracing session.</span></span>

</dd> <dt>

<span data-ttu-id="afd14-167">**MaxFileSize**</span><span class="sxs-lookup"><span data-stu-id="afd14-167">**MaxFileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afd14-168">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="afd14-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="afd14-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="afd14-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afd14-170">Qualificateurs : **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="afd14-170">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="afd14-171">Taille maximale du fichier journal, en mégaoctets.</span><span class="sxs-lookup"><span data-stu-id="afd14-171">Maximum size of the log file, in megabytes.</span></span>

</dd> <dt>

<span data-ttu-id="afd14-172">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="afd14-172">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afd14-173">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="afd14-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="afd14-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="afd14-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afd14-175">Qualificateurs : **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="afd14-175">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="afd14-176">Nombre de processeurs sur le système.</span><span class="sxs-lookup"><span data-stu-id="afd14-176">Number of processors on the system.</span></span>

</dd> <dt>

<span data-ttu-id="afd14-177">**PerfFreq**</span><span class="sxs-lookup"><span data-stu-id="afd14-177">**PerfFreq**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afd14-178">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="afd14-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="afd14-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="afd14-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afd14-180">Qualificateurs : **WmiDataId** (18)</span><span class="sxs-lookup"><span data-stu-id="afd14-180">Qualifiers: **WmiDataId** (18)</span></span>
</dt> </dl>

<span data-ttu-id="afd14-181">Fréquence du compteur de performance haute résolution, s’il en existe un.</span><span class="sxs-lookup"><span data-stu-id="afd14-181">Frequency of the high-resolution performance counter, if one exists.</span></span>

</dd> <dt>

<span data-ttu-id="afd14-182">**PointerSize**</span><span class="sxs-lookup"><span data-stu-id="afd14-182">**PointerSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afd14-183">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="afd14-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="afd14-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="afd14-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afd14-185">Qualificateurs : **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="afd14-185">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="afd14-186">Taille du type de données du pointeur, en octets.</span><span class="sxs-lookup"><span data-stu-id="afd14-186">Size of a pointer data type, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="afd14-187">**ProviderVersion**</span><span class="sxs-lookup"><span data-stu-id="afd14-187">**ProviderVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afd14-188">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="afd14-188">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="afd14-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="afd14-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afd14-190">Qualificateurs : **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="afd14-190">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="afd14-191">Numéro de build du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="afd14-191">Build number of the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="afd14-192">**ReservedFlags**</span><span class="sxs-lookup"><span data-stu-id="afd14-192">**ReservedFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afd14-193">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="afd14-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="afd14-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="afd14-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afd14-195">Qualificateurs : **WmiDataId** (20)</span><span class="sxs-lookup"><span data-stu-id="afd14-195">Qualifiers: **WmiDataId** (20)</span></span>
</dt> </dl>

<span data-ttu-id="afd14-196">Réservé.</span><span class="sxs-lookup"><span data-stu-id="afd14-196">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="afd14-197">**StartBuffers**</span><span class="sxs-lookup"><span data-stu-id="afd14-197">**StartBuffers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afd14-198">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="afd14-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="afd14-199">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="afd14-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afd14-200">Qualificateurs : **WmiDataId** (10)</span><span class="sxs-lookup"><span data-stu-id="afd14-200">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="afd14-201">Réservé.</span><span class="sxs-lookup"><span data-stu-id="afd14-201">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="afd14-202">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="afd14-202">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afd14-203">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="afd14-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="afd14-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="afd14-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afd14-205">Qualificateurs : **WmiDataId** (19)</span><span class="sxs-lookup"><span data-stu-id="afd14-205">Qualifiers: **WmiDataId** (19)</span></span>
</dt> </dl>

<span data-ttu-id="afd14-206">Heure de début de la session de suivi d’événements, en intervalles de 100 nanosecondes depuis le 1er janvier 1601 à minuit.</span><span class="sxs-lookup"><span data-stu-id="afd14-206">Time at which the event tracing session started, in 100-nanosecond intervals since midnight, January 1, 1601.</span></span>

</dd> <dt>

<span data-ttu-id="afd14-207">**TimerResolution**</span><span class="sxs-lookup"><span data-stu-id="afd14-207">**TimerResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afd14-208">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="afd14-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="afd14-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="afd14-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afd14-210">Qualificateurs : **WmiDataId** (6)</span><span class="sxs-lookup"><span data-stu-id="afd14-210">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="afd14-211">Résolution de la minuterie matérielle, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="afd14-211">Resolution of the hardware timer, in units of 100 nanoseconds.</span></span>

</dd> <dt>

<span data-ttu-id="afd14-212">**TimeZoneInformation**</span><span class="sxs-lookup"><span data-stu-id="afd14-212">**TimeZoneInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afd14-213">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="afd14-213">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="afd14-214">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="afd14-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afd14-215">Qualificateurs : **WmiDataId** (16), **extension (« noprint »)**, **Max** (176)</span><span class="sxs-lookup"><span data-stu-id="afd14-215">Qualifiers: **WmiDataId** (16), **Extension("NoPrint")**, **Max** (176)</span></span>
</dt> </dl>

<span data-ttu-id="afd14-216">Structure [**d' \_ \_ informations de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) qui contient le fuseau horaire pour les membres **BootTime**, **EndTime** et **StartTime** .</span><span class="sxs-lookup"><span data-stu-id="afd14-216">A [**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) structure that contains the time zone for the **BootTime**, **EndTime** and **StartTime** members.</span></span>

</dd> <dt>

<span data-ttu-id="afd14-217">**Version**</span><span class="sxs-lookup"><span data-stu-id="afd14-217">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afd14-218">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="afd14-218">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="afd14-219">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="afd14-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afd14-220">Qualificateurs : **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="afd14-220">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="afd14-221">Numéro de version du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="afd14-221">Version number of the operating system.</span></span> <span data-ttu-id="afd14-222">À partir des octets de poids faible, les deux premiers octets contiennent la version principale, les deux octets suivants contiennent une version mineure, les deux octets suivants contiennent Service Pack version principale et les deux derniers octets contiennent Service Pack version mineure.</span><span class="sxs-lookup"><span data-stu-id="afd14-222">Starting with the low-order bytes, the first two bytes contain major version, the next two bytes contain minor version, the next two bytes contain service pack major version, and the last two bytes contain service pack minor version.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="afd14-223">Notes</span><span class="sxs-lookup"><span data-stu-id="afd14-223">Remarks</span></span>

<span data-ttu-id="afd14-224">En règle générale, vous souhaitez enregistrer les valeurs des propriétés suivantes pour une utilisation ultérieure lors du traitement des événements à partir du fichier journal.</span><span class="sxs-lookup"><span data-stu-id="afd14-224">Typically, you want to save the values for the following properties for use later when processing events from the log file.</span></span>

-   <span data-ttu-id="afd14-225">**TimerResolution**: à utiliser avec les membres **KernelTime** et **UserTime** de la structure d' [**\_ \_ en-tête de trace d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) pour déterminer le coût de l’UC pour un ensemble d’instructions.</span><span class="sxs-lookup"><span data-stu-id="afd14-225">**TimerResolution**—use with the **KernelTime** and **UserTime** members of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure to determine the CPU cost for a set of instructions.</span></span> <span data-ttu-id="afd14-226">Pour plus d’informations, consultez la section Notes de l' [**\_ \_ en-tête de suivi d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header).</span><span class="sxs-lookup"><span data-stu-id="afd14-226">For details, see the Remarks section of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header).</span></span>
-   <span data-ttu-id="afd14-227">**PointerSize**: pour les propriétés qui contiennent le qualificateur de **pointeur** , utilisez cette valeur pour déterminer la taille du pointeur.</span><span class="sxs-lookup"><span data-stu-id="afd14-227">**PointerSize**—for properties that contain the **Pointer** qualifier, use this value to determine the size of the pointer.</span></span> <span data-ttu-id="afd14-228">Notez que cette valeur peut ne pas être exacte.</span><span class="sxs-lookup"><span data-stu-id="afd14-228">Note that this value may not be accurate.</span></span> <span data-ttu-id="afd14-229">Par exemple, sur un ordinateur 64 bits, une application 32 bits enregistre les pointeurs de 4 octets ; Toutefois, la session affecte la valeur 8 à **PointerSize** .</span><span class="sxs-lookup"><span data-stu-id="afd14-229">For example, on a 64-bit computer, a 32-bit application will log 4-byte pointers; however, the session will set **PointerSize** to 8.</span></span>
-   <span data-ttu-id="afd14-230">**LogFileMode**: permet de déterminer si cette session est une session privée d’enregistreur d’événements.</span><span class="sxs-lookup"><span data-stu-id="afd14-230">**LogFileMode**—use to determine if this session is a private logger session.</span></span> <span data-ttu-id="afd14-231">Certaines propriétés ne contiennent pas de données pour les sessions privées des journaux.</span><span class="sxs-lookup"><span data-stu-id="afd14-231">There are some properties that do not contain data for private logger sessions.</span></span> <span data-ttu-id="afd14-232">Par exemple, les membres **KernelTime** et **UserTime** de la structure d' [**\_ \_ en-tête de trace d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) .</span><span class="sxs-lookup"><span data-stu-id="afd14-232">For example, the **KernelTime** and **UserTime** members of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="afd14-233">Spécifications</span><span class="sxs-lookup"><span data-stu-id="afd14-233">Requirements</span></span>



| <span data-ttu-id="afd14-234">Condition requise</span><span class="sxs-lookup"><span data-stu-id="afd14-234">Requirement</span></span> | <span data-ttu-id="afd14-235">Valeur</span><span class="sxs-lookup"><span data-stu-id="afd14-235">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="afd14-236">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="afd14-236">Minimum supported client</span></span><br/> | <span data-ttu-id="afd14-237">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="afd14-237">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="afd14-238">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="afd14-238">Minimum supported server</span></span><br/> | <span data-ttu-id="afd14-239">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="afd14-239">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="afd14-240">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="afd14-240">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afd14-241">**EventTraceEvent**</span><span class="sxs-lookup"><span data-stu-id="afd14-241">**EventTraceEvent**</span></span>](eventtraceevent.md)
</dt> <dt>

[<span data-ttu-id="afd14-242">**\_ \_ en-tête du fichier journal de suivi**</span><span class="sxs-lookup"><span data-stu-id="afd14-242">**TRACE\_LOGFILE\_HEADER**</span></span>](/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header)
</dt> </dl>

 

 
