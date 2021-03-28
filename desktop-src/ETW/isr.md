---
description: Cette classe est la classe de type d’événement pour les événements ISR (Interrupt Service routine). La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 2c7ccace-3384-43f4-905e-e7eeeee6f87b
title: ISR (classe)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISR
- ISR.InitialTime
- ISR.Routine
- ISR.ReturnValue
- ISR.Vector
- ISR.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5e27d5aa2712f8493b80ea11884aae1d0ef7abee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973310"
---
# <a name="isr-class"></a><span data-ttu-id="dc6ad-104">ISR (classe)</span><span class="sxs-lookup"><span data-stu-id="dc6ad-104">ISR class</span></span>

<span data-ttu-id="dc6ad-105">Cette classe est la classe de type d’événement pour les événements ISR (Interrupt Service routine).</span><span class="sxs-lookup"><span data-stu-id="dc6ad-105">This class is the event type class for interrupt service routine (ISR) events.</span></span>

<span data-ttu-id="dc6ad-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="dc6ad-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc6ad-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dc6ad-107">Syntax</span></span>

``` syntax
[EventType{67}, EventTypeName{"ISR"}]
class ISR : PerfInfo
{
  object InitialTime;
  uint32 Routine;
  uint8  ReturnValue;
  uint8  Vector;
  uint16 Reserved;
};
```

## <a name="members"></a><span data-ttu-id="dc6ad-108">Membres</span><span class="sxs-lookup"><span data-stu-id="dc6ad-108">Members</span></span>

<span data-ttu-id="dc6ad-109">La classe **ISR** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="dc6ad-109">The **ISR** class has these types of members:</span></span>

-   [<span data-ttu-id="dc6ad-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dc6ad-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dc6ad-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dc6ad-111">Properties</span></span>

<span data-ttu-id="dc6ad-112">La classe **ISR** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="dc6ad-112">The **ISR** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dc6ad-113">**InitialTime**</span><span class="sxs-lookup"><span data-stu-id="dc6ad-113">**InitialTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc6ad-114">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="dc6ad-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="dc6ad-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dc6ad-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc6ad-116">Qualificateurs : WmiDataId (1), extension (« WmiTime »)</span><span class="sxs-lookup"><span data-stu-id="dc6ad-116">Qualifiers: WmiDataId(1), Extension("WmiTime")</span></span>
</dt> </dl>

<span data-ttu-id="dc6ad-117">Heure d’entrée ISR.</span><span class="sxs-lookup"><span data-stu-id="dc6ad-117">ISR entry time.</span></span>

</dd> <dt>

<span data-ttu-id="dc6ad-118">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="dc6ad-118">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc6ad-119">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc6ad-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc6ad-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dc6ad-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc6ad-121">Qualificateurs : WmiDataId (5), pointeur</span><span class="sxs-lookup"><span data-stu-id="dc6ad-121">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="dc6ad-122">Réservé.</span><span class="sxs-lookup"><span data-stu-id="dc6ad-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="dc6ad-123">**ReturnValue**</span><span class="sxs-lookup"><span data-stu-id="dc6ad-123">**ReturnValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc6ad-124">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="dc6ad-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="dc6ad-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dc6ad-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc6ad-126">Qualificateurs : WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="dc6ad-126">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="dc6ad-127">Valeur booléenne indiquant si l’interruption a été revendiquée (a la valeur true si l’interruption a été revendiquée).</span><span class="sxs-lookup"><span data-stu-id="dc6ad-127">Boolean indicating if the interrupt was claimed (is True if the interrupt was claimed).</span></span>

</dd> <dt>

<span data-ttu-id="dc6ad-128">**Simple**</span><span class="sxs-lookup"><span data-stu-id="dc6ad-128">**Routine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc6ad-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc6ad-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc6ad-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dc6ad-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc6ad-131">Qualificateurs : WmiDataId (2), pointeur</span><span class="sxs-lookup"><span data-stu-id="dc6ad-131">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="dc6ad-132">Adresse de la routine ISR.</span><span class="sxs-lookup"><span data-stu-id="dc6ad-132">Address of ISR routine.</span></span> <span data-ttu-id="dc6ad-133">Utilisez l’adresse avec les événements image pour Rechercher l’image qui a démarré.</span><span class="sxs-lookup"><span data-stu-id="dc6ad-133">Use the address with the Image events to find which image started.</span></span>

</dd> <dt>

<span data-ttu-id="dc6ad-134">**Vecteur**</span><span class="sxs-lookup"><span data-stu-id="dc6ad-134">**Vector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc6ad-135">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="dc6ad-135">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="dc6ad-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dc6ad-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc6ad-137">Qualificateurs : WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="dc6ad-137">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="dc6ad-138">Vecteur issu de la table du descripteur d’interruption auquel la routine ISR est assignée.</span><span class="sxs-lookup"><span data-stu-id="dc6ad-138">Vector from interrupt descriptor table to which ISR routine is assigned.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dc6ad-139">Spécifications</span><span class="sxs-lookup"><span data-stu-id="dc6ad-139">Requirements</span></span>



| <span data-ttu-id="dc6ad-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc6ad-140">Requirement</span></span> | <span data-ttu-id="dc6ad-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc6ad-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dc6ad-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc6ad-142">Minimum supported client</span></span><br/> | <span data-ttu-id="dc6ad-143">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc6ad-143">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dc6ad-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc6ad-144">Minimum supported server</span></span><br/> | <span data-ttu-id="dc6ad-145">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc6ad-145">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




