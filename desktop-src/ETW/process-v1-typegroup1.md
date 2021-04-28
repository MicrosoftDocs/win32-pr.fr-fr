---
description: Classe Process_V1_TypeGroup1-cette classe est la classe de type d’événement pour les événements de processus. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: b114d7fd-c308-4f21-8f1a-ab27dc93abc5
title: Classe Process_V1_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V1_TypeGroup1
- Process_V1_TypeGroup1.PageDirectoryBase
- Process_V1_TypeGroup1.ProcessId
- Process_V1_TypeGroup1.ParentId
- Process_V1_TypeGroup1.SessionId
- Process_V1_TypeGroup1.ExitStatus
- Process_V1_TypeGroup1.UserSID
- Process_V1_TypeGroup1.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8d7f4426f34a97ff79dc41806f1e0070013528d2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106327"
---
# <a name="process_v1_typegroup1-class"></a><span data-ttu-id="2dc5f-104">Traiter \_ la \_ classe TypeGroup1 v1</span><span class="sxs-lookup"><span data-stu-id="2dc5f-104">Process\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="2dc5f-105">Cette classe est la classe de type d’événement pour les événements de processus.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="2dc5f-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dc5f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2dc5f-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Process_V1_TypeGroup1 : Process_V1
{
  uint32 PageDirectoryBase;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  object UserSID;
  string ImageFileName;
};
```

## <a name="members"></a><span data-ttu-id="2dc5f-108">Membres</span><span class="sxs-lookup"><span data-stu-id="2dc5f-108">Members</span></span>

<span data-ttu-id="2dc5f-109">La classe **process \_ v1 \_ TypeGroup1** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2dc5f-109">The **Process\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="2dc5f-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2dc5f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2dc5f-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2dc5f-111">Properties</span></span>

<span data-ttu-id="2dc5f-112">La classe **process \_ v1 \_ TypeGroup1** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-112">The **Process\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2dc5f-113">ExitStatus</span><span class="sxs-lookup"><span data-stu-id="2dc5f-113">ExitStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc5f-114">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="2dc5f-114">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2dc5f-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2dc5f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc5f-116">Qualificateurs : WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="2dc5f-116">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="2dc5f-117">État de sortie du processus arrêté.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-117">Exit status of the stopped process.</span></span>

</dd> <dt>

<span data-ttu-id="2dc5f-118">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="2dc5f-118">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc5f-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2dc5f-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2dc5f-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2dc5f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc5f-121">Qualificateurs : WmiDataId (7), StringTermination ("NullTerminated")</span><span class="sxs-lookup"><span data-stu-id="2dc5f-121">Qualifiers: WmiDataId(7), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="2dc5f-122">Chemin d’accès au fichier exécutable du processus.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-122">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="2dc5f-123">PageDirectoryBase</span><span class="sxs-lookup"><span data-stu-id="2dc5f-123">PageDirectoryBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc5f-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2dc5f-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2dc5f-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2dc5f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc5f-126">Qualificateurs : WmiDataId (1), pointeur</span><span class="sxs-lookup"><span data-stu-id="2dc5f-126">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="2dc5f-127">Réservé.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-127">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="2dc5f-128">ParentId</span><span class="sxs-lookup"><span data-stu-id="2dc5f-128">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc5f-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2dc5f-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2dc5f-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2dc5f-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc5f-131">Qualificateurs : WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="2dc5f-131">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="2dc5f-132">Identificateur unique du processus qui crée ce processus.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-132">Unique identifier of the process that creates this process.</span></span> <span data-ttu-id="2dc5f-133">Les numéros d’identificateur de processus sont réutilisés, donc ils identifient uniquement un processus pendant la durée de vie de ce processus.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-133">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="2dc5f-134">Il est possible que le processus identifié par ParentProcessId soit terminé, de sorte que ParentProcessId ne peut pas faire référence à un processus en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-134">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="2dc5f-135">Il est également possible que ParentProcessId fasse incorrectement référence à un processus qui réutilise un identificateur de processus.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-135">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

<span data-ttu-id="2dc5f-136">**Windows Server 2003 :** Inclut le qualificateur format ("x").</span><span class="sxs-lookup"><span data-stu-id="2dc5f-136">**Windows Server 2003:** Includes the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="2dc5f-137">ProcessId</span><span class="sxs-lookup"><span data-stu-id="2dc5f-137">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc5f-138">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2dc5f-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2dc5f-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2dc5f-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc5f-140">Qualificateurs : WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="2dc5f-140">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="2dc5f-141">Identificateur de processus global que vous pouvez utiliser pour identifier un processus.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-141">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="2dc5f-142">La valeur est valide à partir du moment où un processus est créé jusqu’à ce qu’il soit terminé.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-142">The value is valid from the time a process is created until it is terminated.</span></span>

<span data-ttu-id="2dc5f-143">**Windows Server 2003 :** Inclut le qualificateur format ("x").</span><span class="sxs-lookup"><span data-stu-id="2dc5f-143">**Windows Server 2003:** Includes the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="2dc5f-144">SessionId</span><span class="sxs-lookup"><span data-stu-id="2dc5f-144">SessionId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc5f-145">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2dc5f-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2dc5f-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2dc5f-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc5f-147">Qualificateurs : WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="2dc5f-147">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="2dc5f-148">Identificateur unique généré par un système d’exploitation lors de la création d’une nouvelle session.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-148">Unique identifier that an operating system generates when it creates a new session.</span></span> <span data-ttu-id="2dc5f-149">Une session s’étend sur une période allant de l’ouverture de session jusqu’à la fermeture d’une session à partir d’un système spécifique.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-149">A session spans a period of time from log on until log off from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="2dc5f-150">UserSID</span><span class="sxs-lookup"><span data-stu-id="2dc5f-150">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc5f-151">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="2dc5f-151">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="2dc5f-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2dc5f-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc5f-153">Qualificateurs : WmiDataId (6), extension (« SID »)</span><span class="sxs-lookup"><span data-stu-id="2dc5f-153">Qualifiers: WmiDataId(6), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="2dc5f-154">Identificateur de sécurité (SID) du contexte de l’utilisateur sous lequel l’événement se produit.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-154">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2dc5f-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2dc5f-155">Requirements</span></span>



| <span data-ttu-id="2dc5f-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2dc5f-156">Requirement</span></span> | <span data-ttu-id="2dc5f-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="2dc5f-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2dc5f-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2dc5f-158">Minimum supported client</span></span><br/> | <span data-ttu-id="2dc5f-159">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2dc5f-159">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="2dc5f-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2dc5f-160">Minimum supported server</span></span><br/> | <span data-ttu-id="2dc5f-161">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2dc5f-161">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2dc5f-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2dc5f-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dc5f-163">**Traiter \_ v1**</span><span class="sxs-lookup"><span data-stu-id="2dc5f-163">**Process\_V1**</span></span>](process.md)
</dt> <dt>

[<span data-ttu-id="2dc5f-164">**Traiter \_ v1**</span><span class="sxs-lookup"><span data-stu-id="2dc5f-164">**Process\_V1**</span></span>](process-v1.md)
</dt> </dl>

 

 




