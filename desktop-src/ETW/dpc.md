---
description: Cette classe est la classe de type d’événement pour les événements DPC (Device Deferred Procedure Call). La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 46010179-7f0a-47dd-95fd-04d30fc597ba
title: DPC (classe)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DPC
- DPC.InitialTime
- DPC.Routine
api_type:
- NA
api_location: ''
ms.openlocfilehash: e0e756c2b41499a6e5b82129d609befc41d5e916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862089"
---
# <a name="dpc-class"></a><span data-ttu-id="59ace-104">DPC (classe)</span><span class="sxs-lookup"><span data-stu-id="59ace-104">DPC class</span></span>

<span data-ttu-id="59ace-105">Cette classe est la classe de type d’événement pour les événements DPC (Device Deferred Procedure Call).</span><span class="sxs-lookup"><span data-stu-id="59ace-105">This class is the event type class for device deferred procedure call (DPC) events.</span></span>

<span data-ttu-id="59ace-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="59ace-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="59ace-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59ace-107">Syntax</span></span>

``` syntax
[EventType{66, 68, 69}, EventTypeName{"ThreadDPC", "DPC", "TimerDPC"}]
class DPC : PerfInfo
{
  object InitialTime;
  uint32 Routine;
};
```

## <a name="members"></a><span data-ttu-id="59ace-108">Membres</span><span class="sxs-lookup"><span data-stu-id="59ace-108">Members</span></span>

<span data-ttu-id="59ace-109">La classe **DPC** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="59ace-109">The **DPC** class has these types of members:</span></span>

-   [<span data-ttu-id="59ace-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="59ace-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="59ace-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="59ace-111">Properties</span></span>

<span data-ttu-id="59ace-112">La classe **DPC** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="59ace-112">The **DPC** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="59ace-113">**InitialTime**</span><span class="sxs-lookup"><span data-stu-id="59ace-113">**InitialTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59ace-114">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="59ace-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="59ace-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59ace-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59ace-116">Qualificateurs : WmiDataId (1), extension (« WmiTime »)</span><span class="sxs-lookup"><span data-stu-id="59ace-116">Qualifiers: WmiDataId(1), Extension("WmiTime")</span></span>
</dt> </dl>

<span data-ttu-id="59ace-117">Heure d’entrée DPC.</span><span class="sxs-lookup"><span data-stu-id="59ace-117">DPC entry time.</span></span>

</dd> <dt>

<span data-ttu-id="59ace-118">**Simple**</span><span class="sxs-lookup"><span data-stu-id="59ace-118">**Routine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59ace-119">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="59ace-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="59ace-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59ace-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59ace-121">Qualificateurs : WmiDataId (2), pointeur</span><span class="sxs-lookup"><span data-stu-id="59ace-121">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="59ace-122">Adresse de la routine DPC.</span><span class="sxs-lookup"><span data-stu-id="59ace-122">Address of DPC routine.</span></span> <span data-ttu-id="59ace-123">Utilisez l’adresse avec les événements image pour Rechercher l’image qui a démarré.</span><span class="sxs-lookup"><span data-stu-id="59ace-123">Use the address with the Image events to find which image started.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="59ace-124">Notes</span><span class="sxs-lookup"><span data-stu-id="59ace-124">Remarks</span></span>

<span data-ttu-id="59ace-125">Ces événements sont journalisés lors de la saisie d’un DPC.</span><span class="sxs-lookup"><span data-stu-id="59ace-125">These events are logged when a DPC is entered.</span></span> <span data-ttu-id="59ace-126">Vous utilisez ces événements pour surveiller et vérifier le comportement des pilotes et des composants en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="59ace-126">You use these events to monitor and verify the behavior of drivers and kernel-mode components.</span></span> <span data-ttu-id="59ace-127">Par exemple, vous pouvez utiliser les événements DPC, ISR et image pour déterminer les composants qui consacrent trop de temps à des niveaux d’interruption élevés.</span><span class="sxs-lookup"><span data-stu-id="59ace-127">For example, you can use DPC, ISR, and Image events to determine those components that spend too much time at high interrupt levels.</span></span> <span data-ttu-id="59ace-128">Les événements DPC et ISR ont un horodatage d’entrée utilisé pour calculer la durée des routines.</span><span class="sxs-lookup"><span data-stu-id="59ace-128">DPC and ISR events have an entry time stamp which is used to compute the duration of the routines.</span></span> <span data-ttu-id="59ace-129">Les événements d’image sont lus pour construire les régions de mémoire qui mappent à certains modules.</span><span class="sxs-lookup"><span data-stu-id="59ace-129">The image events are read to construct the memory regions that map to certain modules.</span></span> <span data-ttu-id="59ace-130">Vous pouvez utiliser le mappage pour localiser le module qui contient la routine d’interruption.</span><span class="sxs-lookup"><span data-stu-id="59ace-130">You can use the mapping to locate the module that contains the interrupt routine.</span></span>

<span data-ttu-id="59ace-131">L’événement TimerDPC enregistre le moment où un DPC se déclenche à la suite d’un délai d’expiration du minuteur et les enregistrements d’événements ThreadDPC lors de l’exécution d’un thread DPC lié.</span><span class="sxs-lookup"><span data-stu-id="59ace-131">The TimerDPC event records when a DPC fires as a result of a timer expiration and the ThreadDPC event records when a threaded DPC executes.</span></span>

## <a name="requirements"></a><span data-ttu-id="59ace-132">Spécifications</span><span class="sxs-lookup"><span data-stu-id="59ace-132">Requirements</span></span>



| <span data-ttu-id="59ace-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59ace-133">Requirement</span></span> | <span data-ttu-id="59ace-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="59ace-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="59ace-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59ace-135">Minimum supported client</span></span><br/> | <span data-ttu-id="59ace-136">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59ace-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="59ace-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59ace-137">Minimum supported server</span></span><br/> | <span data-ttu-id="59ace-138">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59ace-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




