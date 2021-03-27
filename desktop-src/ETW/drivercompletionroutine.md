---
description: Cette classe est la classe de type d’événement pour les événements de routine complets du pilote. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: deb4f0b2-d73f-4ccf-b39b-6e92b32489fb
title: DriverCompletionRoutine, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverCompletionRoutine
- DriverCompletionRoutine.Routine
- DriverCompletionRoutine.Irp
- DriverCompletionRoutine.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2b43862169cbe8f192f8fb9db561c2e101f377b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862086"
---
# <a name="drivercompletionroutine-class"></a><span data-ttu-id="852b9-104">DriverCompletionRoutine, classe</span><span class="sxs-lookup"><span data-stu-id="852b9-104">DriverCompletionRoutine class</span></span>

<span data-ttu-id="852b9-105">Cette classe est la classe de type d’événement pour les événements de routine complets du pilote.</span><span class="sxs-lookup"><span data-stu-id="852b9-105">This class is the event type class for driver complete routine events.</span></span>

<span data-ttu-id="852b9-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="852b9-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="852b9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="852b9-107">Syntax</span></span>

``` syntax
[EventType{37}, EventTypeName{"DrvComplRout"}]
class DriverCompletionRoutine : DiskIo
{
  uint32 Routine;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a><span data-ttu-id="852b9-108">Membres</span><span class="sxs-lookup"><span data-stu-id="852b9-108">Members</span></span>

<span data-ttu-id="852b9-109">La classe **DriverCompletionRoutine** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="852b9-109">The **DriverCompletionRoutine** class has these types of members:</span></span>

-   [<span data-ttu-id="852b9-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="852b9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="852b9-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="852b9-111">Properties</span></span>

<span data-ttu-id="852b9-112">La classe **DriverCompletionRoutine** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="852b9-112">The **DriverCompletionRoutine** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="852b9-113">**Paquets**</span><span class="sxs-lookup"><span data-stu-id="852b9-113">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="852b9-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="852b9-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="852b9-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="852b9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="852b9-116">Qualificateurs : WmiDataId (2), pointeur</span><span class="sxs-lookup"><span data-stu-id="852b9-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="852b9-117">Paquet de demande d’e/s.</span><span class="sxs-lookup"><span data-stu-id="852b9-117">IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="852b9-118">**Simple**</span><span class="sxs-lookup"><span data-stu-id="852b9-118">**Routine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="852b9-119">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="852b9-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="852b9-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="852b9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="852b9-121">Qualificateurs : WmiDataId (1), pointeur</span><span class="sxs-lookup"><span data-stu-id="852b9-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="852b9-122">Adresse de la fonction de pilote appelée.</span><span class="sxs-lookup"><span data-stu-id="852b9-122">Address of the driver function being called.</span></span>

</dd> <dt>

<span data-ttu-id="852b9-123">**UniqMatchId**</span><span class="sxs-lookup"><span data-stu-id="852b9-123">**UniqMatchId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="852b9-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="852b9-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="852b9-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="852b9-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="852b9-126">Qualificateurs : WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="852b9-126">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="852b9-127">Identificateur qui identifie de façon unique la demande.</span><span class="sxs-lookup"><span data-stu-id="852b9-127">Identifier that uniquely identifies request.</span></span> <span data-ttu-id="852b9-128">Utilisez cet identificateur pour établir une corrélation avec les autres événements de pilote, par exemple l’événement [**DriverCompleteRequest**](drivercompleterequest.md) .</span><span class="sxs-lookup"><span data-stu-id="852b9-128">Use this identifier to correlate with the other driver events, for example, the [**DriverCompleteRequest**](drivercompleterequest.md) event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="852b9-129">Spécifications</span><span class="sxs-lookup"><span data-stu-id="852b9-129">Requirements</span></span>



| <span data-ttu-id="852b9-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="852b9-130">Requirement</span></span> | <span data-ttu-id="852b9-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="852b9-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="852b9-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="852b9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="852b9-133">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="852b9-133">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="852b9-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="852b9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="852b9-135">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="852b9-135">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="852b9-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="852b9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="852b9-137">**E**</span><span class="sxs-lookup"><span data-stu-id="852b9-137">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




