---
description: Cette classe est la classe de type d’événement pour les événements de processus. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 4f06e1af-3f9a-4346-aa50-50f3ee82cd98
title: Classe Process_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_TypeGroup1
- Process_TypeGroup1.UniqueProcessKey
- Process_TypeGroup1.ProcessId
- Process_TypeGroup1.ParentId
- Process_TypeGroup1.SessionId
- Process_TypeGroup1.ExitStatus
- Process_TypeGroup1.DirectoryTableBase
- Process_TypeGroup1.UserSID
- Process_TypeGroup1.ImageFileName
- Process_TypeGroup1.CommandLine
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4ad2ebcd9a3e1563f6e2f4c82d90dd4d2c80112f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863057"
---
# <a name="process_typegroup1-class"></a><span data-ttu-id="96e98-104">Traiter la \_ classe TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="96e98-104">Process\_TypeGroup1 class</span></span>

<span data-ttu-id="96e98-105">Cette classe est la classe de type d’événement pour les événements de processus.</span><span class="sxs-lookup"><span data-stu-id="96e98-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="96e98-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="96e98-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="96e98-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="96e98-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4, 39}, EventTypeName{"Start", "End", "DCStart", "DCEnd", "Defunct"}]
class Process_TypeGroup1 : Process
{
  uint32 UniqueProcessKey;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  uint32 DirectoryTableBase;
  object UserSID;
  string ImageFileName;
  string CommandLine;
};
```

## <a name="members"></a><span data-ttu-id="96e98-108">Membres</span><span class="sxs-lookup"><span data-stu-id="96e98-108">Members</span></span>

<span data-ttu-id="96e98-109">La classe **process \_ TypeGroup1** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="96e98-109">The **Process\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="96e98-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="96e98-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="96e98-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="96e98-111">Properties</span></span>

<span data-ttu-id="96e98-112">La classe **process \_ TypeGroup1** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="96e98-112">The **Process\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="96e98-113">CommandLine</span><span class="sxs-lookup"><span data-stu-id="96e98-113">CommandLine</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96e98-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="96e98-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="96e98-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="96e98-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96e98-116">Qualificateurs : WmiDataId (9), StringTermination ("NullTerminated"), format ("w")</span><span class="sxs-lookup"><span data-stu-id="96e98-116">Qualifiers: WmiDataId(9), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="96e98-117">Ligne de commande complète du processus.</span><span class="sxs-lookup"><span data-stu-id="96e98-117">Full command line of the process.</span></span>

</dd> <dt>

<span data-ttu-id="96e98-118">DirectoryTableBase</span><span class="sxs-lookup"><span data-stu-id="96e98-118">DirectoryTableBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96e98-119">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96e98-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96e98-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="96e98-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96e98-121">Qualificateurs : WmiDataId (6), pointeur</span><span class="sxs-lookup"><span data-stu-id="96e98-121">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="96e98-122">Adresse physique de la table de pages du processus.</span><span class="sxs-lookup"><span data-stu-id="96e98-122">The physical address of the page table of the process.</span></span>

</dd> <dt>

<span data-ttu-id="96e98-123">ExitStatus</span><span class="sxs-lookup"><span data-stu-id="96e98-123">ExitStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96e98-124">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="96e98-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="96e98-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="96e98-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96e98-126">Qualificateurs : WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="96e98-126">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="96e98-127">État de sortie du processus arrêté.</span><span class="sxs-lookup"><span data-stu-id="96e98-127">Exit status of the stopped process.</span></span>

</dd> <dt>

<span data-ttu-id="96e98-128">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="96e98-128">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96e98-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="96e98-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="96e98-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="96e98-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96e98-131">Qualificateurs : WmiDataId (8), StringTermination ("NullTerminated")</span><span class="sxs-lookup"><span data-stu-id="96e98-131">Qualifiers: WmiDataId(8), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="96e98-132">Chemin d’accès au fichier exécutable du processus.</span><span class="sxs-lookup"><span data-stu-id="96e98-132">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="96e98-133">ParentId</span><span class="sxs-lookup"><span data-stu-id="96e98-133">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96e98-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96e98-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96e98-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="96e98-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96e98-136">Qualificateurs : WmiDataId (3), format ("x")</span><span class="sxs-lookup"><span data-stu-id="96e98-136">Qualifiers: WmiDataId(3), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="96e98-137">Identificateur unique du processus qui crée ce processus.</span><span class="sxs-lookup"><span data-stu-id="96e98-137">Unique identifier of the process that creates this process.</span></span> <span data-ttu-id="96e98-138">Les numéros d’identificateur de processus sont réutilisés, donc ils identifient uniquement un processus pendant la durée de vie de ce processus.</span><span class="sxs-lookup"><span data-stu-id="96e98-138">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="96e98-139">Il est possible que le processus identifié par ParentProcessId soit terminé, de sorte que ParentProcessId ne peut pas faire référence à un processus en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="96e98-139">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="96e98-140">Il est également possible que ParentProcessId fasse incorrectement référence à un processus qui réutilise un identificateur de processus.</span><span class="sxs-lookup"><span data-stu-id="96e98-140">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

</dd> <dt>

<span data-ttu-id="96e98-141">ProcessId</span><span class="sxs-lookup"><span data-stu-id="96e98-141">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96e98-142">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96e98-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96e98-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="96e98-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96e98-144">Qualificateurs : WmiDataId (2), format ("x")</span><span class="sxs-lookup"><span data-stu-id="96e98-144">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="96e98-145">Identificateur de processus global que vous pouvez utiliser pour identifier un processus.</span><span class="sxs-lookup"><span data-stu-id="96e98-145">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="96e98-146">La valeur est valide à partir du moment où un processus est créé jusqu’à ce qu’il soit terminé.</span><span class="sxs-lookup"><span data-stu-id="96e98-146">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="96e98-147">SessionId</span><span class="sxs-lookup"><span data-stu-id="96e98-147">SessionId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96e98-148">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96e98-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96e98-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="96e98-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96e98-150">Qualificateurs : WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="96e98-150">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="96e98-151">Identificateur unique généré par un système d’exploitation lors de la création d’une nouvelle session.</span><span class="sxs-lookup"><span data-stu-id="96e98-151">Unique identifier that an operating system generates when it creates a new session.</span></span> <span data-ttu-id="96e98-152">Une session s’étend sur une période allant de l’ouverture de session jusqu’à la fermeture d’une session à partir d’un système spécifique.</span><span class="sxs-lookup"><span data-stu-id="96e98-152">A session spans a period of time from log on until log off from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="96e98-153">UniqueProcessKey</span><span class="sxs-lookup"><span data-stu-id="96e98-153">UniqueProcessKey</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96e98-154">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96e98-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96e98-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="96e98-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96e98-156">Qualificateurs : WmiDataId (1), pointeur</span><span class="sxs-lookup"><span data-stu-id="96e98-156">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="96e98-157">Adresse de l’objet processus dans le noyau.</span><span class="sxs-lookup"><span data-stu-id="96e98-157">The address of the process object in the kernel.</span></span>

</dd> <dt>

<span data-ttu-id="96e98-158">UserSID</span><span class="sxs-lookup"><span data-stu-id="96e98-158">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96e98-159">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="96e98-159">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="96e98-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="96e98-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96e98-161">Qualificateurs : WmiDataId (7), extension (« SID »)</span><span class="sxs-lookup"><span data-stu-id="96e98-161">Qualifiers: WmiDataId(7), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="96e98-162">Identificateur de sécurité (SID) du contexte de l’utilisateur sous lequel l’événement se produit.</span><span class="sxs-lookup"><span data-stu-id="96e98-162">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="96e98-163">Notes</span><span class="sxs-lookup"><span data-stu-id="96e98-163">Remarks</span></span>

<span data-ttu-id="96e98-164">Les types d’événements DCStart et DCEnd énumèrent le processus en cours d’exécution, y compris le processus système et inactif au moment où la session du noyau démarre et se termine, respectivement.</span><span class="sxs-lookup"><span data-stu-id="96e98-164">The DCStart and DCEnd event types enumerate the process that are currently running, including idle and system process, at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="96e98-165">Spécifications</span><span class="sxs-lookup"><span data-stu-id="96e98-165">Requirements</span></span>



| <span data-ttu-id="96e98-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="96e98-166">Requirement</span></span> | <span data-ttu-id="96e98-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="96e98-167">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="96e98-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="96e98-168">Minimum supported client</span></span><br/> | <span data-ttu-id="96e98-169">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="96e98-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="96e98-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="96e98-170">Minimum supported server</span></span><br/> | <span data-ttu-id="96e98-171">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="96e98-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="96e98-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96e98-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96e98-173">**Processus**</span><span class="sxs-lookup"><span data-stu-id="96e98-173">**Process**</span></span>](process.md)
</dt> </dl>

 

 




