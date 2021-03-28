---
description: Cette classe est la classe de type d’événement pour les événements de profil échantillonnés. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 75ea1e5e-2554-40bb-aa9d-c6d4942c5801
title: SampledProfile, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SampledProfile
- SampledProfile.InstructionPointer
- SampledProfile.ThreadId
- SampledProfile.Count
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3d7a69eef1a2a7988569ffcd930b73a559e18d90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973650"
---
# <a name="sampledprofile-class"></a><span data-ttu-id="018f3-104">SampledProfile, classe</span><span class="sxs-lookup"><span data-stu-id="018f3-104">SampledProfile class</span></span>

<span data-ttu-id="018f3-105">Cette classe est la classe de type d’événement pour les événements de profil échantillonnés.</span><span class="sxs-lookup"><span data-stu-id="018f3-105">This class is the event type class for sampled profile events.</span></span>

<span data-ttu-id="018f3-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="018f3-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="018f3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="018f3-107">Syntax</span></span>

``` syntax
[EventType{46}, EventTypeName{"SampleProfile"}]
class SampledProfile : PerfInfo
{
  uint32 InstructionPointer;
  uint32 ThreadId;
  uint32 Count;
};
```

## <a name="members"></a><span data-ttu-id="018f3-108">Membres</span><span class="sxs-lookup"><span data-stu-id="018f3-108">Members</span></span>

<span data-ttu-id="018f3-109">La classe **SampledProfile** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="018f3-109">The **SampledProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="018f3-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="018f3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="018f3-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="018f3-111">Properties</span></span>

<span data-ttu-id="018f3-112">La classe **SampledProfile** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="018f3-112">The **SampledProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="018f3-113">**Count**</span><span class="sxs-lookup"><span data-stu-id="018f3-113">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="018f3-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="018f3-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="018f3-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="018f3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="018f3-116">Qualificateurs : WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="018f3-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="018f3-117">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="018f3-117">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="018f3-118">**InstructionPointer**</span><span class="sxs-lookup"><span data-stu-id="018f3-118">**InstructionPointer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="018f3-119">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="018f3-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="018f3-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="018f3-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="018f3-121">Qualificateurs : WmiDataId (1), pointeur</span><span class="sxs-lookup"><span data-stu-id="018f3-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="018f3-122">Adresse de l’image qui était en cours d’exécution au moment où le processeur a été échantillonné.</span><span class="sxs-lookup"><span data-stu-id="018f3-122">Address of the image that was running at the time the processor was sampled.</span></span>

</dd> <dt>

<span data-ttu-id="018f3-123">**ThreadId**</span><span class="sxs-lookup"><span data-stu-id="018f3-123">**ThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="018f3-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="018f3-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="018f3-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="018f3-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="018f3-126">Qualificateurs : WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="018f3-126">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="018f3-127">Identificateur du thread qui s’exécutait au moment où le processeur a été échantillonné.</span><span class="sxs-lookup"><span data-stu-id="018f3-127">Thread identifier of the thread that was running at the time the processor was sampled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="018f3-128">Notes</span><span class="sxs-lookup"><span data-stu-id="018f3-128">Remarks</span></span>

<span data-ttu-id="018f3-129">Ces événements fournissent un profil d’exécution échantillonné.</span><span class="sxs-lookup"><span data-stu-id="018f3-129">These events provide a sampled execution profile.</span></span> <span data-ttu-id="018f3-130">L’événement enregistre ce qui a été exécuté sur le processeur.</span><span class="sxs-lookup"><span data-stu-id="018f3-130">The event records what was being executed on the processor.</span></span> <span data-ttu-id="018f3-131">Vous pouvez utiliser les événements d’image pour identifier le module binaire contenant cette instruction.</span><span class="sxs-lookup"><span data-stu-id="018f3-131">You can use the Image events to identify the binary module containing that instruction.</span></span> <span data-ttu-id="018f3-132">Vous pouvez ensuite utiliser ces informations pour créer un profil d’exécution pendant la durée de la trace.</span><span class="sxs-lookup"><span data-stu-id="018f3-132">You can then use this information to produce an execution profile for the duration of the trace.</span></span>

## <a name="requirements"></a><span data-ttu-id="018f3-133">Spécifications</span><span class="sxs-lookup"><span data-stu-id="018f3-133">Requirements</span></span>



| <span data-ttu-id="018f3-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="018f3-134">Requirement</span></span> | <span data-ttu-id="018f3-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="018f3-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="018f3-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="018f3-136">Minimum supported client</span></span><br/> | <span data-ttu-id="018f3-137">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="018f3-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="018f3-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="018f3-138">Minimum supported server</span></span><br/> | <span data-ttu-id="018f3-139">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="018f3-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




