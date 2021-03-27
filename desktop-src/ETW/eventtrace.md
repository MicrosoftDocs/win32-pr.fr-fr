---
description: Classe abstraite dont toutes les classes de suivi d’événements sont dérivées.
ms.assetid: 03eea902-5050-4ab2-8a72-9bff7777e234
title: EventTrace, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTrace
- EventTrace.EventSize
- EventTrace.ReservedHeaderField
- EventTrace.EventType
- EventTrace.TraceLevel
- EventTrace.TraceVersion
- EventTrace.ThreadId
- EventTrace.TimeStamp
- EventTrace.EventGuid
- EventTrace.KernelTime
- EventTrace.UserTime
- EventTrace.InstanceId
- EventTrace.ParentGuid
- EventTrace.ParentInstanceId
- EventTrace.MofData
- EventTrace.MofLength
api_type:
- NA
api_location: ''
ms.openlocfilehash: f04399942b39a2da5b746933884a436a65bb370c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752405"
---
# <a name="eventtrace-class"></a><span data-ttu-id="14a61-103">EventTrace, classe</span><span class="sxs-lookup"><span data-stu-id="14a61-103">EventTrace class</span></span>

<span data-ttu-id="14a61-104">Classe abstraite dont toutes les classes de suivi d’événements sont dérivées.</span><span class="sxs-lookup"><span data-stu-id="14a61-104">An abstract class from which all event trace classes are derived.</span></span>

<span data-ttu-id="14a61-105">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="14a61-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="14a61-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14a61-106">Syntax</span></span>

``` syntax
[abstract]
class EventTrace
{
  uint16 EventSize;
  uint16 ReservedHeaderField;
  uint8  EventType;
  uint8  TraceLevel;
  uint16 TraceVersion;
  uint64 ThreadId;
  uint64 TimeStamp;
  uint8  EventGuid[];
  uint32 KernelTime;
  uint32 UserTime;
  uint32 InstanceId;
  uint8  ParentGuid[];
  uint32 ParentInstanceId;
  uint32 MofData;
  uint32 MofLength;
};
```

## <a name="members"></a><span data-ttu-id="14a61-107">Membres</span><span class="sxs-lookup"><span data-stu-id="14a61-107">Members</span></span>

<span data-ttu-id="14a61-108">La classe **EventTrace** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="14a61-108">The **EventTrace** class has these types of members:</span></span>

-   [<span data-ttu-id="14a61-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="14a61-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="14a61-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="14a61-110">Properties</span></span>

<span data-ttu-id="14a61-111">La classe **EventTrace** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="14a61-111">The **EventTrace** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="14a61-112">**EventGuid**</span><span class="sxs-lookup"><span data-stu-id="14a61-112">**EventGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a61-113">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="14a61-113">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="14a61-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14a61-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14a61-115">Qualificateurs : **WmiDataId** (8), **Max** (16)</span><span class="sxs-lookup"><span data-stu-id="14a61-115">Qualifiers: **WmiDataId** (8), **Max** (16)</span></span>
</dt> </dl>

<span data-ttu-id="14a61-116">GUID de classe de trace d’événements de cet événement.</span><span class="sxs-lookup"><span data-stu-id="14a61-116">Event trace class GUID of this event.</span></span>

</dd> <dt>

<span data-ttu-id="14a61-117">**Événements**</span><span class="sxs-lookup"><span data-stu-id="14a61-117">**EventSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a61-118">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="14a61-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="14a61-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14a61-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14a61-120">Qualificateurs : **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="14a61-120">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="14a61-121">Nombre total d’octets de l’événement.</span><span class="sxs-lookup"><span data-stu-id="14a61-121">Total number of bytes of the event.</span></span>

</dd> <dt>

<span data-ttu-id="14a61-122">**EventType**</span><span class="sxs-lookup"><span data-stu-id="14a61-122">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a61-123">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="14a61-123">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="14a61-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14a61-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14a61-125">Qualificateurs : **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="14a61-125">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="14a61-126">Type d’événement défini par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="14a61-126">Provider-defined event type.</span></span> <span data-ttu-id="14a61-127">Indique la classe de type d’événement à utiliser pour déchiffrer les données d’événement définies par le fournisseur (les données pointées par **MofData**.</span><span class="sxs-lookup"><span data-stu-id="14a61-127">Tells you which event type class to use to decipher the provider-defined event data (the data pointed to by **MofData**.</span></span>

</dd> <dt>

<span data-ttu-id="14a61-128">**InstanceId**</span><span class="sxs-lookup"><span data-stu-id="14a61-128">**InstanceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a61-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14a61-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="14a61-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14a61-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14a61-131">Qualificateurs : **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="14a61-131">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="14a61-132">Identificateur de cette instance d’événement.</span><span class="sxs-lookup"><span data-stu-id="14a61-132">Identifier of this event instance.</span></span>

</dd> <dt>

<span data-ttu-id="14a61-133">**KernelTime**</span><span class="sxs-lookup"><span data-stu-id="14a61-133">**KernelTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a61-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14a61-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="14a61-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14a61-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14a61-136">Qualificateurs : **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="14a61-136">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="14a61-137">Durée d’exécution écoulée pour les instructions en mode noyau, en graduations de l’UC.</span><span class="sxs-lookup"><span data-stu-id="14a61-137">Elapsed execution time for kernel-mode instructions, in CPU ticks.</span></span>

</dd> <dt>

<span data-ttu-id="14a61-138">**MofData**</span><span class="sxs-lookup"><span data-stu-id="14a61-138">**MofData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a61-139">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14a61-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="14a61-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14a61-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14a61-141">Qualificateurs : **WmiDataId** (14), **pointeur**</span><span class="sxs-lookup"><span data-stu-id="14a61-141">Qualifiers: **WmiDataId** (14), **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="14a61-142">Pointeur vers les données d’événement spécifiques au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="14a61-142">Pointer to the provider-specific event data.</span></span>

</dd> <dt>

<span data-ttu-id="14a61-143">**MofLength**</span><span class="sxs-lookup"><span data-stu-id="14a61-143">**MofLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a61-144">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14a61-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="14a61-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14a61-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14a61-146">Qualificateurs : **WmiDataId** (15)</span><span class="sxs-lookup"><span data-stu-id="14a61-146">Qualifiers: **WmiDataId** (15)</span></span>
</dt> </dl>

<span data-ttu-id="14a61-147">Longueur des données d’événement spécifiques au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="14a61-147">Length of the provider-specific event data.</span></span>

</dd> <dt>

<span data-ttu-id="14a61-148">**ParentGuid**</span><span class="sxs-lookup"><span data-stu-id="14a61-148">**ParentGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a61-149">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="14a61-149">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="14a61-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14a61-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14a61-151">Qualificateurs : **WmiDataId** (12), **Max** (16)</span><span class="sxs-lookup"><span data-stu-id="14a61-151">Qualifiers: **WmiDataId** (12), **Max** (16)</span></span>
</dt> </dl>

<span data-ttu-id="14a61-152">GUID de classe de trace d’événements de l’instance parente.</span><span class="sxs-lookup"><span data-stu-id="14a61-152">Event trace class GUID of the parent instance.</span></span>

</dd> <dt>

<span data-ttu-id="14a61-153">**ParentInstanceId**</span><span class="sxs-lookup"><span data-stu-id="14a61-153">**ParentInstanceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a61-154">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14a61-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="14a61-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14a61-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14a61-156">Qualificateurs : **WmiDataId** (13)</span><span class="sxs-lookup"><span data-stu-id="14a61-156">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="14a61-157">Identificateur des données de l’instance parente.</span><span class="sxs-lookup"><span data-stu-id="14a61-157">Identifier of the parent instance data.</span></span>

</dd> <dt>

<span data-ttu-id="14a61-158">**ReservedHeaderField**</span><span class="sxs-lookup"><span data-stu-id="14a61-158">**ReservedHeaderField**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a61-159">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="14a61-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="14a61-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14a61-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14a61-161">Qualificateurs : **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="14a61-161">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="14a61-162">Réservé.</span><span class="sxs-lookup"><span data-stu-id="14a61-162">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="14a61-163">**ThreadId**</span><span class="sxs-lookup"><span data-stu-id="14a61-163">**ThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a61-164">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="14a61-164">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="14a61-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14a61-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14a61-166">Qualificateurs : **WmiDataId** (6), **pointeur**</span><span class="sxs-lookup"><span data-stu-id="14a61-166">Qualifiers: **WmiDataId** (6), **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="14a61-167">Identifie le thread qui a généré l’événement.</span><span class="sxs-lookup"><span data-stu-id="14a61-167">Identifies the thread that generated the event.</span></span>

</dd> <dt>

<span data-ttu-id="14a61-168">**Confirmé**</span><span class="sxs-lookup"><span data-stu-id="14a61-168">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a61-169">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="14a61-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="14a61-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14a61-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14a61-171">Qualificateurs : **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="14a61-171">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="14a61-172">Contient la date et l’heure auxquelles l’événement s’est produit.</span><span class="sxs-lookup"><span data-stu-id="14a61-172">Contains the date and time when the event occurred.</span></span>

</dd> <dt>

<span data-ttu-id="14a61-173">**TraceLevel**</span><span class="sxs-lookup"><span data-stu-id="14a61-173">**TraceLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a61-174">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="14a61-174">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="14a61-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14a61-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14a61-176">Qualificateurs : **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="14a61-176">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="14a61-177">Valeur définie par le fournisseur qui définit le niveau de gravité utilisé pour générer l’événement.</span><span class="sxs-lookup"><span data-stu-id="14a61-177">Provider-defined value that defines the severity level used to generate the event.</span></span>

</dd> <dt>

<span data-ttu-id="14a61-178">**TraceVersion**</span><span class="sxs-lookup"><span data-stu-id="14a61-178">**TraceVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a61-179">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="14a61-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="14a61-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14a61-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14a61-181">Qualificateurs : **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="14a61-181">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="14a61-182">Numéro de version défini par le fournisseur de la classe de trace d’événements utilisée pour générer l’événement.</span><span class="sxs-lookup"><span data-stu-id="14a61-182">Provider-defined version number of the event trace class used to generate the event.</span></span>

</dd> <dt>

<span data-ttu-id="14a61-183">**UserTime**</span><span class="sxs-lookup"><span data-stu-id="14a61-183">**UserTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a61-184">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14a61-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="14a61-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14a61-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14a61-186">Qualificateurs : **WmiDataId** (10)</span><span class="sxs-lookup"><span data-stu-id="14a61-186">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="14a61-187">Durée d’exécution écoulée pour les instructions en mode utilisateur, en graduations de l’UC.</span><span class="sxs-lookup"><span data-stu-id="14a61-187">Elapsed execution time for user-mode instructions, in CPU ticks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="14a61-188">Notes</span><span class="sxs-lookup"><span data-stu-id="14a61-188">Remarks</span></span>

<span data-ttu-id="14a61-189">N’utilisez pas ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="14a61-189">Do not use these properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="14a61-190">Spécifications</span><span class="sxs-lookup"><span data-stu-id="14a61-190">Requirements</span></span>



| <span data-ttu-id="14a61-191">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14a61-191">Requirement</span></span> | <span data-ttu-id="14a61-192">Valeur</span><span class="sxs-lookup"><span data-stu-id="14a61-192">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="14a61-193">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14a61-193">Minimum supported client</span></span><br/> | <span data-ttu-id="14a61-194">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14a61-194">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="14a61-195">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14a61-195">Minimum supported server</span></span><br/> | <span data-ttu-id="14a61-196">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14a61-196">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="14a61-197">MOF</span><span class="sxs-lookup"><span data-stu-id="14a61-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="14a61-198"><dt>WMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="14a61-198"><dt>Wmi.mof</dt></span></span> </dl> |



 

 




