---
description: Cette classe est la classe de type d’événement pour les événements de processus. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: ff5c1f64-2087-4238-81f9-6283f0f0e68a
title: Classe Process_V2_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V2_TypeGroup1
- Process_V2_TypeGroup1.UniqueProcessKey
- Process_V2_TypeGroup1.ProcessId
- Process_V2_TypeGroup1.ParentId
- Process_V2_TypeGroup1.SessionId
- Process_V2_TypeGroup1.ExitStatus
- Process_V2_TypeGroup1.UserSID
- Process_V2_TypeGroup1.ImageFileName
- Process_V2_TypeGroup1.CommandLine
api_type:
- NA
api_location: ''
ms.openlocfilehash: 01da5a8254627d6378c9f99aa2ba36dc6714e6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973575"
---
# <a name="process_v2_typegroup1-class"></a><span data-ttu-id="a73b1-104">Traiter \_ la \_ classe TypeGroup1 v2</span><span class="sxs-lookup"><span data-stu-id="a73b1-104">Process\_V2\_TypeGroup1 class</span></span>

<span data-ttu-id="a73b1-105">Cette classe est la classe de type d’événement pour les événements de processus.</span><span class="sxs-lookup"><span data-stu-id="a73b1-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="a73b1-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="a73b1-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a73b1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a73b1-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4, 39}, EventTypeName{"Start", "End", "DCStart", "DCEnd", "Defunct"}]
class Process_V2_TypeGroup1 : Process_V2
{
  uint32 UniqueProcessKey;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  object UserSID;
  string ImageFileName;
  string CommandLine;
};
```

## <a name="members"></a><span data-ttu-id="a73b1-108">Membres</span><span class="sxs-lookup"><span data-stu-id="a73b1-108">Members</span></span>

<span data-ttu-id="a73b1-109">La classe **process \_ v2 \_ TypeGroup1** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a73b1-109">The **Process\_V2\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="a73b1-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a73b1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a73b1-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a73b1-111">Properties</span></span>

<span data-ttu-id="a73b1-112">La classe **process \_ v2 \_ TypeGroup1** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="a73b1-112">The **Process\_V2\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a73b1-113">CommandLine</span><span class="sxs-lookup"><span data-stu-id="a73b1-113">CommandLine</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a73b1-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a73b1-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a73b1-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a73b1-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a73b1-116">Qualificateurs : WmiDataId (8), StringTermination ("NullTerminated"), format ("w")</span><span class="sxs-lookup"><span data-stu-id="a73b1-116">Qualifiers: WmiDataId(8), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="a73b1-117">Ligne de commande complète du processus.</span><span class="sxs-lookup"><span data-stu-id="a73b1-117">Full command line of the process.</span></span>

</dd> <dt>

<span data-ttu-id="a73b1-118">ExitStatus</span><span class="sxs-lookup"><span data-stu-id="a73b1-118">ExitStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a73b1-119">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="a73b1-119">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a73b1-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a73b1-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a73b1-121">Qualificateurs : WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="a73b1-121">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="a73b1-122">État de sortie du processus arrêté.</span><span class="sxs-lookup"><span data-stu-id="a73b1-122">Exit status of the stopped process.</span></span>

</dd> <dt>

<span data-ttu-id="a73b1-123">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="a73b1-123">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a73b1-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a73b1-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a73b1-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a73b1-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a73b1-126">Qualificateurs : WmiDataId (7), StringTermination ("NullTerminated")</span><span class="sxs-lookup"><span data-stu-id="a73b1-126">Qualifiers: WmiDataId(7), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="a73b1-127">Chemin d’accès au fichier exécutable du processus.</span><span class="sxs-lookup"><span data-stu-id="a73b1-127">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="a73b1-128">ParentId</span><span class="sxs-lookup"><span data-stu-id="a73b1-128">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a73b1-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a73b1-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a73b1-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a73b1-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a73b1-131">Qualificateurs : WmiDataId (3), format ("x")</span><span class="sxs-lookup"><span data-stu-id="a73b1-131">Qualifiers: WmiDataId(3), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="a73b1-132">Identificateur unique du processus qui crée ce processus.</span><span class="sxs-lookup"><span data-stu-id="a73b1-132">Unique identifier of the process that creates this process.</span></span> <span data-ttu-id="a73b1-133">Les numéros d’identificateur de processus sont réutilisés, donc ils identifient uniquement un processus pendant la durée de vie de ce processus.</span><span class="sxs-lookup"><span data-stu-id="a73b1-133">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="a73b1-134">Il est possible que le processus identifié par ParentProcessId soit terminé, de sorte que ParentProcessId ne peut pas faire référence à un processus en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a73b1-134">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="a73b1-135">Il est également possible que ParentProcessId fasse incorrectement référence à un processus qui réutilise un identificateur de processus.</span><span class="sxs-lookup"><span data-stu-id="a73b1-135">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

</dd> <dt>

<span data-ttu-id="a73b1-136">ProcessId</span><span class="sxs-lookup"><span data-stu-id="a73b1-136">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a73b1-137">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a73b1-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a73b1-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a73b1-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a73b1-139">Qualificateurs : WmiDataId (2), format ("x")</span><span class="sxs-lookup"><span data-stu-id="a73b1-139">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="a73b1-140">Identificateur de processus global que vous pouvez utiliser pour identifier un processus.</span><span class="sxs-lookup"><span data-stu-id="a73b1-140">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="a73b1-141">La valeur est valide à partir du moment où un processus est créé jusqu’à ce qu’il soit terminé.</span><span class="sxs-lookup"><span data-stu-id="a73b1-141">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="a73b1-142">SessionId</span><span class="sxs-lookup"><span data-stu-id="a73b1-142">SessionId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a73b1-143">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a73b1-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a73b1-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a73b1-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a73b1-145">Qualificateurs : WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="a73b1-145">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="a73b1-146">Identificateur unique généré par un système d’exploitation lors de la création d’une nouvelle session.</span><span class="sxs-lookup"><span data-stu-id="a73b1-146">Unique identifier that an operating system generates when it creates a new session.</span></span> <span data-ttu-id="a73b1-147">Une session s’étend sur une période allant de l’ouverture de session jusqu’à la fermeture d’une session à partir d’un système spécifique.</span><span class="sxs-lookup"><span data-stu-id="a73b1-147">A session spans a period of time from log on until log off from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="a73b1-148">UniqueProcessKey</span><span class="sxs-lookup"><span data-stu-id="a73b1-148">UniqueProcessKey</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a73b1-149">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a73b1-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a73b1-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a73b1-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a73b1-151">Qualificateurs : WmiDataId (1), pointeur</span><span class="sxs-lookup"><span data-stu-id="a73b1-151">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="a73b1-152">Adresse de l’objet processus dans le noyau.</span><span class="sxs-lookup"><span data-stu-id="a73b1-152">The address of the process object in the kernel.</span></span>

</dd> <dt>

<span data-ttu-id="a73b1-153">UserSID</span><span class="sxs-lookup"><span data-stu-id="a73b1-153">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a73b1-154">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="a73b1-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a73b1-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a73b1-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a73b1-156">Qualificateurs : WmiDataId (6), extension (« SID »)</span><span class="sxs-lookup"><span data-stu-id="a73b1-156">Qualifiers: WmiDataId(6), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="a73b1-157">Identificateur de sécurité (SID) du contexte de l’utilisateur sous lequel l’événement se produit.</span><span class="sxs-lookup"><span data-stu-id="a73b1-157">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a73b1-158">Notes</span><span class="sxs-lookup"><span data-stu-id="a73b1-158">Remarks</span></span>

<span data-ttu-id="a73b1-159">Les types d’événements DCStart et DCEnd énumèrent le processus en cours d’exécution, y compris le processus système et inactif au moment où la session du noyau démarre et se termine, respectivement.</span><span class="sxs-lookup"><span data-stu-id="a73b1-159">The DCStart and DCEnd event types enumerate the process that are currently running, including idle and system process, at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="a73b1-160">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a73b1-160">Requirements</span></span>



| <span data-ttu-id="a73b1-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a73b1-161">Requirement</span></span> | <span data-ttu-id="a73b1-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="a73b1-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="a73b1-163">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a73b1-163">Minimum supported client</span></span><br/> | <span data-ttu-id="a73b1-164">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a73b1-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a73b1-165">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a73b1-165">Minimum supported server</span></span><br/> | <span data-ttu-id="a73b1-166">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a73b1-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a73b1-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a73b1-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a73b1-168">**Traitement \_ v2**</span><span class="sxs-lookup"><span data-stu-id="a73b1-168">**Process\_V2**</span></span>](process-v2.md)
</dt> </dl>

 

 




