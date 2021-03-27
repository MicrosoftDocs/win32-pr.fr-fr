---
description: Cette classe est la classe de type d’événement pour les événements de processus. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: fcf2897d-32b4-42b9-892c-f0106687d3c2
title: Classe Process_V0_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V0_TypeGroup1
- Process_V0_TypeGroup1.ProcessId
- Process_V0_TypeGroup1.ParentId
- Process_V0_TypeGroup1.UserSID
- Process_V0_TypeGroup1.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2889feb05bfc396f2c2018ca59d2cf46fba8ec13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972223"
---
# <a name="process_v0_typegroup1-class"></a><span data-ttu-id="d1fbc-104">Traiter \_ la \_ classe TypeGroup1 v0</span><span class="sxs-lookup"><span data-stu-id="d1fbc-104">Process\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="d1fbc-105">Cette classe est la classe de type d’événement pour les événements de processus.</span><span class="sxs-lookup"><span data-stu-id="d1fbc-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="d1fbc-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="d1fbc-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1fbc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1fbc-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Process_V0_TypeGroup1 : Process_V0
{
  uint32 ProcessId;
  uint32 ParentId;
  object UserSID;
  string ImageFileName;
};
```

## <a name="members"></a><span data-ttu-id="d1fbc-108">Membres</span><span class="sxs-lookup"><span data-stu-id="d1fbc-108">Members</span></span>

<span data-ttu-id="d1fbc-109">La classe **process \_ v0 \_ TypeGroup1** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d1fbc-109">The **Process\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="d1fbc-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d1fbc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d1fbc-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d1fbc-111">Properties</span></span>

<span data-ttu-id="d1fbc-112">La classe **process \_ v0 \_ TypeGroup1** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d1fbc-112">The **Process\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d1fbc-113">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="d1fbc-113">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1fbc-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d1fbc-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1fbc-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1fbc-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1fbc-116">Qualificateurs : WmiDataId (4), StringTermination ("NullTerminated")</span><span class="sxs-lookup"><span data-stu-id="d1fbc-116">Qualifiers: WmiDataId(4), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="d1fbc-117">Chemin d’accès au fichier exécutable du processus.</span><span class="sxs-lookup"><span data-stu-id="d1fbc-117">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="d1fbc-118">ParentId</span><span class="sxs-lookup"><span data-stu-id="d1fbc-118">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1fbc-119">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1fbc-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1fbc-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1fbc-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1fbc-121">Qualificateurs : WmiDataId (2), pointeur</span><span class="sxs-lookup"><span data-stu-id="d1fbc-121">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="d1fbc-122">Identificateur unique du processus qui crée un processus.</span><span class="sxs-lookup"><span data-stu-id="d1fbc-122">Unique identifier of the process that creates a process.</span></span> <span data-ttu-id="d1fbc-123">Les numéros d’identificateur de processus sont réutilisés, donc ils identifient uniquement un processus pendant la durée de vie de ce processus.</span><span class="sxs-lookup"><span data-stu-id="d1fbc-123">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="d1fbc-124">Il est possible que le processus identifié par ParentProcessId soit terminé, de sorte que ParentProcessId ne peut pas faire référence à un processus en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d1fbc-124">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="d1fbc-125">Il est également possible que ParentProcessId fasse incorrectement référence à un processus qui réutilise un identificateur de processus.</span><span class="sxs-lookup"><span data-stu-id="d1fbc-125">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

</dd> <dt>

<span data-ttu-id="d1fbc-126">ProcessId</span><span class="sxs-lookup"><span data-stu-id="d1fbc-126">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1fbc-127">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1fbc-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1fbc-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1fbc-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1fbc-129">Qualificateurs : WmiDataId (1), pointeur</span><span class="sxs-lookup"><span data-stu-id="d1fbc-129">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="d1fbc-130">Identificateur de processus global que vous pouvez utiliser pour identifier un processus.</span><span class="sxs-lookup"><span data-stu-id="d1fbc-130">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="d1fbc-131">La valeur est valide à partir du moment où un processus est créé jusqu’à ce qu’il soit terminé.</span><span class="sxs-lookup"><span data-stu-id="d1fbc-131">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="d1fbc-132">UserSID</span><span class="sxs-lookup"><span data-stu-id="d1fbc-132">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1fbc-133">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="d1fbc-133">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="d1fbc-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1fbc-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1fbc-135">Qualificateurs : WmiDataId (3), extension (« SID »)</span><span class="sxs-lookup"><span data-stu-id="d1fbc-135">Qualifiers: WmiDataId(3), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="d1fbc-136">Identificateur de sécurité (SID) du contexte de l’utilisateur sous lequel l’événement se produit.</span><span class="sxs-lookup"><span data-stu-id="d1fbc-136">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d1fbc-137">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d1fbc-137">Requirements</span></span>



| <span data-ttu-id="d1fbc-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1fbc-138">Requirement</span></span> | <span data-ttu-id="d1fbc-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1fbc-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d1fbc-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1fbc-140">Minimum supported client</span></span><br/> | <span data-ttu-id="d1fbc-141">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1fbc-141">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="d1fbc-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1fbc-142">Minimum supported server</span></span><br/> | <span data-ttu-id="d1fbc-143">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1fbc-143">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d1fbc-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1fbc-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1fbc-145">**Processus \_ v0**</span><span class="sxs-lookup"><span data-stu-id="d1fbc-145">**Process\_V0**</span></span>](process-v0.md)
</dt> </dl>

 

 




