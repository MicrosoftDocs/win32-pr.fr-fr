---
description: Cette classe est la classe de type d’événement pour les événements de processus. La syntaxe suivante est simplifiée à partir du code MOF.
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
ms.openlocfilehash: fc2308965de5c06a25858a138d4536763613a4d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320113"
---
# <a name="process_v1_typegroup1-class"></a><span data-ttu-id="0e568-104">Traiter \_ la \_ classe TypeGroup1 v1</span><span class="sxs-lookup"><span data-stu-id="0e568-104">Process\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="0e568-105">Cette classe est la classe de type d’événement pour les événements de processus.</span><span class="sxs-lookup"><span data-stu-id="0e568-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="0e568-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="0e568-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e568-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e568-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="0e568-108">Membres</span><span class="sxs-lookup"><span data-stu-id="0e568-108">Members</span></span>

<span data-ttu-id="0e568-109">La classe **process \_ v1 \_ TypeGroup1** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0e568-109">The **Process\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="0e568-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0e568-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0e568-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0e568-111">Properties</span></span>

<span data-ttu-id="0e568-112">La classe **process \_ v1 \_ TypeGroup1** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="0e568-112">The **Process\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0e568-113">ExitStatus</span><span class="sxs-lookup"><span data-stu-id="0e568-113">ExitStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e568-114">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="0e568-114">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e568-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e568-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e568-116">Qualificateurs : WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="0e568-116">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="0e568-117">État de sortie du processus arrêté.</span><span class="sxs-lookup"><span data-stu-id="0e568-117">Exit status of the stopped process.</span></span>

</dd> <dt>

<span data-ttu-id="0e568-118">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="0e568-118">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e568-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e568-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e568-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e568-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e568-121">Qualificateurs : WmiDataId (7), StringTermination ("NullTerminated")</span><span class="sxs-lookup"><span data-stu-id="0e568-121">Qualifiers: WmiDataId(7), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="0e568-122">Chemin d’accès au fichier exécutable du processus.</span><span class="sxs-lookup"><span data-stu-id="0e568-122">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="0e568-123">PageDirectoryBase</span><span class="sxs-lookup"><span data-stu-id="0e568-123">PageDirectoryBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e568-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e568-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e568-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e568-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e568-126">Qualificateurs : WmiDataId (1), pointeur</span><span class="sxs-lookup"><span data-stu-id="0e568-126">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="0e568-127">Réservé.</span><span class="sxs-lookup"><span data-stu-id="0e568-127">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="0e568-128">ParentId</span><span class="sxs-lookup"><span data-stu-id="0e568-128">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e568-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e568-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e568-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e568-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e568-131">Qualificateurs : WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="0e568-131">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="0e568-132">Identificateur unique du processus qui crée ce processus.</span><span class="sxs-lookup"><span data-stu-id="0e568-132">Unique identifier of the process that creates this process.</span></span> <span data-ttu-id="0e568-133">Les numéros d’identificateur de processus sont réutilisés, donc ils identifient uniquement un processus pendant la durée de vie de ce processus.</span><span class="sxs-lookup"><span data-stu-id="0e568-133">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="0e568-134">Il est possible que le processus identifié par ParentProcessId soit terminé, de sorte que ParentProcessId ne peut pas faire référence à un processus en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="0e568-134">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="0e568-135">Il est également possible que ParentProcessId fasse incorrectement référence à un processus qui réutilise un identificateur de processus.</span><span class="sxs-lookup"><span data-stu-id="0e568-135">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

<span data-ttu-id="0e568-136">**Windows Server 2003 :** Inclut le qualificateur format ("x").</span><span class="sxs-lookup"><span data-stu-id="0e568-136">**Windows Server 2003:** Includes the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="0e568-137">ProcessId</span><span class="sxs-lookup"><span data-stu-id="0e568-137">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e568-138">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e568-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e568-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e568-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e568-140">Qualificateurs : WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="0e568-140">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="0e568-141">Identificateur de processus global que vous pouvez utiliser pour identifier un processus.</span><span class="sxs-lookup"><span data-stu-id="0e568-141">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="0e568-142">La valeur est valide à partir du moment où un processus est créé jusqu’à ce qu’il soit terminé.</span><span class="sxs-lookup"><span data-stu-id="0e568-142">The value is valid from the time a process is created until it is terminated.</span></span>

<span data-ttu-id="0e568-143">**Windows Server 2003 :** Inclut le qualificateur format ("x").</span><span class="sxs-lookup"><span data-stu-id="0e568-143">**Windows Server 2003:** Includes the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="0e568-144">SessionId</span><span class="sxs-lookup"><span data-stu-id="0e568-144">SessionId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e568-145">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e568-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e568-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e568-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e568-147">Qualificateurs : WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="0e568-147">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="0e568-148">Identificateur unique généré par un système d’exploitation lors de la création d’une nouvelle session.</span><span class="sxs-lookup"><span data-stu-id="0e568-148">Unique identifier that an operating system generates when it creates a new session.</span></span> <span data-ttu-id="0e568-149">Une session s’étend sur une période allant de l’ouverture de session jusqu’à la fermeture d’une session à partir d’un système spécifique.</span><span class="sxs-lookup"><span data-stu-id="0e568-149">A session spans a period of time from log on until log off from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="0e568-150">UserSID</span><span class="sxs-lookup"><span data-stu-id="0e568-150">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e568-151">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="0e568-151">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="0e568-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e568-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e568-153">Qualificateurs : WmiDataId (6), extension (« SID »)</span><span class="sxs-lookup"><span data-stu-id="0e568-153">Qualifiers: WmiDataId(6), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="0e568-154">Identificateur de sécurité (SID) du contexte de l’utilisateur sous lequel l’événement se produit.</span><span class="sxs-lookup"><span data-stu-id="0e568-154">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0e568-155">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0e568-155">Requirements</span></span>



| <span data-ttu-id="0e568-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e568-156">Requirement</span></span> | <span data-ttu-id="0e568-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e568-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0e568-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e568-158">Minimum supported client</span></span><br/> | <span data-ttu-id="0e568-159">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e568-159">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="0e568-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e568-160">Minimum supported server</span></span><br/> | <span data-ttu-id="0e568-161">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e568-161">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0e568-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e568-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e568-163">**Traiter \_ v1**</span><span class="sxs-lookup"><span data-stu-id="0e568-163">**Process\_V1**</span></span>](process.md)
</dt> <dt>

[<span data-ttu-id="0e568-164">**Traiter \_ v1**</span><span class="sxs-lookup"><span data-stu-id="0e568-164">**Process\_V1**</span></span>](process-v1.md)
</dt> </dl>

 

 




