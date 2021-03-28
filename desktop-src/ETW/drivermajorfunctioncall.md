---
description: Cette classe est la classe de type d’événement pour les événements d’appel de fonction principale du pilote. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 8c913145-ac50-4d40-8519-5fed79d977ba
title: DriverMajorFunctionCall, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverMajorFunctionCall
- DriverMajorFunctionCall.MajorFunction
- DriverMajorFunctionCall.MinorFunction
- DriverMajorFunctionCall.RoutineAddr
- DriverMajorFunctionCall.FileObject
- DriverMajorFunctionCall.Irp
- DriverMajorFunctionCall.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: c944b11c9019ba5244850f035bfc7c02d5ca3350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971943"
---
# <a name="drivermajorfunctioncall-class"></a><span data-ttu-id="357a1-104">DriverMajorFunctionCall, classe</span><span class="sxs-lookup"><span data-stu-id="357a1-104">DriverMajorFunctionCall class</span></span>

<span data-ttu-id="357a1-105">Cette classe est la classe de type d’événement pour les événements d’appel de fonction principale du pilote.</span><span class="sxs-lookup"><span data-stu-id="357a1-105">This class is the event type class for driver major function call events.</span></span>

<span data-ttu-id="357a1-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="357a1-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="357a1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="357a1-107">Syntax</span></span>

``` syntax
[EventType{34}, EventTypeName{"DrvMjFnCall"}]
class DriverMajorFunctionCall : DiskIo
{
  uint32 MajorFunction;
  uint32 MinorFunction;
  uint32 RoutineAddr;
  uint32 FileObject;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a><span data-ttu-id="357a1-108">Membres</span><span class="sxs-lookup"><span data-stu-id="357a1-108">Members</span></span>

<span data-ttu-id="357a1-109">La classe **DriverMajorFunctionCall** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="357a1-109">The **DriverMajorFunctionCall** class has these types of members:</span></span>

-   [<span data-ttu-id="357a1-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="357a1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="357a1-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="357a1-111">Properties</span></span>

<span data-ttu-id="357a1-112">La classe **DriverMajorFunctionCall** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="357a1-112">The **DriverMajorFunctionCall** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="357a1-113">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="357a1-113">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="357a1-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="357a1-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="357a1-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="357a1-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="357a1-116">Qualificateurs : WmiDataId (4), pointeur</span><span class="sxs-lookup"><span data-stu-id="357a1-116">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="357a1-117">Faire correspondre la valeur de ce pointeur à la valeur de pointeur **FileObject** dans un événement [**\_ TypeGroup1 e**](diskio-typegroup1.md) pour déterminer le type d’opération d’e/s.</span><span class="sxs-lookup"><span data-stu-id="357a1-117">Match the value of this pointer to the **FileObject** pointer value in a [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event to determine the type of I/O operation.</span></span>

</dd> <dt>

<span data-ttu-id="357a1-118">**Paquets**</span><span class="sxs-lookup"><span data-stu-id="357a1-118">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="357a1-119">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="357a1-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="357a1-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="357a1-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="357a1-121">Qualificateurs : WmiDataId (5), pointeur</span><span class="sxs-lookup"><span data-stu-id="357a1-121">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="357a1-122">Paquet de demande d’e/s.</span><span class="sxs-lookup"><span data-stu-id="357a1-122">IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="357a1-123">**MajorFunction**</span><span class="sxs-lookup"><span data-stu-id="357a1-123">**MajorFunction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="357a1-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="357a1-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="357a1-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="357a1-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="357a1-126">Qualificateurs : WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="357a1-126">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="357a1-127">Code qui identifie la fonction principale appelée.</span><span class="sxs-lookup"><span data-stu-id="357a1-127">Code that identifies the major function being called.</span></span>

</dd> <dt>

<span data-ttu-id="357a1-128">**MinorFunction**</span><span class="sxs-lookup"><span data-stu-id="357a1-128">**MinorFunction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="357a1-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="357a1-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="357a1-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="357a1-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="357a1-131">Qualificateurs : WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="357a1-131">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="357a1-132">Code qui idenitifies la fonction mineure appelée.</span><span class="sxs-lookup"><span data-stu-id="357a1-132">Code that idenitifies the minor function being called.</span></span>

</dd> <dt>

<span data-ttu-id="357a1-133">**RoutineAddr**</span><span class="sxs-lookup"><span data-stu-id="357a1-133">**RoutineAddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="357a1-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="357a1-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="357a1-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="357a1-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="357a1-136">Qualificateurs : WmiDataId (3), pointeur</span><span class="sxs-lookup"><span data-stu-id="357a1-136">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="357a1-137">Adresse de la fonction de pilote appelée.</span><span class="sxs-lookup"><span data-stu-id="357a1-137">Address of the driver function being called.</span></span>

</dd> <dt>

<span data-ttu-id="357a1-138">**UniqMatchId**</span><span class="sxs-lookup"><span data-stu-id="357a1-138">**UniqMatchId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="357a1-139">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="357a1-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="357a1-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="357a1-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="357a1-141">Qualificateurs : WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="357a1-141">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="357a1-142">Identificateur qui identifie de façon unique la demande.</span><span class="sxs-lookup"><span data-stu-id="357a1-142">Identifier that uniquely identifies request.</span></span> <span data-ttu-id="357a1-143">Utilisez cet identificateur pour établir une corrélation avec les autres événements de pilote, par exemple l’événement [**DriverCompleteRequest**](drivercompleterequest.md) .</span><span class="sxs-lookup"><span data-stu-id="357a1-143">Use this identifier to correlate with the other driver events, for example, the [**DriverCompleteRequest**](drivercompleterequest.md) event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="357a1-144">Spécifications</span><span class="sxs-lookup"><span data-stu-id="357a1-144">Requirements</span></span>



| <span data-ttu-id="357a1-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="357a1-145">Requirement</span></span> | <span data-ttu-id="357a1-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="357a1-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="357a1-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="357a1-147">Minimum supported client</span></span><br/> | <span data-ttu-id="357a1-148">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="357a1-148">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="357a1-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="357a1-149">Minimum supported server</span></span><br/> | <span data-ttu-id="357a1-150">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="357a1-150">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="357a1-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="357a1-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="357a1-152">**E**</span><span class="sxs-lookup"><span data-stu-id="357a1-152">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




